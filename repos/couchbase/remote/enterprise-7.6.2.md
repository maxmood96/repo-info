## `couchbase:enterprise-7.6.2`

```console
$ docker pull couchbase@sha256:c238043defee47aff4f24bd187eec7f5f0907b6ca4f8a3ee7c5900d1048575f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:76783756b711356a59a68c962caa18fa053edd20d6eb6b80dd7d74e95563f38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **733.8 MB (733836598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263074b98e019339f4abd061d7f12eb9d89b75a4a8ebe1726f6fa84b289fbf15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:00:11 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:00:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:00:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:00:11 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:00:11 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 19 Jul 2024 19:00:11 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:00:11 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:00:11 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:00:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:00:11 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:00:11 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:00:11 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369ac5abc321aa28fd00fdd93e408edf8355b9e2ada761d39e4e29de45b813ff`  
		Last Modified: Wed, 09 Apr 2025 01:13:57 GMT  
		Size: 6.2 MB (6200199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4990ee7d104e89a13a2492dec7a41568db5435ff1cfdc60fb6cae2d938dfd8`  
		Last Modified: Wed, 09 Apr 2025 01:13:57 GMT  
		Size: 864.3 KB (864272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb99c1d0d993c36d0e5fdbe64d8df168545771e1bd57a014619fc82d317b226f`  
		Last Modified: Wed, 09 Apr 2025 01:13:56 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d529adb444c131e5075712259397e42933a816438f18f7c381e30e969afd3c4e`  
		Last Modified: Wed, 09 Apr 2025 01:14:10 GMT  
		Size: 699.3 MB (699256733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37ae71006bfc1fef262d14348edd65f7d3fc169c87d27d9587d37de41bcb7e4`  
		Last Modified: Wed, 09 Apr 2025 01:13:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de49b8424a4ac3c5cb9f98710bfad31e012b3e862e1ebbbd148c513a148b244`  
		Last Modified: Wed, 09 Apr 2025 01:13:58 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec04fc08c684450a125d640ab765821a115a5030f227fa9cfa3177f50eaad865`  
		Last Modified: Wed, 09 Apr 2025 01:13:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fddf65ab69b67cd93eae11ad68d629ea1b64244c8a9dde8d888dd883b79a1c3`  
		Last Modified: Wed, 09 Apr 2025 01:13:58 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3c7627b10bb815ae4855b4dabd7be8aab8f6df05c20ca3a09bbd5410643c22`  
		Last Modified: Wed, 09 Apr 2025 01:13:59 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debdab67051b8ee7c38e64c4e8041deab11d3469cfbf3a7264712b5e26830bc2`  
		Last Modified: Wed, 09 Apr 2025 01:13:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:bc324f9b55b27396089aaad5f8200f90ca8a00ed7ecb2fa5fb59624d383e998d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31cb2c4de065bafc766b1bf70c5aad4d6c0f4e9d3d055e00cfdf54933019917`

```dockerfile
```

-	Layers:
	-	`sha256:b3b7a22c79e35a60ab7a8dbf4248b907751f63ef06fa0e7ad432abecb36b587a`  
		Last Modified: Wed, 09 Apr 2025 01:13:56 GMT  
		Size: 35.8 KB (35805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9ba3545c30ac921f21915dc9a8f41237d1cba549085240999c7bab90b5b74f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.8 MB (710754920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a623fe04e8eaeeee7e5d6dd3f942dfa377c0d0c9c6cc19e76fc7ebe2086a6fa7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:00:11 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:00:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:00:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:00:11 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:00:11 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 19 Jul 2024 19:00:11 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:00:11 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:00:11 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:00:11 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:00:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:00:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:00:11 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:00:11 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:00:11 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ea4356529f36aa4ec113178da8c456d97039bc5389ed018accb808bf12b8`  
		Last Modified: Tue, 25 Mar 2025 18:35:30 GMT  
		Size: 6.0 MB (6032186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52e32c96548e469a4ffdb44999a305d8072afd7ab8c0f7cace809d3ed1a7828`  
		Last Modified: Tue, 25 Mar 2025 18:35:30 GMT  
		Size: 5.4 MB (5380096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285b0bbeaa06987bb065c0f04e5f5b2dda67886e91c8f3d363189f6c58979e52`  
		Last Modified: Tue, 25 Mar 2025 18:35:30 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b305d16aabdaac2a4566edd3be8dda5da3fe0ec1764d4e17b19fc0a67384a6cf`  
		Last Modified: Tue, 25 Mar 2025 18:35:44 GMT  
		Size: 673.4 MB (673363801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac89706089c40523ed42c35799172d6ba02c638651ceb9b18ae1b5f171bddae`  
		Last Modified: Tue, 25 Mar 2025 18:35:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceba9ee4b53cd08e98842d4d0c1d1ae97ca532fc31239ffacedfa3bd03e09ae6`  
		Last Modified: Tue, 25 Mar 2025 18:35:31 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18682a361ee8896cb4cc01208769cebf3e0942d385c3552ed9fe6cad9b20928`  
		Last Modified: Tue, 25 Mar 2025 18:35:32 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c409e3f36e4c94b0b4c05c462621d3a24dd273206bae493b3be6a066510de`  
		Last Modified: Tue, 25 Mar 2025 18:35:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd65b9ad82d910df448497b19f760884c8d80c07137da55c57839a101f0a8c6`  
		Last Modified: Tue, 25 Mar 2025 18:35:33 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3496f1648d6750ea74bafad18586d40804d601f3031fa4a6cb044e09f876a9bd`  
		Last Modified: Tue, 25 Mar 2025 18:35:33 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:82c4876c0b0527ba8ff114e97014a760ce9537a1ea53e027d433d3247360b1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (36000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73f05f37244dda2d170e8dad44d714550b6e27133965b8e7c47475ab9b68ee6`

```dockerfile
```

-	Layers:
	-	`sha256:46de8c3f03a76ebdfeb313c3425e72cac08d35379e2649b41bb6ac38922e77c0`  
		Last Modified: Tue, 25 Mar 2025 18:35:30 GMT  
		Size: 36.0 KB (36000 bytes)  
		MIME: application/vnd.in-toto+json
