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

Author
------
[Rafał Pocztarski](https://github.com/rsp)

License
-------
MIT License (Expat). See [LICENSE.md](LICENSE.md) for details.
