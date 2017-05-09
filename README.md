# pi-gen with Ansible

Automating the generation of Raspbian images for the Raspberry Pi using Ansible.
This started as part of a university final year computer science project.

## Getting Started

The original pi-gen script can be found here - [pi-gen](https://github.com/RPi-Distro/pi-gen)

### Prerequisites
#### Vagrant
- Vagrant
- VirtualBox
- pi-gen box - https://atlas.hashicorp.com/adampie/boxes/pi-gen

#### Manual
Debian system with *Ansible* installed along with the following packages for pi-gen:
```
quilt parted realpath qemu-user-static debootstrap zerofree pxz zip dosfstools bsdtar libcap2-bin grep rsync
```
or run (will be integrated automatically with build in the future)
```
ansible-playbook dependencies.yml
```
### Generating the images
#### Automated
```
vagrant init adampie/pi-gen; vagrant up --provider virtualbox; vagrant ssh

cd pi-gen; mv config.example config; sudo ./build.sh
```
#### Manual
Create a file called 'config' with the following inside.
```
IMG_NAME='Raspbian'
```
or do
```
mv config.example config
```

Run the 'build' script as root to start.
```
sudo ./build.sh
```

## Built With
* [pi-gen](https://github.com/RPi-Distro/pi-gen) - The original pi-gen project.
* [Ansible](https://www.ansible.com/) - Configuration management and deployment tool.
* [Packer](https://www.packer.io/) - Tool for creating machine and container images for multiple platforms, repo [here](https://github.com/adampie/pi-gen-packer).

## Contributing
You are more than welcome to contribute to this project.

## License
This project is licensed under the BSD-3-Clause License - see the [License.md](License.md) file for details.
