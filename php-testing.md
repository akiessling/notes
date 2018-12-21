# Testing for PHP code compatibility

* Install https://github.com/PHPCompatibility/PHPCompatibility  either with the described method or globally

```
composer global require phpcompatibility/php-compatibility
```

Run the compat test

```
phpcs --runtime-set installed_paths ~/.composer/vendor/phpcompatibility/php-compatibility --standard=PHPCompatibility --runtime-set testVersion 7.2 --extensions=php .
```
