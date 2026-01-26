# Remove build folder

`rm -rf ./build`

# Create build files

```sh
cmake -B build \
    -DGGML_CUDA=ON \
    -DCMAKE_CUDA_COMPILER=/usr/local/cuda-13.1/bin/nvcc \
    -DCMAKE_C_COMPILER=gcc-12 \
    -DCMAKE_CXX_COMPILER=g++-12 \
    -DCMAKE_CUDA_HOST_COMPILER=g++-12 \
    -DCMAKE_CUDA_ARCHITECTURES="native"
```


# Compile
`cmake --build build --config Release -j 8`

