[![LXD](https://linuxcontainers.org/static/img/containers.png)](https://linuxcontainers.org/lxd)
# lxc-utils

This repo provides the well-known and heavily tested command line utilities to
interact with the [LXC](https://github.com/lxc/lxc) low-level Linux container
runtime. The main tools it provides are:

## Container Commands

Commands that operate on individual containers can be given the name of the
container either via the traditional unix-style command line flag syntax
(`lxc-start -n <container-name>`) syntax or without it (`lxc-start <container-name>`).
This includes:

- `lxc-attach`
- `lxc-cgroup`
- `lxc-checkpoint`
- `lxc-console`
- `lxc-copy`
- `lxc-create`
- `lxc-destroy`
- `lxc-device`
- `lxc-execute`
- `lxc-freeze`
- `lxc-info`
- `lxc-snapshot`
- `lxc-start`
- `lxc-stop`
- `lxc-unfreeze`
- `lxc-wait`

## Generic Commands

These commands do not operate on multiple containers or system settings for
containers.

- `lxc-autostart`
- `lxc-config`
- `lxc-ls`
- `lxc-monitor`
- `lxc-top`

## Utility Commands

These commands are generic helpers usually for interacting with generic
containerization features provided by the Linux kernel. They have mostly been
surpassed by generic Linux core utilities and are kept around for legacy
reasons.

- `lxc-unshare`

## Status
Type            | Service               | Status
---             | ---                   | ---
CI (Linux)      | Jenkins               | [![Build Status](https://jenkins.linuxcontainers.org/job/lxc-github-commit/badge/icon)](https://jenkins.linuxcontainers.org/job/lxc-github-commit/)
CI (Linux)      | Travis                | [![Build Status](https://travis-ci.org/lxc/lxc.svg?branch=master)](https://travis-ci.org/lxc/lxc/)
Project status  | CII Best Practices    | [![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/1087/badge)](https://bestpractices.coreinfrastructure.org/projects/1087)

## Reporting Security Issues

The LXC project has a good reputation in handling security issues quickly and
efficiently. If you think you've found a potential security issue, please
report it by e-mail to all of the following persons:

- serge.hallyn (at) ubuntu (dot) com
- stgraber (at) ubuntu (dot) com
- christian.brauner (at) ubuntu (dot) com

For further details please have a look at

- https://linuxcontainers.org/lxc/security/

## Becoming Active in LXC development

We always welcome new contributors and are happy to provide guidance when
necessary. LXC follows the kernel coding conventions. This means we only
require that each commit includes a `Signed-off-by` line. The coding style we
use is identical to the one used by the Linux kernel. You can find a detailed
introduction at:

- https://www.kernel.org/doc/html/v4.10/process/coding-style.html

and should also take a look at the [CONTRIBUTING](CONTRIBUTING) file in this
repo.

If you want to become more active it is usually also a good idea to show up in
the LXC IRC channel `#lxc-dev` on `Freenode`. We try to do all development out
in the open and discussion of new features or bugs is done either in
appropriate Github issues or on IRC.

When thinking about making security critical contributions or substantial
changes it is usually a good idea to ping the developers first and ask whether
a PR would be accepted.

## Semantic Versioning

LXC and its related projects strictly adhere to a [semantic
versioning](http://semver.org/) scheme.

## Downloading the current source code

Source for the latest released version can always be downloaded from

- https://linuxcontainers.org/downloads/

You can browse the up to the minute source code and change history online

- https://github.com/lxc/lxc

## Building LXC

Without considering distribution specific details a simple

    ./autogen.sh && ./configure && make && sudo make install

is usually sufficient.

### Discuss Forum

We maintain an discuss forum at

- https://discuss.linuxcontainers.org/

where you can get support.

### IRC

You can find support by joining `#lxcontainers` on `Freenode`.

### Mailing Lists

You can check out one of the two LXC mailing list archives and register if
interested:

- http://lists.linuxcontainers.org/listinfo/lxc-devel
- http://lists.linuxcontainers.org/listinfo/lxc-users
