# Ansible Test Environment

Simple vagrantfile to provisioning test environment to evaluate the ansible capabilities.

## Requirements

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads). Tested on 5.1.x.
- [Vagrant](http://www.vagrantup.com/downloads.html). Tested on 1.9.6
- [Ansible](http://docs.ansible.com/intro_installation.html). Tested on 2.3.

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

## Testing

1. Run the following command to connect to ansible-master virtual machine. 

```
vagrant ssh ansible-master
```

2. Run the following command to clone sgonzalezmo/ansible-examples repository in ansible-master

```
git clone https://github.com/sgonzalezmo/ansible-examples.git
```

3. Create a file hosts in ansible-examples/ping and add all ansible-nodes. Example:

```
10.0.0.11
10.0.0.12
10.0.0.13
```

4. Finally, run the following command to execute ping playbook.

```
ansible-playbook ping.yml -i hosts
```

## License

MIT license.

## Author Information

Created in 2017 by [Samuel Gonzalez Morro](mailto:sgonzalezmo@gmail.com).
