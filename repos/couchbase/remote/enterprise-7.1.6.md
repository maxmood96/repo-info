## `couchbase:enterprise-7.1.6`

```console
$ docker pull couchbase@sha256:f0e3c3da34dd032ebd3ed87d63c05d24f18be3f4a9442bf0f08f744d2f2c17f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:b0d1006f11a5c83d9c958d76f98cd73e3b6c7581812a4db1ff94dc34adc4cdcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.0 MB (652023981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1681128e5c9666985cc446615a82be106d44247cd0daca4023c820dc48855487`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Fri, 26 Apr 2024 00:17:11 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 26 Apr 2024 00:17:11 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 26 Apr 2024 00:17:11 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 26 Apr 2024 00:23:49 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 26 Apr 2024 00:24:50 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Fri, 26 Apr 2024 00:24:50 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Fri, 26 Apr 2024 00:24:50 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 26 Apr 2024 00:24:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 26 Apr 2024 00:24:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 26 Apr 2024 00:26:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 26 Apr 2024 00:26:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 26 Apr 2024 00:26:15 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 26 Apr 2024 00:26:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 26 Apr 2024 00:26:16 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 26 Apr 2024 00:26:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 26 Apr 2024 00:26:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 26 Apr 2024 00:26:17 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 26 Apr 2024 00:26:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 00:26:17 GMT
CMD ["couchbase-server"]
# Fri, 26 Apr 2024 00:26:17 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 26 Apr 2024 00:26:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905b9f5ca2a463183da118b09302ea43e0707e2f34db20749deaa5b4ceef76eb`  
		Last Modified: Fri, 26 Apr 2024 00:33:49 GMT  
		Size: 6.3 MB (6286737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36d8f8fb1120968fbab99dd4a80281aa5e6b430b4e68fd49bffb6e67358d45`  
		Last Modified: Fri, 26 Apr 2024 00:34:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e05e2e7c2a97c72b05e00668c826f65d3427d0d5b4113153286119c5d06527`  
		Last Modified: Fri, 26 Apr 2024 00:35:37 GMT  
		Size: 617.1 MB (617148277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122a03cef7f9db364021af3fe67f46e8c725196d7bff38feedd7250c56eeb6ed`  
		Last Modified: Fri, 26 Apr 2024 00:34:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fa41ab3b4d7bc1e09d5594e0ce02130774514a8cc2a2af32a7e60e4add9501`  
		Last Modified: Fri, 26 Apr 2024 00:34:39 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956ce4f39ca2c942381445f99ea5c91a2b7c5b29d5d8c25fbe0d830ba4151420`  
		Last Modified: Fri, 26 Apr 2024 00:34:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9364e50c0d1ff8e6e72390cd00047154dd83e63d7281ef3626e42ef6515d6a5d`  
		Last Modified: Fri, 26 Apr 2024 00:34:39 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beb81e8e2f62e2206d798fa1cd0219009322347fd29bbbc9324bf2d4b3da8f1`  
		Last Modified: Fri, 26 Apr 2024 00:34:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9577c88a382736bae2b9e275ca5f2cb89f0a5bc1f6120a4500892057257ec7`  
		Last Modified: Fri, 26 Apr 2024 00:34:39 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.1.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:5333eac2306f9f8e6cbafa91825b87a4676e6f70d9eeb2e397bf10175a2625ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.6 MB (622649207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ae5a88b381dbee9837df243e175b650cad3658aba3ee0151d03fc93cd00a8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 17 Apr 2024 17:57:12 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:57:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:57:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:57:14 GMT
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
# Wed, 17 Apr 2024 17:57:14 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:11:57 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 25 Apr 2024 22:11:57 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 25 Apr 2024 22:11:57 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:17:35 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 25 Apr 2024 22:18:25 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Thu, 25 Apr 2024 22:18:25 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:18:25 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:18:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:18:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:19:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:19:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:19:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:19:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 25 Apr 2024 22:19:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:19:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:19:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:19:32 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 25 Apr 2024 22:19:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:19:33 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:19:33 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:19:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9520c4b30446c55e7e55d09aade902332430a20e44eadd7edd756de5a6d4e25c`  
		Last Modified: Thu, 25 Apr 2024 22:23:25 GMT  
		Size: 6.1 MB (6111742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d9d2aff333c561f659b3b48e20d2d3e69f50d3898bd07fd34878a47e378b96`  
		Last Modified: Thu, 25 Apr 2024 22:24:00 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a3d4946c07be7ef872651bd9f49314160e495a66b0fb76277dd3bc7ee869c0`  
		Last Modified: Thu, 25 Apr 2024 22:24:40 GMT  
		Size: 589.3 MB (589326080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07cf03be08df5bae3ada92a90c53933e8db93c04bfc5a2355fc3d0cb12a3549`  
		Last Modified: Thu, 25 Apr 2024 22:24:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501553d951bcaa58554658b60d4314837824b37a1d77c1d9b7daa2499bbf0da8`  
		Last Modified: Thu, 25 Apr 2024 22:23:58 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7761d0d302364c6b8afe9ecbc95e7d6ae8201e21d18953ba81af0844a0e945b`  
		Last Modified: Thu, 25 Apr 2024 22:23:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf31d19a3ea6f8f26fd37959825e20dd2334dd17d1d76de1253ac2e4e2c4f18d`  
		Last Modified: Thu, 25 Apr 2024 22:23:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef2601fa4ce079d0e38b669e36d690b91b90dc8ecdbc8a52c305f32ca034f42`  
		Last Modified: Thu, 25 Apr 2024 22:23:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39fcd85d06cbb09e7219aa5e513f8cf44e0c20850191dac3d4788a1945565c7`  
		Last Modified: Thu, 25 Apr 2024 22:23:58 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
