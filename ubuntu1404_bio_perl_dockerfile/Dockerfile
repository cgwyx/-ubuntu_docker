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

# Install perl 
RUN apt-get install -y perl

# Install perl modules 
RUN apt-get install -y cpanminus perl-doc

RUN cpanm --mirror http://mirrors.163.com/cpan --mirror-only \
 Pod::Perldoc::ToMan \
 CPAN::Meta \
 readline \
 YAML \
 Digest::SHA \
 Module::Build \
 ExtUtils::MakeMaker \
 Test::More \
 Data::Stag \
 Config::Simple \
 Statistics::Lite \
 Statistics::Descriptive 

RUN apt-get install -y \
 libarchive-zip-perl

# Install BioPerl dependancies, mostly from cpan
RUN apt-get install -y \
 libpixman-1-0 \
 libpixman-1-dev \
 graphviz \
 libxml-parser-perl \
 libsoap-lite-perl 

RUN apt-get install -y \
 libxml-libxml-perl \
 libxml-dom-xpath-perl \
 libxml-libxml-simple-perl \
 libxml-dom-perl

# Install BioPerl last built
RUN cpanm --mirror http://mirrors.163.com/cpan --mirror-only \
 CJFIELDS/BioPerl-1.6.924.tar.gz

CMD ["/bin/bash"]


