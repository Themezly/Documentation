<div class="thz-doc-image max">
<a class="thz-lightbox mfp-iframe" href="https://www.youtube.com/watch?v=QNfQwrPnMLw" data-mfp-title="Creatus WordPress Theme Thz Background Option Type" data-modal-size="large">
	<img src="../../docs-media/splash-thz-background.jpg" alt="Creatus WordPress Theme Thz Background Option Type" />
</a>
</div>

Thz Background is option type with multiple background selection such as none, color, gradient, image, video or shape.

#### option snippet simple

<pre class="pre-scrollable prettyprint light">
'option_name' => array(
	'type' => 'thz-background',
	'label' =>__('Option label', '{domain}'),
	'desc' => esc_html__('Option description.', '{domain}'),
	'help' => esc_html__('Option help.', '{domain}'),
	'value'=> array(),
	//'disable' => array('image','color','video','gradient','shape'),
)
</pre>

#### option snippet full

<pre class="pre-scrollable prettyprint light">
'option_name' => array(
	'type' => 'thz-background',
	'label' =>__('Option label', '{domain}'),
	'desc' => esc_html__('Option description.', '{domain}'),
	'help' => esc_html__('Option help.', '{domain}'),
	'value'=> array(
		'type' => 'none',
		'color' => '',
		'image' => '',
		'repeat' => 'no-repeat',
		'position' => 'left-top',
		'size' => 'cover',
		'attachment' => 'scroll',
		'gradient-style' => 'linear', // linear, radial
		'gradient-angle' => '0',
		'gradient-size' => 'farthest-corner',//closest-corner, closest-side,farthest-corner,farthest-side
		'gradient-shape' => 'circle',//circle,ellipse
		'gradient-h-poz' => '50',
		'gradient-v-poz' => '50',
		'gradient-start' => '0',
		'gradient-start-color' => '#ffffff',
		'gradient-add-stop' => array(),
		'gradient-end' => '100',
		'gradient-end-color' => 'color_1',
		'video-link' => '',
		'video-poster' => '',
		'video-sound' => 0,
		'video-loop' => 1,
		'shape' => array(
			's' =>'waves', // shape name
			'p' =>'bottom', // shape position
			'f' =>'no', // shape flip
			'c' =>'color_1', // shape color
			'b' =>'',//  background color
			'w' => 100,// shape  width
			'h' =>''//  shape height
		)
	)
)
</pre>
