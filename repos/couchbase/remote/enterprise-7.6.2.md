## `couchbase:enterprise-7.6.2`

```console
$ docker pull couchbase@sha256:d2330052acd849e907d10892d07f22f66aeedecd3ee10990ce8ca5c4e383001a
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369ac5abc321aa28fd00fdd93e408edf8355b9e2ada761d39e4e29de45b813ff`  
		Last Modified: Fri, 09 May 2025 00:15:14 GMT  
		Size: 6.2 MB (6200199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4990ee7d104e89a13a2492dec7a41568db5435ff1cfdc60fb6cae2d938dfd8`  
		Last Modified: Fri, 09 May 2025 00:15:14 GMT  
		Size: 864.3 KB (864272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb99c1d0d993c36d0e5fdbe64d8df168545771e1bd57a014619fc82d317b226f`  
		Last Modified: Fri, 09 May 2025 00:15:14 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d529adb444c131e5075712259397e42933a816438f18f7c381e30e969afd3c4e`  
		Last Modified: Fri, 09 May 2025 00:15:25 GMT  
		Size: 699.3 MB (699256733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37ae71006bfc1fef262d14348edd65f7d3fc169c87d27d9587d37de41bcb7e4`  
		Last Modified: Fri, 09 May 2025 00:15:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de49b8424a4ac3c5cb9f98710bfad31e012b3e862e1ebbbd148c513a148b244`  
		Last Modified: Fri, 09 May 2025 00:15:15 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec04fc08c684450a125d640ab765821a115a5030f227fa9cfa3177f50eaad865`  
		Last Modified: Fri, 09 May 2025 00:15:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fddf65ab69b67cd93eae11ad68d629ea1b64244c8a9dde8d888dd883b79a1c3`  
		Last Modified: Fri, 09 May 2025 00:15:16 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3c7627b10bb815ae4855b4dabd7be8aab8f6df05c20ca3a09bbd5410643c22`  
		Last Modified: Fri, 09 May 2025 00:15:16 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debdab67051b8ee7c38e64c4e8041deab11d3469cfbf3a7264712b5e26830bc2`  
		Last Modified: Thu, 08 May 2025 18:31:49 GMT  
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
$ docker pull couchbase@sha256:538e288400018eee5a45898aa49d8ac7694355bfebedd950fc9df1836a6559ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.1 MB (706095375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fa6408d2d97045f212ca89a60acffff1b4c75fa3d5505f6eeb1298573163a6`
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
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f22907e823d1a774759243aa597f19c9616b4abbbe3d11b0079cf32c4ef8a`  
		Last Modified: Sat, 07 Jun 2025 10:14:32 GMT  
		Size: 6.0 MB (6036710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ae80e71ec25b1a33366b2c2cbb750cfcc24e86e2e103b262ceaa1b63c8dd20`  
		Last Modified: Sat, 07 Jun 2025 10:14:32 GMT  
		Size: 711.8 KB (711840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfe82ba28d47f6ac5e53415b255a2fcedcaa8629215ee291ffd01dc9a548bfa`  
		Last Modified: Sat, 07 Jun 2025 10:14:31 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e631b271d39ee3c502749875ca3cc662d728d3aee62d1c658e89a26498b64640`  
		Last Modified: Sat, 07 Jun 2025 10:14:57 GMT  
		Size: 673.4 MB (673364159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4cfe67d88280b4868484189a0a8d4765085d9dc82bedd1b5dc32b6fd358e3f`  
		Last Modified: Sat, 07 Jun 2025 10:14:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8831dcba1605d92fd460017c14cac3e0c270e1a57593eabbc5c59e7e2b15a9`  
		Last Modified: Sat, 07 Jun 2025 10:14:32 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c314685db78119e0cb1aa7cc13c39af9bae17ebf6734a0a932decafeb2366b`  
		Last Modified: Sat, 07 Jun 2025 10:14:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ec45cb69f0b113f3c48f294efff2704a9dc06d0fdcd272261177064ae5ec0`  
		Last Modified: Sat, 07 Jun 2025 10:14:31 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71329593ed024822cede7b136eae22f19ebf157596e32266aaf58e61b9d33174`  
		Last Modified: Sat, 07 Jun 2025 10:14:30 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d748683becb873efd09e0d57f175996a61a0fdd10ee3782e02a071c7cb0aea39`  
		Last Modified: Sat, 07 Jun 2025 10:14:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:1d888bce23cda93c225a27f0415d0278e3c8b75ef38c4e9d15eb87029f73a58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3d6499dfed44e3cf60b1477b527ae829242e9d2fc0f25bdd224eea846adea1`

```dockerfile
```

-	Layers:
	-	`sha256:74d57e836e1658186ff39070a21ee9f56fa71c42f29482aea4af37ebd230f536`  
		Last Modified: Wed, 09 Apr 2025 18:00:14 GMT  
		Size: 36.0 KB (35990 bytes)  
		MIME: application/vnd.in-toto+json
