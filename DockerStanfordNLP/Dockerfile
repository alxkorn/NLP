FROM nvidia/cuda:10.0-cudnn7-runtime-ubuntu18.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y python3-minimal \
  python3-pip \
  wget \
  unzip \
  vim \
  graphviz 


RUN pip3 install https://download.pytorch.org/whl/cu100/torch-1.1.0-cp36-cp36m-linux_x86_64.whl stanfordnlp jupyterlab graphviz && rm -r /root/.cache/pip


