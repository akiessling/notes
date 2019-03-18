

Adding a field to the site configuration
```php
// Configure a new simple required input field to site
$GLOBALS['SiteConfiguration']['site']['columns']['myNewField'] = [
    'label' => 'A new custom field',
    'config' => [
        'type' => 'input',
        'eval' => 'required',
    ],
];

// And add it to showitem
$GLOBALS['SiteConfiguration']['site']['types']['0']['showitem'] = str_replace(
    'base,',
    'base, myNewField, ',
    $GLOBALS['SiteConfiguration']['site']['types']['0']['showitem']
);
```

Accessing the extended field in a cObject
```
SITE_VALUE = TEXT
SITE_VALUE.data = site:myNewField
```

Accessing the extended field in a condition
```
[site("configuration")["myNewField"] == "myCustomValue"]
...
```
