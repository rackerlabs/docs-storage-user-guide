Images for Rackspace Cloud Core Infrastructure Services User Guide
=======================================================================
All images must reside in this *_images* directory.

"All images" includes:

* Figures

Figures are drawings related to an idea discussed
in the text. The drawings show how things work conceptually but
not procedurally. Figures visually explain a concept.

*Use the figure directive to include figures;
give each figure alternate text and a caption.*

* Logos

Logos represent a single word or phrase such as the  
the name of a product

*Use the image directive to include logos;
give each logo alternate text.*

* Screenshots

Screenshots show how a Cloud Control Panel session looks.
Screenshots visually demonstrate a process
or a portion of a process.

*Use the figure directive to include screenshots;
give each screenshot alternate text and a caption.*

For everything stored in *_images*,
use this *README* to maintain an inventory describing what we have,
where we got it, and how we use it.


----
To include any image in the guide:

* Save the image (probably of type .png)
  in the *_images* directory
  with a descriptive filename. "CloudServerCreation"
  is a descriptive filename; "Image01" is not.

* On the page where you intend the image to appear,
  at the location where you intend it to appear,
  call for it from ``/_images/`` followed by its filename,
  providing descriptive alternate text
  so non-visual browsers can verbally summarize its meaning.

  If the image is a figure or a screenshot,
  also provide an italicized caption.  
  Follow this model:

```
  .. figure:: /_images/screenshots/ExampleProcess.png
     :alt: Cloud Servers are awesome.
           If I say more than one line,
           I indent.

     *Italicize a caption explaining the screenshot.*
```

* Update the inventory (below), connecting the image to
  its intended use, its age, its source, and at least one human
  responsible for it.
  Keep the inventory grouped by image type
  (figures, logos, screenshots)
  and alphabetized by filename within image type.

----
**Inventory of logos**



----
**Inventory of screenshots**

* **accountresourcelimits.png**
  * used at storage-interfaces/gui/index.html
  * collected from https://mycloud.rackspace.com
  * collection date 2015-05-18
  * contributed by Rose Coste

* **chromeviewdevelopertools.png**
  * used at storage-interfaces/api/rackspacecdn-api.html
  * collected from https://mycloud.rackspace.com
  * collection date 2015-05-15
  * contributed by Rose Coste

* **controlpanelrackspacecdn.png**
  * used at storage-interfaces/gui/rackspacecdn-gui.html
  * collected from https://mycloud.rackspace.com
  * collection date 2015-08-14
  * contributed by Stephanie Fillmon

* **createticketserversresourcelimit.png**
  * used at storage-interfaces/gui/index.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-18
  * contributed by Rose Coste

* **rackspacecdnlistservicesget.png**
  * used at storage-interfaces/api/rackspacecdn-api.html
  * collected from http://api.rackspace.com/
  * collection date 2015-08-25
  * contributed by Stephanie Fillmon

* **rackspacecdnsdkphp.png**
  * used at storage-interfaces/api/rackspacecdn-sdk.html
  * collected from https://developer.rackspace.com/
  * collection date 2015-08-25
  * contributed by Stephanie Fillmon 
