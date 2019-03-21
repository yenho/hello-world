

 > Ref (binomial theorem)
https://medium.com/datadriveninvestor/binomial-theorem-cecfb0224183

---

 > Ref (maxwells equaqtions)
https://medium.com/dialogue-and-discourse/maxwells-equations-7484212839b1

---
 * Tennenbaum’s Proof that Square Root 2 is Irrational

```shell
Proofs are the bedrock of mathematics. It’s how we know that every rule and theorem we use holds true. Without the logical rigor of proofs, math would be a bunch of wishy-washy assumptions. Proofs come in all shapes and sizes. Some are long and arduous discernible by very few, others stand on such fundamental logic most anyone could reproduce them with a little motivation.

One such classic proof of number theory and analysis is demonstrating that irrational numbers exist, most commonly that the square root of 2 is irrational. Now there are many ways to prove this result, and I’ve talked about this before…but that was before I encountered Tennenbaum’s proof. A magnificently clever, yet straight-forward proof of irrationality. Using a basic understanding of geometry we can logically show that square root 2 is irrational. It’s quite a fun little proof!

Interestingly, this proof has been largely overlooked historically. Perhaps that’s because our problem is an ancient problem that’s been solved many times over, yet this proof wasn’t concocted until the mid-twentieth century by American mathematician Stanley Tennenbaum. The proof was overlooked until the 1990’s when a past student of Tennenbaum’s published it in a book on the power of mathematics. Finally, the proof began to be appreciated for its beauty and simplicity. Watch or read on!!
 > Ref
https://medium.com/i-math/a-beautiful-geometric-proof-a8275c981e1b
```
 > Ref
https://medium.com/i-math/a-beautiful-geometric-proof-a8275c981e1b
---

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

---


