<div class="thz-notification thz-notification-blue thz-align-left">
	<h3 class="thz-notification-title">Info</h3>
	<div markdown="1">__Max Post Size__ is the maximum size for all POST body data.</div>
</div>
The __post_max_size__ directive can be set in `.htaccess`, `php.ini` , `.user.ini` or `wp-config.php` file. To gain access to these files you will need __[FTP](http://en.wikipedia.org/wiki/File_Transfer_Protocol)__ credentials. If you do not have these please contact your hosting provider.

1. In your WordPress root installation locate any of these `.htaccess`, `php.ini`, `.user.ini` or `wp-config.php`
2. Edit the file and paste the directive code
3. Once you are done making changes save the file. If you have downloaded the file to make this change, upload it back to your server and override the existing file.

#### Directive for .htaccess
```
php_value post_max_size 32M
```
#### Directive for php.ini or .user.ini
```
post_max_size=32M
```
#### Directive for wp-config.php
```
@ini_set( 'post_max_size' , '32M' );
```
<div class="thz-notification thz-notification-blue thz-align-left">
	<div markdown="1">The minimum recommended size is 32M</div>
</div>	
<div class="thz-notification thz-notification-yellow thz-align-left">
	<h3 class="thz-notification-title">Warning</h3>
	<div>Changing server directives is recommended to site owners who are confident to do so. If you rather have professionals do this for you, contact your hosting provider.
	</div>
</div>