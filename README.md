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

#### 1. Download the latest version of the script:
It doesn't really matter where you do this in the filesystem, as we will move the script to it's new home in the next step.
```sh
wget https://raw.githubusercontent.com/BenButterfield/m2purge/master/m2purge
```

#### 2. Make the script executable (requires sudo rights):
Without doing this, you will not be able to run the script.
```sh
sudo chmod +x m2purge
```

#### 3. Make the script available to all users (requires sudo rights):
This allows you to use a shorthand command anywhere you like in your filesystem.
```sh
sudo mv m2purge /usr/local/bin/m2p
```



## Usage
Navigate to your Magento 2 root directory and then run:
```sh
m2p
```