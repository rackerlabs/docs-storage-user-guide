.. _rackspace-cdn-actions:

^^^^^^^^^^^^^^^^^^^^^^^^^
Actions for Rackspace CDN
^^^^^^^^^^^^^^^^^^^^^^^^^
You can use Rackspace CDN to perform the following actions.

To learn how to perform Rackspace CDN by using your choice of
interface, begin at one of the following topics:

* :ref:`rackspacecdn-gui`
* :ref:`rackspacecdn-api`

Create a service
''''''''''''''''
A service represents an application that has its content
cached to the edge nodes, such as a website. You can create a
service by using the Cloud Control Panel, or the API.

The service defines the domain used to access the website
via CDN, and the origin from which to pull content.

Add and manage domains
''''''''''''''''''''''
You can add an additional domain to your service, however
you must always create a CNAME for that domain.

You can use a CNAME record to shorten your CDN URL to a
shorter or branded URL.

Create and manage caching rules
'''''''''''''''''''''''''''''''
Caching rules are designed to determine how long your content
should live on the edge nodes before the origin is
checked for an update.

If your content changes frequently, you might want to
set up a time to live (TTL) rule that pulls content from
the origin every few minutes. If your content does not change
frequently, you can set a longer TTL of 12-24 hours.

Purge content
'''''''''''''
You can remove content from an edge node so that it is
refreshed from the origin.

Delete a service
''''''''''''''''
