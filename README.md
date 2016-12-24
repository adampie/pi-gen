# pi-gen with Ansible

Automating the generation of Raspbian images for the Raspberry Pi using Ansible. 
This started as part of a university final year computer science project.

## Getting Started

The original pi-gen script can be found here - [pi-gen](https://github.com/RPi-Distro/pi-gen) 

Latest integration - a9c27d2 from Dec 6, 2016

*This will get updated as the project progresses*

|Code|Status|
|----|--------------|
|stage4| Code done (FIX PYTHON GAMES), Not implemented yet |
|stage3| Code done, Not implemented yet |
|stage2| Code 50% done, Not implemented yet|
|stage1|Not yet|
|stage0|Not yet|
|scripts|Not yet|

### TeamCity
*Insert when done*

### Prerequisites
#### Vagrant
- Vagrant
- VirtualBox
- pi-gen box - https://atlas.hashicorp.com/adampie/boxes/pi-gen

#### Docker
- Docker

#### Manual
Debian system with *Ansible* installed along with the following packages for pi-gen:
```
quilt kpartx realpath qemu-user-static debootstrap zerofree pxz zip dosfstools bsdtar libcap2-bin
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
Create a file called 'config' with the following inside
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
* [pi-gen](https://github.com/RPi-Distro/pi-gen) - The original pi-gen project
* [Ansible](https://www.ansible.com/) - Configuration management and deployment tool
* [Packer](https://www.packer.io/) - Tool for creating machine and container images for multiple platforms.

## Contributing
You are more than welcome to contribute to this project.

## License
This project is licensed under the BSD-3-Clause License - see the [License.md](License.md) file for details.
