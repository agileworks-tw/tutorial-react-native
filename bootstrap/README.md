# Bootstrap 介紹

**Bootstrap 是什麼？**

* 由 Twitter 在 2010 年 8 月釋出 Bootstrap
* CSS 框架 / 「行動優先」設計的前端框架
* RWD：響應式網頁設計，英文全名 Responsive Web Design。
* 總體結構包含：
    * CSS
    * 元件 (Component)
    * Javascript
    * 自訂架構

**其他類似的框架**

* [Foundation](http://foundation.zurb.com/)
* [Pure](http://purecss.io/)：Yahoo Inc.
* [Semantic UI](https://semantic-ui.com/)
* [Materialize CSS](http://materializecss.com/)

[各框架比較](http://usablica.github.io/front-end-frameworks/compare.html)

**特色**

* Grid system and responsive design
* Understanding CSS stylesheet
* Re-usable components
* JavaScript components and plug-ins

**版本**

* 預編譯版
* 原始版

**認識檔案結構**

```
bootstrap/
├── css/
│   ├── bootstrap.css
│   ├── bootstrap.css.map
│   ├── bootstrap.min.css
│   ├── bootstrap.min.css.map
│   ├── bootstrap-theme.css
│   ├── bootstrap-theme.css.map
│   ├── bootstrap-theme.min.css
│   └── bootstrap-theme.min.css.map
├── js/
│   ├── bootstrap.js
│   └── bootstrap.min.js
└── fonts/
    ├── glyphicons-halflings-regular.eot
    ├── glyphicons-halflings-regular.svg
    ├── glyphicons-halflings-regular.ttf
    ├── glyphicons-halflings-regular.woff
    └── glyphicons-halflings-regular.woff2
```

> 聊聊：以前 icon 的做法，現在 icon 的做法。

* [網路開放字型格式 (WOFF) - Web 開發者指引 | MDN](https://developer.mozilla.org/zh-TW/docs/Web/Guide/WOFF)

**安裝 Bootstrap**

* CDN
* [下載 bootstrap 原始檔](https://github.com/twbs/bootstrap/releases/download/v3.3.7/bootstrap-3.3.7-dist.zip)

**基礎樣板**

* [bootstrap - basic template](http://getbootstrap.com/getting-started/#template)

```html
<!DOCTYPE html>
<html lang="zh">
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Title Page</title>

        <!-- Bootstrap CSS -->
        <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">

        <!-- HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries -->
        <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
        <!--[if lt IE 9]>
            <script src="https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"></script>
            <script src="https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"></script>
        <![endif]-->
    </head>
    <body>
        <h1 class="text-center">Hello World</h1>

        <!-- jQuery -->
        <script src="http://code.jquery.com/jquery.js"></script>
        <!-- Bootstrap JavaScript -->
        <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" integrity="sha384-Tc5IQib027qvyjSMfHjOMaLkfuWVxZxUPnCJA7l2mCWNIpG9mGCD8wGNIcPD7Txa" crossorigin="anonymous"></script>
    </body>
</html>
```

### 視埠 (viewport)

* 裝置或監視器在網頁的可見區域
* 作用是告訴瀏覽器，目前裝置有多寬(或多高)，以便在縮放時有個基準。

**參數**

* width：可設定數值，或者指定為 device-width
* height：可設定數值，或者指定為 device-height
* initial-scale：第一次進入頁面的初始比例，最小0.25，最大5
* minimum-scale：允許縮小最小比例，最小0.25，最大5
* maximum-scale：允許放大最大比例，最小0.25，最大5
    * maximum-scale 設為1，其實就是不讓使用者縮放，以維持頁面的設計，行動裝置專用的網頁常有必要這樣做。
* user-scalable：允許使用者縮放，1 or 0 (yes or no)

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

### 延伸閱讀

* [回應式網頁設計基礎 | Web | Google Developers](https://developers.google.com/web/fundamentals/design-and-ui/responsive/?hl=zh-tw)