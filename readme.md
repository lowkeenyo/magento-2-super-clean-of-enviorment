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
