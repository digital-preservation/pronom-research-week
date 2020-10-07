# Proposed changes for fmt/279 (FLAC)

- Format name: FLAC (Free Lossless Audio Codec)
- Version number: ~1.2.1~ ([see below](#version-number))
- PUID: fmt/279
- File format identification signatures: ... ([see below](#signature))

## Version number

Currently, fmt/279 has format version 1.2.1 but the version number should be
removed altogether because of this statement in the [format
specification](https://xiph.org/flac/format.html):

> FLAC has no format version information, but it does contain reserved space in
> several places. Future versions of the format may use this reserved space
> safely without breaking the format of older streams.

The current signature does not check for the mentioned reserved space (which
would probably be quite fragile anyway), so IMHO no claim about version numbers
should be made.

## Signature

The [attached signature file](flac.pronom.xml) improves the signature currently
in PRONOM by changing it from `664C6143 00 000022` (max offset 4) to `664C6143
(80|00) 000022` (no max offset).

It still looks for the pattern `FLAC stream marker "fLaC" (4 bytes) +
last-metadata-block-flag (1 bit) + block type STREAMINFO (7 bits)
+ block size (3 bytes)` but introduces two changes:

1. The current signature allows a maximum offset of 4 bytes which as far as I
   can tell is not justified by the spec. → Removed.
2. The current signature expects a last-metadata-block-flag with value 0. It
   will thus only match FLAC files where the mandatory STREAMINFO block is
   followed by other metadata blocks. These are optional though, so the
   signature should allow both 0 (this is not the last metadata block before the
   audio data, others follow) and 1 (this is the last block). → Amended.

## Example file

The [attached example file](example.flac) has no metadata blocks except for the
mandatory STREAMINFO block. It can be identified with the improved signature but
not with the signature currently in PRONOM.

For reference, it is based on [this WAVE file](https://github.com/marhop/literate-binary/blob/master/examples/wave/wave.md)
converted to FLAC with the optional blocks removed:

    $ flac example.wav
    $ metaflac --remove-all --dont-use-padding example.flac

# Attribution

Landesarchiv Nordrhein-Westfalen
