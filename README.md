![GitHub](https://img.shields.io/github/license/maxiledesma/m2wh?style=flat-square)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/maxiledesma/m2wh?style=flat-square)
# M2WH
### Warden helper for Magento 2
By **Maximiliano Ledesma**

M2WH is a tool to create easier access to common commands in Magento 2 environments created using Warden.

### Installation

Download **m2wh** from server and make it executable:

```shell
$ wget http://files.maximilianoledesma.com/m2wh
$ sudo chmod +x m2wh
```
If you want to use the tool locally:

```shell
$ sudo cp m2wh /usr/local/bin/m2wh
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
|**FRONTEND**|
|`-cs, --clear-static theme`  | Remove all static files deployed on pub folder for specific theme
|`-sd, --static-deploy theme` | Clear the cache, remove static files and deploy static content through bin/magento setup:static-content:deploy command for specified theme
|**CACHE**|  |
|`-cc, --cache-clear`| Clear cache with bin/magento cache:clear command
|`-cf, --cache-flush`| Flush cache with bin/magento cache:flush command
|`-fr, --flush-redis`| Flush REDIS cache using warden env exec redis redis-cli flushall command
|**USERS**|
|`-auc, --admin-user-create`|Runs bin/magento admin:user:create to create an Admin User<br>
|`-cuc, --customer-user-create`|Runs n98-magerun customer:create to create a customer<br>
|**DEVELOPMENT**|
|`-de, --developer-enable`|Set deploy mode to developer
|`-he, --hints-enable`|Enable template hints and clear cache
|`-hd, --hints-disable`|Disable template hints and clear cache
|`-td, --tail-debug`|Show the last var/log/debug.log entries
|`-ts, --tail-system`|Show the last var/log/system.log entries

