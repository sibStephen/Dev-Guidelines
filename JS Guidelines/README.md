JS Guidelines
=============

**Common Guide**
----------------

* Use single quotes '' for strings.

* No additional trailing comma in options.

* Always wrap code with anonymous function.
```js
(function() {

})();
```

* Always use `var` to declare variables. Not doing so will result in global variables.
Bad:
```js
  x = 'Batman';
```
Good:
```js
  var x = 'Batman';
```

* Prefix jQuery object variables with a `$`.
```js
var $sidebar = $('.sidebar');
```

* Use shorthands.
Bad:
```js
var selector = jQuery('.sidebar');
var obj = new Object();
var arr = new Array();
```

Good:
```js
var selector = $('.sidebar');
var obj = {};
var arr = [];
```

* Always cache DOM selection if you plan to re-use data.
```js
var $search_form = $('#block-search').find('form');
```

  * Save reference to `this` as variable too.
    ```js
    var _this = $(this); OR var _this = this;
    ```

* Avoid using `$.each` for repeated or performance critical functionality. Instead use a `for` loop.

**Drupal JS API**
-----------------

* Always use Drupal.behaviours in Drupal
Bad:
```js
(function($, Drupal) {
  $(document).ready(function() {

  });
})(jQuery, Drupal);
```

Good:
```js
(function($, Drupal) {
  Drupal.behaviour.behaviour_name = {
    attach: function (context, settings) {

    }
  };
})(jQuery, Drupal);
```

* Use dot notation when accessing properties.
Bad:
```js
Drupal.settings['base_url']
```

Good:
  ```js
Drupal.settings.base_url
```

* Keep DOM manipulation after page load in theme js.
