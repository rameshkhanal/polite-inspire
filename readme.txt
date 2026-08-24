=== Polite Inspire ===

Contributors: templatesell
Theme URI: https://www.templatesell.com/item/polite-inspire-blog-wordpress-theme/
Author URI: https://www.templatesell.com/
Tags: grid-layout, one-column, two-columns, three-columns, four-columns, left-sidebar, right-sidebar, custom-background, custom-logo, custom-menu, featured-images, threaded-comments, translation-ready, footer-widgets, custom-colors, custom-header, editor-style, rtl-language-support, theme-options, blog, news
Requires at least: 6.0
Requires PHP: 7.4
Tested up to: 7.1
Stable tag: 1.0.4
License: GNU General Public License v2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

A perfect theme for blog and magazine site. With masonry layout and multiple blog page layout, this theme is the awesome and minimal theme. It is a child theme of Polite. This theme has search option, off-canvas sidebar, multiple sidebar options, footer options, featured slider, promo boxed, footer widgets and many more. Besides that, this theme comes with added custom widgets for author information, featured posts, social icons, etc. It comes with primary color option to change the whole site color with a single click. More Details: https://www.templatesell.com/item/polite-inspire/

== Description ==

A perfect theme for blog and magazine site. With masonry layout and multiple blog page layout, this theme is the awesome and minimal theme.
== Installation ==

1. In your admin panel, go to Appearance > Themes and click the Add New button.
2. Click Upload Theme and Choose File, then select the theme's .zip file. Click Install Now.
3. Click Activate to use your new theme right away.

== Changelog ==
= 1.0.4 - August 24 2026 =

Fixed
* The selectable body font was fetched from fonts.googleapis.com on every page view, over a protocol-relative URL and with no version, so WordPress appended its own to the request. The families this theme's picker offers that the parent does not already bundle are served from the theme now, so no visitor data leaves the site. Each family keeps its unicode-range, so a browser downloads only the faces the selected font actually needs
* The Customizer's font list was built with a stray space before one of the family names. Google does not reject such a request, it silently drops the families it cannot parse - so the dropdown whose whole purpose is to show each option in its own typeface could not render all of them. The same stray space appeared in the array that builds the preview CSS, giving a selector that matched nothing. Both now derive from the theme's own font list, so they cannot drift apart
* The parent's 'polite-style' handle was re-registered with no version, which makes WordPress substitute its own - the parent stylesheet was served as style.css?ver=7.1. It carries the parent's version now. The handle does still have to be registered here, because the parent enqueues it with get_stylesheet_uri(), which on a child install resolves to this theme's style.css
* The dynamic font rule read the font array without checking the stored key exists. The parent offers its own font list, so a value set or left over from the parent was an undefined array key; it falls back to the theme default now
* $parent_style was assigned and never used, and the stylesheet enqueue ended in a double semicolon
* A default string in this child theme was tagged with the parent's text domain, so a language pack for this theme could never translate it
* The child theme's text domain was loaded without being told where its language files are
* 'no-cotent' was a misspelling of the class the theme meant to output
* readme.txt gave the PHP requirement as 4.7, a PHP version that has never existed, and a stable tag that did not match the theme

Performance
* The reading-time counter ran the whole content pipeline on every post in the loop purely to count words: apply_filters( 'the_content' ) renders blocks, expands shortcodes, runs wpautop and resolves every oEmbed - and then do_shortcode() was called on the result a second time. It counts the raw content now, with strip_shortcodes(), which removes shortcode tags without executing them
* _n()'s third argument selects the plural form and has to be a number; it was being passed number_format_i18n(), which returns a formatted string

Other
* Added languages/polite-inspire.pot
* Tested up to WordPress 7.1

= 1.0.3 - May 19 2025 =
* Fixing Track Issue

= 1.0.2 - May 17 2025 =
* Fixed prefix theme slug

= 1.0.1 - May 17 2025 =
* Fixed prefix theme slug

= 1.0.0 - May 15 2025 =
* Initial Submission

== Credits ==
Polite Inspire is a child theme of Polite by, Template Sell.
Polite Inspire is distributed under the terms of the GNU GPL v2 or later.

Polite is free WordPress theme by, Template Sell.
Polite is distributed under the terms of the GNU GPL v2 or later.

* Lato, Copyright (c) Lukasz Dziedzic, [SIL Open Font License 1.1](https://scripts.sil.org/OFL) - bundled in assets/fonts/
* Open Sans, Copyright (c) The Open Sans Project Authors, [SIL Open Font License 1.1](https://scripts.sil.org/OFL) - bundled in assets/fonts/
* Montserrat, Copyright (c) The Montserrat Project Authors, [SIL Open Font License 1.1](https://scripts.sil.org/OFL) - bundled in assets/fonts/
* Alegreya, Copyright (c) Juan Pablo del Peral, Huerta Tipografica, [SIL Open Font License 1.1](https://scripts.sil.org/OFL) - bundled in assets/fonts/
* Alex Brush, Copyright (c) TypeSETit LLC, [SIL Open Font License 1.1](https://scripts.sil.org/OFL) - bundled in assets/fonts/

== Screenshot Images [CCO License] ==
License: https://stocksnap.io/license
https://stocksnap.io/photo/woman-thinking-MLZIHL9GLY - License: CC0 1.0 Universal (CC0 1.0) - Copyright Bruce Mars 
https://stocksnap.io/photo/smiling-woman-QEFMGVEVEM - License: CC0 1.0 Universal (CC0 1.0) - Copyright Authentic Stock
https://stocksnap.io/photo/beautiful-woman-ALVGSSERRY - License: CC0 1.0 Universal (CC0 1.0) - Copyright  Lucas Allmann

