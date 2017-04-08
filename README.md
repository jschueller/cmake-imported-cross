# cmake-imported-cross


git clone https://github.com/jschueller/cmake-imported-cross.git
cd cmake-imported-cross
mkdir build
cd build
cmake ..
make # ok
cmake -DCROSS_COMPILING_EMULATOR=/usr/bin/python ..
make VERBOSE=1 # fail
