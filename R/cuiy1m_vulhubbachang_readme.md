# Vulhub - Pre-Built Vulnerable Environments Based on Docker-Compose

[![Docker Stars](https://img.shields.io/badge/docker%20stars-20k-blue.svg)](https://hub.docker.com/u/vulhub/) [![GitHub](https://img.shields.io/github/license/vulhub/vulhub.svg)](https://github.com/vulhub/vulhub/blob/master/LICENSE)
 [![Chat on Discord](https://img.shields.io/discord/485505185167179778.svg)](https://discord.gg/GhMB3Z) [![Backers and sponors on Patreon](https://img.shields.io/badge/sponsor-patreon-73d6a1.svg)](https://www.patreon.com/phith0n) [![Backers and sponors on Opencollective](https://img.shields.io/badge/backer-opencollective-f89a76.svg)](https://opencollective.com/vulhub#backer)

[中文版本(Chinese version)](README.zh-cn.md)

 Vulhub is an open-source collection of pre-built vulnerable docker environments. No pre-existing knowledge of docker is required, just execute two simple commands and you have a vulnerable environment.

## Installation

Install the docker/docker-compose on Ubuntu 16.04:

```bash
# Install pip
curl -s https://bootstrap.pypa.io/get-pip.py | python3

# Install the latest version docker
curl -s https://get.docker.com/ | sh

# Run docker service
service docker start

# Install docker compose
pip install docker-compose
```

The installation steps of docker and docker-compose for other operating systems might be slightly different, please refer to the [docker documentation](http://u.720life.cn/g/fe36d46bcf13791bdad89a5e154210d994ad984a1bc907472e7c73c1a5a147cf)  for details.

## Usage

```bash
# Download project
wget https://github.com/vulhub/vulhub/archive/master.zip -O vulhub-master.zip
unzip vulhub-master.zip
cd vulhub-master

# Enter the directory of vulnerability/environment
cd flask/ssti

# Compile environment
docker-compose build

# Run environment
docker-compose up -d
```

There is a **README** document in each environment directory, please read this file for vulnerability/environment testing and usage.

After the test, delete the environment with the following command.
```
docker-compose down -v
```

It is recommended to use a VPS of at least 1GB memory to build a vulnerability environment. The `your-ip` mentioned in the documentation refers to the IP address of your VPS. If you are using a virtual machine, it refers to your virtual machine IP, not the IP inside the docker container.

**All environments in this project are for testing purposes only and should not be used as a production environment!**

## Notice

1. To prevent permission errors, it is best to use the root user to execute the docker and docker-compose commands.
2. Some docker images do not support running on ARM machines.

## Contribution

This project relies on docker. So any error during compilation and running are thrown by docker and related programs. Please find the cause of the error by yourself first. If it is determined that the dockerfile is written incorrectly (or the code is wrong in vulhub), then submit the issue. More details please 👉[Common reasons for compilation failure](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468365c021e869ef2659f63a6def80e020d82de5d453cbd5665b32fed2ff3bca2b3da2cda8d195e147e6ff217c654806ea092c29da2e7435123161de9dae094a1245f4356ece136fd86956c2d4b33a86c75986ae9b6d3dc91c00e9f8f3338330bf  hope it can help you.

For more question, please contact:

- [Discord](http://u.720life.cn/g/f2a7d7b12e1fc16eaafd863db538a1832edb4cf002f5304e331c492471e6e87d) 
- [Twitter](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54feedec4c05accb40a33c7990133bfbd545) 

Thanks for the following contributors:

[![](https://opencollective.com/vulhub/contributors.svg?width=890&button=false)](https://github.com/vulhub/vulhub/graphs/contributors)

More contributors：[Contributors List](contributors.md)

## Backer and Sponsor

Sponsor:

 
     
     
     
 

Sponsor vulhub on patreon 🙏

   

Sponsor vulhub on opencollective 🙏

 
     
     
 

More[Donate]http://vulhub.org/#/docs/donate/)。

## License

Vulhub is licensed under the MIT License. See [LICENSE](LICENSE) for the full license text.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)