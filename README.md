![GitHub](https://img.shields.io/github/license/maxiledesma/whelper?style=flat-square)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/maxiledesma/whelper?style=flat-square)
# WHELPER
### Warden helper for Magento 2
By **Maximiliano Ledesma**

A tool that helps to run commands more easily, in environments created with Warden.

### Installation

```shell
$ mkdir $HOME/bin
$ echo 'export PATH="$HOME/bin:$PATH"' >> $HOME/.bashrc
$ source ~/.bashrc
$ wget --no-check-certificate https://github.com/maxiledesma/whelper/tarball/1.0.1-beta -P /tmp/

```

### Usage:
```shell
$ whelper [options]
```

### Options:

`h, --help`
Show brief help

### Available commands:
##### Frontend:
`-cs, --clear-static theme`: Remove all static files deployed on pub folder for specific theme<br>
`-sd, --static-deploy theme`: Clear the cache, remove static files and deploy static content through bin/magento setup:static-content:deploy command for specified theme

#### Cache:
`-cc, --cache-clear` Clear cache with bin/magento cache:clear command<br>
`-cf, --cache-flush` Flush cache with bin/magento cache:flush command<br>
`-fr, --flush-redis` Flush REDIS cache using warden env exec redis redis-cli flushall command

#### Users:
`-auc, --admin-user-create` Runs bin/magento admin:user:create to create an Admin User<br>
`-cuc, --customer-user-create` Runs n98-magerun customer:create to create a customer<br>

#### Development:
`-de, --developer-enable` Set deploy mode to developer<br>
`-he, --hints-enable` Enable template hints and clear cache<br>
`-hd, --hints-disable` Disable template hints and clear cache<br>
`-td, --tail-debug` Show the last var/log/debug.log entries<br>
`-ts, --tail-system` Show the last var/log/system.log entries
