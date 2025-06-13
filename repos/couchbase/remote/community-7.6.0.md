## `couchbase:community-7.6.0`

```console
$ docker pull couchbase@sha256:bd46dce15b21f00fd4dbf509a7751b62153f7fee7d7f9d5a51a53446fa4ded54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:6b07bc4d22080c3953d4f5978ec91ec6d22e23414a45096f9bec35f98a2ed919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419960373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002d3ebfd8219fd2f0f2ccb8322ec2550ec2ede1003a6e26a40f40ff0ca4a6f7`
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
# Thu, 12 Jun 2025 11:31:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:31:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:31:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:31:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:31:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:31:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b03d98297cc38a443efd99f01320186009a5a295fa6c49cb246849feb35b70`  
		Last Modified: Thu, 12 Jun 2025 22:53:43 GMT  
		Size: 39.7 MB (39662185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea77eea3a30e2235dad6a616e8235fce75e4e562b0b54df3fd8ca74ed82585a`  
		Last Modified: Thu, 12 Jun 2025 22:53:28 GMT  
		Size: 926.7 KB (926677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e5752e35e7fc9e1127fec3d74e58a811d011d504410b5d2c61e72ab7f6488e`  
		Last Modified: Thu, 12 Jun 2025 22:53:29 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dec065f52fb6e81e3b2ddf0277c1e03b9726b6a673f9a95b0e8550f7cc53e6`  
		Last Modified: Thu, 12 Jun 2025 23:32:55 GMT  
		Size: 349.8 MB (349833336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ebac61a2a85b42389f2867163c7f70577b3bd34c57852176226c03be284a`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8c95845b73bf6a2c43b56973cd31a3a49f355ce48e97d493936a1bf6d8abdf`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d22ea1d9fba16d6c73adef07f8ddafbfc5b38f0d5afa162e9693b6d7876cd5`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ecb2df0194a13004e032e0d793c1b36c9c560c40f044bf06e344a85003efcd`  
		Last Modified: Thu, 12 Jun 2025 22:53:30 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45454ed7c42a240fbd8bafcb746165c75c6e06830210c90d78d99a46ceaf403f`  
		Last Modified: Thu, 12 Jun 2025 22:53:31 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301379a5b8cda0e7d01d8ecfdb1645425e3835dd7f7c19959ec1391e88cbbb56`  
		Last Modified: Thu, 12 Jun 2025 22:53:31 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:0fcaf67706c9d72ff840c51cc421f94ff1b444b4b0f53b04436ca04dc34c2752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97cbd03c9ec274c864d85b1ff8b1bbee194ea4561e55335423cafdd009f86a3`

```dockerfile
```

-	Layers:
	-	`sha256:4b3817f4950ed4493f3b597b592e03056d421b2d330765f3869a1bf9d7952b41`  
		Last Modified: Thu, 12 Jun 2025 23:32:29 GMT  
		Size: 37.3 KB (37252 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:53c06ce187bc3c64d8a39fd1500204ac7d0a4bcb6d424c4a35db4222149397a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400708204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcde1835d6030e1bf5c96c13ee2373c208f36da31f760968a1aa163628e14e8f`
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
# Thu, 12 Jun 2025 11:31:30 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:31:30 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:31:30 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:31:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:31:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:31:30 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:31:30 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:31:30 GMT
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
	-	`sha256:97ae30acbc3f8af9b40fe37c4226589be7f6bb56e244c0f5249677bcaa36a20b`  
		Last Modified: Fri, 13 Jun 2025 00:27:09 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2384be9b2669a53b8813eaa237221019c06b1fe04d1ae549814a8938ccfc10`  
		Last Modified: Fri, 13 Jun 2025 02:32:53 GMT  
		Size: 333.4 MB (333369702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6ebc92cefa1f6f63e2779b9d93a1a05ed09716b356c4e91b0dbd9299eea7c`  
		Last Modified: Fri, 13 Jun 2025 00:27:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab05a16a0abaab25102e554bdb02630e5bbc8dcaf837acd7fb213abcc102410`  
		Last Modified: Fri, 13 Jun 2025 00:27:13 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ecd8ccf6341c3d18a4642bdcae9d2e4a8ca0f77b95532ba1c82cfee4fd2e77`  
		Last Modified: Fri, 13 Jun 2025 00:27:16 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5a9faf88d0a1d13ad62584492a2142d554e57799dc9084a7e3ccad38cc7afc`  
		Last Modified: Fri, 13 Jun 2025 00:27:18 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e565fdf24e2569945e9ef1c04b41675d2d7ad75fd35558378a952dfcbb5b6ae`  
		Last Modified: Fri, 13 Jun 2025 00:27:20 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a327e18d69be829d0968738ece5eb97ab458bd9860c3b441d198c6cb90c971b`  
		Last Modified: Fri, 13 Jun 2025 00:27:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:08a3aa94b09be9d92bd1c9772dcbb9a17742ad407ec2493943380ebe22ec657e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3007f918fbae712b4d85a1ee2d2ac45a8666feb97c6072f687a9c05eb6dc798c`

```dockerfile
```

-	Layers:
	-	`sha256:ca0ff933b34f92c630e197259b8281954cb7ae9afbf3737b7de97e2f10715847`  
		Last Modified: Fri, 13 Jun 2025 02:32:31 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json
