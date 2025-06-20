cmake -DCMAKE_INSTALL_PREFIX=/usr -DCPACK_GENERATOR=DEB -B build -S .
cmake -B build
export LD_LIBRARY_PATH="$(pwd)/build/lib"
cmake --build build/ --target package
