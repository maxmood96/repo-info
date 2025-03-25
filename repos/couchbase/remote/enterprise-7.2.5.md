## `couchbase:enterprise-7.2.5`

```console
$ docker pull couchbase@sha256:93cfe6a606035bcb77ee1c2950e8bd7b7b9a8ae195d43b02cf3bc3f0c94a1114
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:105aaa8d62e3d3d740dbd2d93ef75aaf236178bc1faf7a847a0c14c08b75d95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.3 MB (648289068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c30f0fb224458b0ffd83760590dad46925c729f4378927ac8a209e36b466ef5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 24 Apr 2024 22:56:23 GMT
ARG RELEASE
# Wed, 24 Apr 2024 22:56:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 24 Apr 2024 22:56:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 24 Apr 2024 22:56:23 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 24 Apr 2024 22:56:23 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Wed, 24 Apr 2024 22:56:23 GMT
CMD ["/bin/bash"]
# Wed, 24 Apr 2024 22:56:23 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 24 Apr 2024 22:56:23 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 24 Apr 2024 22:56:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 22:56:23 GMT
CMD ["couchbase-server"]
# Wed, 24 Apr 2024 22:56:23 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 24 Apr 2024 22:56:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c935f4cbbbcd0baed8ca0b443981698441481fc8db8484d313ed077ef33af46b`  
		Last Modified: Tue, 25 Mar 2025 18:27:04 GMT  
		Size: 6.2 MB (6196191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df402c84820ad2cdd67a4a0a9e5eee62c6c4d103c09cded056f3e12b75660c1`  
		Last Modified: Tue, 25 Mar 2025 18:27:05 GMT  
		Size: 6.4 MB (6448223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f991d3c54e99ae3602acbe310667b1722d0a3154dbe486b9c405933bab678166`  
		Last Modified: Tue, 25 Mar 2025 18:27:04 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f4d1c6a83a8bbfe352f1de14916b825a0af425de7339b2f19bd7865d06274c`  
		Last Modified: Tue, 25 Mar 2025 18:27:14 GMT  
		Size: 608.1 MB (608128595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6843507af5a35cbeed19529b00abf076e60be6e1c26fbf1a327b2a998d7ded55`  
		Last Modified: Tue, 25 Mar 2025 18:27:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9feabba94d792a6c40c57ae6528a678299552e5109dbf7786586b519e4d093`  
		Last Modified: Tue, 25 Mar 2025 18:27:05 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6947a034a32e8d6ee65cdbee704800df496a5292193caba775450b57535110`  
		Last Modified: Tue, 25 Mar 2025 18:27:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908c5c22ff2007f1c7fb12e90bfe1793d0da5111b1f52db2a8c60479b3d1456a`  
		Last Modified: Tue, 25 Mar 2025 18:27:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0406129055a0f61c293e6e9556668d291d692b294cebc200ac29f49d12d516c5`  
		Last Modified: Tue, 25 Mar 2025 18:27:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e949a7b7c2c7a3bdce61dd1ea2befd45e76c83e25cfc35ac8846ec7206003f`  
		Last Modified: Tue, 25 Mar 2025 18:26:43 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:3d29628de0464c8709450a7c3ee3d6935b0be375be8742f37d64d955ca486739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef2bdd232420a1bc31899e17aee412a1a959ab911e724adadc089770958f86f`

```dockerfile
```

-	Layers:
	-	`sha256:413d703e510d45a6f0afdea8721b1ed1a219911792d79c55afb1409f4b6ca120`  
		Last Modified: Tue, 25 Mar 2025 18:27:04 GMT  
		Size: 35.8 KB (35765 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:b50018ecbfea08f7a6fb4601d534e6a5ade0c5544e96d861efa6071df6fdc0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.8 MB (622784029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e00935014551d916fd73f8dbd2f4e52028c254be812918792a4c12c005d031`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 24 Apr 2024 22:56:23 GMT
ARG RELEASE
# Wed, 24 Apr 2024 22:56:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 24 Apr 2024 22:56:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 24 Apr 2024 22:56:23 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 24 Apr 2024 22:56:23 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Wed, 24 Apr 2024 22:56:23 GMT
CMD ["/bin/bash"]
# Wed, 24 Apr 2024 22:56:23 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 24 Apr 2024 22:56:23 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Wed, 24 Apr 2024 22:56:23 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 24 Apr 2024 22:56:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 24 Apr 2024 22:56:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 22:56:23 GMT
CMD ["couchbase-server"]
# Wed, 24 Apr 2024 22:56:23 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 24 Apr 2024 22:56:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb73578c2ebc0b44814f195c8623d930f21b5fb1c9d030aecb29384565b7bd7`  
		Last Modified: Tue, 25 Mar 2025 18:47:37 GMT  
		Size: 6.0 MB (6032132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606727abd30c590173bda71e805a24661d7c4d07b7174356935173758de0dd08`  
		Last Modified: Tue, 25 Mar 2025 18:47:37 GMT  
		Size: 5.4 MB (5380081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490d61fc6d45b7ce12d53248a4f6017e160adc23e4e0eff8a3c124e1acb2c2a1`  
		Last Modified: Tue, 25 Mar 2025 18:47:37 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b575e633767c2e453aa4f97a695af2100d4e6a22e35290e86c7fb6b9b2f9c025`  
		Last Modified: Tue, 25 Mar 2025 18:47:49 GMT  
		Size: 585.4 MB (585392981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5764739aa419c91f6a07d961198a5e10973abdc9188de9b72fb34cabd0dd9608`  
		Last Modified: Tue, 25 Mar 2025 18:47:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1c6957b672f68f0e630a592d04a2dbddb66ff8d6c83ebd09dd3743c28f4b24`  
		Last Modified: Tue, 25 Mar 2025 18:47:39 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873e49b791bd25aecec8b93a7800fc02bc6598aa67ca093af12b662b0647fef6`  
		Last Modified: Tue, 25 Mar 2025 18:47:39 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71c357b99e4fe221dd400e103389e21eb62fa14d7de225b458c1251b363855c`  
		Last Modified: Tue, 25 Mar 2025 18:47:39 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfa4c3e5e7f8165d708dd2c859cd30ae425bce2525176982845ade875288062`  
		Last Modified: Tue, 25 Mar 2025 18:47:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed1e8ab3886e954ec7fc5812d6fc815c299188341c254445f0f853ef7318ba4`  
		Last Modified: Tue, 25 Mar 2025 18:47:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:07811d834cb58ddd993b0e21918de323160ece6a059a7ceb9a8eaa8617590c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e616c6a911b6ae3573b6f5dd0c49679cfa1ffecaa2ba2485ebdd454934fcecb`

```dockerfile
```

-	Layers:
	-	`sha256:0f153c50cc45e65970fed43648f6118d5acf59d225a429eb5c1175626745fda3`  
		Last Modified: Tue, 25 Mar 2025 18:47:37 GMT  
		Size: 36.0 KB (35950 bytes)  
		MIME: application/vnd.in-toto+json
