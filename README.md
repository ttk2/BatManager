#BatManager

This is an Ansible Playbook for managing a BATMAN-adv development mesh across heterogenous architectures.

Please note that it requires a backend connection that will remain online while the new mesh is installed.

##What It Does

* Copies local development repositories to mesh nodes
* Installs complilation dependencies
* Compiles and installs code pushed earlier
* Sets up interfaces and mesh attributes
* Starts the mesh

##What's Currently Supported

* Intel Compute Stick running Fedora
* Raspberry PI 3's running Raspbian


##Usage

* Clone batctl, batman-adv and other requirements into the same folder as this script
* Configure the `group_vars/all.yml` with repositories, interface names, mesh names, and other variables as required
* Add mesh devices to the hosts file, be sure to overlap a hardware category with the general mesh category to allow hardware specific setup
* Finally run `ansible-playbook -i hosts update-batman.yml`
