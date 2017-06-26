<div class="thz-doc-image max">
<a class="thz-lightbox mfp-iframe" href="https://www.youtube.com/watch?v=jgR34qZv0Ic" data-mfp-title="Creatus WordPress Theme Thz Typography Option Type" data-modal-size="large">
	<img src="../../docs-media/splash-thz-typography.jpg" alt="Creatus WordPress Theme Thz Typography Option Type" />
</a>
</div>

Thz Typography option type is an option type that will let you pick font family from 15 predefined web safe fonts families or choose font familly from__[800+ Google fonts](https://fonts.google.com/)__. You ca also adjust font size, weight, letter spacing, line height, style, text transform, alignment and color or use built in text shadow generator to aditionaly style your font.

#### option snippet

<pre class="pre-scrollable prettyprint light">
'option_name' => array(
	'type' => 'thz-typography',
	'label' =>__('Option label', '{domain}'),
	'desc' => esc_html__('Option description.', '{domain}'),
	'help' => esc_html__('Option help.', '{domain}'),
	'value' => array(
		'family'  		=> 'Arial, Helvetica, sans-serif',
		'style'     	=> '400',
		'subset'    	=> false,
		'transform' 	=> 'default',
		'align'     	=> 'default',
		'size' 			=> '',
		'line-height' 	=> '',
		'spacing'		=> '',
		'color' 		=> '',
		'text-shadow' 	=> array()
	),
	'preview' => true, // show/hide font preview

)
</pre>



#### frontend typography processing function 

<pre class="pre-scrollable prettyprint light">
$typography 	= thz_get_option('option_name');
$typography_css = thz_typo_print( $typography );
</pre>