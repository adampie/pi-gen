# pi-gen with Ansible

Automating the generation of Raspbian images for the Raspberry Pi using Ansible. 
This started as part of a university final year computer science project.

## Getting Started

The original pi-gen script can be found here - [pi-gen](https://github.com/RPi-Distro/pi-gen) 

Latest integration - a9c27d2 from Dec 6, 2016

*This will get updated as the project progresses*

|Code|Status|
|----|--------------|
|stage4| Code 100% done, Not implemented yet |
|stage3| Code 100% done, Not implemented yet |
|stage2| Code 50% done, Not implemented yet|
|stage1|Not yet|
|stage0|Not yet|
|scripts|Not yet|

|Extra|Status|
|----|--------------|
|Jenkins integrated|Soon|
|Automated build images|Soon|

### Prerequisites
#### Automated
Using docker - *Insert when done*

Using vagrant - *Insert when done*

Extra - *https://github.com/adampie/pi-gen-packer*

#### Manual
Debian system with Ansible installed with the following packages for pi-gen:
```
quilt kpartx realpath qemu-user-static debootstrap zerofree pxz zip dosfstools bsdtar libcap2-bin
```

### Generating the images
#### Automated
*Insert when implemented*
#### Manual
Create a file called 'config' with the following inside, you can change Raspbian if you want:
```
IMG_NAME='Raspbian'
```

Run the 'build' script as root to start. 

```
sudo ./build.sh
```
## Built With

* [pi-gen](https://github.com/RPi-Distro/pi-gen) - The original pi-gen project
* [Ansible](https://www.ansible.com/) - Configuration management and deployment tool

## Contributing

You are more than welcome to contribute to this project.

## License

This project is licensed under the BSD-3-Clause License - see the [License.md](License.md) file for details.
