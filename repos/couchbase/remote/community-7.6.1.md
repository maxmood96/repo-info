## `couchbase:community-7.6.1`

```console
$ docker pull couchbase@sha256:459babf3a90c04cd34907ac56fddf7614680fe119e856ba1a30790526fa5a7b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:ae92eec50c8344eee9ec0ecd7b4d7407c36daafe3ca66ba5a0ae8f3b59581dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419974142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94e6378527be12858e17f7781a9c4ba6bfe903fe875060d6c8a58fb8e65b9eb`
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
# Thu, 12 Jun 2025 11:40:31 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:40:31 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:40:31 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:40:31 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:40:31 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6ac01f224511bf7f1856637dd6b11b210101a6cc273fe9c0894f0e9109a98f`  
		Last Modified: Thu, 12 Jun 2025 22:53:43 GMT  
		Size: 39.7 MB (39662200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ca3aa854a62486cbeb88cbd68ec34e50336aed040ac992c14ad771275151b`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 926.7 KB (926674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253115d6642fe26b2dd6c76057db7d1492eb4ce70fb2333ec76976078d6c974f`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2bee851e7ecc10a5f4523300397da9badb6b5973db0745d2af56f3220d8c0`  
		Last Modified: Thu, 12 Jun 2025 23:32:59 GMT  
		Size: 349.8 MB (349847083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5991c11c75dfa100df22dfcaf93bda7cedf1a8cd4a849de820c6027684d059c`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be40716a5abe70a2c74d03a8d8bd6b0567561bdccf786f253ddb6823b4e0c1ab`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1927373b5e2edac1d3d394295ca2e42ce5e8dc38e488dc58fbb5073c141d0ffb`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7139af2cdd6430113123ca8cc20abdd252fc0c57d6de9b835ffb11d7f5b9a913`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd244474f66484c7bf389c7a384900ab2982f32710711e6b62c992b83b095a`  
		Last Modified: Thu, 12 Jun 2025 22:53:41 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4790857e1cc2dad01c5da2bffd3d1dab5d6c2d096b70dec4545bc41e3b0d0f68`  
		Last Modified: Thu, 12 Jun 2025 22:53:42 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:bd00b7d93f6e7c8b11e84a8f1210d4a4af9495b961483989eb54bee943510972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5663061b70c75e0409411172fcfdd428553d25bd66898d20440d1d3c2cc484`

```dockerfile
```

-	Layers:
	-	`sha256:9d7812bf3466e8611e00395aafc1cf07b5eb7c2c364e3e1581ea4857af59b825`  
		Last Modified: Thu, 12 Jun 2025 23:32:34 GMT  
		Size: 37.3 KB (37252 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:4b206078fdcf37055bcab7a99d73ca407a9f772f3ed883c69b1c0888567d4f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 MB (400385079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255e34ddb91c0d69000197498459b7a8b7e1b771596fb7756703462c99c04569`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 12 Jun 2025 11:40:31 GMT
ARG RELEASE
# Thu, 12 Jun 2025 11:40:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Jun 2025 11:40:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Jun 2025 11:40:31 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Jun 2025 11:40:31 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Thu, 12 Jun 2025 11:40:31 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:40:31 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:40:31 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:40:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:40:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:40:31 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:40:31 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:40:31 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b4a208b9c475ece693c22152a3bcaf5bd41b1a23414724be0a26eafb45fbb8`  
		Last Modified: Wed, 02 Jul 2025 04:29:19 GMT  
		Size: 38.9 MB (38851951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8873c330b232144aafe4f5b5f3f45de4aff270c5d8445df96f63aa7ac15f7f0c`  
		Last Modified: Wed, 02 Jul 2025 04:29:15 GMT  
		Size: 770.9 KB (770863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efaf4050eea1b19385fce534ae6bfeba1c427dcf1ab2cbb5db9c4fc2f79d441`  
		Last Modified: Wed, 02 Jul 2025 04:44:43 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db32fae9e643d7c738da607e2774c216d78b40fd116963ff7bdf29dcee7dc92`  
		Last Modified: Wed, 02 Jul 2025 05:33:25 GMT  
		Size: 333.4 MB (333397808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c307b1dae95710816f9ace402329432c7f96cfdc819cad81678a112755c0ab40`  
		Last Modified: Wed, 02 Jul 2025 04:44:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf73e4ebbaac9a869dc7c9711396ad4a75b401d1895e9455692c9b970f22db3`  
		Last Modified: Wed, 02 Jul 2025 04:44:43 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e591c13e40bebb73d9684d1aad96070a5b74224d3ac9989479643fc8b4ea7c0a`  
		Last Modified: Wed, 02 Jul 2025 04:44:43 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb31fc43c1ea2778b7bb94f30308ff7a71b906cca411e241bd113fef87b9bd6`  
		Last Modified: Wed, 02 Jul 2025 04:44:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0044d4c2890b5923ab68a162c5d2dddf253d8368c4e40655bcad53e3da909f46`  
		Last Modified: Wed, 02 Jul 2025 04:44:43 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fe7df34b08cb9a4fad1b9ce2cbd6d3df49930ff5a5a30e5721414c1a59920b`  
		Last Modified: Wed, 02 Jul 2025 04:44:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.1` - unknown; unknown

```console
$ docker pull couchbase@sha256:5c95de9e8121553b167cf580ea046553f051ebf3baa31d97698e882da972b923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe71645b2931dc1d96c359e16e34b3c97c165aa9328736684d0cf0606bcdc7cc`

```dockerfile
```

-	Layers:
	-	`sha256:5d7a5a865026899824babf1ed9162eab46178835cbe3d76faa71fd0e88e6e8fc`  
		Last Modified: Wed, 02 Jul 2025 05:33:06 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json
