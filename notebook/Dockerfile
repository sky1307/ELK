FROM jupyter/scipy-notebook:c094bb7219f9

LABEL maintainer="Jupyter Project <jupyter@googlegroups.com>"

# Fix DL4006
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

USER root

WORKDIR /

WORKDIR /

RUN apt-get update && \
    apt-get install -yq tzdata && \
    ln -fs /usr/share/zoneinfo/Asia/Ho_Chi_Minh /etc/localtime && \
    dpkg-reconfigure -f noninteractive tzdata


RUN echo "Asia/Ho_Chi_Minh" > /etc/timezone

RUN pip install tweepy elasticsearch

USER $NB_UID

# Install pyarrow
# RUN conda config --set allow_conda_downgrades true && \
#     conda install conda=4.6.11
RUN pip install tweepy elasticsearch textblob pandas



WORKDIR $HOME
