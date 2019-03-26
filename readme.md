## For clearing the cache:
* bin/magento cache:clean

## For reindex new xml files:
* bin/magento index:reindex

## List item
* bin/magento cache:clean

## For refresh or insert new plugins:
* bin/magento setup:upgrade
* -d memory_limit=-1 bin/magento setup:static-content:deploy de_DE
* bin/magento index:reindex
* bin/magento cache:clean

## If you need a "full-cleanup/refresh":
* bin/magento setup:upgrade
* -d memory_limit=-1 bin/magento setup:di:compile
* -d memory_limit=-1 bin/magento setup:static-content:deploy de_DE
* bin/magento index:reindex
* bin/magento cache:clean

## Deletering of directories with temporary or generated files
rm -rf var/page_cache/* var/cache/* var/composer_home/* generated/code/* generated/metadata/* var/view_preprocessed/*


## extra 

Tool name	Brief description	What it clears
magento setup:upgrade	Update Magento database schema and data	generated/metadata and generated/code
magento setup:di:compile	Generates code	generated/code prior to compiling
magento deploy:mode:set {mode}	Switch between developer and production mode	generated/metadata, generated/code, var/view_preprocessed
magento cache:clean {type}	Clears the cache	var/cache and var/page_cache
