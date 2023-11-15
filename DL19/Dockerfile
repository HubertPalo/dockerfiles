FROM nvidia/cuda:12.3.0-runtime-ubuntu20.04

RUN apt update && apt install tzdata -y
ENV TZ='America/Sao_Paulo'

RUN apt update && apt install -y python3.9 python3-pip
RUN wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-keyring_1.1-1_all.deb
RUN dpkg -i cuda-keyring_1.1-1_all.deb

RUN apt-get install libcudnn8=8.9.5-1+12.3
RUN apt-get install libcudnn8-dev=8.9.5-1+12.3
RUN apt-get install libcudnn8-samples=8.9.5-1+12.3
COPY requirements.txt /requirements.txt
RUN python3 -m pip install -r /requirements.txt
RUN python3 -m pip install torch
