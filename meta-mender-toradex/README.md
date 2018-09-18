# Mender integration for Toradex SoMs

Supported SoMs:

- Colibri VF61
- Colibri iMX7 (NAND)

## Build

Download the source:

    $ mkdir mender-toradex
    $ cd mender-toradex
    $ repo init \
           -u https://github.com/mirzak/meta-mender-community \
           -m meta-mender-toradex/scripts/manifest-toradex.xml \
           -b rocko

Setup environment

    $ export MENDER_LAYER=${PWD}/sources/meta-mender-community/meta-mender-toradex
    $ export TEMPLATECONF=${MENDER_LAYER}/templates/
    $ . sources/openembedded-core/oe-init-build-env build

Build

    $ bitbake core-image-base
