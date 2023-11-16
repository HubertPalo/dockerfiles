FROM nvidia/cuda:11.3.1-cudnn8-runtime-ubuntu20.04

RUN apt update && apt install tzdata -y
ENV TZ='America/Sao_Paulo'

RUN apt update && apt install -y python3.9 python3-pip
COPY requirements.txt /requirements.txt
RUN python3 -m pip install -r /requirements.txt
RUN python3 -m pip install torch