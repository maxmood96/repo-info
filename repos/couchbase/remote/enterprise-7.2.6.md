## `couchbase:enterprise-7.2.6`

```console
$ docker pull couchbase@sha256:1dac0baa8d3aa50c8805d470251e7e7439b788dc65352a89b081946e8206ab91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:4b58e0f8320f4bcaa514e02825a9f8b5e9b0db273b3aede57566531df5be959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650159192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483933a28486d97ddc44bbaa28bdf7ea70d9a3e4b677f7db49bd7c65ca6db17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Wed, 08 Jan 2025 01:50:06 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bce8dc623fb4f3b3e2f2cc90f532dac81793aacbfd9a8bc34c7f272703f7a04`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 6.2 MB (6203640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19b7a1a5cddb1dd4cc46227271aebc5b7e04e4a597533097f72215b6de729a9`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 864.1 KB (864102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254b5ffe8533432799b56c6292c531117f209ee875676174e3188c2cd6b67c76`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e6bd39cd5ff83a20414e99f19041663a8313b4e0b5b69f78776e581d85181`  
		Last Modified: Tue, 12 Nov 2024 00:58:21 GMT  
		Size: 615.6 MB (615575393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d278f5fbb4ee15892c99cac6533847d979ee97e0e2b63098ca5edd4b181b0df`  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d0cc313a835e05978d3a22e3dde75ae46d8d17a0e7db6fcdf13ed201b50cf`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159862f14c611065e1095187d03c984757591a20abe4438321678feb502d9abe`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8028c515492bf94343b675e5ffdf634023b92257b9ce84725ae8c515f7db4283`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e6789d74bcbcf727c3b7a0b84ec13e12667d062fba4be39233407cc8ae5477`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ece909dec61e564cba6a304fe5fb8d33cb6caee4a492b8a6f3007f86f3044`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:07b7ddfcbbc6654d535c6f8e3aa740fc5686593c93e326761d5ca322ef7e456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6d9fe49c4d25b47cb627b75fba8083241e331d3cb80a914c8c43703509d432`

```dockerfile
```

-	Layers:
	-	`sha256:34e1cbdcc69402662d39f078751cc241871754e7f67167f99131512e449d1730`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 35.8 KB (35805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:7d6e356fbf2f30d7ae3b911cf30a838def123ad5cdc478f4c28ffc70e29b7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.1 MB (625088287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5969a5713480f17d7527249193f24bb3bc7ac4993aaab6b130a8b41df733d931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c396dd29f50bcc388cd0a519fac3f34e943a627c9613af69542b47bc466da9`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 6.0 MB (6041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d496ab92773d4bdd2c16f3738ba1c83e773a36e0751d0d35726afa7c5a8e82f`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 711.5 KB (711539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c75c5ebbbf48135024eccbbe96b521716a04200202d2875050b09064894d0`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319800ef44742b499fcfbc93d09de12fea172ea219d05d004f91261026c1c30`  
		Last Modified: Tue, 12 Nov 2024 01:21:19 GMT  
		Size: 592.4 MB (592356189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4482d826458e6222a04fe76268240d36790979884f96d96bb5b497326d52182`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4274ccec6ea478230d9bcca8679cdf9aa16736185b4f153f0a55f9c0eb9d8681`  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925dc1477caa9acc381dcf8926803bf1a1cdf324feebd4f41c09da0839e0645`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4336c388f739dae1fd4292ccdf7c2ff11aadc5007eae6d45c269546dc0aba440`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365adc0efea529df15fec109eb02b13100a35d2ce7f790c19926d9dcebcb9b88`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f473ad2dfa83535574df9224f6c6e39650fac01ba4b6f717dfeb0cf4dbfb5f1`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:d6a3d2e1a5b12207764e6ba8007e41e07ca6c779a070cfd4927bc79370c17581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c65b08c9d54fe98556a645b20872297f9b7901d89dac7dad2fc39816b1d9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3800b8a1e257590c56d807e081dc422f2914c16ec2c2f9193abd124d3ef823d`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 36.0 KB (35990 bytes)  
		MIME: application/vnd.in-toto+json
