<div class="thz-doc-image max">
<a class="thz-lightbox mfp-iframe" href="https://www.youtube.com/watch?v=tCjrF-m14fk" data-mfp-title="Creatus WordPress Theme Custom Theme Presets" data-modal-size="large">
	<img src="../../docs-media/splash-custom-theme-presets.jpg" alt="Creatus WordPress Theme Custom Theme Presets" />
</a>
</div>

<div markdown="1">

Creatus WordPress Theme comes with presets __Export/import__ utility that will help you create custom theme presets. For your convenience we have gathered a list of theme presets that come in handy when you don't need the complete theme demo but rather just want the demo theme settings.  

### Creating new theme preset
To create new theme preset, adjust the theme settings the way you need them, go to theme __Export/import__ tab, click on __Export theme settings__ button and save the preset in child theme presets folder. Note that preset file __must be .json type__;


	├─creatus-child/
	  ├─inc/
	  └──thzframework/
	      └─presets/
	          └──preset_name.json



### Assign custom default theme preset

To assign a custom theme preset to be a default preset on theme install or reset button click add this filter in your __creatus child__ theme __functions.php__;

	function my_filter_default_theme_preset(){
		return 'preset_name';
	}
	
	add_filter( 'thz_filter_set_preset', 'my_filter_default_theme_preset');



### Custom preset CSS file
If you are using custom theme presets you can also take advantage of custom theme preset CSS file and __auto load__ assigned preset CSS file. To do so simple create <b>preset_name.css</b> file and add it in __creatus-child__ assets CSS folder;


	├─creatus-child/
	  ├─assets/
	  └──css/
	       └─preset_name.css 

</div>