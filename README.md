Yii 2 Ajax Button
==================

Yii 2 Ajax Button based on "JQuery".
Widget to manage ajax calls for Yii2 Framework

USAGE
-----

Example usage of ajax button widget

###Basic usage

```
dmstr\ajaxbutton\AjaxButton::widget([
  'method' => 'get',
  'url' => ['/path/to/action','name' => 'key']
]);
```
###Advanced usage

 ```
dmstr\ajaxbutton\AjaxButton::widget([
  'method' => 'post',
  'params' => ['status' => 'active'],
  'url' => ['/path/to/action'],
  'options' => ['class' => 'btn btn-primary'],
  'errorExpression' => new JsExpression('function(resp,status,xhr) {if (xhr.status === 200) {button.html("Success")}}'),
  'successExpression' => new JsExpression('function(xhr) {if (xhr.status === 404) {button.html("Error");console.error(xhr.responseJSON)}}')
]);
```

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download).

Add repository url to the required section of your `composer.json` file.

    "repositories": [
        {
            "type": "git",
            "url": "https://github.com/dmstr/yii2-ajax-button.git"
        }
    ],

Either run

`php composer.phar require dmstr/yii2-ajax-button` or `composer require dmstr/yii2-ajax-button`

or add

    "dmstr/yii2-ajax-button": "*"


to the required section of your `composer.json` file.
