![GitHub](https://img.shields.io/github/license/maxiledesma/m2wh?style=flat-square)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/maxiledesma/m2wh?style=flat-square)
# M2WH
### Warden helper for Magento 2
By **Maximiliano Ledesma**

M2WH is a tool to create easier access to common commands in Magento 2 environments created using Warden.

### Installation

If there is no `~/bin/` folder created, you should run these commands:

```shell
$ mkdir $HOME/bin
$ echo 'export PATH="$HOME/bin:$PATH"' >> $HOME/.bashrc
$ source ~/.bashrc
```
Now, in order to download **m2wh**:

```shell
$ wget --no-check-certificate https://github.com/maxiledesma/m2wh/tarball/1.0.0-beta -P /tmp/ && cd /tmp/
$ tar -xzvf m2wh.tar.gz
$ mv m2wh ~/bin/
$ sudo chmod +x ~/bin/m2wh
```
### Usage:
```shell
$ m2wh [options]
```

### Options:
|Command| Description|
|----|---|
|`h, --help`|Show brief help

### Available commands:
##### Frontend:
|Command| Description|
|----|---|
|`-cs, --clear-static theme`  | Remove all static files deployed on pub folder for specific theme
|`-sd, --static-deploy theme` | Clear the cache, remove static files and deploy static content through bin/magento setup:static-content:deploy command for specified theme

#### Cache:
|Command| Description|
|----|---|
|`-cc, --cache-clear`| Clear cache with bin/magento cache:clear command
|`-cf, --cache-flush`| Flush cache with bin/magento cache:flush command
|`-fr, --flush-redis`| Flush REDIS cache using warden env exec redis redis-cli flushall command

#### Users:
|Command| Description|
|----|---|
|`-auc, --admin-user-create`|Runs bin/magento admin:user:create to create an Admin User<br>
|`-cuc, --customer-user-create`|Runs n98-magerun customer:create to create a customer<br>

#### Development:
|Command| Description|
|----|---|
|`-de, --developer-enable`|Set deploy mode to developer
|`-he, --hints-enable`|Enable template hints and clear cache
|`-hd, --hints-disable`|Disable template hints and clear cache
|`-td, --tail-debug`|Show the last var/log/debug.log entries
|`-ts, --tail-system`|Show the last var/log/system.log entries

