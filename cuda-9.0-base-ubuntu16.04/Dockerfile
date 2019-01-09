FROM nvidia/cuda:9.0-base-ubuntu16.04 

LABEL maintainer="MichaelJiang <dita51519961@gmail.com>" 

RUN apt-get update && apt-get install -y --no-install-recommends\
        build-essential\
        cuda-command-line-tools-9-0\
        cuda-cublas-9-0 \
        cuda-curand-9-0 \
        cuda-cufft-9-0 \
        cuda-curand-9-0 \
        cuda-cusolver-9-0 \
        cuda-cusparse-9-0 \
        curl\
        git\
        libcudnn7=7.2.1.38-1+cuda9.0\
        libcudnn7-dev=7.2.1.38-1+cuda9.0\
        libcurl3-dev\
        libfreetype6-dev\
        libpng12-dev\
        libzmq3-dev\
        pkg-config\
        python-dev\
        rsync\
        software-properties-common\
        unzip\
        zip\
        zlib1g-dev\
        wget\
        &&\
    rm -rf /var/lib/apt/lists/* &&\
    find /usr/local/cuda-9.0/lib64/ -type f -name 'lib*_static.a' -not -name 'libcudart_static.a' -delete &&\
    rm /usr/lib/x86_64-linux-gnu/libcudnn_static_v7.a 

# apt-get update && apt-get install -y --no-install-recommends\
#     libnccl2=2.3.7-1+cuda9.0 libnccl-dev=2.3.7-1+cuda9.0\
#     &&\
# rm -rf /var/lib/apt/lists/* &&\
# find /usr/local/cuda-9.0/lib64/ -type f -name 'lib*_static.a' -not -name 'libcudart_static.a' -delete &&\
# rm /usr/lib/x86_64-linux-gnu/libcudnn_static_v7.a 