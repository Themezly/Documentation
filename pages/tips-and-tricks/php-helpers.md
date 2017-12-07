
This is a extended list of most used PHP helpers. For a complete list of helpers and utility functions please browse  `creatus/inc/helpers.php` and `creatus/inc/utility.php` files.  
Beside Creatus PHP helpers here is a list of [__Unyson PHP Helpers__](http://manual.unyson.io/en/latest/helpers/php.html) that you can use. 

#### Get option
Return theme option value. If theme option __is set__ in __post/taxonomy custom option__, it returns __post/taxonomy custom option value__ instead.

	thz_get_option( $option_id, $default_value = null );


#### Get theme option
Return only theme option value.

	thz_get_theme_option( $option_id, $default_value = null );
	
#### Get post option	
Return post or tax option value.

	thz_get_post_option( $option_id = null, $default_value = null );

#### Get global option
Return portfolio, category, post or page option

	_thz_fw_get_global_option ( $option_id, $default_value = null );

#### WP file system
Return wp_filesystem, initiate if not available.

	thz_wp_file_system()


#### Theme uri
Return theme url. If child-theme is active return child-theme url.

	thz_theme_uri()

#### Theme dir
Return theme dir. If child-theme is active return child-theme dir.

	thz_theme_dir();


#### Theme file url
Return theme file uri. If file exists in child-theme return child-theme file uri.

	/**
	 * Search relative path in child than in parent theme directory and return URI
	 * @param  string $rel_path '/some/path_to_dir' or '/some/path_to_file.php'
	 * @return string URI
	 */
	thz_theme_file_uri( $rel_path );

#### Theme file path
Return theme file path. If file exists in child-theme return child-theme file path.

	/**
	 * Search relative path in child then in parent theme directory and return full path
	 * @param  string $rel_path '/some/path_to_dir' or '/some/path_to_file.php'
	 * @return string path
	 */
	thz_theme_file_path( $rel_path )


#### Theme version
Return current theme version.

	thz_theme_version()

#### Sanitize class names
Retur sanitized HTML element class names.

	thz_sanitize_class( $classnames, $fallback = null )



#### Property unit
Returns clean number with specified unit. If no match, fallback is used as unit.  
Allowed units are __px, %, rem, em, vw, vh, vmin ,vmax__.  
If __$auto__ is set to true it allows `auto` as value if found. If __$none__ is set to true it allows `none` as value if found.

	thz_property_unit( $val, $default, $auto = false, $none = false )



#### Replace palette colors
Creatus color options can use palette codes like `color_1` in output. Use this function to convert the color palette strings with actual color value. 
The function is able to convert multiple color codes and large strings like complete CSS files.  

	thz_replace_palette_colors( $string, $palette = false)
