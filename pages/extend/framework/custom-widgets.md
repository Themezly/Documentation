<div class="thz-lightbox-gallery" markdown="1">
<div class="thz-doc-image max">
<img src="../../docs-media/creatus-screenshot.jpg" alt="Creatus WordPress Theme" />
</div>

<div markdown="1">
Creatus WordPress theme comes with [__custom widgets__](https://themezly/documentation/plugins-and-widgets/) that you can take advantage of. You can extend these widgets at any time. 
If a widget is located in Creatus inc widgets folder, the__Creatus child theme__is able to override the__widget.php__file by copying it to child theme corresponding folder;

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



			  

</div>

Once you copy the file over you can make desired changes to widget file and extend your__creatus-child__theme widget. 
<div class="thz-notification thz-notification-red">
	<h3 class="thz-notification-title">Info</h3>
	<div>
	Please note that widget extend is your responsibility and we offer only limited support fur such tasks.
	</div>
</div>


</div>