FROM ubuntu:18.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y openjdk-8-jdk \
  python3-pip \
  wget \
  unzip \
  vim

RUN wget http://nlp.stanford.edu/software/stanford-corenlp-full-2018-10-05.zip
RUN unzip stanford-corenlp-full-2018-10-05.zip
RUN rm stanford-corenlp-full-2018-10-05.zip

RUN echo 'for file in `find /stanford-corenlp-full-2018-10-05 -name "*.jar"`; do export CLASSPATH="$CLASSPATH:`realpath $file`"; done' >> /root/.bashrc

RUN pip3 install https://download.pytorch.org/whl/cpu/torch-1.1.0-cp36-cp36m-linux_x86_64.whl
RUN pip3 install https://download.pytorch.org/whl/cpu/torchvision-0.3.0-cp36-cp36m-linux_x86_64.whl
RUN pip3 install stanfordnlp




