docker-available-tools
======================

https://github.com/rsp/docker-available-tools

Test what tools that are useful in shell scripts are available by default
in Docker containers with some popular distribution minimal images
(or any image).

Prerequisites
-------------
* [Bash](https://www.gnu.org/software/bash/)
* [Docker](https://www.docker.com/)

It should work on any standard Linux distribution. If it doesn't,
please [sumbit an issue](https://github.com/rsp/docker-available-tools/issues).

It is written and tested on Ubuntu 14.04
with Docker version 1.5.0, build a8a31ef.

### Note:
Make sure you have sufficient permissions to run `docker`.
You may need to run the scripts with: `sudo ./script-name`.
You need to be in the same directory as the scripts
becasue they run each other with `./script-name`.

Commands
--------

### `check-images "image1 image2 ..."`

E.g. `sudo ./check-images "centos debian ubuntu"`

Checks if the given list of images can be run. Used by other scripts.

### `system-info "image1 image2 ..."`

E.g. `sudo ./system-info "centos debian ubuntu"`

Shows the name and version of the operating system distribution
that is run using that image name.

Results of experiments
----------------------

Here are some results of experiments that were done with those scripts.

### Names and versions of OS distributions

Here are the names and versions of OS distros
used by some of the popular images - as of 2015-03-07:

Image | OS
----- | --
debian | Debian GNU/Linux 7 (wheezy)
ubuntu | Ubuntu 14.04.2 LTS
centos | CentOS Linux 7 (Core)
fedora | Fedora 21 (Twenty One)
opensuse | openSUSE 13.2 (Harlequin) (x86_64)
mageia | Mageia 4
busybox | Buildroot 2014.02
python | Debian GNU/Linux 8 (jessie)
ruby | Debian GNU/Linux 8 (jessie)
perl | Debian GNU/Linux 8 (jessie)
gcc | Debian GNU/Linux 7 (wheezy)
node | Debian GNU/Linux 8 (jessie)
iojs | Debian GNU/Linux 8 (jessie)
redis | Debian GNU/Linux 7 (wheezy)
nginx | Debian GNU/Linux 7 (wheezy)
postgres | Debian GNU/Linux 7 (wheezy)
mysql | Debian GNU/Linux 7 (wheezy)
mongo | Debian GNU/Linux 7 (wheezy)
rethinkdb | Debian GNU/Linux 8 (jessie)

Almost every image except specific distributions
seems to be based on Debian - some on version 7, some on 8.

Author
------
[Rafał Pocztarski](https://github.com/rsp)

License
-------
MIT License (Expat). See [LICENSE.md](LICENSE.md) for details.
