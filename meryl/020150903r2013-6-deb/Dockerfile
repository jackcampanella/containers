FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="meryl" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="meryl" \ 
    about.summary="in- and out-of-core kmer counting and utilities" \ 
    about.home="http://kmer.sourceforge.net" \ 
    software.version="020150903r2013-6-deb" \ 
    version="1" \ 
    about.copyright=" 2002 PE Corporation (NY) through the Celera Genomics Group" \ 
    about.license="GPL-2+" \ 
    about.license_file="/usr/share/doc/meryl/copyright" \ 
    extra.binaries="/usr/bin/existDB,/usr/bin/kmer-mask,/usr/bin/mapMers,/usr/bin/mapMers-depth,/usr/bin/meryl,/usr/bin/positionDB,/usr/bin/simple" \ 
    about.tags=""

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y meryl || apt-get install -y meryl) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker
