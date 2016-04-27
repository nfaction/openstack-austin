# OpenStackAnsible: Work session

## Ubuntu 16.04

### Differences we know about:
* init vs systemd vs openrc
* package names, groups, versions
* some of this is covered in the apt/yum var pattern: [https://review.openstack.org/274290]()
* network configuration mechanisms
* configuration requirements (policy kit, selinux, apparmor)
* lxc base image and changes to it for our requirements
* <https://review.openstack.org/307856>
* python 3 / different default python versions.  Python2 is available, just needs to be installed
* file placement locations for core infrastructure components (mariadb, rabbitmq)
* whether to use the distro packages, or the package from the source (mariadb, rabbitmq)


## Main discussion over how Refstack is used

Big discussion over anonymous vs non-anonymous and how data should be retained.