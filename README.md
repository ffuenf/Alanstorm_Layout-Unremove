An Unremove Tag for Magento Layout XML
====================================

Every so often a theme developer will ask if it’s possible to use the local.xml layout file to reverse the effects of a <remove /> tag.

Unfortunately, this isn’t possible out of the box with Magento. Once a block has been removed there’s no layout XML command that will restore its output.

Fortunately, Magento’s layout system includes the right event hooks to allow you to implement this functionality yourself, so I’ve gone ahead and created a simple Layout Unremove extension. The new extension is pending release on Magento Connect, and I’ve made the package available here as well. The Layout Undelete extension is released under an MIT open source license, which makes it free to use and incorporate in your own projects.

Usage
-----

Usage of the tag is simple, and similar to the delete tag itself. In your local.xml, simply add the following to any handle where you wish to reverse the effects of a removal

```xml
<your_handle_name>
	<x-unremove name="left" />
</your_handle_name>
```

The tag name to use is <x-unremove name="left" />. The name attribute should be the name of the block that has been previously removed.


Basic modification
------------------

added modman config for standard magento installation 


Authors
-------

**Alan Storm**

+ http://http://alanstorm.com/


License
-------

MIT open source license