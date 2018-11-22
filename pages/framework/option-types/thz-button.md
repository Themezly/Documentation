<div class="thz-doc-image max">
<a class="thz-lightbox mfp-iframe" href="https://vimeo.com/302181862" data-mfp-title="Creatus WordPress Theme Thz Button Option Type" data-modal-size="large">
	<img src="../../docs-media/splash-thz-button.jpg" alt="Creatus WordPress Theme Thz Button Option Type" />
</a>
</div>


Thz Button is a button generator option type.

#### option snippet

<pre class="pre-scrollable prettyprint light">
'option_name' => array(
	'type' => 'thz-button',
	'label' => __('Option label', '{domain}'),
	'desc' => esc_html__('Option description.', '{domain}'),
	'help' => esc_html__('Option help.', '{domain}'),
	'value' => array(
		'buttonText'=>'Button',
		'activeColor' => 'theme',
		'buttonSizeClass' => 'small',
	),
)
</pre>
