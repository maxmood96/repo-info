## `couchbase:enterprise-7.2.7`

```console
$ docker pull couchbase@sha256:382d6fa22ca1dd1aaa93e2a5ca495768afed5eac93c2c9e7939ad7dcfc9e694d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.7` - linux; amd64

```console
$ docker pull couchbase@sha256:fb3befa9606c6c6594652225edefa2c1e1ede35f9977f681014f911b46f5eba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.7 MB (658747385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905936e2867daea62f94ef142ac21fac3001c6c079fec7918c31198875771425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 31 Mar 2025 21:57:55 GMT
ARG RELEASE
# Mon, 31 Mar 2025 21:57:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Mar 2025 21:57:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Mar 2025 21:57:55 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 31 Mar 2025 21:57:55 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 31 Mar 2025 21:57:55 GMT
CMD ["/bin/bash"]
# Mon, 31 Mar 2025 21:57:55 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 31 Mar 2025 21:57:55 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 31 Mar 2025 21:57:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 21:57:55 GMT
CMD ["couchbase-server"]
# Mon, 31 Mar 2025 21:57:55 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 31 Mar 2025 21:57:55 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74f04b3106d44d61a0dee503bb94173d044c59f01f66bc7b22273904f6b8f8`  
		Last Modified: Thu, 08 May 2025 17:13:01 GMT  
		Size: 6.2 MB (6200246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d494afd2993c2438bf4d09439c40a8c2c4ab4f05fbdffe28053113bfd0e0ad`  
		Last Modified: Thu, 08 May 2025 17:13:01 GMT  
		Size: 864.3 KB (864285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220228b2cdc75c5b87ff6af2b4ada40ff598c669009e93bcd0d59e82214c11d9`  
		Last Modified: Thu, 08 May 2025 17:13:01 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e066448eb45969431b31a21687ae7fb819fd2122c9e8e5290ef239b90e3cc5`  
		Last Modified: Thu, 08 May 2025 17:22:07 GMT  
		Size: 624.2 MB (624167463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ac307f9c3baeed673b83030dfeb241bd8c321d74de40f253d495a3abef800e`  
		Last Modified: Thu, 08 May 2025 17:13:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59580abca60be75a8c1f38f51ffc925809fb28e89d7bf13c9681107d8aa157b7`  
		Last Modified: Thu, 08 May 2025 17:13:01 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2e17e4ea2fc7f24ad67a1dca13cbfb80289869f356dc0cd8092b3308da08cb`  
		Last Modified: Thu, 08 May 2025 17:13:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a1a548c78b0bd227bb6b131aae98cd3ea0c3806ced3ca7bc2b1b52a45429e7`  
		Last Modified: Thu, 08 May 2025 17:13:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670f2170d1980150e1f2b29984f40c2bdfaeb9332a621a9f988747008299cef9`  
		Last Modified: Thu, 08 May 2025 17:13:02 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efe7e00db4ee56e7568e4c5fdd585567d2d08d8f87dc7f956b5dcac3b83b25a`  
		Last Modified: Thu, 08 May 2025 17:13:02 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:fe2709fbed4dc312ab669f15ed0d15fd850b12864edec7ab89adc6e32a103da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2782c4e1459aa15804da6854e494637ba32acc8c5d09e5f1ea982776980057`

```dockerfile
```

-	Layers:
	-	`sha256:3e34170df1de4740bf2eed1aa1ba944e9070081deb3e5967dac5a230ccece523`  
		Last Modified: Wed, 09 Apr 2025 01:14:41 GMT  
		Size: 35.8 KB (35805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.7` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:96e9b46599901b33851f152c7a0d2c94407f9fb27fb2c384e076715ff9097dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 MB (636542511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b0bbe75824ddff4c67a8df9a7ec6e7e0a27339f8425f31cf699991c9b20144`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 31 Mar 2025 21:57:55 GMT
ARG RELEASE
# Mon, 31 Mar 2025 21:57:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Mar 2025 21:57:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Mar 2025 21:57:55 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 31 Mar 2025 21:57:55 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 31 Mar 2025 21:57:55 GMT
CMD ["/bin/bash"]
# Mon, 31 Mar 2025 21:57:55 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 31 Mar 2025 21:57:55 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb
# Mon, 31 Mar 2025 21:57:55 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 31 Mar 2025 21:57:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=00115e7e10447a1f2e16aedad43cc33205a30e546e0c881e6dd8703bf8b6acf9            ;;          'amd64')            CB_SHA256=40e45a65a78bf5c9bea0f0d16a1c2e3aab3704aaadd41dccc2d8db2308f30fcd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.7 CB_PACKAGE=couchbase-server-enterprise_7.2.7-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 21:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 21:57:55 GMT
CMD ["couchbase-server"]
# Mon, 31 Mar 2025 21:57:55 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 31 Mar 2025 21:57:55 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ccdccb08ab290f1bf5f33c9b3a1de3e29ab99b5710fa7325de743454880281`  
		Last Modified: Thu, 08 May 2025 18:01:31 GMT  
		Size: 6.0 MB (6036543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44c4d997a0d024e276867f67d250c5b7f3b7980a7de4c0fe0ea2b4169c01c46`  
		Last Modified: Thu, 08 May 2025 18:01:27 GMT  
		Size: 711.8 KB (711813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba3060f524ca18b57f45804692e8c1503f31df6572fbc9a7220e62d1a74b888`  
		Last Modified: Fri, 09 May 2025 06:27:25 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a81bcc8e040d234af7ff6b66cd79b1c7a92d5439214d4499c6a6b1c74ff573`  
		Last Modified: Wed, 09 Apr 2025 06:40:12 GMT  
		Size: 603.8 MB (603811486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60aa25aceeac83e06b34f172883eee2149abc170d17021042dbcb9fa5ac44bd`  
		Last Modified: Fri, 09 May 2025 06:27:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39178a1484b4716feec8961d7ba39c2836ded71febd86780faee90cf40894ba`  
		Last Modified: Fri, 09 May 2025 06:27:25 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cfa48d46093fa985f92cd4953ee7b753d45d7f2a3a81a4822ab8363a05a0e4`  
		Last Modified: Fri, 09 May 2025 06:27:25 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b199f66892aa8c90fb91a827c97a047b60e2235b337cddc49699e05d0d0e5ac5`  
		Last Modified: Fri, 09 May 2025 06:27:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e612106620b196beaacf8feb522ca8fd6df6d9b4dffcb184c4993af88e588c4a`  
		Last Modified: Fri, 09 May 2025 06:27:25 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c13feae052d7cd2edc7c3c64306068b5117928f975351c1fb2243dbeb77a7c6`  
		Last Modified: Fri, 09 May 2025 06:27:25 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.7` - unknown; unknown

```console
$ docker pull couchbase@sha256:2f7da807f56c2370500f68d6d4e04606f4fbd1f1519d8642fefb7f217cd98878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ccaee57b122cb1cce7cd1e27673f5ed74c7a4593fd345d4dec7133fcfb40ad`

```dockerfile
```

-	Layers:
	-	`sha256:670fd75f180c9c01e66385ab7c0a7e15edb6b2b530b94fe52597c1c754dce399`  
		Last Modified: Wed, 09 Apr 2025 06:39:58 GMT  
		Size: 36.0 KB (35990 bytes)  
		MIME: application/vnd.in-toto+json
