# About

This is a collection of tools and scripts that we use at [WOW WP](https://wowwp.com) to cleanup a hacked WordPress website. Some of these tools/scripts are written in bash, so will require shell access. Shell access is faster, but you may not always get it in shared hosting setup, so I have added equivalent PHP scripts.

## Scripts

1. **.htaccess** - .htaccess rules to block all traffic except yours. Please, remember to replace the IP. 
2. **backup.sh** - This script will install wp-cli, which will be used to backup the database, core files, plugins, etc. 