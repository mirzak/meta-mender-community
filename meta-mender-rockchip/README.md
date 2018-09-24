# Mender integration for Rockchip based boards

Supported boards:

- Tinker Board

## Build

Download the source:

    $ mkdir mender-rockchip
    $ cd mender-rockchip
    $ repo init \
           -u https://github.com/mirzak/meta-mender-community \
           -m meta-mender-rockchip/scripts/manifest-rockchip.xml \
           -b wip/poc-append
    $ repo sync

Setup environment

    $ . setup-environment rockchip

Build

    $ bitbake core-image-base
