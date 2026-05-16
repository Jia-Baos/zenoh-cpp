# build 指令

```BASH
mkdir build && cd build

cmake .. \
  -DZENOHC_BUILD_WITH_UNSTABLE_API=true \
  -DZENOHC_BUILD_WITH_SHARED_MEMORY=true \
  -DCMAKE_PREFIX_PATH=/home/jia-baos/Project-Cpp/zenoh-c/install-prefix \
  -DCMAKE_INSTALL_PREFIX="$(pwd)/../install-prefix"

cmake .. -DZENOHCXX_ZENOHC=ON -DZENOHCXX_ZENOHPICO=OFF # to configure  only for zenoh-c backend

cmake .. -DZENOHCXX_ZENOHC=OFF -DZENOHCXX_ZENOHPICO=OFF # to configure for none of the backends

cmake .. -DZENOHCXX_ZENOHC=ON -DZENOHCXX_ZENOHPICO=ON # to configure for both backends

cmake --build . --config Release

cmake --build . --target examples

cmake --build . --target tests

cmake --install . # or make install

export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/jia-baos/Project-Cpp/zenoh-c/install-prefix/lib
```
