# Start with CUDA Torch dependencies 2
FROM nvidia/cuda:8.0-cudnn5-devel
MAINTAINER Guodong Shen

# Install some dependency
RUN apt-get update && apt-get -y install git ca-certificates

# Install torch7
RUN git clone https://github.com/torch/distro.git ~/torch --recursive && \
    cd ~/torch && \
    sed 's/sudo//g' install-deps > install-deps-without-sudo && \
    chmod u+x install-deps-without-sudo && \
    bash install-deps-without-sudo && \
    bash install.sh && \
    source ~/.bashrc

WORKDIR /root
