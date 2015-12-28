############################################################
# Dockerfile to build bioperl biopython container images
# docker name;unutu1404:bio_perl_python
# Based on Ubuntu 
############################################################

# Set the base image to Ubuntu
FROM ubuntu:14.04

MAINTAINER cheng gong <512543469@qq.com>

# Update the repository sources list
RUN apt-get update

# Install compiler
RUN apt-get install -y \
 build-essential \
 gcc-multilib \
 apt-utils \
 expat \
 libexpat-dev 

# Install python
RUN apt-get install -y python2.7

# Install Numpy and Scipy
#RUN apt-get build-dep -y python-biopython
RUN apt-get install -y python-numpy python-scipy python-matplotlib

# Install BioPython
RUN apt-get install -y \
 python-biopython=1.63-1 \
 python-biopython-sql=1.63-1

# Install pip
RUN apt-get install -y \
 python-pip

CMD ["/bin/bash"]


