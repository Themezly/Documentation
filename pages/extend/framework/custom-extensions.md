<div class="thz-lightbox-gallery" markdown="1">
<div class="thz-doc-image max">
<img src="../../docs-media/creatus-screenshot.jpg" alt="Creatus WordPress Theme" />
</div>

<div markdown="1">
Creatus WordPress theme comes with__extended Unyson framework extensions__that you can take advantage of. You can extend these extensions at any time. 
If an extension is located in Creatus framework extensions folder, the__Creatus child theme__is able to override the extension files by copying them in to child theme corresponding folder;

	├─creatus/
	│ ├─inc/
	│ └──thzframework/
	│     └─extensions/
	│       └─megamenu/
	│         ├─views/
	│         └──item-link.php
	│   
	└─creatus-child/
	  ├─inc/
	  └──thzframework/
	      └─extensions/
	        └─megamenu/
	          ├─views/
	          └──item-link.php



			  

</div>

Once you copy the files over you can make desired changes to extension files and extend your__creatus-child__theme extensions. 
<div class="thz-notification thz-notification-red">
	<h3 class="thz-notification-title">Info</h3>
	<div>
	Please note that shortcodes extend is your responsibility and we offer only limited support fur such tasks.
	</div>
</div>

### Creating custom extension
Creatus theme is built on top of [__Unyson theme framework__](http://manual.unyson.io) and you can take advantage of all it's extending features. To create new extension from scratch follow this useful [__Unyson Extension Cookbook__](http://manual.unyson.io/en/latest/extensions/introduction.html#content) instructions.



</div>