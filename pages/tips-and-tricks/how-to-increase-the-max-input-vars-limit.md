<div class="thz-notification thz-notification-blue thz-align-left">
	<h3 class="thz-notification-title">Info</h3>
	<div markdown="1">__PHP Max Input Vars__ is the maximum number of variables your server can use for a single function to avoid overloads.</div>
</div>
The __max_input_vars__ directive can be set in `.htaccess`, `php.ini` , `.user.ini` or `wp-config.php` file. To gain access to these files you will need __[FTP](http://en.wikipedia.org/wiki/File_Transfer_Protocol)__ credentials. If you do not have these please contact your hosting provider.

1. In your WordPress root installation locate any of these `.htaccess`, `php.ini`, `.user.ini` or `wp-config.php`
2. Edit the file and paste the directive code
3. Once you are done making changes save the file. If you have downloaded the file to make this change, upload it back to your server and override the existing file.

#### Directive for .htaccess
```
php_value max_input_vars 4000
```
#### Directive for php.ini or .user.ini
```
max_input_vars =4000
```
#### Directive for wp-config.php
```
@ini_set( 'max_input_vars' , 4000 );
```
<div class="thz-notification thz-notification-blue thz-align-left">
	<div markdown="1">The minimum recommended limit is 4000</div>
</div>	
<div class="thz-notification thz-notification-yellow thz-align-left">
	<h3 class="thz-notification-title">Warning</h3>
	<div>Changing server directives is recommended to site owners who are confident to do so. If you rather have professionals do this for you, contact your hosting provider.
	</div>
</div>