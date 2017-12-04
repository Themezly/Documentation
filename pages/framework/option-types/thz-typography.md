<div class="thz-doc-image max">
<a class="thz-lightbox mfp-iframe" href="https://www.youtube.com/watch?v=JpFx-tWElHQ" data-mfp-title="Creatus WordPress Theme Thz Typography Option Type" data-modal-size="large">
	<img src="../../docs-media/splash-thz-typography.jpg" alt="Creatus WordPress Theme Thz Typography Option Type" />
</a>
</div>

Thz Typography is an option type that will let you pick font family from 15 predefined web safe fonts families, choose font familly from __[800+ Google fonts](https://fonts.google.com/)__. You ca also adjust font size, weight, letter spacing, line height, style, text transform, alignment and color or use built in text shadow generator to aditionaly style your font. 

If your favorite webfont is not in the list or you simply need more webfonts please see __[Import fonts utility](https://themezly.com/docs/import-fonts/)__

#### option snippet

<pre class="pre-scrollable prettyprint light">
'option_name' => array(
	'type' => 'thz-typography',
	'label' => __('Option label', '{domain}'),
	'desc' => esc_html__('Option description.', '{domain}'),
	'help' => esc_html__('Option help.', '{domain}'),
	'value' => array(
		'family'  		=> 'default',
		'size' 			=> '',
		'weight'     	=> 'default',
		'style'     	=> 'default',
		'subset'    	=> false, // array of font subsets if used
		'line-height' 	=> '',
		'spacing'		=> '',
		'transform' 	=> 'default',
		'align'     	=> 'default',
		'color' 		=> '',
		'hovered' 		=> '',
		'text-shadow' 	=> array()
	),
	'cssprint' => true, // auto saves font CSS
	'cssclasses' => false, // auto saves font class names
	'disable' => array(), // what to disable, ex: array('size')
	/* used to limit class names, 
	 * ex: biggest font classs size is thz-fs-100, 
	 * if you increase it dont forget to add new class names in your stylesheet
	 */
	'sizelimit' => 100, 

)
</pre>



#### frontend typography processing function 

<pre class="pre-scrollable prettyprint light">
$typography 	= thz_get_option('option_name');
$typography_css = thz_typo_print( $typography );
</pre>