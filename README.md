# Magento 2 Purge - a simple Magento 2 purge tool for developers
A simple bash script that will completely purge all Magento 2 static content, dependency injection, generated classes and then flush the cache with the built in Magento 2 CLI.

This script empties the following Magento 2 directories:

```sh
pub/static/*
generated/*
var/cache/*
var/di
var/composer_home/*
var/generation/*
var/page_cache/*
var/view_preprocessed/*
```

## Installation
To download the script and make it available to run from anywhere, run these commands:

### Download the latest script:
It doesn't really matter where you do this in the filesystem, as we will move the script to it's new home in the next step.
```sh
wget https://github.com/BenButterfield/m2purge/blob/master/m2purge
```

### Make the script executable (requires sudo rights):
Without doing this, you will not be able to run the script.
```sh
sudo chmod +x m2purge
```

### Make the script available to all users (requires sudo rights):
If you have multiple 
```sh
sudo mv m2purge /usr/local/bin/m2p
```



## Usage
Navigate to your Magento 2 root directory and then run:
```sh
m2p
```