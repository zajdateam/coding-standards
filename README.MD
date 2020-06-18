# Zajda Coding Standards
Run command
``` 
composer require zajda/coding-standards --dev
```
Add scripts to composer.json
```
"scripts": {
    "zajda-cs": "php vendor/squizlabs/php_codesniffer/bin/phpcs --standard=vendor/zajda/coding-standards/phpcs_ruleset.xml --extensions=php --encoding=utf-8 -sp src tests",
    "zajda-cbf": "php vendor/squizlabs/php_codesniffer/bin/phpcbf --standard=vendor/zajda/coding-standards/phpcs_ruleset.xml --extensions=php --encoding=utf-8 -pv src tests",
    "zajda-md": "php vendor/phpmd/phpmd/src/bin/phpmd src,tests text vendor/zajda/coding-standards/phpmd_ruleset.xml --extensions=php",
    "zajda-lint-php": "php vendor/php-parallel-lint/php-parallel-lint/parallel-lint src tests",
    "zajda-standards": [
        "@zajda-lint-php",
        "@zajda-cs",
        "@zajda-md"
    ]
}
```

### Inspired by [xemel/code-standards](https://bitbucket.org/xemelteam/coding-standards/)
Thank XeMeL team especially Jakub Dolba for the creation the code standards.
