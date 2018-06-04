# Demo Site For Bricks Talk At MiniCamp Online 2018

This is a simple Dupal 8 site used to demo site building using Bricks and ECK. It uses [Docksal](https://docksal.io/) but that isn't required.

## Setup

If you're using Docksal just run the following commands starting in the root directory.

```
fin start
cd docroot
fin exec composer install
fin exec "drush sqlc <../backup/db.sql"
cd sites/default
unzip ../../../backup/file.zip
chmod -R a+w files
fin drush cr all
```

Note: The sites/default/services.local.yml and sites/default/settings.local.php files are checked into git so the above should work out of the box. If you're not using docksal or have different database connection information just modify the sites/default/settings.local.php file.

## Database and Files Content

The backup directory contains a database dump and and archive of the sites/default/files directory you can use to get a site very similar to (or the same as) the site at the end of the demo.
