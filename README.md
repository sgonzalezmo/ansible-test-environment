# Ansible Test Environment

Simple vagrantfile to provisioning test environment to evaluate the ansible capabilities.

## Requirements

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads). Tested on 6.1.x.
- [Vagrant](http://www.vagrantup.com/downloads.html). Tested on 2.2.14
- [Ansible](http://docs.ansible.com/intro_installation.html). Tested on 2.10.

## Usage

1. Clone the repository:

```
git clone https://github.com/sgonzalezmo/ansible-test-environment.git
```

2. Edit de Vagrantfile and modify de NODES variable, enter the number of nodes to be provisioned.

```
NODES = 1
```

3. Run the following command:

```
vagrant up
```

## License

MIT license.

## Author Information

Created in 2017 by [Samuel Gonzalez Morro](mailto:sgonzalezmo@gmail.com).
