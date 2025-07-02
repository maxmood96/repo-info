## `couchbase:enterprise-7.2.2`

```console
$ docker pull couchbase@sha256:cf5d7fd7891166e6aef3e19df938391b31d451fc7669bc09f7965f1db38bb8a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:a19ec58565546640ce8da4ac8b0e0497d40eaf4ecb5b88bc9d05633bc4d6989c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.9 MB (703930557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4138389afc9331760e16d223619951f7ee9e35b71c2908426c0c75c61183233c`
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
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:32:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:32:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:32:06 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:32:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:32:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f107907d53e2361344dfc4357ed319d478ba4b6f9887ee23afba17e518916eed`  
		Last Modified: Thu, 12 Jun 2025 22:54:44 GMT  
		Size: 39.7 MB (39662068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabaa524eb5ff279a762749c414210ccc99844adc93606e3c015527962f0ac10`  
		Last Modified: Thu, 12 Jun 2025 22:54:42 GMT  
		Size: 926.7 KB (926688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7c0fb24f91c6cc3996a50c59d93f19a70ba469f8880e388fa76bc1f39f859`  
		Last Modified: Thu, 12 Jun 2025 22:54:42 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba7cab0bd2d2e1c28b5ce8a2505a30d64515b1d87bd6ba4f7fe0bcba74d3ef`  
		Last Modified: Thu, 12 Jun 2025 23:32:30 GMT  
		Size: 633.8 MB (633803620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0a628e0db4d8c44f66fd8747a09914ffe9d6cb37ed6e56d9239090edae5c52`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bed21221646d551c31846945d48cb58743f3bb6eee0c86479df6c7ed90c280`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80478c4edacff4457e1dd268637ef6815d811ef0758eda8036ff2d4e798f6839`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec7c0dfcc59e9a3413516b8adfb4b0ff66c88d423be768c31104bee25efbbf0`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843f0de77d8204f29306599e736b20ed821768ba72baf61618faf7df519008f6`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fc1d36fa5094a22cf3d3ba7f00b59dd9a7a347b4d4bf9ce9f1e023ef56592a`  
		Last Modified: Thu, 12 Jun 2025 22:54:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:bff2c164c8649a3eb3302805491042c3fff28f9e85ccb626d72107457077fc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63800db6e89a8e49a61f95f5c865d8200ad220f377af01ac3248c614af1553a`

```dockerfile
```

-	Layers:
	-	`sha256:3f06e294a709aca3d5765f412553f9225c8c17dc5225dc7bf12fd0aa15b23a3f`  
		Last Modified: Thu, 12 Jun 2025 23:31:24 GMT  
		Size: 37.6 KB (37564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2b2081614fece91ff2230b79dc467bb106678c6f879e64d0a3ea87583a4ba07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 MB (673836387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5a718acbce818fb5d4a52a7e0a97b05db64a102103a258b1ac2ee43882c80e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 12 Jun 2025 10:32:06 GMT
ARG RELEASE
# Thu, 12 Jun 2025 10:32:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Jun 2025 10:32:06 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Thu, 12 Jun 2025 10:32:06 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:32:06 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:32:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:32:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:32:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:32:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:32:06 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:32:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:32:06 GMT
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
	-	`sha256:989ec1fef1372972206f005c667187784314b5cb8ce35157867651799b47ca0f`  
		Last Modified: Wed, 02 Jul 2025 05:01:01 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c485a49db74b7278e6d3dc74d4ee985910db941496c63874792209af2554a865`  
		Last Modified: Wed, 02 Jul 2025 05:31:50 GMT  
		Size: 606.8 MB (606849118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568f97099a37291b8ae37f0cd8f7533eb9c186a62f625f907792533b0121fc9`  
		Last Modified: Wed, 02 Jul 2025 05:01:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68d35cbb6f6c6c64cdfa6c362274bc3b618984a28e1d7e11fc0da58fa29f314`  
		Last Modified: Wed, 02 Jul 2025 05:01:02 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381dfa9f4e04030955a07289c3215c35710cf2aa3715dac51e9e47a9bd00ac1f`  
		Last Modified: Wed, 02 Jul 2025 05:01:02 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d07c5ef5ab76e0176c9e1aa44babe1001e6529105079798c8673422c3193439`  
		Last Modified: Wed, 02 Jul 2025 05:01:01 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bc793a0294870e8acc22b45b81756e6c4ea76a967087715f1d304a588e6963`  
		Last Modified: Wed, 02 Jul 2025 05:01:00 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5fe16715cb69ef8deec411cd7700025bff8de2dd6913f20d10e60307dfc5d4`  
		Last Modified: Wed, 02 Jul 2025 05:01:00 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:8e41c6061d609ff1c73e454444849662c3145d30b1d5b5887f367d9d3c02e1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b07a5be52e263bc47de8a78127d7b29ecdb67f5deb02e205badba2928d4095`

```dockerfile
```

-	Layers:
	-	`sha256:47fc14d5b8808516065da084a9f878df494cf783e7028612296880b9fc5fa396`  
		Last Modified: Wed, 02 Jul 2025 05:31:25 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json
