## `couchbase:enterprise-7.1.6`

```console
$ docker pull couchbase@sha256:caaffdc32520e19d03e313cf8f54db669d66a4dcc305d01c47d7f07fcb013485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:f6fbfea040c78f888b1b371de3af6c2ab9d7a3e61802a191ea49cdae564621eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650734358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d966266515710c09ca1890e71d9b6b0d607ba26c42a75cb7a82ba286fe02b57`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8afbf2f1c19b5c3d3c4cbe897177ce3c9840d161fc0565a3c6efab784eb292f`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 6.3 MB (6299173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400bc3fbd7c94e788acf49bf00e316d1fcd9b182010d90c30381eae089bc06bb`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c89ce562297e58a96cd81b8b1fe5443d7b6ff2b214d58811cada4e2e83db8`  
		Last Modified: Tue, 12 Nov 2024 00:58:22 GMT  
		Size: 616.9 MB (616919823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae46418d8da2075f00a6844dabd34032253c4a34143808208e0077ea08f6b96d`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c4ca65edb4e0fa9d1ca9147de9136660a5418572cb221bfdcf3e59a1750e8f`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8eccd799a40e46d685be5d2f321899fbc66a74a23b60363a6993bed99d683`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214065218982b6113375606491ab1e634762ddca3ef5504388b1d3c6a1ac08c`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a64633e343063c6181b8f3ce93821d5b254c9e5f0a77263f25a7c0eb54a0b0`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294c219b884b9fd09349a24cc63f25d90265beb5881f638f0c09cb366e2bd622`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.1.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:a4c36fc1e6c3f05f62dd3df670c85649a01553185c648974b3032e776ecc9ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 KB (31813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3ed1fb568a61057e0c783454f0fcc75a21c9e7cabab4f9af4c1ab6cd7414b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e11c7f979d544df66d02f8b3b68d4a0e4c6a4b1896a8e8feeedbf448902f81d`  
		Last Modified: Tue, 12 Nov 2024 00:58:11 GMT  
		Size: 31.8 KB (31813 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.1.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:a1812991005eccfabfdc0716b625f330d285680c861e6007d54ad74e59038376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.2 MB (621187507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c752912932861ea9210e7c12b4a4f44415a6039d5a95eb49ae81c58512ab716`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 18 Mar 2024 15:52:02 GMT
ARG RELEASE
# Mon, 18 Mar 2024 15:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 18 Mar 2024 15:52:02 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["/bin/bash"]
# Mon, 18 Mar 2024 15:52:02 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 18 Mar 2024 15:52:02 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND} # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 18 Mar 2024 15:52:02 GMT
CMD ["couchbase-server"]
# Mon, 18 Mar 2024 15:52:02 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 18 Mar 2024 15:52:02 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bf66eb50e8cdc352eff12e1fead418e3a3069f2b2e1b344a29ba629e80aad`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 6.1 MB (6128819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55ec91a8a8ab44c73e38b108b6051c0c41897a7053b0caea198d097c7408fcc`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304b9525db2a3ae82e431ea7618920d0656b09a5fcda75072fb8827e35f26cb`  
		Last Modified: Tue, 12 Nov 2024 01:25:01 GMT  
		Size: 589.1 MB (589080548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8e7f1f525ddfd8ba3fb674f34e1da488c194c5ad1f91668a5e58026e5e75cb`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e232a340d660eaf24f630fc363a56a6ee6f56857c6ca27ac814e23966940aa3`  
		Last Modified: Tue, 12 Nov 2024 01:24:50 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91989d7df9f972a800f38d69c3b7d9d75c8473fce3c5291ba58818a8cf085190`  
		Last Modified: Tue, 12 Nov 2024 01:24:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b99df0e555bfeec0a317a4b7a5de6d951b36f478df438ac0350779e07ed73a`  
		Last Modified: Tue, 12 Nov 2024 01:24:50 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb2faafb6c289081e19c8a37e45938c7e0451f3cab96fa7b0bd41decb162963`  
		Last Modified: Tue, 12 Nov 2024 01:24:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d3399400d923e4249292c833b72e5a635d8c8a4f5ccba6a78b1de6387d59f5`  
		Last Modified: Tue, 12 Nov 2024 01:24:51 GMT  
		Size: 868.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.1.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:7387d305d5f1917cf1c656d014a8b1bd9aad911777a073be61fdf8101e13c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 KB (31983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f60df3c3ae69e504e3b73274cc5906fbb4f3327a5b010f53cd340284aaacf`

```dockerfile
```

-	Layers:
	-	`sha256:ab9f27b2d1466175015fad95fd3e806017463f7b7fedbf46377195b7b44fc701`  
		Last Modified: Tue, 12 Nov 2024 01:24:49 GMT  
		Size: 32.0 KB (31983 bytes)  
		MIME: application/vnd.in-toto+json
