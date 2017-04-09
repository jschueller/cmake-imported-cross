# cmake-imported-cross

```
git clone https://github.com/jschueller/cmake-imported-cross.git
cd cmake-imported-cross
mkdir build
cd build
cmake ..
make # ok
cmake -DCMAKE_CROSSCOMPILING_EMULATOR=/usr/bin/echo ..
make VERBOSE=1 # fail
```
