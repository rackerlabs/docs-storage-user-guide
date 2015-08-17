.. _cdn-files-differences:

-------------------------------------------------
Differences between Rackspace CDN and Cloud Files
-------------------------------------------------
* With Rackspace CDN, you can specify the origins that
  host your content, and the CDN pulls the content from those
  origins. Following are possible origins for Rackspace
  CDN:

  * Dedicated servers
  * Cloud servers
  * Cloud load balancers
  * Servers hosting outside of Rackspace

  In Cloud Files, you can CDN-enable a container, distributing the
  contents of that container to the CDN's edge nodes. In Rackspace
  CDN, it is not yet possible to specify a container as an origin.

* Rackspace CDN has no limit on purges.

* Rackspace CDN currently does not support streaming video from
  Cloud Files CDN-enabled containers, or serving CDN-enabled
  content over SSL/TLS.
