.. _cloudblockstorage-cli:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Block Storage and CLIs: cinder
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To interact with Cloud Block Storage at the command line, you can
use tools created specifically for the purpose of interacting
with OpenStack-based clouds, such as Rackspace CLI (rack), nova,
and cinder, or general-purpose tools (cURL).

For more information about these tools, see the following
resources:

* :ref:`rack`
* :ref:`cinder`
* :user-guide:`nova <cloud-interfaces/cli/nova>`
* :ref:`curl`

In working with Cloud Block Storage, you might find that you
need to use nova for some functions and cinder for others.
You should install both tools. You can see an example
of using nova and cinder together at
:kc-article:`Configuring OpenStack Block Storage <configuring-openstack-block-storage>`
where in the "Create a Volume" section, ``nova volume-attach`` associates
a volume with a server and ``cinder list`` confirms that
association.

Alternatively, you can use Rackspace CLI to interact with
most cloud services without having to switch clients.

Before you can use one of these tools, you must install
a local (client) copy. The installation procedure varies for
each tool and is documented with the tool.

The commands that you can send are the same as the requests
that you can send to the API endpoint, but they are wrapped in
the syntax of the client. The
:rax-api:`API cross-reference <api-ref-blockstorage.html>`
lists those requests for Cloud Block Storage.

If you have both the cinder client and a cURL client
installed on your local computer,
you can choose to issue commands either through your
local copy of the cinder client or by using a general-purpose client
such as cURL, by sending a request to the instance of
the python-cinderclient that is active at the API endpoint for
Cloud Block Storage.
You can see both methods demonstrated in the Cloud Block Storage
API documentation, under
:rax-docs:`Cloud Block Storage quotas <cbs/api/v1.0/cbs-devguide/content/serviceQuotas-d1e01.html>`.

* cinder users send a short command,
  reusing details provided when the cinder client was configured::

    cinder quota-usage yourAccountID

* cURL users send a long command or series of commands,
  specifying details required to perform the API request::

    curl -i -X GET https://dfw.blockstorage.api.rackspacecloud.com/v1/yourAccountID/os-quota-sets/yourAccountID?usage=True \
    -H "X-Auth-Project-Id: yourAccountID" \
    -H "User-Agent: python-cinderclient" \
    -H "Accept: application/json" \
    -H "X-Auth-Token: yourAuthToken"



.. toctree:: :hidden:
   :maxdepth: 2

   cinder
   curl
   rack
