## `couchbase:community-7.6.0`

```console
$ docker pull couchbase@sha256:a5e34de4807100f3169df6f9f89ec63436fad4a2e4ed3b5c6a14a6845b945129
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:c0252786d2b8a3fc0ae3f6e8c0a0d666a35fd6f86e28735a879435791bc4e949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.8 MB (419809601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c3fa77f292fc9c2728fc03d9bbffbd3426d37e1604846259a10174dd488abe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:30 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:12:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:12:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Fri, 15 May 2026 21:12:51 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:12:51 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:12:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:12:51 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:13:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:13:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:13:26 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:13:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:13:26 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:13:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:13:27 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:13:27 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:13:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:13:27 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:13:27 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:13:27 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b4d64f82c03937e66443d14a7af4e114acda668cfe6f940c63274cb4393a2`  
		Last Modified: Fri, 15 May 2026 21:13:59 GMT  
		Size: 39.3 MB (39307598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317d7e0a407ffd90548026b86020f5200040af817079fd4e040c6ab1b89cefd`  
		Last Modified: Fri, 15 May 2026 21:13:58 GMT  
		Size: 926.8 KB (926766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d9aa8bd97df4e667094824f4aab4c0f47b80e7be1b6213db5753e86805bdf`  
		Last Modified: Fri, 15 May 2026 21:13:58 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2dda5a9b60138a7f9e0475fe7da6592a8cc4f81ea8ad78a035691d52920051`  
		Last Modified: Fri, 15 May 2026 21:14:06 GMT  
		Size: 349.8 MB (349833375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f502c87b90d89e054348704b5527af0dce067cd1b372e70af4d8b4fd1d6e16f1`  
		Last Modified: Fri, 15 May 2026 21:13:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6027193ebe1ccec7914524f6bcfc009b5d1466eafa4493783d2897c6048bb8c2`  
		Last Modified: Fri, 15 May 2026 21:13:59 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4df657232be32aebca64e6ce377352c19df63a85bade32dc88afbe7bb7dba0`  
		Last Modified: Fri, 15 May 2026 21:14:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d4c755b8d3e8ce83a63803fd6a6f341c5d22a395de14275b0f4666990b4a42`  
		Last Modified: Fri, 15 May 2026 21:14:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246929d4cac020ee3a96494edbac6b37bec300e6f4ac99f5a73e231597801206`  
		Last Modified: Fri, 15 May 2026 21:14:01 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d62fb5247aa2c95eb01b970b6ab7f9750d5c4db9c526f24268a836357041c02`  
		Last Modified: Fri, 15 May 2026 21:14:02 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:3a415c0a0c0fbbf36f14c3c5f68fdfa407d8f3fd9dcde53311a12c2e9e1f3472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d846c7e3f3a1f5f41796bd1b26e8d86fc698137d2d4f011a8a6bdc9ce5a8c6fe`

```dockerfile
```

-	Layers:
	-	`sha256:6280ff1f9c4750fb5a1370f701693a197129eb33436c0659af1aacd34c72edd9`  
		Last Modified: Fri, 15 May 2026 21:13:57 GMT  
		Size: 37.2 KB (37207 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:492a74c8c4d31d31cd070798c52cb80be3c6813f07be933f7856d72670751051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.6 MB (400623754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6563f122b2c0ef3ef560f1bf88d67e08a9801a935751f3c189b0424b49998ff0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:12:54 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 15 May 2026 21:12:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 15 May 2026 21:12:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 15 May 2026 21:12:54 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 15 May 2026 21:13:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 15 May 2026 21:13:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Fri, 15 May 2026 21:13:43 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Fri, 15 May 2026 21:13:43 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 15 May 2026 21:13:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 15 May 2026 21:13:44 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Fri, 15 May 2026 21:14:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 15 May 2026 21:14:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 15 May 2026 21:14:21 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 15 May 2026 21:14:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 15 May 2026 21:14:21 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 21:14:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 15 May 2026 21:14:21 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 15 May 2026 21:14:21 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 15 May 2026 21:14:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:14:21 GMT
CMD ["couchbase-server"]
# Fri, 15 May 2026 21:14:21 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 15 May 2026 21:14:21 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6822369c748f3ee6ab67f1a2023a0a75a07191887da06dbe362d22c4b2ebd052`  
		Last Modified: Fri, 15 May 2026 21:14:59 GMT  
		Size: 38.9 MB (38866860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82d56262fb4d45572e4a067ea449745ea51b44b1de42d35bbd908390f6ebebf`  
		Last Modified: Fri, 15 May 2026 21:14:57 GMT  
		Size: 775.3 KB (775292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dc3c0f3745a70152c299089e0cdcee459141fa11a132fadb107cdb4ba65ef6`  
		Last Modified: Fri, 15 May 2026 21:14:57 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114291b27dda558f3b6c4d2c9333523fbeadd33fcae5971a94026c77c364c3d`  
		Last Modified: Fri, 15 May 2026 21:15:05 GMT  
		Size: 333.4 MB (333369792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e92d09beb9b178ff04cc4e1fe8a9bd91ab3355af525db9ed78f29bbd465c1`  
		Last Modified: Fri, 15 May 2026 21:14:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fe446a9a403fa20c77126ec80f7f1ed6ea2aab42183c6be69b4c6b341325cb`  
		Last Modified: Fri, 15 May 2026 21:14:59 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df581fc1fd91fdbf62bf9f7bd9ba9f05eff7621d2f8a2aa84b450578b30bb57`  
		Last Modified: Fri, 15 May 2026 21:15:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fd5f618a8151a228adaf0c17f2f46866a367c2e48edbd818df069603d2663`  
		Last Modified: Fri, 15 May 2026 21:15:00 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de24f1416a222f7c2f2a827714386dd321fe34e072b6a3ecddd51e1448823dd`  
		Last Modified: Fri, 15 May 2026 21:15:01 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e06c21e7e5778e7e2d4650c88b9ee64fce6d48be923db19ee89a960b05ecf0`  
		Last Modified: Fri, 15 May 2026 21:15:02 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:6af3c34906d088644134148f680eb9f21d1f19b7f405790ee48a53a0832f084c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9263951dcd086ec7c96fc5ca9a74db762f598392bcef07ae278797bf167560`

```dockerfile
```

-	Layers:
	-	`sha256:58b347d7ab992c8c9260a1a9a1226fe24e97d1c48daa46f37f0d67a31cda8861`  
		Last Modified: Fri, 15 May 2026 21:14:57 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json
