# M2Purge - a simple purge tool for Magento 2 developers
There's nothing more annoying than making a change on Magento 2, flushing the cache, and then not seeing your change reflected. This super simple tool provides an easy way for you to purge Magento 2 in a safe, quick and convenient way.

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

And then flushes the cache using the built in Magento 2 CLI:

```sh
bin/magento cache:flush
```

## Installation

#### 1. Download the latest version of the script
It doesn't really matter where you are in your filesystem, as we will move the script to it's new home in step 3.
```sh
wget https://raw.githubusercontent.com/BenButterfield/m2purge/master/m2purge.sh
```

#### 2. Make the script executable (requires sudo rights)
This allows a user to execute the script in an SSH terminal.
```sh
sudo chmod +x m2purge.sh
```

#### 3. Make the script available to all users (requires sudo rights)
By moving the script here and changing the name, you allow it to be run from anywhere in your filesystem using shorthand.
```sh
sudo mv m2purge.sh /usr/local/bin/m2p
```



## Usage
Navigate to your Magento 2 root directory and then run:
```sh
m2p
```