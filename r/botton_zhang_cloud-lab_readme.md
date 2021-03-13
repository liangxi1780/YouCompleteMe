**关注作者公众号**：
 
 
 

# Cloud Lab

[Cloud Lab](http://u.720life.cn/g/89ec319fe9b4a8ac67d6206b627413f1a515851983456c9bede72c960a920931)  is a Docker based online lab center, it integrates many popular computer
science courses and provides a Docker based experiment environment as-is.

## Quickstart

### Install docker

Cload Lab is docker based, please make sure docker environment is installed with [Docker CE](http://u.720life.cn/g/fbcb5bd9a3bc55a12a4e45d1e387dd7ef3463024c5ce40665d158e68e4e437ac97d206a0b52434428869f67ee27268db59874547d6875b09bcd3787ca14b3b8bee2ecf19aefe0cdae8db28366b5e9b7e  Docker CE support Mac, Windows, Ubuntu, Debian, Fedora, CentOS, Azure and AWS, we have tested Cloud Lab with Docker CE in Ubuntu and Mac.

The old install method for Windows and Mac OSX is [Docker Toolbox](http://u.720life.cn/g/d13d2b0ef4a5c92b4f4a6e9ed4270e653fd0e1904962069996af3d80a15b889109da835a996235354ee6ae7742495d63 

### Configure docker

In order to run docker without password, please make sure your user is added in the docker group:

    $ sudo usermod -aG docker $USER

In order to speedup docker images downloading, please configure a local docker mirror in `/etc/default/docker`, for example:

    $ grep registry-mirror /etc/default/docker
    DOCKER_OPTS="$DOCKER_OPTS --registry-mirror=https://docker.mirrors.ustc.edu.cn"
    $ service docker restart

In order to avoid network ip address conflict, please try following changes and restart docker:

    $ grep bip /etc/default/docker
    DOCKER_OPTS="$DOCKER_OPTS --bip=10.66.0.10/16"
    $ service docker restart

If the above changes not work, try something as following:

    $ grep dockerd /lib/systemd/system/docker.service
    ExecStart=/usr/bin/dockerd -H fd:// --bip=10.66.0.10/16 --registry-mirror=https://docker.mirrors.ustc.edu.cn
    $ service docker restart

If installed via Docker Toolbox, to access the Lab page, we must get and use the `eth1` ip address, just replace 'localhost' with this ip in the Lab page url:

    $ ifconfig eth1 | grep 'inet addr' | tr -s ' ' | tr ':' ' ' | cut -d' ' -f4
    192.168.99.100

If the Linux system is installed on Virtualbox by ourselves, to access the Lab page outside, we must add the eth1 network device at first via setting: 'Network -> Adapter2 -> Host-only Adapter'.

### Choose a working directory

If installed via Docker Toolbox, please enter into the `/mnt/sda1` directory of the `default` system on Virtualbox, otherwise, after poweroff, the data will be lost for the default `/root` directory is only mounted in DRAM.

    $ cd /mnt/sda1

For Linux or Mac OSX, please simply choose one directory in `~/Downloads` or `~/Documents`.

    $ cd ~/Documents

### Download cloud-lab

    $ git clone https://github.com/tinyclub/cloud-lab.git

### Choose a Lab

    $ tools/docker/choose

    Current Lab is: linux-lab

    Available Labs:

         1	cs630-qemu-lab
         2	linux-0.11-lab
         3	linux-lab
         4	markdown-lab
         5	qing-lab
         6	tinylab.org

    Choose the lab number: 2
         2	linux-0.11-lab


    Download the lab...

### Run the Lab

    $ tools/docker/run

### Remove the Lab

    $ tools/docker/rm

### Stop the Lab

    $ tools/docker/stop

### Start the Lab

    $ tools/docker/start

### Update everything

    $ tools/docker/update

### Autostart everything

    $ tools/docker/autostart

### Run as root without password

If get syntax error under `/etc/sudoers*`, please use `pkexec visudo` to fix up it.

    $ sudo -s
    $ echo "$SUDO_USER ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/$SUDO_USER



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)