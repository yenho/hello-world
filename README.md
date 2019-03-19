
In MS ELL,

1. ubuntu 18.04, cannot be compiled even with the below command --
```shell
cmake -DLLVM_DIR=/usr/lib/llvm-3.9/lib/cmake/llvm ..
```

2. MAC OS, should use the below cmake command to build the code --
```shell 
 cmake -DLLVM_DIR=/usr/local/Cellar/llvm@3.9/3.9.1_1/lib/cmake/llvm ..
```

From: https://github.com/Microsoft/ELL/blob/master/INSTALL-Ubuntu.md
and https://github.com/Microsoft/ELL/blob/master/INSTALL-Mac.md

--

Netdata

 * Pre
```shell 
sudo apt-get install build-essential zlib1g-dev gcc make git autoconf autogen automake pkg-config
 ** Alternative for git clone method
sudo apt-get install zlib1g-dev uuid-dev libmnl-dev gcc make autoconf autoconf-archive autogen automake pkg-config curl
sudo apt-get install python python-yaml python-mysqldb python-psycopg2 nodejs lm-sensors netcat
```

```shell 
Linux 64bit installation: bash <(curl -Ss https://my-netdata.io/kickstart-static64.sh)
```

 * Alternative from L64
```shell 
git clone https://github.com/firehol/netdata.git --depth=1 ~/netdata
sudo ./netdata-installer.sh
```

 * Netdata Docker
```shell 
docker run -d --name=netdata \
  -p 19999:19999 \
  -v /proc:/host/proc:ro \
  -v /sys:/host/sys:ro \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
```

 > Ref (docker)
```shell 
https://docs.netdata.cloud/packaging/docker/#install-netdata-with-docker
```

---

Jenkins

 * Installation

```shell 
$ wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
$ sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'
$ sudo apt-get update
$ sudo apt-get install jenkins
```
