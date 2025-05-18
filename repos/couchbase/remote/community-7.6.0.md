## `couchbase:community-7.6.0`

```console
$ docker pull couchbase@sha256:697a0d32928e66fc01123f16cc55a77c4c1ae2c270f787d5592341bc1957b5a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:03a3f6d094a4b64a7b30ad336ac00686067bc9cb4bbe0e0a2e87486edcecca4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384388821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fcde25cd1f6906618b25f78ab8576fb569d81d7a84510a10f619b5bf90de82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Mar 2024 02:04:28 GMT
ARG RELEASE
# Mon, 25 Mar 2024 02:04:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Mar 2024 02:04:28 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["/bin/bash"]
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Mar 2024 02:04:28 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 02:04:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 02:04:28 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Mar 2024 02:04:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d282a2a869781de3fe3753d217ff6b74fc62098383bb36e656dd1c6cff4e0b`  
		Last Modified: Sun, 18 May 2025 04:23:32 GMT  
		Size: 6.2 MB (6200197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f986f8cfac2911bcf64104eb92730d1d8b1254521799f40c82992f20185497`  
		Last Modified: Sun, 18 May 2025 04:23:32 GMT  
		Size: 864.2 KB (864242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce9f6459180c6c925afe4edfc2f142e31de6ef18377c03d7a714e46cda044b1`  
		Last Modified: Sun, 18 May 2025 04:23:31 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57754dac14608dced3afabe558d94d3f5ababcd5f03232d513abcae9b3a2fd84`  
		Last Modified: Sun, 18 May 2025 04:24:23 GMT  
		Size: 349.8 MB (349809310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f939329dd809a4af370b0fd9e4e5fc119089f713ddd17871deb2ace8b79c798`  
		Last Modified: Sun, 18 May 2025 04:23:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe064c86b5ecf6b4184587470f392bb5009e5150af940f52846c99620871d33e`  
		Last Modified: Sun, 18 May 2025 04:23:33 GMT  
		Size: 659.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db9fbd9e5b4797a680178ec977e13676ba8cb6913d4870394965f08736d6f21`  
		Last Modified: Sun, 18 May 2025 04:23:33 GMT  
		Size: 692.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cc156d42dea1e4e377ec833916985b1b82bdb2a7ad20f5c983061655c6e64f`  
		Last Modified: Sun, 18 May 2025 04:23:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7934d5877b7a7cdae9db61ab2d109af3e772839457b3087dd41db005c7530b`  
		Last Modified: Sun, 18 May 2025 04:23:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25de5aa80e8ea08253fb3eb79b300126ca8ee636fe6f15605135c8f5a92b06fd`  
		Last Modified: Sun, 18 May 2025 04:23:34 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:028baa41bffec1af923498133142273afba9706282d3f10c852c0e342339149b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e75c4527f83c96a4a7424de49bbc83d2b01ca9d5fc94502a2b6579805e556729`

```dockerfile
```

-	Layers:
	-	`sha256:5f08f5fd7a1ce27d32297678ee0c7ed36a240a9ee9d579d94c9bf5eab3bc11ce`  
		Last Modified: Wed, 09 Apr 2025 01:14:04 GMT  
		Size: 35.4 KB (35442 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2bc721944346ff4e9775fed852c5858fa4a540d8102082108e3896bc95af34a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366076039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4bd53d2fe411a7431013ce1c3c48b80970b0365a4097735d300de796473ff7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 25 Mar 2024 02:04:28 GMT
ARG RELEASE
# Mon, 25 Mar 2024 02:04:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 25 Mar 2024 02:04:28 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["/bin/bash"]
# Mon, 25 Mar 2024 02:04:28 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 25 Mar 2024 02:04:28 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 02:04:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 02:04:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
COPY scripts/entrypoint.sh / # buildkit
# Mon, 25 Mar 2024 02:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 02:04:28 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 02:04:28 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Mon, 25 Mar 2024 02:04:28 GMT
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
	-	`sha256:bca22554b206b910ab8cf5d910a4c33c22c90d882e35067926b778f316e5b7eb`  
		Last Modified: Wed, 09 Apr 2025 06:37:59 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91870417984b47a7c254ca01d58af3add8691ad18653f22453b56f2d42563363`  
		Last Modified: Wed, 09 Apr 2025 06:38:06 GMT  
		Size: 333.3 MB (333345331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1458bdbd9856ae195e9bda03f0021580b306a7d8d8826a98049a6abed35f0`  
		Last Modified: Wed, 09 Apr 2025 06:37:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e967a15704c0154b7064e71e2437bec52c2ff7c59deb7f44c3c879ae908274b`  
		Last Modified: Wed, 09 Apr 2025 06:37:59 GMT  
		Size: 659.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2962d7c3e75544b9a1312b6977bb4f7d0c688d4eb2e885489128eabc2073b3d`  
		Last Modified: Wed, 09 Apr 2025 06:38:00 GMT  
		Size: 692.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486d77e0263a23f46c2428d633a6b0609bcc442d1ce7fd7cbf5152bd046c11a3`  
		Last Modified: Wed, 09 Apr 2025 06:38:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c64a068fe47a87085ea27d7fcd61196f3e28da6e1f461fbd0f459032d5a146`  
		Last Modified: Wed, 09 Apr 2025 06:38:00 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d629cb26b9dd2c884e1001766b6eb4ad30c0e31daca1bcf9d8be761137fe853`  
		Last Modified: Wed, 09 Apr 2025 06:38:01 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:44f412027cda852589a27ccbd8907fb218c9f9ca5b019e2f2006b68aaa14aa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84134458b70feeebd8f96595e7f46aa6ffe1df10fcba93e15d5bb01db6627704`

```dockerfile
```

-	Layers:
	-	`sha256:8939feba39e927106f410e56c159be4ff1b293cb19608a035260047a7eabab0b`  
		Last Modified: Wed, 09 Apr 2025 06:37:59 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
