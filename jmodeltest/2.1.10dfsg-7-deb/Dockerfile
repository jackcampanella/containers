FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="jmodeltest" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="jmodeltest" \ 
    about.summary="HPC selection of models of nucleotide substitution" \ 
    about.home="https://github.com//ddarriba/jmodeltest2" \ 
    software.version="2.1.10dfsg-7-deb" \ 
    upstream.version="2.1.10" \ 
    version="1" \ 
    about.copyright="2008-2015 Diego Darriba <diegodl84@gmail.com>" \ 
    about.license="GPL-2+" \ 
    about.license_file="/usr/share/doc/jmodeltest/copyright" \ 
    extra.binaries="/usr/bin/jmodeltest,/usr/bin/runjmodeltest-cluster,/usr/bin/runjmodeltest-gui" \ 
    about.tags=""

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y jmodeltest || apt-get install -y jmodeltest) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker
