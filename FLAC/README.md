# Proposed changes for fmt/279 (FLAC)

- Format name: FLAC (Free Lossless Audio Codec)
- Version number: ~1.2.1~ ([see below](#version-number))
- PUID: fmt/279

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

# Attribution

Landesarchiv Nordrhein-Westfalen
