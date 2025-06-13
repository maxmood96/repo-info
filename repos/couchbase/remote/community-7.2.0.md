## `couchbase:community-7.2.0`

```console
$ docker pull couchbase@sha256:84d404d1e25db14853a4ea25e370cb39d492a23e47b3a00c9bf15cac2ccc9fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:aa97c97854ec24464294c853574998868ac418f6f31e04ba3fed5b93ed79d88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 MB (392203771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6e06624ca0063dd3aa39aa933d3936338ca07e4fd927951bbad853d017ef3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:00:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:00:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:00:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:00:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:00:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:00:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948adea9c6e9887afd4a745b302ab5a64c689803527affa87d330f3668761ec4`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 39.7 MB (39662183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37d469eed07bb6f18e14bda532d0d50327816da2b0ba25714ea0792b724a5a9`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 926.7 KB (926712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e529d7e0a21ccb91d13fd3e716b783f4bb49e47ba71d9635bff35c0394343f47`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c094bf4e449d4d24396fedae9bb0b5c2eaa0da5d46e7113bbbeff770bc353607`  
		Last Modified: Thu, 12 Jun 2025 23:33:26 GMT  
		Size: 322.1 MB (322076691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ada0f50a6f1bf9f95cf2b0a1d6c7e43714c8c2a7fe108f2233ff40f0b07321`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8861cc98a1c40b30cac2f74a24d67514a916b4a6bdbbe3582727c26c45510690`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f25c40f5d0ec1997030a7ca1d32fcfdd3e418ab1d5dfa5b0e0108245ff4e36`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec366e3ad4f37bd70a69e1fdd84425b4589bed9214f5a15c3ed8295a55cfc4ba`  
		Last Modified: Thu, 12 Jun 2025 22:53:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de59c0b13d14776da90abc23a4d4390fa346d7548fccf8a138a6188ce6f696b`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4676b7734b33c165c9858d1434ef2c87085668c13b5048c99de6466ca24165`  
		Last Modified: Thu, 12 Jun 2025 22:53:54 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:86e06956d01757485c78d1ef3c0ec82071cdc7105fba4a609fd61ae4df961773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23a7539c830c15111ddaef4e7c41ce8cfa5e4887ab52e7c1139731d1892ce2f`

```dockerfile
```

-	Layers:
	-	`sha256:90f48e50b357a3ec27b0695a4de3011504cd78309853e25bc85d4d818e8f3e87`  
		Last Modified: Thu, 12 Jun 2025 23:32:15 GMT  
		Size: 37.3 KB (37252 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:04355630282b1f61ea0a9e03850948cb5c8135afcfb931f0530dbdd8a77abdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.5 MB (369463904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d60a4549feed2f97e172ec89eb8f098c3b9f5e1089bdce60645fc2b837ff4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:00:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:00:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:00:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:00:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:00:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:00:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:00:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:00:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b871ae0d3232d9d48af99e40c095f90401627db530330bd41c8b7f4260e7d559`  
		Last Modified: Fri, 13 Jun 2025 00:18:19 GMT  
		Size: 39.2 MB (39206797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59dacdc4bb2b1acfe5ead4be9078fcce112b971dc328349f5703bcd8d536d6`  
		Last Modified: Fri, 13 Jun 2025 00:18:18 GMT  
		Size: 770.9 KB (770937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f1a7d9cbd13dc9489ddbc0811761abd2ab8f494c7beea6c412c38bd2a317d7`  
		Last Modified: Fri, 13 Jun 2025 02:32:33 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c47ca088d1a7df0320133ee69da8881858859f7054b67d5fbd6141e9f6bf689`  
		Last Modified: Fri, 13 Jun 2025 02:32:46 GMT  
		Size: 302.1 MB (302125403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dad79c0aa1d4a1a9869d612c5599c57461904f0beb24bf87b1caeaa72990a3`  
		Last Modified: Fri, 13 Jun 2025 02:32:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec4d3e00e91ffc9950d626df8e09d1eaad8aeecd29dfdb5577379221f62403e`  
		Last Modified: Fri, 13 Jun 2025 02:32:33 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366dcd52a67f70ae9733927b3e8e343c25ca8fc2d1af519c3e218c83ac69f75a`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46556941a0bf13b36e28bfdcacbe30e872cdb2ea501f2aa15207f44450ca8f85`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8195c1aecf83d92580b76b5681c69377250a64c4622f0bfa8aaba88c36b1e186`  
		Last Modified: Fri, 13 Jun 2025 02:32:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453f50bce8fb0b94d4d85059a6057d9e4d0443a41f60330a52b8d3f441a94a9b`  
		Last Modified: Fri, 13 Jun 2025 02:32:36 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:3b5f26466722aeb9ec479cb71d82e6ff7184dc45c2c75d38e60d9ea31c86d47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc084c62cf6bfeba02b9db6c53e08c90cbc812ab08b418b4c933d2fad957e2cb`

```dockerfile
```

-	Layers:
	-	`sha256:b173b3e09d397dc383b0c3fe7b6b6cf5ba27e492fc5b398d047b10952da74f4f`  
		Last Modified: Fri, 13 Jun 2025 02:32:17 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json
