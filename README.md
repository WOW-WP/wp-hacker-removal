# WordPress Malware/Backdoor Removal

This is a collection of tools and scripts that we use at [WOW WP](https://wowwp.com) to cleanup a hacked WordPress website. Some of these tools/scripts are written in bash, so will require shell access. Shell access is faster, but you may not always get it in shared hosting setup, so I have added equivalent PHP scripts.

## Checklist 
 - [ ] Take the website offline ([Maintainance](https://wordpress.org/plugins/maintenance/)/[.htaccess](https://github.com/WOW-WP/wp-hacker-removal/blob/main/htaccess)/ask hosting).
 - [ ] Revoke all access and change passwords ([cPanel](https://docs.cpanel.net/knowledge-base/security/how-to-reset-a-cpanel-account-password/), WordPress, FTP/SFTP, Shell, etc.).
 - [ ] Backup database and core files ([cPanel](https://docs.cpanel.net/cpanel/files/backup-for-cpanel/)/[Updraft](https://wordpress.org/plugins/Updraftplus/)/[script for VPS](https://github.com/WOW-WP/wp-hacker-removal/blob/main/backup.sh)).
 - [ ] Restore all WordPress core, plugin and theme files.
 - [ ] Clean up the database  (check for injected scripts, etc.)
 - [ ] Scan, remove any unwanted files in the installation directory.
 - [ ] Clean up upload folder (remove any code or unwanted files).
 - [ ] Change all [salts](https://api.wordpress.org/secret-key/1.1/salt/) in wp-config.php and update database credentials.
 - [ ] Set correct file permissions (Folders: 755, Files: 644).
 - [ ] Disable file editing in wp-config.php
 - [ ] Install a security plugin (Wordfence, Sucuri, etc.)
 - [ ] Limit login attempts and enable 2FA for all admin users.
 - [ ] Check [Google Search Console](https://search.google.com/search-console) for issues and request review if [blacklisted](https://sitecheck.sucuri.net/).
 - [ ] Resubmit sitemap after cleaning.
 - [ ] Setup weekly malware scans. 

## Scripts

 1. **.htaccess** - .htaccess rules to block all traffic except yours. Please, remember to replace the IP. 
2. **backup.sh** - This script will install wp-cli, which will be used to backup the database, core files, plugins, etc. 

## Need help?
In some cases, you may need to inspect the uploads directory and the database for injected scripts. If you need our help, feel free to reach out to us at help@wowwp.com