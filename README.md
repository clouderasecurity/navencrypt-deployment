# Navigator encrypt Bash Deployment Scripts

## Overview

This repository houses Cloudera's Bash scripts built to enhance the user experience of a Cloudera Navigator encrypt deployment.

In order to encrypt and protect your data, there are two separate steps:
* Install Navigator encrypt (`navencrypt-install.sh`), all automated
* Configure Navigator encrypt (`navencrypt-configure.sh`), which will prompt you for input through every step of the process
* Automatically configure Navigator encrypt (`navencrypt-autoconfigure.sh`), all automated (if you modify the appropriate variables first)

Please note that these scripts are meant for testing purposes only, and come with absolutely no warranty *whatsoever*.

## Install

Simply copy the following command into a Linux terminal to get started:
```
curl -sL https://archive.gazzang.com/deployment/navencrypt-install.sh | sudo bash
```

This will attempt to install Navigator encrypt based on your current environment. This script can be run multiple times without conflict.

## Configure

Once Navigator encrypt is installed, you will need to apply the correct settings in order to encrypt (and access) your data.

### Automated

If you want to automatically configure Navigator encrypt without being prompted, you can do so by copying the following command into your terminal:

```
curl -O https://archive.gazzang.com/deployment/navencrypt-autoconfigure.sh
```

And then edit the 8 variables at the top of the `navencrypt-autoconfigure.sh` script with the appropriate values pertaining to your environment. This script was designed to be run multiple times without issue (assuming the variables don't change between runs).

### Interactive

To be prompted at every step of the configuration, we have an 'interactive install' script designed to guide you through the process.

To get started, copy the following command into a Linux terminal to configure:

```
curl -sL https://archive.gazzang.com/deployment/navencrypt-configure.sh | sudo bash
```

Which will prompt you for input to register and configure Navigator encrypt. This script can also be run multiple times without issue. Please note that this script was designed for very simple deployments, and should not be used for anything too complicated.
