# drupal-config-snapshot
Script for creating a snapshot of configuration in a git repository

## Installation
Requirements:
* Drupal needs to have 'drush' installed and it should be available as `vender/bin/drush/` from drupal's directory.
* In drupal's settings.php the 'config_sync_directory' should be enabled with the path `config` from drupal's directory.
* Create the `config` directory and run `git init` to initialize the repository.

Installation of the script:
```sh
cd /path/to/drupal
git clone https://github.com/plepe/drupal-config-snapshot
mkdir config
cd config ; git init
```

## Snapshot
Create a snapshot (you might want to create cronjob):
```sh
DRUPAL_PATH=/path/to/drupal drupal-config-snapshot/config-snapshot
```
