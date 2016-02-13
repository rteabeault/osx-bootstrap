# OS X Bootstrap
Prepares OS X to be bootstrapped with Ansible.

### bootstrap
Running `bootstrap` will prepare OS X to run ansible.

##### Assumptions
* Your user is in the admin group.

##### What it does
* Prompt you for your sudo password
* Enable passwordless sudo for the admin account. This will create the 
file `/private/etc/sudoers.d/01_admin_passwordless_sudo` with the content
  `%admin ALL=(ALL) NOPASSWD: ALL`
* Install the OS X command Line Tools. 
* Installs `pip` using `easy_install`.
* Installs `ansible` using `pip`.
* Installs any requirements specified in `requirements.yml` using `ansible-galaxy`.
