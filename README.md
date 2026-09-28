```shell
~project> composer update composer-test/common -vvv
[...]
Running security advisory pool filter.
Reading /home/guillaume/.cache/composer/repo/https---repo.packagist.org/packages.json from cache
Downloading https://repo.packagist.org/packages.json if modified
[304] https://repo.packagist.org/packages.json
Downloading https://repo.packagist.org/p2/composer-test/common.json
[404] https://repo.packagist.org/p2/composer-test/common.json
Downloading https://packagist.org/api/security-advisories/
[200] https://packagist.org/api/security-advisories/
Running pool optimizer.
Updating dependencies
[...]
```

In particular, the following should not happen as the repository is a local one:
```shell
Downloading https://repo.packagist.org/p2/composer-test/common.json
[404] https://repo.packagist.org/p2/composer-test/common.json
```
