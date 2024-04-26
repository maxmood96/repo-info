## `couchbase:latest`

```console
$ docker pull couchbase@sha256:911fbdf52b20887eb32e6eb0b8f6de45a8e3f4b8f8c5ed3ff068896f8eee9e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:9fff1113e92fe64ed002ef9b5ade301441f9dc49072299392adac200b3010382
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.5 MB (731499554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59a9d5e4c0cef2dbcef262b7425b1efa12568b42db5987068454fa87144378`
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
# Fri, 26 Apr 2024 00:17:50 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Fri, 26 Apr 2024 00:19:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Fri, 26 Apr 2024 00:19:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Fri, 26 Apr 2024 00:19:22 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Fri, 26 Apr 2024 00:19:22 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 26 Apr 2024 00:19:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 26 Apr 2024 00:19:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 26 Apr 2024 00:20:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 26 Apr 2024 00:20:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 26 Apr 2024 00:20:57 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 26 Apr 2024 00:20:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Fri, 26 Apr 2024 00:20:57 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 26 Apr 2024 00:20:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 26 Apr 2024 00:20:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 26 Apr 2024 00:20:58 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Fri, 26 Apr 2024 00:20:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 00:20:59 GMT
CMD ["couchbase-server"]
# Fri, 26 Apr 2024 00:20:59 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 26 Apr 2024 00:20:59 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4210eee2952de039c1f5b3a89963cda4dd0159b52c4ed2a7c9c9935bcd31d5c`  
		Last Modified: Fri, 26 Apr 2024 00:30:32 GMT  
		Size: 6.2 MB (6186384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b3ef1aa85d84f41109a0dc4463a916abd2530926a9aa7c4e286d0c2cbbaa29`  
		Last Modified: Fri, 26 Apr 2024 00:30:30 GMT  
		Size: 6.5 MB (6461363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51e7be19ba2b31eddc0c28799e48c14df58c6e288a0a10bb61ff2792729a0dc`  
		Last Modified: Fri, 26 Apr 2024 00:30:29 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a3fdf133de0ad4a3f90049406587a007080665ee676e9735c83056878e74e`  
		Last Modified: Fri, 26 Apr 2024 00:31:32 GMT  
		Size: 690.3 MB (690262460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc8d7525cba67d7b14f93fa40d942e1e5b0d07e073c76945e0fa48bddc8cb7c`  
		Last Modified: Fri, 26 Apr 2024 00:30:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2dcc4c8cf6ca5e8857931aded49322ae9081256c1269597c2949cea485d18b`  
		Last Modified: Fri, 26 Apr 2024 00:30:27 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da6c8caf7e13c3567cebd7293e13a4c3f3f8aa594eb2f30cb53d9aa9853944f`  
		Last Modified: Fri, 26 Apr 2024 00:30:27 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14009705846c843f54a11e57270fc421a7096323b53fbe810c1472b0d780e2fb`  
		Last Modified: Fri, 26 Apr 2024 00:30:27 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1035e7655e5d0f8a2bc1de73a72d8f84890b291fab586d6e37281ca124eefc04`  
		Last Modified: Fri, 26 Apr 2024 00:30:27 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e804061cb6b3da6612d6064f1c79b19faa689790d2ca354cb095229ab0f5d003`  
		Last Modified: Fri, 26 Apr 2024 00:30:27 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:3c7cb2e8687a2528b7ac04fb9b14b2c538dfe095afb351a0d188f3d0a7b69150
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.8 MB (703771319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a4f2c3341a8c62749680e337bc12319fc18c937badd228a55e6e5f66964281`
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
# Thu, 25 Apr 2024 22:12:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 25 Apr 2024 22:13:54 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 25 Apr 2024 22:13:54 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 25 Apr 2024 22:13:54 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:13:54 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:13:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:13:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:15:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:15:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:15:12 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:15:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 22:15:13 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:15:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:15:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:15:14 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 22:15:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:15:14 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:15:14 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:15:14 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4af69279356560dda607e861531c3eac816ea59cc9d1cb1ba210c3c8982e1e`  
		Last Modified: Thu, 25 Apr 2024 22:20:50 GMT  
		Size: 6.0 MB (6028807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4ddf32a1f599a85f69a0735c9366f7a08b9c75d7545b1d3a93cb6f76650928`  
		Last Modified: Thu, 25 Apr 2024 22:20:49 GMT  
		Size: 5.4 MB (5395255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d77c9f32c59fd9515b1f1297169be2f77371c81fcf04482fffec43ff62afbf1`  
		Last Modified: Thu, 25 Apr 2024 22:20:49 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fee93de215588dfad992f6cf8f293b7362605e67f352471f7a940f480cc7ff`  
		Last Modified: Thu, 25 Apr 2024 22:21:37 GMT  
		Size: 665.1 MB (665135487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34671df1221d626b9e96611089c33673b460bcd38de2285ae27e4ac1d617aac6`  
		Last Modified: Thu, 25 Apr 2024 22:20:48 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e684cfc6e7b61a6180d5bb31fdde95641e949fa32e48f24b648f48d2ea0ad168`  
		Last Modified: Thu, 25 Apr 2024 22:20:47 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a28e02ae7fda51e8911b667e628998b0e1abe244b9e11168fa136703fda215`  
		Last Modified: Thu, 25 Apr 2024 22:20:46 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0962720b26c6d954a5f15d26ade134cb70bd5875236b0683e2917a70fc844125`  
		Last Modified: Thu, 25 Apr 2024 22:20:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3faa071d6a05cd8959633f22ce649891f4c15253c780d8eeffbbf5304a74f6`  
		Last Modified: Thu, 25 Apr 2024 22:20:47 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5c6bedba5ebf906fc9c399881ce933b058c32a799b749284589057e00fe5a3`  
		Last Modified: Thu, 25 Apr 2024 22:20:47 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
