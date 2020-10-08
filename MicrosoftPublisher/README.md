# Microsoft Publisher

http://fileformats.archiveteam.org/wiki/Microsoft_Publisher

### Proposed Changes:

1. Remove dependency on CompObj "MSPublisher" signature. Many samples do not have a CompObj, also too vaugue for versions. 
2. New signatures based on "Contents" header.

### Signature Changes

* x-fmt/252 (2.0), x-fmt/253 (95), x-fmt/257 (2002) Adjusted to new signature specific to version.
* Added signature to x-fmt/254 (97), x-fmt/255 (98), x-fmt/256 (2000)
* New entry for CHLdev/1 (1.0), CHLdev/2 (2003), CHLdev/3 (2007), CHLdev/4 (2010), CHLdev/5 (2013 onwards)



Testing Samples retrieved from [UK Web Archive](https://www.webarchive.org.uk/shine/search?page=1&facet.fields=postcode_district&facet.fields=crawl_year&invert=&facet.fields=domain&invert=&facet.fields=links_domains&invert=&facet.fields=public_suffix&invert=&facet.fields=content_type_norm&invert=&facet.fields=content_language&invert=&addFacet=content_type_ext&action=add-facet&query=content_ffb:%22d0cf11e0%22&tab=results&totalCount=totalCount&sort=crawl_date&order=asc&mode=&facet.in.content_type_ext=%22pub%22) and [LinkedIn Learning](https://www.linkedin.com/learning/)
