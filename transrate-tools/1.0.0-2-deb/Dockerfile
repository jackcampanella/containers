FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="transrate-tools" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="transrate-tools" \ 
    about.summary="helper for transrate" \ 
    about.home="http://hibberdlab.com/transrate/" \ 
    software.version="1.0.0-2-deb" \ 
    upstream.version="1.0.0" \ 
    version="1" \ 
    about.copyright=" 2015 Richard Smith-Unna & Chris Boursnell" \ 
    about.license="MIT" \ 
    about.license_file="/usr/share/doc/transrate-tools/copyright" \ 
    extra.binaries="/usr/bin/bam-read" \ 
    about.tags=""

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y transrate-tools || apt-get install -y transrate-tools) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker
