# yii2-bootswatch4-asset

Asset bunlde around the Bootswatch theme suite based on **bootstrap 4**. Visit [Bootswatch](http://bootswatch.com/) for more.

[![Latest Stable Version](https://poser.pugx.org/raoul2000/yii2-bootswatch4-asset/v/stable.svg)](https://packagist.org/packages/raoul2000/yii2-bootswatch4-asset) [![Total Downloads](https://poser.pugx.org/raoul2000/yii2-bootswatch4-asset/downloads.svg)](https://packagist.org/packages/raoul2000/yii2-bootswatch4-asset) 


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist raoul2000/yii2-bootswatch4-asset "*"
```

or add

```
"raoul2000/yii2-bootswatch4-asset": "*"
```

to the require section of your `composer.json` file.


Usage
-----

Note that this asset bundle  **does NOT include Bootstrap 4 files**, but only the [Bootswatch](http://bootswatch.com/) CSS files dedicated to *overload* Bootstrap default theme. To use the Bootstrap 4 files with your Yii2 application, check the [yii2-bootstrap4](https://github.com/yiisoft/yii2-bootstrap4) extension.

To use a bootswatch theme in your Yii2 application add the **BootswatchAsset** bundle to your main *AppAsset* bundle:

```php

// ./assets/AppAsset.php

class AppAsset extends AssetBundle
{
    public $basePath = '@webroot';
    public $baseUrl = '@web';
    public $css = [
        'css/site.css',
    ];
    public $js = [
    ];
    public $depends = [
        'yii\web\YiiAsset',
    	'raoul2000\bootswatch4\BootswatchAsset',
    ];
}
?>
```

Then at some point you must select the theme name you want to use. In the example below, the theme [materia](https://bootswatch.com/materia/) is set in the main layout file.

```php

// ./views/layouts/main.php

raoul2000\bootswatch4\BootswatchAsset::$theme = 'materia';
AppAsset::register($this);

```

License
-------

**yii2-bootswatch4-asset** is released under the BSD 3-Clause License. See the bundled `LICENSE.md` for details.
