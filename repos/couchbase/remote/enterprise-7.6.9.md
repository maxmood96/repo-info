## `couchbase:enterprise-7.6.9`

```console
$ docker pull couchbase@sha256:0e08dc9c34effa8b69481b4509cd37ef8607e358d85724db70eac261f35fb173
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.9` - linux; amd64

```console
$ docker pull couchbase@sha256:b3b6fff94f5be0437958aa6706a7c7a37f5ca964a0ce96371e4fd699b88bb586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **820.7 MB (820677106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5e345e8a30353e6ef8cd0163e2b29a14e124d306b19a15f6381b34d26d71e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:47:52 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:47:52 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:47:52 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:47:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:48:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:48:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9
# Tue, 07 Apr 2026 01:48:25 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:48:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:48:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:48:25 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:48:52 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=ce070178588d34a08a792a63f11200c383b7c6d885f337101d13992850c282e5            ;;          'amd64')            CB_SHA256=51cd89e7db43bf5858d6b98e50c43e6217694d814fddabafdf5e798bf8460e43            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:48:53 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:48:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:48:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91428358bb714b3628105f318c4bcbde0861935a00337fd0aa4f26c3bfa4712d`  
		Last Modified: Tue, 07 Apr 2026 01:49:45 GMT  
		Size: 43.8 MB (43816115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27067e43a809bd4d306cb041a1155e40d08391625cecba19f51a70ce9a83aa91`  
		Last Modified: Tue, 07 Apr 2026 01:49:43 GMT  
		Size: 878.0 KB (878043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0e4ca99da0d6211a63fa34ade78fe532ee6d37a318a9ef86ab7fae396dc2de`  
		Last Modified: Tue, 07 Apr 2026 01:49:43 GMT  
		Size: 3.7 KB (3721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f21dc913dbddc2121de586c9948240576878ace408ba1227f7116cd3003470d`  
		Last Modified: Tue, 07 Apr 2026 01:49:59 GMT  
		Size: 746.2 MB (746242518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad2e326c9f7f34bd7279c9ecafd068627796af0927b745a3e751c88f6625ca`  
		Last Modified: Tue, 07 Apr 2026 01:49:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df56c2119a426528ebb0790e50dfb2f602516e95c6942638e919cb14d69e277`  
		Last Modified: Tue, 07 Apr 2026 01:49:45 GMT  
		Size: 813.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f51451b84f5cc5f09bbe20a14aabcd367a6fc7072db27a24fce31627a95a88`  
		Last Modified: Tue, 07 Apr 2026 01:49:46 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4def94d9ca67e40b622763c9e880a639220e527bb5bd0d2a34648d5f8a541c6e`  
		Last Modified: Tue, 07 Apr 2026 01:49:46 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6116636219f3f3808cc7529e1ecd3e4fbaafb57bc0972ff6edcfe059b9d1efca`  
		Last Modified: Tue, 07 Apr 2026 01:49:35 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997ca1d9af6ae92a85f6bcc4c5a03c20fc6fdab1d3e248df36e23820f37ef453`  
		Last Modified: Tue, 07 Apr 2026 01:49:47 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.9` - unknown; unknown

```console
$ docker pull couchbase@sha256:dc9ff54d8a9e5bd2fd03c4584544599215d3c62ce5a7015dec3b602d639ffe03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23304a57212ba3fd557e6c775910df7ae603429d57b3f646d6843a497278f43`

```dockerfile
```

-	Layers:
	-	`sha256:78c54623b57dbe9ebca9ec930d7da69f42f0fdd025d35326ea07aac6d66ecf03`  
		Last Modified: Tue, 07 Apr 2026 01:49:43 GMT  
		Size: 37.5 KB (37522 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.9` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:77a633a82d5b6b225aa607c5587b27c2eeb2c0ef7df64998aa6594c742400cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **787.1 MB (787054799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f196e2a9323c748ff382d281d97732a5c53156021dd9df9d9b32639f3fe20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:09 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:51:09 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:51:09 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:51:09 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:51:42 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:51:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9
# Tue, 07 Apr 2026 01:51:42 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:51:42 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:51:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:51:42 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=ce070178588d34a08a792a63f11200c383b7c6d885f337101d13992850c282e5            ;;          'amd64')            CB_SHA256=51cd89e7db43bf5858d6b98e50c43e6217694d814fddabafdf5e798bf8460e43            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.9 CB_PACKAGE=couchbase-server-enterprise_7.6.9-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:52:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:26 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:52:26 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:52:26 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbb9d8f0ba5a4a004bcabb8363d0dce4b4bfaa5666047137274ca3a80391a5d`  
		Last Modified: Tue, 07 Apr 2026 01:53:18 GMT  
		Size: 43.6 MB (43633260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40ab0e8cf353fcce40282266ecb45dd08f0604657c67ce45cabceab322fdaa7`  
		Last Modified: Tue, 07 Apr 2026 01:53:17 GMT  
		Size: 765.0 KB (765018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a2bf79f5feeff46fb7e5426dd2128bcec1d45c79c10bb53071864b9feeea82`  
		Last Modified: Tue, 07 Apr 2026 01:53:16 GMT  
		Size: 3.7 KB (3724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5539cdff8c013df32eff3489647dbe1edc86d20dad2603952266852e55832489`  
		Last Modified: Tue, 07 Apr 2026 01:53:31 GMT  
		Size: 713.8 MB (713775463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a3da760cbd9fb4237c3d64987214a731341cfb4cac9ed6b6540fe6bb3471c2`  
		Last Modified: Tue, 07 Apr 2026 01:53:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9601704e793ee8d23e301f42e30654aeed9d4e2ee4c6657d982ba94874a3b41b`  
		Last Modified: Tue, 07 Apr 2026 01:53:18 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bff59963ae93bd3085349c12e6f3cb717d47849454095d2ef1d2a196ee79b6`  
		Last Modified: Tue, 07 Apr 2026 01:53:19 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed666b35de508d5abab862cf0f38f233c683aa4aa5b2d1652792e587d54ce24`  
		Last Modified: Tue, 07 Apr 2026 01:53:19 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8df099b9e2e90bc7fda6524c74fc387d129b744d83c0a29e4e0549b9b93795`  
		Last Modified: Tue, 07 Apr 2026 01:53:20 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d479fe770fe218ddbd8d52f5ac4edfa81b1c2cca24af42e13761b28c2b285d`  
		Last Modified: Tue, 07 Apr 2026 01:52:46 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.9` - unknown; unknown

```console
$ docker pull couchbase@sha256:a49dec7de29b00786da9626096457c251399fe38ea9c40208c9f76b686621ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f7c15079ec5246e9124ad9baa26de98a09f25dff3f01c04a8cf61a682a82d2`

```dockerfile
```

-	Layers:
	-	`sha256:714f8f2b9805821f8a9ebf93c9843e07db03a3f49972ad019053a9b5b278909d`  
		Last Modified: Tue, 07 Apr 2026 01:53:16 GMT  
		Size: 37.7 KB (37707 bytes)  
		MIME: application/vnd.in-toto+json
