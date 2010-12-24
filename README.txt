Baha'i calendar css and images created by David Hunt
http://dnotes.net

INSTALLATION
============

In order to use this with the Drupal calendar module, you will need to apply the patch at http://drupal.org/node/679496#comment-3860894.  Works with calendar-6.x-2.x-dev as of December 2010.  For patching instructions, see http://drupal.org/patch/apply.

SETUP
=====

There are two basic ways that you can tell Drupal about bahaical:

### Theme

To use bahaical as part of your theme, just copy it into your theme directory and add a single line to your theme's .info file.  Something like the following should work, though you'll have to adjust it to your specific theme:

    stylesheets[all][] = css/bahaical/bahaical.css

### Module

To use bahaical as a part of your module, you will need to copy it into your module's directory and add the css with drupal_add_css().  To add the file to every page, for example, you would implement hook_init().  In a module named "mymodule", this would be as follows:

    function mymodule_init() {
      drupal_add_css(drupal_get_path('module', 'mymodule') . '/css/bahaical');
    }

After that, you simply need to install the patched calendar module, and everything should work.

