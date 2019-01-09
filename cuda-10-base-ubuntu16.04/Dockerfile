FROM nvidia/cuda:10.0-base-ubuntu16.04

LABEL maintainer="MichaelJiang <dita51519961@gmail.com>" 

RUN apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        cuda-command-line-tools-10-0 \
        cuda-cublas-dev-10-0 \
        cuda-cudart-dev-10-0 \
        cuda-cufft-dev-10-0 \
        cuda-curand-dev-10-0 \
        cuda-cusolver-dev-10-0 \
        cuda-cusparse-dev-10-0 \
        libcudnn7=7.4.1.5-1+cuda10.0 \
        libcudnn7-dev=7.4.1.5-1+cuda10.0 \
        libcurl3-dev \
        libfreetype6-dev \
        libhdf5-serial-dev \
        libpng12-dev \
        libzmq3-dev \
        pkg-config \
        rsync \
        software-properties-common \
        unzip \
        zip \
        zlib1g-dev \
        wget \
        curl\
        git \
        && \
    find /usr/local/cuda-10.0/lib64/ -type f -name 'lib*_static.a' -not -name 'libcudart_static.a' -delete && \
    rm /usr/lib/x86_64-linux-gnu/libcudnn_static_v7.a

# apt-get update && apt-get install -y --no-install-recommends\
#     libnccl2=2.3.7-1+cuda9.0 libnccl-dev=2.3.7-1+cuda9.0\
#     &&\
# rm -rf /var/lib/apt/lists/* &&\
# find /usr/local/cuda-9.0/lib64/ -type f -name 'lib*_static.a' -not -name 'libcudart_static.a' -delete &&\
# rm /usr/lib/x86_64-linux-gnu/libcudnn_static_v7.a 

RUN apt-get update && \
        apt-get install nvinfer-runtime-trt-repo-ubuntu1604-5.0.2-ga-cuda10.0 \
        && apt-get update \
        && apt-get install -y --no-install-recommends libnvinfer-dev=5.0.2-1+cuda10.0 \
        && rm -rf /var/lib/apt/lists/*