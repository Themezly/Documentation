<div class="thz-doc-image max">
<a class="thz-lightbox mfp-image" href="../../docs-media/background_layer_shape.jpg" data-mfp-title="Creatus WordPress Theme Background Layer Shape" data-modal-size="large">
	<img src="../../docs-media/background_layer_shape.jpg" alt="Creatus WordPress Theme Background Layer Shape" />
</a>
</div>
Creatus theme container elements like __hero sections, section, section slider, column and inner column__ have a layer option that adds a background layer to the container. These particular elements also have a __Shape__ background type enabled that comes with over __25__ custom shapes that you can use. If these do not fit to your design, follow the instruction below to add your own SVG shapes to the list;

1. Create a __responsive__ SVG shape. Recommended viewBox should be __1000x500__ px
2. Edit the SVG file and add a class `thz-svg-shape thz-svg-{shape_file_name}`
3. Place your __shape__  in `creatus_child/assets/images/shapes` folder.
4. Add action to `creatus_child/functions.php` file

```
/*
 * Adds shape to shape background list
 * svg needs to be created like this for preview to work and the,
 * class name should contain the exact file name, eg; thz-svg-myfan
 * <svg xmlns="http://www.w3.org/2000/svg" class="thz-svg-shape thz-svg-smoke" viewBox="0 0 1000 500" preserveAspectRatio="none">
 *	...  your paths
 * </svg>
 */
 
function my_filter_background_shapes_list ($list, $id){

	$new_list = array(
		/*
		 * key must be same as the svg file , no extension;
		 * smoke.svg = smoke
		 */	
		'smoke' => esc_html__('Smoke', 'creatus'),
		'myfan' => esc_html__('My Fan', 'creatus'),
	
	);
	
	foreach ( $new_list as $shape => $name ){
		$list[$shape]= array(
			'text' => $name,
			'attr' => array(
				/*
				 * enable|disable flip option
				 */	
				'data-enable' => '.'.$id.'-shape-flip-parent',
			)
		);		
	}
	
	unset( $new_list );

    return $list;
}

add_filter('thz_filter_background_shapes_list', 'my_filter_background_shapes_list', 10, 2 );
```