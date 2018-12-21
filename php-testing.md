# Testing for PHP code compatibility

* Install https://github.com/PHPCompatibility/PHPCompatibility  either with the described method or globally

```
composer global require phpcompatibility/php-compatibility
```

Run the compat test

```
phpcs --runtime-set installed_paths `composer config home`/vendor/phpcompatibility/php-compatibility --standard=PHPCompatibility --runtime-set testVersion 5.3 --extensions=php .
```
