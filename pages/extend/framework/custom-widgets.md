<div class="thz-lightbox-gallery" markdown="1">
<div class="thz-doc-image max">
<img src="../../docs-media/creatus-screenshot.jpg" alt="Creatus WordPress Theme" />
</div>

<div markdown="1">
Creatus WordPress theme comes with [__custom widgets__](https://themezly/documentation/plugins-and-widgets/) that you can take advantage of. You can extend these widgets at any time. 
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



			  

</div>

Once you copy the file over you can make desired changes to widget file and extend your __creatus-child__ theme widget. 
<div class="thz-notification thz-notification-red">
	<h3 class="thz-notification-title">Info</h3>
	<div>
	Please note that widget extend is your responsibility and we offer only limited support fur such tasks.
	</div>
</div>


</div>