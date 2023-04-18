# Why

You want to be able to prove someone said something at a specific time. For legal
reasons, for archival reasons, or whatever.

## How

Web service. You give it a link to the resource, it downloads and archives it along
with the full HTTPS conversation including certificate chain. Then adds the archive to
IPFS and returns the CID.

Add some JavaScript libraries to deal with 

## Uses?

* Share facts with other people using IPFS gateways. Create a knowledge tree that is
  incorruptable.
* Use TLS servers that have a datetime timestamp in a 404 error page as proof of existence
  of some content.
* Legal disputes
* Use them as filters for adding data to datasets for ML. "X said Y about Z" doesn't make
  it true, but it's very hard to fake tha they said it.
* Nation state tampering with certificate chains becomes part of the historical record.
* Makes your penis grow by at least 2 inches, if not more.
