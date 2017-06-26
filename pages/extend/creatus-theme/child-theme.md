<div class="thz-lightbox-gallery" markdown="1">
<div class="thz-doc-image max">
<a class="thz-lightbox mfp-image" href="../../docs-media/creatus-child.jpg" data-mfp-title="Creatus WordPress Theme Child Theme" data-modal-size="large">
	<img src="../../docs-media/creatus-child.jpg" alt="Creatus WordPress Theme Theme Child Theme" />
</a>
</div>

<div id="search" markdown="1">

Once you [__install__]( http://themezly.com/how-to-install-creatus-wordpress-theme/ ) and __activate__ Creatus WordPress Theme you are taken to the __Auto Setup__ screen that gives you two auto setup options that automatically __download__ and __activate__ Creatus Child Theme.  

<div class="thz-doc-image max">
<a class="thz-lightbox mfp-image" href="../../docs-media/creatus-child-auto-setup.jpg" data-mfp-title="Creatus WordPress Theme Child Theme" data-modal-size="large">
	<img src="../../docs-media/creatus-child-auto-setup.jpg" alt="Creatus WordPress Theme Theme Child Theme" />
</a>
</div>

- Plugins & Demo Content &nbsp;-&nbsp;  __installs all required plugins and dependencies and redirects to demo content install screen __
- Plugins Only  &nbsp;-&nbsp; __ installs all required plugins and dependencies __

Clicking on any of the two options will auto install and activate Creatus child theme for you. __We strongly recommend to use child-theme__ to make sure that your custom changes will still be effective after the theme has been updated. 
  
### Why use child theme?

WordPress child theme inherits all features and functionalities from a parent theme. This way you can  modify or extend parent theme without changing it and any future theme updates are not going to remove your custom theme modifications. 

Beside being able to extend the theme files, with Creatus you can also extend or modify the parent theme framework theme options, shortcodes ( elements ), extensions or widgets;


### Extend Creatus theme options
If theme options set is located in Creatus framework theme options folder, the __Creatus child theme__ is able to override the options set files by copying the file in to child theme corresponding folder;


	├─creatus/
	│ ├─inc/
	│ └──thzframework/
	│     └─theme/
	│       └─options/
	│         ├─posts/
	│         └──post_media.php
	│   
	└─creatus-child/
	  ├─inc/
	  └──thzframework/
	      └─theme/
	        └─options/
	          ├─posts/
	          └──post_media.php


### Extend Creatus shortcodes ( elements ) 
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
			  
### Extend Creatus extensions
If an extension is located in Creatus framework extensions folder, the __Creatus child theme__ is able to override the extension files by copying them in to child theme corresponding folder;

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


### Extend Creatus widgets		  
If a widget is located in Creatus inc widgets folder, the __Creatus child theme__ is able to override the __widget.php__ file by copying it to child theme corresponding folder;

	├─creatus/
	│ ├─inc/
	│ └──widgets/
	│     └─thz-flickr/
	│       └─views/
	│         └──widget.php
	│   
	└─creatus-child/
	  ├─inc/
	  └──widgets/
	      └─thz-flickr/
	        └─views/
	          └──widget.php
			  
			  
<div class="thz-notification thz-notification-blue">
	<h3 class="thz-notification-title">Info</h3>
	<div markdown="1">
For more information about Unyson [__extensions__](http://manual.unyson.io/en/latest/extensions/introduction.html#child-extensions) and [__shortcodes__](http://manual.unyson.io/en/latest/extension/shortcodes/index.html#overwriting-shortcodes) extend please visit [__Unyson Theme Framework manual__](http://manual.unyson.io).
	</div>
</div>
			  

</div>

</div>