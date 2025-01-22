# Overleaf Toolkit

This repository contains the Overleaf Toolkit, the standard tools for running a local
instance of [Overleaf](https://overleaf.com). This toolkit will help you to set up and administer both Overleaf Community Edition (free to use, and community supported), and Overleaf Server Pro (commercial, with professional support).

The [Developer wiki](https://github.com/overleaf/overleaf/wiki) contains further documentation on releases, features and other configuration elements.


# Getting Started: Deployment Notes

## Build the necessary images first

Build the community image Overleaf-ce (lean version).

```
git clone git@github.com:florentchandelier/overleaf.git
cd /overleaf/server-ce
git checkout overleaf-ce
make lean
```

## Build and Deploy the services

```
git clone git@gitlab.com:invariantinc/it/overleaf-toolkit.git
cd overleaf-toolkit
bin/init
```

Edit `config/overleaf.rc` as necessary.

... and deploy

```
bin/up
```

## Documentation

See [Quick Start Guide](./doc/quick-start-guide.md).
See [Documentation Index](./doc/README.md)


## Getting Help

Users of the free Community Edition should [open an issue on github](https://github.com/overleaf/toolkit/issues). 

Users of Server Pro should contact `support@overleaf.com` for assistance.

In both cases, it is a good idea to include the output of the `bin/doctor` script in your message.

