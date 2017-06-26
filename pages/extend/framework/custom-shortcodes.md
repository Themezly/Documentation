<div class="thz-lightbox-gallery" markdown="1">
<div class="thz-doc-image max">
<img src="../../docs-media/creatus-screenshot.jpg" alt="Creatus WordPress Theme" />
</div>

<div markdown="1">
Creatus WordPress theme comes with __over 40 shortcodes ( elements ) __ that you can take advantage of. You can extend these shortcodes at any time. 
If a shortcode is located in Creatus framework extensions shortcodes folder, the __Creatus child theme__ is able to override the shortcode files by copying them in to child theme corresponding folder;


	├─creatus/
	│ ├─inc/
	│ └──thzframework/
	│     └─extensions/
	│       └─shortcodes/
	│         ├─shortcodes/
	│         ├──text/
	│         └───...
	│   
	└─creatus-child/
	  ├─inc/
	  └──thzframework/
	      └─extensions/
	        └─shortcodes/
	          ├─shortcodes/
	          ├──text/
	          └───...



			  

</div>

Once you copy the files over you can make desired changes to shortcode files and extend your __creatus-child__ theme shortcode. 
<div class="thz-notification thz-notification-red">
	<h3 class="thz-notification-title">Info</h3>
	<div>
	Please note that shortcodes extend is your responsibility and we offer only limited support fur such tasks.
	</div>
</div>

### Creating custom shortcode
Creatus theme is built on top of [__Unyson theme framework__](http://manual.unyson.io) and you can take advantage of all it's extending features. To create new shortcode from scratch follow this useful [__Unyson Shortcode Cookbook__](http://manual.unyson.io/en/latest/extension/shortcodes/index.html#cookbook) instructions.


</div>