
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
