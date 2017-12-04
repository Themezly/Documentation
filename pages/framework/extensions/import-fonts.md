<div class="thz-doc-image max">
<a class="thz-lightbox mfp-iframe" href="https://www.youtube.com/watch?v=b05JiHxNid8" data-mfp-title="Creatus WordPress Theme Import Fonts Utility" data-modal-size="large">
	<img src="../../docs-media/splash-import-fonts.jpg" alt="Creatus WordPress Theme Import Fonts Utility" />
</a>
</div>
Beside the ability to use any of the 800+ __[Google Fonts](https://fonts.google.com/)__, Creatus comes with an advanced import fonts utility that will import fonts from __[FontSquirel](https://www.fontsquirrel.com/)__, __[Typekit](https://typekit.com/)__ and __your own @font-face kits__. Once imported, all the fonts that you have chosen will be visible in typography option an their styles are automatically enqued. 

### FontSquirel

To add the fonts from __[FontSquirel](https://www.fontsquirrel.com/)__ go to Creatus Import Fonts area __FontSquirel tab__ , find the font you need and click on it's download icon. After the download the font will be available in the typography options throughout the site. 


### Typekit

To add the fonts from __[Typekit](https://typekit.com/)__ go to Creatus Import Fonts area __Typekit tab__;
1. Add your __[Typekit API Token](https://typekit.com/account/tokens)__
1. Click on the __ Click to add kit ID button__ . 
1. In the addable input text add your __kit ID__ . 
1. After the font is available in the list click on __Save Changes__ button. 

Your Typekit fonts are now  available in the typography options throughout the site.

### Custom @font-face kits

To add custom @font-face kits folow these simple steps;

1. Place your __fontfacekit fonts in __ `creatus_child/assets/fontfacekits/{preset_name}` folder. __Last select__ option in __Export/import__ theme settings tab is the current __assigned theme preset__. 
2. Rename your fontfacekit CSS file to __thz-ff-kit.css__
3. Make sure that font files and CSS file are in same folder
4. In __functions.php add a filter__ with your font info;

<pre class="prettyprint light">
/*
 * First make sure that your fontfacekit fonts are
 * located in creatus_child/assets/fontfacekits/{preset_name} folder
 * Last select option in Export/import theme settings tab is  
 * the current assigned theme preset.
 * Rename your fontfacekit CSS file to thz-ff-kit.css
 * Make sure that font files and CSS file are in same folder
 */
function my_filter_add_fontface_kits ( $custom_kits ){
	
	$custom_kits = array(
		
		 /* 
		  *	Preset name must be set and must match the current preset
		  *	otherwise the font will not be visible in typography list
		  */
		'clean' => array(
			 /* 
			  * Set custom key for the font
			  */
			'open_sans' => array(
				 /* 
				  * Font display name in typography option list
				  */				
				'name' => 'Open Sans',
				 /* 
				  * Font family used in CSS, do not use fallbacks, 
				  * just the main fontfacekit font-family
				  */					
				'family' => 'Open Sans', 
				 /* 
				  * Set to false if no variants and font family is different for each weight
				  * otherwise use fonts.google example;
				  * array( '300','300italic','400','400italic')...
				  */					
				'variants' => false,
			)			
		)	
	
	);
	
	return $custom_kits;
}

add_filter('thz_filter_add_fontface_kits', 'my_filter_add_fontface_kits' );
</pre>