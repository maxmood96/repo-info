## `couchbase:community-7.6.2`

```console
$ docker pull couchbase@sha256:76113c61aa8b62a7bf1e19d73e02f2aed7b9cb787d84ce18b62546fb5a4cac8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:62fd50ed1fb655669d61bfc64768da76c3286a8c3f6170531b6f92cee3e94d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396852559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915ac37d9f95f5176ddb6e2b581654d708eefc03962aee390cea19da722262dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:05:07 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:05:07 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:05:07 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:05:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:05:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:05:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46231b11fc1eff4816b1909c93e6ef4c96e3a5bbcfbb718d50902c2bfb3c8dca`  
		Last Modified: Thu, 08 May 2025 18:31:45 GMT  
		Size: 6.2 MB (6200266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a006f279ad06a8b251b8451510cd86fe922697667cb65cde3fa0c2f03baad6`  
		Last Modified: Thu, 08 May 2025 18:31:46 GMT  
		Size: 864.3 KB (864287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feeab769a8db3bc7f0c6fbe5c213840fabf2553338c8f2f2b7565f83bf1cd2c2`  
		Last Modified: Thu, 08 May 2025 18:31:46 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632684a3f4db9b408af62c8443433b679ff9be2fab04866cbf9d9ded16734c36`  
		Last Modified: Thu, 08 May 2025 18:31:55 GMT  
		Size: 362.3 MB (362272611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7159fa9677488c30d27458e71ba7911e0492188b014762bc74ed6135a5312de`  
		Last Modified: Thu, 08 May 2025 18:31:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04bdc8fed0b5973f3dcb09da8e2e17b810d26018495b91cdab411a066246be7`  
		Last Modified: Thu, 08 May 2025 18:31:47 GMT  
		Size: 816.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d633927a5782b0ca8a9803a16a6eb44cdfe60216c79c26508980fe56357ce`  
		Last Modified: Thu, 08 May 2025 18:31:47 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55f70d7032325ae8aa56fbe3343722805fbcabfa22e219e4f90f564e7462553`  
		Last Modified: Thu, 08 May 2025 18:31:48 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925a95dc429308f6bc9c98eebcba4afc6564270e49b0b42c8fc13b6e5b1273bf`  
		Last Modified: Thu, 08 May 2025 18:31:48 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debdab67051b8ee7c38e64c4e8041deab11d3469cfbf3a7264712b5e26830bc2`  
		Last Modified: Thu, 08 May 2025 18:31:49 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:cb22eebdc69318a0284a4115363831e569549079b0c5840c802fee326c6e7398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa99b932f259cf989620bf09fde6020733c7c6cfb1eaa91368e16704ac36736`

```dockerfile
```

-	Layers:
	-	`sha256:6c47ed4e184f9f5c9c89b4f5e982b4ce93b3c099d176d1037988e56300de747e`  
		Last Modified: Wed, 09 Apr 2025 01:13:07 GMT  
		Size: 35.8 KB (35802 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:f96e6d12d43e7fcfe1bf517e928cb5ac1e4a523085e9c7f724e5759fb44e3455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374265319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde83bdfb155afafec17b9f4dc79302b1e683caa8e6c1423cf36d50ad1c43919`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 19 Jul 2024 19:05:07 GMT
ARG RELEASE
# Fri, 19 Jul 2024 19:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 19 Jul 2024 19:05:07 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["/bin/bash"]
# Fri, 19 Jul 2024 19:05:07 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 19 Jul 2024 19:05:07 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb
# Fri, 19 Jul 2024 19:05:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 19 Jul 2024 19:05:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c91d413632649ac9900c11137ddcf439b8b19852938e442a1c4591632d0da4c8            ;;          'amd64')            CB_SHA256=60c76f5ddc412b202a79ee927010cb0ede334cb7e6849429dd00bc0d7f1ffbcc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-community_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 19 Jul 2024 19:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Jul 2024 19:05:07 GMT
CMD ["couchbase-server"]
# Fri, 19 Jul 2024 19:05:07 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 19 Jul 2024 19:05:07 GMT
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
	-	`sha256:92b9c92f4e52079132b26b88745e43af3bb8682ebb153c4649a5dd6f40a79fc2`  
		Last Modified: Thu, 08 May 2025 22:01:58 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb83066502ec3c1e7c1ba929fca4fd90aa5b188fc84b90f62b3de119618847e3`  
		Last Modified: Thu, 08 May 2025 22:02:23 GMT  
		Size: 341.5 MB (341534296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5fd4b553258c86074314150b27cac0c2bcda54c82f68a9635317ba5c1a4f33`  
		Last Modified: Thu, 08 May 2025 22:01:59 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02708bbec07aad7d61d5b3a22102d825539f5584d6fbb7c910715c2a5d5fb369`  
		Last Modified: Thu, 08 May 2025 22:01:59 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94842701483618cfcf57464ee7eb36a2f2a68d9d4e98404b198e9a701dec5644`  
		Last Modified: Thu, 08 May 2025 22:02:00 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451d8e3f4e83a849acab9c5c050d6674822fdd0d240fe8acd93aa06b0e069edd`  
		Last Modified: Thu, 08 May 2025 22:02:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddd319cdf6f91fed85ee178e9976fbe257576c968fcd1ddfc36f5328db47473`  
		Last Modified: Thu, 08 May 2025 22:02:00 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeef668030dabc4094b69d7cb92883af5e634b9e3d24ae0924f7519647ace73`  
		Last Modified: Thu, 08 May 2025 22:02:00 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:2e46fc71fcae119249b5d68c007e64a085983da6b4094bbd5568a317fe238e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce07d627e2f910b9242446024d8675575faf8932c4d84c0f9f87aa8b9e90263`

```dockerfile
```

-	Layers:
	-	`sha256:cc9a8c5f87c05a4bd346fc6a41ad85f603d13807ed7d55961ba1f18b6ab53e2b`  
		Last Modified: Wed, 09 Apr 2025 06:30:35 GMT  
		Size: 36.0 KB (35987 bytes)  
		MIME: application/vnd.in-toto+json
