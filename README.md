
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
```

```shell 
Linux 64bit installation: bash <(curl -Ss https://my-netdata.io/kickstart-static64.sh)
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
