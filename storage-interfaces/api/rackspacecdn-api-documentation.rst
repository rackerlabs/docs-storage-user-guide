.. _rackspacecdn-api-documentation:

----------------------------------------------
Learn about Rackspace CDN in API documentation
----------------------------------------------
In the :rax-api:`API cross-reference<>`, you can see all
available API operations for all cloud services. The
operations are grouped according to the service they
interact with (for example, Cloud Files or Rackspace CDN) and
the scope they act on (for example, containers or services).

You can see all Rackspace CDN operations in the
:rax-api:`API cross-reference <api-ref-raxCDN.html>`. In
the group of
:rax-api:`operations that act on services <api-ref-raxCDN.html#raxcdn_ServicesOperations>`,
you can see that:

* Sending a ``POST`` request to the ``v1.0/{project_id}/services``
  URI requests creation of a new service

* Sending a ``GET`` request to the ``v1.0/{project_id}/services`` URI
  requests a basic list of all services

.. figure:: /_images/rackspacecdnlistservicesget.png
   :scale: 80%
   :alt: The API cross-reference lists all API operations. Click
         detail to see more about how the API handles this request.

   *The API cross-reference lists all API operations. Click "detail"
   to see more about how the API handles each request.*

The request parameters and sample responses shown here can help you
formulate a basic *List services* request to the API and
understand the API's response.

In the sample response, ``domains`` and ``origins`` correspond
to the information available in the Cloud Control Panel.

Following is an example of how to retrieve information about
a created service by using cURL and a sample response:

.. code::

   curl -i -X GET https://global.cdn.api.rackspacecloud.com/v1.0/yourAccountID/services/yourServiceID \
   -H "X-Auth-Token: yourAuthToken" \
   -H "Content-type: application/json"

.. code::

   HTTP/1.1 200 OK
   Content-Type: application/json

   {
       "id": "yourServiceID",
       "name": "mywebsite.com",
       "domains": [
           {
               "domain": "www.mywebsite.com",
               "protocol": "https"
           }
       ],
       "origins": [
           {
               "origin": "mywebsite.com",
               "port": 443,
               "ssl": false,
                "rules": []
           }
       ],
       "caching": [
           {
               "name": "default",
               "ttl": 3600
           },
           {
               "name": "home",
               "ttl": 17200,
               "rules": [
                   {
                       "name": "index",
                       "request_url": "/index.htm"
                   }
               ]
           },
           {
               "name": "images",
               "ttl": 12800,
               "rules": [
                   {
                       "name": "images",
                       "request_url": "*.png"
                   }
               ]
           }
       ],
       "restrictions": [
           {
               "name": "website only",
               "rules": [
                   {
                       "name": "mywebsite.com",
                       "referrer": "www.mywebsite.com"
                   }
               ]
           }
       ],
       "flavor_id": "cdn",
       "status": "deployed",
       "errors": [],
       "links": [
           {
               "href": "https://global.cdn.api.rackspacecloud.com/v1.0/yourAccountID/services/yourServiceID",
               "rel": "self"
           },
           {   "href": "https://global.cdn.api.rackspacecloud.com/v1.0/yourAccountID/flavors/cdn",
               "rel": "flavor"
           },
           {
               "href": "www.mywebsite.com.cdn1.raxcdn.com",
               "rel": "access_url"
           }
       ]
   }
