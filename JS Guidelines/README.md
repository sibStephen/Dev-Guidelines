JS Guidelines
=============

**Common Guide**
----------------

* Use single quotes '' for strings.

* No additional trailing comma in options.

* Always wrap code with anonymous function.
(function() {

})();

* Always use `var` to declare variables. Not doing so will result in global variables.
Bad:
  x = 'Batman';
Good:
  var x = 'Batman';

* Prefix jQuery object variables with a `$`.
var $sidebar = $('.sidebar');

* Use shorthands.
Bad:
var selector = jQuery('.sidebar');
var obj = new Object();
var arr = new Array();

Good:
var selector = $('.sidebar');
var obj = {};
var arr = [];

* Always cache DOM selection if you plan to re-use data.
var $search_form = $('#block-search').find('form');

  * Save reference to `this` as variable too.
    var _this = $(this); OR var _this = this;

* Avoid using `$.each` for repeated or performance critical functionality. Instead use a `for` loop.

**Drupal JS API**
-----------------

* Always use Drupal.behaviours in Drupal
Bad:
(function($, Drupal) {
  $(document).ready(function() {

  });
})(jQuery, Drupal);

Good:
(function($, Drupal) {
  Drupal.behaviour.behaviour_name = {
    attach: function (context, settings) {

    }
  };
})(jQuery, Drupal);

* Use dot notation when accessing properties.
Bad:
  Drupal.settings['base_url']

Good:
  Drupal.settings.base_url

* Keep DOM manipulation after page load in theme js.
