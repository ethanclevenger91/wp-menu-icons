<!-- DO NOT EDIT THIS FILE; it is auto-generated from readme.txt -->
# Menu Icons

Easily add icons to your nav menu items.

**Contributors:** [kucrut](http://profiles.wordpress.org/kucrut)  
**Tags:** [menu](http://wordpress.org/plugins/tags/menu), [nav-menu](http://wordpress.org/plugins/tags/nav-menu), [icons](http://wordpress.org/plugins/tags/icons), [navigation](http://wordpress.org/plugins/tags/navigation)  
**Requires at least:** 3.8  
**Tested up to:** 3.8.1  
**Stable tag:** 0.2.0  
**License:** [GPLv2](http://www.gnu.org/licenses/gpl-2.0.html)  
**Donate Link:** http://kucrut.org/#coffee  

## Description ##

### Usage ###
1. After the plugin is activated, go to *Appearance* > *Menus* to edit your menus
1. Each menu item will now have new *Icon Type* selection field with their corresponding sub-fields
1. Select the desired icon type
1. Select the icon from the second drop-down
1. Save the menu

### Currently supported icon types ###
- Dashicons (WordPress core icon fonts)
- [Font awesome](http://fortawesome.github.io/Font-Awesome/)
- [Genericons](http://genericons.com/) by [Automattic](http://automattic.com/)

### Planned supported icon types ###
- Image (attachment file & URL)

### Planned features ###
1. Provide menus preview on the front end
1. Provide setting page

Development of this plugin is done on [GitHub](https://github.com/kucrut/wp-menu-icons). **Pull requests welcome**. Please see [issues reported](https://github.com/kucrut/wp-menu-icons/issues) there before going to the plugin forum.


## Screenshots ##

### Menu Editor

![Menu Editor](assets/screenshot-1.png)

### Icon selection

![Icon selection](assets/screenshot-2.png)

### Twenty Fourteen with Dashicons

![Twenty Fourteen with Dashicons](assets/screenshot-3.png)

### Twenty Fourteen with Genericons

![Twenty Fourteen with Genericons](assets/screenshot-4.png)

### Twenty Thirteen with Dashicons

![Twenty Thirteen with Dashicons](assets/screenshot-5.png)

### Twenty Thirteen with Genericons

![Twenty Thirteen with Genericons](assets/screenshot-6.png)

## Installation ##

1. Upload `menu-icons` to the `/wp-content/plugins/` directory
1. Activate the plugin through the *Plugins* menu in WordPress

## Frequently Asked Questions ##

### The icons are not showing! ###
Make sure that your active theme is using the default walker for displaying the nav menu. If it's using its own custom walker, make sure that the menu item titles are filterable (please consult your theme author about this).

### The icon positions don't look right ###
If you're comfortable with editing your theme stylesheet, then you can override the styles from there.
Otherwise, I recommend you to use the [Simple Custom CSS plugin](http://wordpress.org/plugins/simple-custom-css/)

### Some font icons are not rendering correctly ###
This is a bug with the font icon itself. When the font is updated, this plugin will update its font too.

### Is this plugin extendable? ###
**Certainly!** Here's how you can remove an icon type from your plugin/theme:
```php
function myplugin_remove_menu_icons_type( $types ) {
	unset( $types['genericon'] );
	return $types;
}
add_filter( 'menu_icons_types', 'myplugin_remove_menu_icons_type' );
```

To add a new icon type, take a look at the `type-*.php` files inside the `includes` directory of this plugin.

### Can you please add X icon font? ###
Let me know via [GitHub issues](https://github.com/kucrut/wp-menu-icons/issues) and I'll see what I can do.

### Can I disable the extra stylesheet loaded by this plugin? ###
**YES!** Simply add the following to your plugin/theme:
```php
add_filter( 'menu_icons_load_extra_style', '__return_false' );
```


## Changelog ##

### 0.2.0 ###
* Media frame for icon selection
* New font icon: Font Awesome

### 0.1.5 ###
* Invisible, but important fixes and improvements

### 0.1.4 ###
* Fix menu saving

### 0.1.3 ###
* Provide icon selection fields on newly added menu items

### 0.1.2 ###
* Improve extra stylesheet

### 0.1.1 ###
* Improve icon selection UX

### 0.1.0 ###
* Initial public release


