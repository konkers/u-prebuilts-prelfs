# Building Clang

## Checking out src

``` shell
git clone https://github.com/GorNishanov/llvm.git
cd llvm
git checkout coro-snapshot-20160915
cd tools
git clone https://github.com/GorNishanov/clang.git
cd clang
git checkout coro-snapshot-20160915
```

## Generating build files

From directory containing llvm/:
``` shell
mkdir build
cd build
cmake -G Ninja -DCMAKE_INSTALL_PREFIX=~/play/u/prebuilts/clang/darwin-x86_64 \
    -DCMAKE_BUILD_TYPE=Release -DLLVM_LINK_LLVM_DYLIB=ON ../llvm
```

## Building

``` shell
cmake --build .
```

## Installing


``` shell
cmake --build . --target install
```
