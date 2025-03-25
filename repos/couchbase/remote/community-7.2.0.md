## `couchbase:community-7.2.0`

```console
$ docker pull couchbase@sha256:9d56619d7edecde1efa6258722b6dc958a01e993e80aebb69fb10fdd40cdbe20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:0670848c8dac7f9bf6e6e8efcc3e8c3b571a95cfe29f013cb86177d815434160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355847515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4310f8163051914520143402eeedf16361deeec67fd5377a8cc1d9317caf0c9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 23 May 2023 21:54:16 GMT
ARG RELEASE
# Tue, 23 May 2023 21:54:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 21:54:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 21:54:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 May 2023 21:54:16 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 23 May 2023 21:54:16 GMT
CMD ["/bin/bash"]
# Tue, 23 May 2023 21:54:16 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 23 May 2023 21:54:16 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 23 May 2023 21:54:16 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Tue, 23 May 2023 21:54:16 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Tue, 23 May 2023 21:54:16 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Tue, 23 May 2023 21:54:16 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 23 May 2023 21:54:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 23 May 2023 21:54:16 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Tue, 23 May 2023 21:54:16 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 23 May 2023 21:54:16 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 23 May 2023 21:54:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 May 2023 21:54:16 GMT
CMD ["couchbase-server"]
# Tue, 23 May 2023 21:54:16 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 23 May 2023 21:54:16 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d861be828cb169634ca9187c0d2b93ec577c9671757c54bb354be1f6eb3d9`  
		Last Modified: Tue, 25 Mar 2025 18:47:06 GMT  
		Size: 6.3 MB (6289525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77657fa8fb5788d43c9c4d38b6c01a8294182cbe83ac9ae66e0090fd11111476`  
		Last Modified: Tue, 25 Mar 2025 18:47:05 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d47dbaf25cab489461c831c6abf1a62d13bf3c46103f928548662156d52258`  
		Last Modified: Tue, 25 Mar 2025 18:47:10 GMT  
		Size: 322.0 MB (322042625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d36dba159c36a46494647779e58deb1a0b175944c82ebae32aed2ed748102bd`  
		Last Modified: Tue, 25 Mar 2025 18:47:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f4806611704844a21505b526b9649b52dc6d9afe11c1809a3835bee0d1ed1c`  
		Last Modified: Tue, 25 Mar 2025 18:47:06 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84b9a8df87141134b679981e0b42e4567afcd642adc532e17b8c777059922bd`  
		Last Modified: Tue, 25 Mar 2025 18:47:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b9fb034df7562a119e5d74d61bc0dc22410aa5289c555cd2c5f116f2ddb87f`  
		Last Modified: Tue, 25 Mar 2025 18:47:07 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2002c5e7bb164fd278e14b96ced380d5b001890e55ece8eb2ed2c67b23bab89`  
		Last Modified: Tue, 25 Mar 2025 18:47:07 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4f8e7a62603677239b05e686f26ecf404376f09c2a014aba4004ff033984b4`  
		Last Modified: Tue, 25 Mar 2025 18:47:07 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:3a291e91dd906b058a05987bceb928751443cedccc8111786f290a4c00c70e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c64061440c5163172f4f5961283fb98e05b951ce75eae3308c05840466fc5e`

```dockerfile
```

-	Layers:
	-	`sha256:24f993dd969c346615b4449228081e3fd32d54f883cf399bf6f10e14900b81ad`  
		Last Modified: Tue, 25 Mar 2025 18:47:05 GMT  
		Size: 31.5 KB (31500 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:d97ea904dbfd4e52979b9f13e338c81431f1938c33fd485b21abcc852938ddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334188472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88175afffb49d009d4e9bc9a71aae44e2bd4f8cf586a62c908e02e5a2d381c78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 23 May 2023 21:54:16 GMT
ARG RELEASE
# Tue, 23 May 2023 21:54:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 21:54:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 21:54:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 May 2023 21:54:16 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 23 May 2023 21:54:16 GMT
CMD ["/bin/bash"]
# Tue, 23 May 2023 21:54:16 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 23 May 2023 21:54:16 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 23 May 2023 21:54:16 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Tue, 23 May 2023 21:54:16 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Tue, 23 May 2023 21:54:16 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Tue, 23 May 2023 21:54:16 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 23 May 2023 21:54:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 23 May 2023 21:54:16 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Tue, 23 May 2023 21:54:16 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 23 May 2023 21:54:16 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 23 May 2023 21:54:16 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 23 May 2023 21:54:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 May 2023 21:54:16 GMT
CMD ["couchbase-server"]
# Tue, 23 May 2023 21:54:16 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 23 May 2023 21:54:16 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86512eb5a9b274725da32b11ba5d1128b4b12b2177d9d6f7c0dfa5f1cd4e88c2`  
		Last Modified: Tue, 25 Mar 2025 18:59:01 GMT  
		Size: 6.1 MB (6119223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf83803fdc184c4c3417c93ecdc646b99de23158d13c8be67cb97e81793cc7`  
		Last Modified: Tue, 25 Mar 2025 18:59:00 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd94f7fe4bbaa04fddf6d22598b3b8e8bb2f3158ae64e1031f5ee07fa1f6eeae`  
		Last Modified: Tue, 25 Mar 2025 18:59:08 GMT  
		Size: 302.1 MB (302091106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f20b0e9ad2200c7dc107450c9f0e863273171dccc27016f2874df7479d3e6c6`  
		Last Modified: Tue, 25 Mar 2025 18:59:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caec78545428600bbf5dcffe47a07f9af6e88cfbb65a8847f1fd3e4345702a3`  
		Last Modified: Tue, 25 Mar 2025 18:59:01 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218d280fc11a9d1e82261fff444fcccb26585a19f5ad9eb657f0afefc0857550`  
		Last Modified: Tue, 25 Mar 2025 18:59:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aaa20ac1d670628d35825c81944982506ac50fc33c52c355859c2e2f3094b2b`  
		Last Modified: Tue, 25 Mar 2025 18:59:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924783ceeac81c79bf9b0f8aa9319bf16e82029c755963e69f575988ca87026f`  
		Last Modified: Tue, 25 Mar 2025 18:59:02 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62c51dc660ebcb0b5ed82e1e7b643b7afe7e5b967e2fdd50b785e49ce6b4404`  
		Last Modified: Tue, 25 Mar 2025 18:59:03 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:dfd7f2bdb034f33d1e230c101cb1b783c43dff57945530be864daf70d1af8c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f881a49269e7bed60ad02d4c7c6a1491517c69b95a7dbf994714e491ee938350`

```dockerfile
```

-	Layers:
	-	`sha256:fc5ca3914488fa479deb5d41d8df16db649ad353e7df62a4aea3a8f586ece04e`  
		Last Modified: Tue, 25 Mar 2025 18:59:01 GMT  
		Size: 31.7 KB (31657 bytes)  
		MIME: application/vnd.in-toto+json
