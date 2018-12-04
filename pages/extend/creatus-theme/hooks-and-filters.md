<div class="thz-doc-image max">
<img src="../../docs-media/creatus-screenshot.jpg" alt="Creatus WordPress Theme Hooks and Filters" />
</div>

<div markdown="1">

Creatus WordPress Theme comes with several WordPress hooks and filters that can help you extend or change theme functionality. To use the filter or hook just copy the snippet to your `creatus-child/functions.php` file and hit save. 



#### Change logo html tag

<pre class="prettyprint light">
// logoid | logo = default header logo |  logomobile =  mobile menu logo
function my_filter_textual_logo_data( $data ){

	$h_tag = is_front_page() && 'logo' == $data['logoid'] ? 'h1' :'div';
	
	$data['tag'] = $h_tag;
	
	return $data;
}

add_filter( 'thz_filter_textual_logo_data', 'my_filter_textual_logo_data' );
</pre>


#### Change Image logo alt tags

<pre class="prettyprint light">
function my_filter_image_logo_alt() {
	return 'My logo alt';
}
add_filter( 'thz_filter_logo_alt', 'my_filter_image_logo_alt' );
</pre>

<pre class="prettyprint light">
function my_filter_mini_header_image_logo_alt() {
	return 'My mini logo alt';
}
add_filter( 'thz_filter_mini_logo_alt', 'my_filter_mini_header_image_logo_alt' );
</pre>


#### Add standard font to typography option font list

<pre class="prettyprint light">
function my_filter_standard_fonts() {
	return array('Verdana, Geneva, sans-serif' =>'Verdana, Geneva, sans-serif');
}
add_filter( 'thz_typography_standard_fonts', 'my_filter_standard_fonts' );
</pre>


#### Change widget list class
<pre class="prettyprint light">
function my_filter_list_class_name(){
	return 'my-awesome-lists-class-name';
}

add_filter( 'thz_filter_list_class', 'my_filter_list_class_name');
</pre>


#### Add more colors to theme colors palette
You must use `color_` prefix for the colors to be recongnized. 

<pre class="prettyprint light">
function my_filter_add_palette_colors( $palette ){
    $palette['color_11']='#ff6600';
    return $palette;
}
add_filter('thz_filter_palette_colors', 'my_filter_add_palette_colors' );
</pre>

#### Include files action 

The `do_action( 'thz_filter_init_includes' );` fires before any Creatus files inclusion. This way you can add 
own files on init. 

<pre class="prettyprint light">
function my_filter_init_include_files (){
    
	require_once get_stylesheet_directory_uri(). '/inc/my-awesome-class.php';
}

add_action('thz_filter_init_includes','my_filter_init_include_files');
</pre>


#### Add own local host to combine shortcodes CSS files

If you are working on your localhost, during changes of any builder elements CSS files there is a function that 
runs only if files have been changed and it is combining all elements CSS in to the `thz-shortcodes.css` file. 
This is the default local hosts list. 

<pre class="prettyprint light">
$locals = array(
	'localhost', 
	'127.0.0.1', 
	'192.168',
	'.test', 
	'.example', 
	'.invalid', 
);
</pre>

If the function does not run for you or you need to add a new local to the list use this filter


<pre class="prettyprint light">
function my_filter_add_local_host ( $local_hosts ){
    $local_hosts[]='my_local_host';
    return $local_hosts;
}

add_filter('thz_filter_combine_shortcodes_local_hosts', 'my_filter_add_local_host' );
</pre>


#### Enable Gutenberg ( block ) editor
By default Creatus disables Gutenberg editor and let you use the Tinymce editor for all posts types and pages.
To modify this filter or enable Gutenberg on specific post type you can redeclare the filter function in your
child theme `functions.php` file.

<pre class="prettyprint light">
/*
 * Disable block editor
 * in case you need some logic see:
 * https://gist.github.com/danyj/ec00057550fd6f73995ab2f8fc8b729f
 */
function _thz_filter_disable_block_editor_pt( $use_block_editor, $post_type ){
  
  $use_block_editor = true;
  return  $use_block_editor;
  
}
</pre>

</div>