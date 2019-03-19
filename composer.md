# Using a local package repository

```json
{
	"repositories": {
		"the_module": {
			"type": "path",
			"url": "./Repository/the_module"
		}
    ...
    
```

Run
```bash
composer require myvendor/the_module @dev
```

Results in 

```bash
  - Installing myvendor/the_module (dev-whatever-branch-you-are-in): Symlinking from ./Repository/the_module
```
