## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:fa93f8af64ab435a1f01a011f457a7e758b3ca46a921ff3d2925c71f8c85f598
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:1bb4113c68ac536fc0fccbb6d075ebf581e9f367f14e96a6c51f6f9212e3a844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401235480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e5f097bb07985d17366bedd49780165e7edae103c1f8ce5b734a05c6538cf0`
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
# Thu, 12 Jun 2025 10:54:55 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:54:55 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:54:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:54:55 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:54:55 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:54:55 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afa078af841314ff548ba6e0cda8bbb83c389b01d91607b0f46921d1161a0a6`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 39.7 MB (39662967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb2e9d71200b41ec8772e457447047b3e3eee1cbe8c58f73a51f0180dc34218`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 926.7 KB (926680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb671a6ebd1f8cfbe7b2fa6251e8fad648723fd2de3066c7b21c3e954a55885c`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff9fc089897c83480eb9a5aaaac75dcef0ab48cb8ef0bc3ef5463a61bc646a`  
		Last Modified: Thu, 12 Jun 2025 23:32:52 GMT  
		Size: 331.1 MB (331107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edd253a9fe4f87e84bee0e4af96829d587cb461684558bcf1fd4ea1e895738e`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f0ee9e819f635c8012db6225821be48614b64c81b9e453c0e9072e3a0c0f2c`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd333bf99cb3e0f907e7f2654e3a11570f31d41d339d6c098920c32a3e98a9fb`  
		Last Modified: Thu, 12 Jun 2025 22:53:33 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba246f4da36bdd9237ad37ad9ac91509883abf6896713844c960f7959fdebdad`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a418d74445bb4e26ce3783bcf201bb85b48ec8069eb5a1fc8087b3f0244ed4be`  
		Last Modified: Thu, 12 Jun 2025 22:53:34 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc677471f0f056e9af64d9629051a57021fd998de85cc7c5d372bd1faf35bce7`  
		Last Modified: Thu, 12 Jun 2025 22:53:35 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:fc0a3a3f871070a557a9881e3c74b720d4c0941a2420d4771dc139c7689bdb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a0e765ba47c7c9327f762b09373c2d340bf86707e79db5fda9784b344c2bf3`

```dockerfile
```

-	Layers:
	-	`sha256:1138c0c933d303f9cda64d715ba8280596412b458d4539639bbf90cf50e270f3`  
		Last Modified: Thu, 12 Jun 2025 23:32:24 GMT  
		Size: 37.3 KB (37251 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:70e588ed34beb3e53caec94a82c23cfdd9f5372344ac6bf8b7a5fe9b7d290fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 MB (379883694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc7da25c6faadc624d5a41d4073cebf75c5e569a0c156cd7b816726debd9acb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 12 Jun 2025 10:54:55 GMT
ARG RELEASE
# Thu, 12 Jun 2025 10:54:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Jun 2025 10:54:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Jun 2025 10:54:55 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Jun 2025 10:54:55 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Thu, 12 Jun 2025 10:54:55 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 10:54:55 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 10:54:55 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 10:54:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 10:54:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 10:54:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 10:54:55 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 10:54:55 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 10:54:55 GMT
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
	-	`sha256:e091bce34397f7f57f70c654f507ead48f331ddb7dc2c6fc3274c37192bd2c2a`  
		Last Modified: Wed, 02 Jul 2025 04:56:57 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060e8512e039d15731a3842f8efebfe04046461fc4a305a253eb999f3939242`  
		Last Modified: Wed, 02 Jul 2025 05:33:05 GMT  
		Size: 312.9 MB (312896426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100bf97d8b713d5da47960245eb1b43515fb302ba6cd59d4901280a485f32243`  
		Last Modified: Wed, 02 Jul 2025 04:56:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a2bc2dbc17cd7ca27fe648598c6e55c53631e7fe391d1fa2f99bdcc636c7a9`  
		Last Modified: Wed, 02 Jul 2025 04:56:57 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b30c14686e635f37e087e402cb5b7d1bc913360e85b1c8c256831a560bc0d`  
		Last Modified: Wed, 02 Jul 2025 04:56:58 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cd278759248776dd123a3c8a35f29e9644e1f4a337b6b3cd0dedb8f8b7d63b`  
		Last Modified: Wed, 02 Jul 2025 04:56:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567e972622f1cc4b5f40c7b4c82447aecdbaddf8307cbff93354002cccee14ee`  
		Last Modified: Wed, 02 Jul 2025 04:56:57 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857442f439966369ed65eb48667ad88f5d5e07bdb3d00a39572bc132c5a6da0a`  
		Last Modified: Wed, 02 Jul 2025 04:56:58 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:67c2e9aef03496dc5b4da0c11aa29e12cf22495a0c8b6a95346961bc5ce5639f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6f2a069614f385d8ee3c2cdb9019bd4cc7641e0227462ecafab0179b0857b6`

```dockerfile
```

-	Layers:
	-	`sha256:5e9a450aca83d837a9eb58cdfca680e960b37858a5c5feff226d17177fde69a4`  
		Last Modified: Wed, 02 Jul 2025 05:32:52 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json
