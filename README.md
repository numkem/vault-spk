# vault-spk

This package is heavily based from the work done for [gogs-spk](https://github.com/alexandregz/gogs-spk)

[vault](https://vaultproject.io) (Secret storage) SPK package ([Synology PacKages](https://www.synology.com/en-us/dsm/app_packages))

Install vault into a Synology NAS.

## Requirements

Only tested on x64 (DS916+) could work on ARM since a vault binary exists.

## Usage

Change **Package Center -> Trust Level** to **Any Publisher** and import manually the package from **Manual install**.
Finally, install with vault web installation.

## Configuration

You can store your configuration using a `conf.d` folder inside `1_create_package/vault/`. If you don't want to ship your configurations with the package, you can use `/etc/vault`.

## To use with another arch

Download the binary from https://www.vaultproject.io/downloads.html, replace the content from **1_create_package/vault** directory and exec create_spk.sh:

```~/src/vault-spk(master)$ rm -rf 1_create_package/vault/ && unzip vault_1.1.2.zip && mv vault ./1_create_package/```

```$ sh create_spk.sh```

