## `couchbase:community-8.0.0`

```console
$ docker pull couchbase@sha256:1dbbdb3b75c83f47af9bfa4508523d19a4cf88a543e29347d543ccb292743183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-8.0.0` - linux; amd64

```console
$ docker pull couchbase@sha256:14ccbf6459c59a138b5a2b34adf6e5c3843ce39eba13628c82a529097884dc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.6 MB (490643758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b859b49257aea88844cd7f7be4caf4b35e2c0bca403a5cf1712edd39d9271d21`
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
# Tue, 07 Apr 2026 01:47:53 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:47:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:47:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:47:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:48:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:48:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0
# Tue, 07 Apr 2026 01:48:24 GMT
ARG CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:48:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:48:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:48:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=6c3a94bfb0f5599e1df94bcfa82b45e9b1bfc6a457d0a5186ff01e0f451df5d8            ;;          'amd64')            CB_SHA256=ef4c87749b4d724362609a11aee9624cb85eefbf141e3b5dc14804749bf0717e            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:48:54 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:48:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:48:54 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:48:54 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:48:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba5a4a9ee7a101f450eb713179a937c5a92bcf1da1dc2310fc0276f9fc28de`  
		Last Modified: Tue, 07 Apr 2026 01:49:33 GMT  
		Size: 43.8 MB (43816091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb42f9d0f21d36d3b1b965fe4f89bbe2d3133df3d4a94ef681b27390ae32663c`  
		Last Modified: Tue, 07 Apr 2026 01:49:31 GMT  
		Size: 878.1 KB (878059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a160814037f17096bc4c938740c2c4e60c0e334245a72c589b1d0b457ca4ec`  
		Last Modified: Tue, 07 Apr 2026 01:49:31 GMT  
		Size: 3.7 KB (3721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61f586b0a2b07e2bf1027fb0295fe13f18e1a16e44b0a01dd8f2bc5a14f2306`  
		Last Modified: Tue, 07 Apr 2026 01:49:40 GMT  
		Size: 416.2 MB (416209169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4090bdd588997b0e544dca3d732c90714e8e1b8a3d57d5d35d070ef9d2f094`  
		Last Modified: Tue, 07 Apr 2026 01:49:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43c24d7b1fbee41008fa4fdf1c84ca88f879160b6e44f9e1d08e20886252628`  
		Last Modified: Tue, 07 Apr 2026 01:49:33 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656a78eae2b199b9b70233f93bb1f0e7c24194fcfcbce076a3b1434aed386f06`  
		Last Modified: Tue, 07 Apr 2026 01:49:34 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f8a1324e030299412e6134837d83734038fd76725f18cb2b66662b495ecd22`  
		Last Modified: Tue, 07 Apr 2026 01:49:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6116636219f3f3808cc7529e1ecd3e4fbaafb57bc0972ff6edcfe059b9d1efca`  
		Last Modified: Tue, 07 Apr 2026 01:49:35 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea894bd291391222b432974199b1360cc6f3581a01d92c95c7ebc54f5a76f06`  
		Last Modified: Tue, 07 Apr 2026 01:49:35 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-8.0.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:4cdb0377c8ce28ce70f7f3e7a4cb16730f0bb10872ad5dd5c46a6006ceda649d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 KB (37208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e189e489fa4fedd65593be951bd64742912dbbefdd3159a5289dec5103bbae1`

```dockerfile
```

-	Layers:
	-	`sha256:38d4f5422fcd7070c3d050c383ffaa9b506f5218bcf00e5a69800c22ce058973`  
		Last Modified: Tue, 07 Apr 2026 01:49:31 GMT  
		Size: 37.2 KB (37208 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-8.0.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:46edc0b8645fe74984c4d08aebfff3c28dd225195e9f643deb9e1ada042b5411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.0 MB (463980165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ada31bd66a808d5571c3e6fade16eb2a0b11d111a8e3baf934c53e7e4ec1922`
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
# Tue, 07 Apr 2026 01:51:11 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 07 Apr 2026 01:51:11 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 07 Apr 2026 01:51:11 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Apr 2026 01:51:11 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 07 Apr 2026 01:51:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 07 Apr 2026 01:51:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0
# Tue, 07 Apr 2026 01:51:43 GMT
ARG CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb
# Tue, 07 Apr 2026 01:51:43 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 07 Apr 2026 01:51:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Apr 2026 01:51:43 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=6c3a94bfb0f5599e1df94bcfa82b45e9b1bfc6a457d0a5186ff01e0f451df5d8            ;;          'amd64')            CB_SHA256=ef4c87749b4d724362609a11aee9624cb85eefbf141e3b5dc14804749bf0717e            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/8.0.0 CB_PACKAGE=couchbase-server-community_8.0.0-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 01:52:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:06 GMT
CMD ["couchbase-server"]
# Tue, 07 Apr 2026 01:52:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 07 Apr 2026 01:52:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5facfbfb0f51d8381b0e0eea2e0b4c39269c73433695bc6c7edeb93bc378915`  
		Last Modified: Tue, 07 Apr 2026 01:52:44 GMT  
		Size: 43.6 MB (43633244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17a6c93d28e1dc3f5506b97cd4a1d93708f1c66d648f2ecbe2ab2a87a590a09`  
		Last Modified: Tue, 07 Apr 2026 01:52:43 GMT  
		Size: 765.0 KB (765026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7c91d4ae7c258b8af10135a86a47aa62667d143470e16c19baa6f8f0466953`  
		Last Modified: Tue, 07 Apr 2026 01:52:43 GMT  
		Size: 3.7 KB (3721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad71d7c2ffb058fb036563b1dd8073d39556b70971e1ae6b8bdfc2e9542eca`  
		Last Modified: Tue, 07 Apr 2026 01:52:51 GMT  
		Size: 390.7 MB (390700837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbfeb88a8fdc0894e359fe6a578ca17bc03ad6992d07c60faff6f91654631d2`  
		Last Modified: Tue, 07 Apr 2026 01:52:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b2a2d7d49fc356c0d1f45622f01cddda53cf8184ea30dab9e9ce70df7ea835`  
		Last Modified: Tue, 07 Apr 2026 01:52:44 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef85dff26e08df3fe840fa194067a50d0dff7eb79dbc73bd8e3f537883beb44`  
		Last Modified: Tue, 07 Apr 2026 01:52:45 GMT  
		Size: 846.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589c602ea03b464ff80b482fcd129a232a2f0df48aa2154b0d68e5c2e5465f9e`  
		Last Modified: Tue, 07 Apr 2026 01:52:45 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c810a6a724f2e9518c7894697379a4acb6851dd9941ca4e453d8c0cbacded3e`  
		Last Modified: Tue, 07 Apr 2026 01:52:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d479fe770fe218ddbd8d52f5ac4edfa81b1c2cca24af42e13761b28c2b285d`  
		Last Modified: Tue, 07 Apr 2026 01:52:46 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-8.0.0` - unknown; unknown

```console
$ docker pull couchbase@sha256:ee1ec3bf5bc3a4f37d3ecb19a0bcd1fcee86401cf50230eea96da2ffae22c616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ab2a8a82b7fcd231c5c886b82aea40604cac500952a31540daf8c08615fbde`

```dockerfile
```

-	Layers:
	-	`sha256:cc62c72bd9de7f4d0c21f1392253b9e084a07a54ad21a9867afaa147f6ceb2d2`  
		Last Modified: Tue, 07 Apr 2026 01:52:42 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json
