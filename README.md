
# yii2-related-form (Fork)

This is a maintained fork of the original `tolik505/yii2-related-form` package.
It has been updated for modern PHP versions and compatibility with the latest Symfony DomCrawler & CssSelector components.

The widget allows cloning form fields for related models in Yii2 — useful for dynamic form collections inside CRUD interfaces.

## 🔧 Fork Improvements

- Full compatibility with **PHP 8.x**
- Updated Symfony dependencies:
    - `symfony/dom-crawler` — `^2.6 || ^3.0 || ^4.0 || ^5.0 || ^6.0 || ^7.0`
    - `symfony/css-selector` — `^2.6 || ^3.0 || ^4.0 || ^5.0 || ^6.0 || ^7.0`
- Confirmed working with **Yii2 2.0.52 / 2.0.53**
- Minor internal refactoring for updated Symfony API
- Fixes for deprecated methods
- Improved DOM parsing stability

## 📦 Installation (Fork Version)

### 1. Add the repository to your `composer.json`:

```
"repositories": {
    "tolik505-related-form-fork": {
        "type": "vcs",
        "url": "https://github.com/Polishchyk/yii2-related-form"
    }
}
```

### 2. Require the package:

```
composer require tolik505/yii2-related-form:dev-master
```

Or manually:

```
"require": {
    "tolik505/yii2-related-form": "dev-master"
}
```

## 🧰 Usage

Inside `getFormConfig()`:

```php
[
    'class' => tolik505\relatedForm\RelatedFormWidget::class,
    'relation' => 'tests',
]
```

## 📡 JavaScript Events

```javascript
$(".dynamicform_wrapper").on("beforeInsert", function(e, item) {
    console.log("beforeInsert");
});
```

## ✔️ Compatibility Matrix

| Component | Version |
|----------|---------|
| PHP | 8.0 – 8.3 |
| Yii2 | 2.0.45 – 2.0.53 |
| symfony/dom-crawler | 2.6 – 6.4 |
| symfony/css-selector | 2.6 – 6.4 |

## 📄 License

BSD-3-Clause
