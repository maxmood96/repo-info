<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:7.2.0`](#couchbase720)
-	[`couchbase:7.2.2`](#couchbase722)
-	[`couchbase:7.2.3`](#couchbase723)
-	[`couchbase:7.2.4`](#couchbase724)
-	[`couchbase:7.2.5`](#couchbase725)
-	[`couchbase:7.2.6`](#couchbase726)
-	[`couchbase:7.6.0`](#couchbase760)
-	[`couchbase:7.6.1`](#couchbase761)
-	[`couchbase:7.6.2`](#couchbase762)
-	[`couchbase:7.6.3`](#couchbase763)
-	[`couchbase:7.6.4`](#couchbase764)
-	[`couchbase:7.6.5`](#couchbase765)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-7.2.0`](#couchbasecommunity-720)
-	[`couchbase:community-7.2.2`](#couchbasecommunity-722)
-	[`couchbase:community-7.2.4`](#couchbasecommunity-724)
-	[`couchbase:community-7.6.0`](#couchbasecommunity-760)
-	[`couchbase:community-7.6.1`](#couchbasecommunity-761)
-	[`couchbase:community-7.6.2`](#couchbasecommunity-762)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-7.2.0`](#couchbaseenterprise-720)
-	[`couchbase:enterprise-7.2.2`](#couchbaseenterprise-722)
-	[`couchbase:enterprise-7.2.3`](#couchbaseenterprise-723)
-	[`couchbase:enterprise-7.2.4`](#couchbaseenterprise-724)
-	[`couchbase:enterprise-7.2.5`](#couchbaseenterprise-725)
-	[`couchbase:enterprise-7.2.6`](#couchbaseenterprise-726)
-	[`couchbase:enterprise-7.6.0`](#couchbaseenterprise-760)
-	[`couchbase:enterprise-7.6.1`](#couchbaseenterprise-761)
-	[`couchbase:enterprise-7.6.2`](#couchbaseenterprise-762)
-	[`couchbase:enterprise-7.6.3`](#couchbaseenterprise-763)
-	[`couchbase:enterprise-7.6.4`](#couchbaseenterprise-764)
-	[`couchbase:enterprise-7.6.5`](#couchbaseenterprise-765)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:7.2.0`

```console
$ docker pull couchbase@sha256:76114e559a863fde21c7b327ac82c3b5e265599e259ea8731f3c739c42e65464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:772a2c8fcc3e4a65e410053e5b4f1a4c5349da0ccb78de4d458cf91e49719263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.7 MB (663685101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232147af3c363497c044401c3a221e39f18ad490a26bf4efc84e5e972db019c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:54:54 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Aug 2023 02:54:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Aug 2023 02:54:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 02:55:09 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Aug 2023 02:55:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 03 Aug 2023 02:55:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 03 Aug 2023 02:55:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 03 Aug 2023 02:55:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Aug 2023 02:55:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Aug 2023 02:56:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 02:56:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Aug 2023 02:56:26 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Aug 2023 02:56:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Aug 2023 02:56:26 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Aug 2023 02:56:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Aug 2023 02:56:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Aug 2023 02:56:27 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Aug 2023 02:56:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Aug 2023 02:56:28 GMT
CMD ["couchbase-server"]
# Thu, 03 Aug 2023 02:56:28 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 03 Aug 2023 02:56:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35618df5c9a71269b91577e6aea59155f8edb63501d542ce129979a4d9e328b`  
		Last Modified: Thu, 03 Aug 2023 03:03:49 GMT  
		Size: 6.3 MB (6285930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76951ffea2eb9305de925d27044022b82719478ca00eb5b6aa7c90bef872ed3a`  
		Last Modified: Thu, 03 Aug 2023 03:03:47 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91aeb93d2aa72ad20c4cf699740572ef7fd37fa590584cbbb57e54731b7b6cad`  
		Last Modified: Thu, 03 Aug 2023 03:04:45 GMT  
		Size: 628.8 MB (628814146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d05cef67ec666d42e81e534724fed4d45134c72ee363e7a29f01a2ce99df6f`  
		Last Modified: Thu, 03 Aug 2023 03:03:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f693b82a631465ff6992c15eb0c719a8520cd5aea5e5b792f56780e5198372`  
		Last Modified: Thu, 03 Aug 2023 03:03:46 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9f16769ccd60bfc6c37bac170d94eaea8450f86e7037af4bbdd76ffd32dd9c`  
		Last Modified: Thu, 03 Aug 2023 03:03:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610602c4cf5517d76cf7f4d8e9441310dbd2ba991dc2a93f94bb0c791e5ba0b3`  
		Last Modified: Thu, 03 Aug 2023 03:03:45 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18677c045c6414523bb2312b313c88a51526e6a391a04e30d03d247b089d724`  
		Last Modified: Thu, 03 Aug 2023 03:03:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0adce102afa0b1f44d32dfba2af0957cf3eee275bade93e91635ab108fe7a9`  
		Last Modified: Thu, 03 Aug 2023 03:03:46 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:191e40485c3d7a0404733af87322a7b02149d074bf1adc03eb8949e17aa62ebd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 MB (636755632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0b7899f3ccdee4d8441e1232f6633f1a2d9b4ae1c6c28580194d087884f836`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:13:43 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Aug 2023 01:13:43 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Aug 2023 01:13:43 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 01:14:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Aug 2023 01:14:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 03 Aug 2023 01:14:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 03 Aug 2023 01:14:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 03 Aug 2023 01:14:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Aug 2023 01:14:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Aug 2023 01:15:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 01:15:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Aug 2023 01:15:13 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Aug 2023 01:15:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Aug 2023 01:15:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:15:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Aug 2023 01:15:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Aug 2023 01:15:15 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Aug 2023 01:15:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Aug 2023 01:15:15 GMT
CMD ["couchbase-server"]
# Thu, 03 Aug 2023 01:15:15 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 03 Aug 2023 01:15:15 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad91e7dfaee3352f726a7133ee4af8e38e1f989f4a537f0618abd00bb4c784e`  
		Last Modified: Thu, 03 Aug 2023 01:18:32 GMT  
		Size: 6.1 MB (6110566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d117fae1bda3d1ce14ae0cf3990cf2156ac7e81f990b54bc4ae483f50d6a6e`  
		Last Modified: Thu, 03 Aug 2023 01:18:31 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d8d44e8dd52499dbe81834a7c9b340f54094d3b65d3b4c324924c8a48d350`  
		Last Modified: Thu, 03 Aug 2023 01:19:14 GMT  
		Size: 603.4 MB (603440121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742a874d02c82e1540e5b6c7ff63495b2312be683041805df65174a1a9bd9b9b`  
		Last Modified: Thu, 03 Aug 2023 01:18:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ac7f9d2f4e2ad03a33ad57c9287d472fc372ac96ed3c4e908b2f0e2245e36`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4430dfb88cb992b7c4d808078a7d23f2ff4883b459d0b099adf44f58e3145cb0`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e93e4ab3785185d50863b20c222c5bb80dd625a42cd01491ff351314eb78f2`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59147a009b35da6ae2cd75b9fc14052375adb5467ab8c193ba79f63cfae342a6`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083a640e5a13d39b2c983bb586c2fcd1283a577da7c1c718d014d05e5a281a10`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.2.2`

```console
$ docker pull couchbase@sha256:fdd84aed2ea79384a0223080651ca06ac2c9a137b149725a5c7d9bdbbb2f789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:16ea62e32f96fa27d0e1fc3ab84e0877f0fa19d0ea0baf494de98793de087e1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.9 MB (668875225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2894333b48a5b7ef3bd9fea7da57f98a57c056f7562411034712619b2378121`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:34:46 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 13 Oct 2023 07:34:46 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 13 Oct 2023 07:34:46 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 07:35:15 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 13 Oct 2023 07:35:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 13 Oct 2023 07:35:16 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Fri, 13 Oct 2023 07:35:16 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 13 Oct 2023 07:35:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 13 Oct 2023 07:35:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 13 Oct 2023 07:36:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 07:36:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 13 Oct 2023 07:36:46 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 13 Oct 2023 07:36:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 13 Oct 2023 07:36:46 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 13 Oct 2023 07:36:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 13 Oct 2023 07:36:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 13 Oct 2023 07:36:47 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 13 Oct 2023 07:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 07:36:48 GMT
CMD ["couchbase-server"]
# Fri, 13 Oct 2023 07:36:48 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 13 Oct 2023 07:36:48 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f74dd8ee7b698aa30f6021db1eba8fe81ac68ece2c5829894a3fcc95667e11`  
		Last Modified: Fri, 13 Oct 2023 07:45:16 GMT  
		Size: 6.3 MB (6285994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f719fafe0b994fb15b24cf6d3c25952e43fb9aea27536d12b441fff0590cfe`  
		Last Modified: Fri, 13 Oct 2023 07:45:15 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1b00b6ed63000d00ec4f85352eb288d152551dbfeaf88a9551ab3c5394829`  
		Last Modified: Fri, 13 Oct 2023 07:46:14 GMT  
		Size: 634.0 MB (634004190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97b4d65bdddc8424ef131ab99944ee044d73a4a75838eb33141954066697655`  
		Last Modified: Fri, 13 Oct 2023 07:45:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f621a143a41ed5304d93bf556dd005d9a5a37bee913adb6c51fa73a5ac847d1d`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 742.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6593905d712fac24f86d21544b6e259bfc0f04d60bce8a754a2d4a48b3c4e2fb`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e73873d14d11576c1686a77f0f248a99a7ad8da429f5b36a48a67d27ae21f6`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a445bbeb8054941d3516c04c3749ab81421520836941fff2a7399a985bb96fbd`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3ab2ca4efb0b01347210fb5176c132ba36a49db49a24fcb317837ef70b8f5`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6b388f27b914f0f9f57b843c2675f084727dcfd42f4771653d4e92f25100cbf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 MB (640369682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a94a2ed1d241646d5e83ef4b6aab188551f2293767f606b3912ff7bc99816c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 03:56:50 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 13 Oct 2023 03:56:50 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 13 Oct 2023 03:56:50 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 03:57:08 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 13 Oct 2023 03:57:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 13 Oct 2023 03:57:09 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Fri, 13 Oct 2023 03:57:09 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 13 Oct 2023 03:57:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 13 Oct 2023 03:57:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 13 Oct 2023 03:58:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 03:58:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 13 Oct 2023 03:58:21 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 13 Oct 2023 03:58:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 13 Oct 2023 03:58:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 13 Oct 2023 03:58:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 13 Oct 2023 03:58:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 13 Oct 2023 03:58:22 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 13 Oct 2023 03:58:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 03:58:23 GMT
CMD ["couchbase-server"]
# Fri, 13 Oct 2023 03:58:23 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 13 Oct 2023 03:58:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e1c15a1b1f2e05138fe2b49be3e2f9ea9a9dcd2a096c2ee69d1636a18082ef`  
		Last Modified: Fri, 13 Oct 2023 04:01:39 GMT  
		Size: 6.1 MB (6109875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650354a58c417d4e2144895bce1598e3e897806b813a323182f8bb387e41615d`  
		Last Modified: Fri, 13 Oct 2023 04:01:39 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c375bb8cb7f5c39c87b4b30e1dc5a9b80ff1c0e7f607c7404b29655c522aa`  
		Last Modified: Fri, 13 Oct 2023 04:02:22 GMT  
		Size: 607.1 MB (607055943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf3a287bfa03cf1499527ebd79713fc030bb3f840e6312e5179bf53bc59c6b7`  
		Last Modified: Fri, 13 Oct 2023 04:01:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14c1cfa00c110bdc0b4e6f78bc70bb4ea6c7885140339b4a4ef4a30f3ec8090`  
		Last Modified: Fri, 13 Oct 2023 04:01:37 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c96446b8555fe77fd9136bd14317211f48d02ebe24313effe313e888069b16`  
		Last Modified: Fri, 13 Oct 2023 04:01:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd91b09193923acf20558fcedeeaa0f1ea5a19816b3f9aa659876e5e5fb3a731`  
		Last Modified: Fri, 13 Oct 2023 04:01:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26a88b5a9cfb6a0b6cb06b081ce695e444891ab3b656672021f981c386354de`  
		Last Modified: Fri, 13 Oct 2023 04:01:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6beda31d1c3b875888f514a497d0d74b03676af327382f13bbddf8a03dd0afef`  
		Last Modified: Fri, 13 Oct 2023 04:01:36 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.2.3`

```console
$ docker pull couchbase@sha256:daea166ce4cf8c1b2472d3cfbd0fa6675f33f23eec4ed1e9ee6f66d5ebe40610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.2.3` - linux; amd64

```console
$ docker pull couchbase@sha256:18415c4cbdb61fc0da3c58eead4d78525dff2ee655155109aa61cde2bdb92faf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.0 MB (670029391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbb0f5f6965e30ec7917749c4de1fab9b1e5e297d971c35bef9eeb725426a81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:25:59 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 10:26:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 10:26:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:26:18 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 10:26:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 10:26:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 10:27:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:27:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 10:27:40 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 10:27:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 10:27:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 10:27:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 10:27:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 10:27:42 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 10:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 10:27:42 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 10:27:42 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 10:27:42 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78735bf4de6f426e7422bf3d534899d82db0f0d2d66034d6db341ce8d26f0b2`  
		Last Modified: Sat, 16 Dec 2023 10:35:19 GMT  
		Size: 6.3 MB (6286008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de84f8aa811274c19311a984e5405ac2a61a5227477fe24ec3fbe305f97cf89`  
		Last Modified: Sat, 16 Dec 2023 10:35:17 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e041a4b9d588c08b72d8f7f657e4ce93467fcd9cc539126b43484ab1fe9e28`  
		Last Modified: Sat, 16 Dec 2023 10:36:12 GMT  
		Size: 635.2 MB (635154999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9164d43e9daf583b22402ce0651a77e6c21552b2521860a0d998cf102362612`  
		Last Modified: Sat, 16 Dec 2023 10:35:17 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b90a6de88b7882e89a2584cb53f3c93dcca0c1eb69ad8f184163e59380e33`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ec37b4f6e10362278fd677e1e15d6f434617739b005fdbcccae021278f3701`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4513a22f09dd3d7fe1df2c2a9a17deb0aab7d12e935ebfa6df33c1c2fffa049b`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98488eff588073c8b3ca3cbdb24074de5ad27a496b39903482f0b4dacd8b898`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804c21d7cb8de5ef4419d5b801ab528eeb39863ae8cce22b694174a8f3185fdb`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.2.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9070a162a941ab9d43e2f8b0d361a4e7f5aec53ee89cfdf26c5860e1893e7370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.4 MB (641439491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c85bcaca8610743429a4a9374dadd7fc73deebb41fa34f63dad4d4c4d74b1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:54:01 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 09:54:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 09:54:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:54:19 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 09:54:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Sat, 16 Dec 2023 09:54:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 09:54:20 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 09:54:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 09:54:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 09:55:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:55:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 09:55:27 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 09:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 09:55:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 09:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 09:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 09:55:29 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 09:55:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 09:55:29 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 09:55:29 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 09:55:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a83d6afdb30f174382ab5039378b0bae25520129e600a54c8d3a1ee404eeae`  
		Last Modified: Sat, 16 Dec 2023 09:58:48 GMT  
		Size: 6.1 MB (6109493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955fe360ffe527e18bb09ebf93804eed1ffda89965d306366b2a5ac16cf6d9a`  
		Last Modified: Sat, 16 Dec 2023 09:58:47 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911e51334194534bc793dd194873bc3795c3971d6a92ed68ac67b61a2d242f35`  
		Last Modified: Sat, 16 Dec 2023 09:59:28 GMT  
		Size: 608.1 MB (608122491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8a7f3860597d49bff454f019588b40bea00ae01a7969f22ecb8b92b6c3f361`  
		Last Modified: Sat, 16 Dec 2023 09:58:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1084ffb17cf83af9888747528711823416c81e65d2ef29a3d48f161727879ec6`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ca2c8f48efc6c50ae6e750a7a8540fa98baa2c39790395af00ffa6c21ac99c`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbd4a2f5d8034e2b86a45be911af0069430b9f298f1ed28722a6253273645ac`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dfa9429a7aa09076fada3bf7151afedd3bba71e3b44d043918ac62ca95cdc0`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd10be5c4525a4962ee0d31225e6c568a680f6f9a75d03c13715f122c850b4ef`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.2.4`

```console
$ docker pull couchbase@sha256:c2f921c253e8ff868e96b0afc535fb611473c3c7b3c0381d8d717b638a162de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:396086ccc8a180fb085b73d57cb26ff80f1768078e01ae3f0741731282eee134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.8 MB (640753927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2265daaa10bfb096cc2b697863cfd7d91dd051b1cd3e35be666e7514fa9609`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:43:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Tue, 16 Apr 2024 04:43:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:43:44 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:43:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:43:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:44:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:45:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:45:03 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:45:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:45:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:45:05 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:45:05 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:45:05 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:45:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f13bf02912f439e34bca8c94fcdad907768c193ca0d2d336e45368f629d1f`  
		Last Modified: Tue, 16 Apr 2024 04:53:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd5306cc5ca74bf36574560ae5d4db54aa59f87af511c9f111195d7e2a318e7`  
		Last Modified: Tue, 16 Apr 2024 04:54:47 GMT  
		Size: 605.9 MB (605878411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35aeb2a5afb5a5a671b91d4b5cb8c2b9033df03be8719eb6c9cfa2786e474174`  
		Last Modified: Tue, 16 Apr 2024 04:53:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd8c73c7c23291ecc35c4cc14b9d15e7acdc482c416e66bbdb3f3c5ccea2d1`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1d59efddd5be2f0b371bd100c7245d9e9adb335846af64aaa6be03f9be0fba`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74b4d7fa4a71ae091abe170e37cd1ecbb5372620506ca2863fbfdc039e50b7`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d9a7ddcb35252a922bd19ca94bce025a15ef7cd76ef40a5e8220eae923e393`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876d28a90fc70e06bc6fa398052a97d4922897452aa8a2db1367a31e0bd30d12`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:cb0d3bcfc90b44709a057ae5bfd66b0556f610286a773e575c0d134549120780
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615930332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae52aa3b8d05afcbedea1f7290dcb7035f0cc3ab2dcded9802fe5ccc9b2a7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:22:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Tue, 16 Apr 2024 03:22:22 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:22:22 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:22:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:22:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:23:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:23:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:23:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:23:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 03:23:32 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:23:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:23:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:23:33 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 03:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:23:33 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:23:33 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:23:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63a620f1ecf9579c760cf290f09f23af0305d47d3bb6f3cbcaf31145979bb8`  
		Last Modified: Tue, 16 Apr 2024 03:28:32 GMT  
		Size: 6.1 MB (6110804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db1cb36f52f81614935cd6dd44cf22439186895e6198859fe1cc7c5a1298fc`  
		Last Modified: Tue, 16 Apr 2024 03:28:31 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05138313d3eff50a8b91f16c8d6df5b9e8bd313609e8dc9ee886f240c2db999c`  
		Last Modified: Tue, 16 Apr 2024 03:29:12 GMT  
		Size: 582.6 MB (582610179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcd6463ec7d5ad156ca56e4589e735be34e7c909ac5f6763b320d95137492e5`  
		Last Modified: Tue, 16 Apr 2024 03:28:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1817853d4050bddeff14bb376210616831126c8952f52082f5e29ba8d14ba739`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a91053c9390921bef945eb15171ed04baf15fb026992c2380e2109150a5893f`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174697aa7f6bc87a5ca9ef758d5d25554ee48c62d2bbcdd61a800bcffcc5075`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae688037262871a8b79a71a738f292d3fad93887fae54bdcea5e0f7f203db735`  
		Last Modified: Tue, 16 Apr 2024 03:28:30 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d11b91b7e0e5f4ea147d1df339cdf3a3c1521d6f7eacc39abcc58a7cafabf62`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.2.5`

```console
$ docker pull couchbase@sha256:3bb926a13a9d46fd8a44bfe42625f610bc3a10f8657b3886b5f22604bb8cb681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:fc54d3c6ed5ff6293e3f24ce44ea715749b9c4b604b88074e9dc2faba6ad6383
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644241117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf1d526853d30263ae34dd0d990eec906e7d37e795a07b63fee79eaff9d8f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:22:12 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 16 Oct 2024 02:22:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 16 Oct 2024 02:22:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:22:28 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 16 Oct 2024 02:22:55 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 16 Oct 2024 02:24:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Wed, 16 Oct 2024 02:24:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Wed, 16 Oct 2024 02:24:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 16 Oct 2024 02:24:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 16 Oct 2024 02:24:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 16 Oct 2024 02:25:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:25:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 16 Oct 2024 02:25:35 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Wed, 16 Oct 2024 02:25:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 16 Oct 2024 02:25:35 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 16 Oct 2024 02:25:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 16 Oct 2024 02:25:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 16 Oct 2024 02:25:37 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 16 Oct 2024 02:25:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 02:25:37 GMT
CMD ["couchbase-server"]
# Wed, 16 Oct 2024 02:25:37 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 16 Oct 2024 02:25:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a75f1093d68c4a4df16d8da90c0a7fa5de10d215bc15c4dfb921639b3da9d`  
		Last Modified: Wed, 16 Oct 2024 02:32:33 GMT  
		Size: 6.2 MB (6204670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b2d185509813a24f9505cb9d5a616a84d04580eaea45ae3f2e4d2afdf5757`  
		Last Modified: Wed, 16 Oct 2024 02:32:32 GMT  
		Size: 1.1 MB (1092446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6687ab00d3b506b39a9a5bd5fb095e14dcc2bd3de974060420f4c06f980c7060`  
		Last Modified: Wed, 16 Oct 2024 02:33:24 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c200ff7db29f8e412443beae9a0010823c2bbac99d7f416179bd22952a8712`  
		Last Modified: Wed, 16 Oct 2024 02:34:19 GMT  
		Size: 608.4 MB (608355047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b8428bcb6049e629792216a6372f3053c6a9486d34cf2dd303ad962797c863`  
		Last Modified: Wed, 16 Oct 2024 02:33:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1deea5194a5cc887c2f95bec477c12d05e59a44faa83c99bfbb8cb772cb99a8`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 821.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8c44ef19e976a6de5a58b04610dc15b5c36dc79d8dc63821e6c7ffccec1ffd`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2259fd86f971d980baf3cc55cdd8d1f43a264352ee6ad57885b6aaf07e8c38`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6c315b3ac4fea94dfe8a835e58497f65bc961a0bf1e4d8c3e75ebc4947976`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d0dccfb2833e2b58b4ff5d17a6554065b98640ee30e4cfb2ed2989a6060218`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:66b3fdd690d608ffbe551dcdd5e1c9e9cb92ed55fc0f0ee3f2a95c6af2732833
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619821330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d12fe4f829d544aeca6ae2616502b9a918de98fe99b3e06fb39504ca672fff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 00:58:37 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 16 Oct 2024 00:58:38 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 16 Oct 2024 00:58:38 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 00:59:12 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 16 Oct 2024 01:00:25 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 16 Oct 2024 01:01:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Wed, 16 Oct 2024 01:01:31 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Wed, 16 Oct 2024 01:01:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 16 Oct 2024 01:01:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 16 Oct 2024 01:01:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 16 Oct 2024 01:02:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 01:02:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 16 Oct 2024 01:02:45 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Wed, 16 Oct 2024 01:02:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 16 Oct 2024 01:02:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 16 Oct 2024 01:02:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 16 Oct 2024 01:02:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 16 Oct 2024 01:02:46 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 16 Oct 2024 01:02:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 01:02:47 GMT
CMD ["couchbase-server"]
# Wed, 16 Oct 2024 01:02:47 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 16 Oct 2024 01:02:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78e6f6941d8212e81ac25e018b1ead37c0c44c9ed155d6f48148bda886de531`  
		Last Modified: Wed, 16 Oct 2024 01:06:15 GMT  
		Size: 6.0 MB (6041871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc7c114f093f2a5b8b90e9f681ab5cbe80a551963e43c9758c3323999f692b6`  
		Last Modified: Wed, 16 Oct 2024 01:06:13 GMT  
		Size: 938.0 KB (938015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fc261a6e4a2cc3d68c2b67288a62a642ecbb69f1c9c7c7cbbf5f85dd93e262`  
		Last Modified: Wed, 16 Oct 2024 01:06:54 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caa32686ca5cae50370a02f540cc662ec955316c99c3c4dd48c8e6bce2a762a`  
		Last Modified: Wed, 16 Oct 2024 01:07:37 GMT  
		Size: 585.6 MB (585632177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b14238faa625d7777e9bff471bcefde1e58938085005ddab026ab2ddc8b6d`  
		Last Modified: Wed, 16 Oct 2024 01:06:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013f7d889ea6ddd3e81ee17b06ef00e086b5184ca20a951e2be005b66ee663d9`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49592155f8ad68ac3353dae4f34310ac1a5ecd89bf00292588e8f8cfbe856975`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3116ffaf5958283ea6802017ee637c1a401a136fca83b56a181436ed395d95`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3443a0240c8bbe3ecb1731a12727cd6c8d4f69244e9ab032e7837700726678fe`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40c2c4a5f84e8e3299bba0c8142bf84898cd1a4c529250e1b6b57438a88aaeb`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.2.6`

```console
$ docker pull couchbase@sha256:1dac0baa8d3aa50c8805d470251e7e7439b788dc65352a89b081946e8206ab91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:4b58e0f8320f4bcaa514e02825a9f8b5e9b0db273b3aede57566531df5be959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650159192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483933a28486d97ddc44bbaa28bdf7ea70d9a3e4b677f7db49bd7c65ca6db17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bce8dc623fb4f3b3e2f2cc90f532dac81793aacbfd9a8bc34c7f272703f7a04`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 6.2 MB (6203640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19b7a1a5cddb1dd4cc46227271aebc5b7e04e4a597533097f72215b6de729a9`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 864.1 KB (864102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254b5ffe8533432799b56c6292c531117f209ee875676174e3188c2cd6b67c76`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e6bd39cd5ff83a20414e99f19041663a8313b4e0b5b69f78776e581d85181`  
		Last Modified: Tue, 12 Nov 2024 00:58:21 GMT  
		Size: 615.6 MB (615575393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d278f5fbb4ee15892c99cac6533847d979ee97e0e2b63098ca5edd4b181b0df`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d0cc313a835e05978d3a22e3dde75ae46d8d17a0e7db6fcdf13ed201b50cf`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159862f14c611065e1095187d03c984757591a20abe4438321678feb502d9abe`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8028c515492bf94343b675e5ffdf634023b92257b9ce84725ae8c515f7db4283`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e6789d74bcbcf727c3b7a0b84ec13e12667d062fba4be39233407cc8ae5477`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ece909dec61e564cba6a304fe5fb8d33cb6caee4a492b8a6f3007f86f3044`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:07b7ddfcbbc6654d535c6f8e3aa740fc5686593c93e326761d5ca322ef7e456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6d9fe49c4d25b47cb627b75fba8083241e331d3cb80a914c8c43703509d432`

```dockerfile
```

-	Layers:
	-	`sha256:34e1cbdcc69402662d39f078751cc241871754e7f67167f99131512e449d1730`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 35.8 KB (35805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:7d6e356fbf2f30d7ae3b911cf30a838def123ad5cdc478f4c28ffc70e29b7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.1 MB (625088287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5969a5713480f17d7527249193f24bb3bc7ac4993aaab6b130a8b41df733d931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c396dd29f50bcc388cd0a519fac3f34e943a627c9613af69542b47bc466da9`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 6.0 MB (6041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d496ab92773d4bdd2c16f3738ba1c83e773a36e0751d0d35726afa7c5a8e82f`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 711.5 KB (711539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c75c5ebbbf48135024eccbbe96b521716a04200202d2875050b09064894d0`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319800ef44742b499fcfbc93d09de12fea172ea219d05d004f91261026c1c30`  
		Last Modified: Tue, 12 Nov 2024 01:21:19 GMT  
		Size: 592.4 MB (592356189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4482d826458e6222a04fe76268240d36790979884f96d96bb5b497326d52182`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4274ccec6ea478230d9bcca8679cdf9aa16736185b4f153f0a55f9c0eb9d8681`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925dc1477caa9acc381dcf8926803bf1a1cdf324feebd4f41c09da0839e0645`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4336c388f739dae1fd4292ccdf7c2ff11aadc5007eae6d45c269546dc0aba440`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365adc0efea529df15fec109eb02b13100a35d2ce7f790c19926d9dcebcb9b88`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f473ad2dfa83535574df9224f6c6e39650fac01ba4b6f717dfeb0cf4dbfb5f1`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:d6a3d2e1a5b12207764e6ba8007e41e07ca6c779a070cfd4927bc79370c17581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c65b08c9d54fe98556a645b20872297f9b7901d89dac7dad2fc39816b1d9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3800b8a1e257590c56d807e081dc422f2914c16ec2c2f9193abd124d3ef823d`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 36.0 KB (35990 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.0`

```console
$ docker pull couchbase@sha256:2725d8a339831cecaf28f124bd52b5bc8c323b184e1f47f4ef474c489a83c068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:3e7eb016088f1a7b3fc28f014cfed0c7a49248fc4df1d64853d95b3a4ebb8c90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726110733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc41528b1bb6a83d70e8c361a27276e926cd9886b5c961aec69183db1bb1fcaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:47:13 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 06 Mar 2024 05:47:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 06 Mar 2024 05:47:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 19:53:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Mon, 25 Mar 2024 19:54:15 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Mon, 25 Mar 2024 19:54:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 19:54:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 19:54:15 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 19:54:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 19:54:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 25 Mar 2024 19:55:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 19:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 25 Mar 2024 19:55:28 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 25 Mar 2024 19:55:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Mon, 25 Mar 2024 19:55:29 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 25 Mar 2024 19:55:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 25 Mar 2024 19:55:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 25 Mar 2024 19:55:30 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Mon, 25 Mar 2024 19:55:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:55:30 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 19:55:30 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Mon, 25 Mar 2024 19:55:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c70b701cc06e2eb6819cce35006c4488c4b5a0d155a9907f97b364b735c9098`  
		Last Modified: Mon, 25 Mar 2024 19:56:58 GMT  
		Size: 6.2 MB (6186179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70ffc4db4d8f1e8937df0d6247cb7bf8ba89311ba720503180a95df5a30247d`  
		Last Modified: Mon, 25 Mar 2024 19:56:57 GMT  
		Size: 1.1 MB (1092117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee74925a0aa53f2d73d2c7fc78af3699f5651b3ca9b135328e03a0b7577c43ec`  
		Last Modified: Mon, 25 Mar 2024 19:56:57 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c4c1c484fc891727c034f8b70547c5e102d96a8e9cd13db032d64c4634ca72`  
		Last Modified: Mon, 25 Mar 2024 19:58:00 GMT  
		Size: 690.2 MB (690243366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369dc8e57ef9e2847ed34d7d3ee11cd3d0a00276bc9938672f32d7afb847e8c6`  
		Last Modified: Mon, 25 Mar 2024 19:56:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851a17038a0d8e533365e5b0c9e79226d09554b437bbffdf78257ced2a79fe5d`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b5b586db13e1fa4863a831ff0fbdd0fc317f569e4afd2604b430b4943c5200`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f17e26a77d2b5883a2e5b33b7afc581f8964a019e6a9376acf78aa2ee43e91b`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf97f95dfae3eee59e488fd9e998a534c8a2b44bd885abe3fedfc9fcda4029a4`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7265d35ae73387cce84e60c7a510283337094849bb5fdc29cf028b890a6df136`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:3000e1f9550ce49e8a6c1456ac0293937040b1daaea08edd7f33ed9176f3b299
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699275743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ac23c76f00b8455293f0a75f1509e3b356118a0d0676a861203149a2a364ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:53:20 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 06 Mar 2024 03:53:20 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 06 Mar 2024 03:53:20 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 20:09:44 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Mon, 25 Mar 2024 20:10:37 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Mon, 25 Mar 2024 20:10:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 20:10:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 20:10:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 20:10:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 20:10:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 25 Mar 2024 20:11:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 20:11:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 25 Mar 2024 20:11:54 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 25 Mar 2024 20:11:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Mon, 25 Mar 2024 20:11:54 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 25 Mar 2024 20:11:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 25 Mar 2024 20:11:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 25 Mar 2024 20:11:55 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Mon, 25 Mar 2024 20:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:11:55 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 20:11:56 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Mon, 25 Mar 2024 20:11:56 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a70596a0a7145916afe9432e93cb09ff5afcb23b36d2e34b6ae25193d2b9ba`  
		Last Modified: Mon, 25 Mar 2024 20:13:26 GMT  
		Size: 6.0 MB (6027552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fd1b0caa23b4cff84ef14dd8c48fb56d2da767b34c863298692c154ab1491b`  
		Last Modified: Mon, 25 Mar 2024 20:13:25 GMT  
		Size: 937.9 KB (937892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693ceb773c091ecfd338ecd6a6b79478c857d06f64a6ec17b9ea49e1d38b6c6d`  
		Last Modified: Mon, 25 Mar 2024 20:13:24 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3e601f979953f24e1506ac87152e038abcb9cbeb0dcde753ed118cfcadbd24`  
		Last Modified: Mon, 25 Mar 2024 20:14:10 GMT  
		Size: 665.1 MB (665101253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c5b66cf8d66e5bcbd3b0df24be085b898261b8f24885de27db8a30638a9c2a`  
		Last Modified: Mon, 25 Mar 2024 20:13:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c757f4a852e02ada3140a9b176e07176090aebcf58e90b290e73e587d4f30813`  
		Last Modified: Mon, 25 Mar 2024 20:13:23 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cbd7bbb21b3cf07ea9ce9c584d8b81b4c2444125654d925b2f11ba57596293`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271cc0ba7958e06e2093df6eb127abf059d11f021c8a7c1000d6a889fb59e95`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bb590d20c882bb9af049fa740a4b7abc4803a3b74998c74e8545660c5220f1`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af65230ed87acd09c4aff658c30d964a4425be9c0c32cca852947de5cd1b141`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.6.1`

```console
$ docker pull couchbase@sha256:fd94ce4abaaccaa55d9d45ed1dd18bcbe1b30ca2bf72a1bb7c9f8d3008b7aeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:337482c7db431e6b0bbf13e4dc584bb9928274dfa25ee632425e03f653f4e9e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726129645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58c10fdcacdbe999cd31c8759e946000814c67ff84ba2cc1607ea6de22c4dc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:15:47 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 05:15:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 05:15:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:16:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 05:16:47 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 05 Jun 2024 05:16:48 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 05 Jun 2024 05:16:48 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Wed, 05 Jun 2024 05:16:48 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 05 Jun 2024 05:16:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 05 Jun 2024 05:16:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 05 Jun 2024 05:18:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:18:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 05 Jun 2024 05:18:18 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 05 Jun 2024 05:18:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 05 Jun 2024 05:18:18 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 05 Jun 2024 05:18:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 05 Jun 2024 05:18:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 05 Jun 2024 05:18:20 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 05 Jun 2024 05:18:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Jun 2024 05:18:20 GMT
CMD ["couchbase-server"]
# Wed, 05 Jun 2024 05:18:20 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 05 Jun 2024 05:18:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2034c2147aa55eac433cfa8e83637c42989b33107ea886069ff5b5d5bee96e59`  
		Last Modified: Wed, 05 Jun 2024 05:27:56 GMT  
		Size: 6.2 MB (6186275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fad3b9e423454fa6e83992e4bbe4c11eaf6c1ae328dca66778e3f76a9ec96a`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 1.1 MB (1092231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9a5d6a077730b14f7c41ecb61f99276201c4c689a2baf803fb12894796dea6`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a09216a074eec63c6df1993ccb5c47953902be8a97fd75bfc59fa8e13bfbabc`  
		Last Modified: Wed, 05 Jun 2024 05:28:58 GMT  
		Size: 690.3 MB (690262214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a40c2f022aa56d900d4bc4fd4a1ca0c62d493b5dced90011ac4d96e322a0a9`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4646d6b8dfa5bd18b9f17d46ecef0bceb8ad3b40a1d94128f7aca1a43fddf235`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fd883698752db7f3b1c10957ecde555282507023af3a6f712bb63d7b3ff041`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead79c6ba554441124b1fe3780c322a8f07a3e706ce44323b1db3e56644b775a`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2763561b33b75afc5ebcf03fc296efe76c59df84d299cd5616f3cb1b36be5cc`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43b51fcbc7a8324004e7cf52e5784f6f8d8b49a4e913b8046ff525a8dc4ff48`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:65eafe602fc11638ccf500d3d984bb166a2b8835da7982f82f384c6ec20d2a36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699309271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee32de1bac9dde7d88abb9936a34068ed6a1c47644a9483379fae04da3f41dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:29 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 04:37:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 04:37:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:37:51 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 04:38:14 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 05 Jun 2024 04:38:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 05 Jun 2024 04:38:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Wed, 05 Jun 2024 04:38:15 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 05 Jun 2024 04:38:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 05 Jun 2024 04:38:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 05 Jun 2024 04:39:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:39:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 05 Jun 2024 04:39:30 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 05 Jun 2024 04:39:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 05 Jun 2024 04:39:30 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 05 Jun 2024 04:39:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 05 Jun 2024 04:39:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 05 Jun 2024 04:39:31 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 05 Jun 2024 04:39:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Jun 2024 04:39:32 GMT
CMD ["couchbase-server"]
# Wed, 05 Jun 2024 04:39:32 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 05 Jun 2024 04:39:32 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd764ccf72f3934668b26d77c587c626d519a4000fe05b91cd9adbd69046e17`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 6.0 MB (6027453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f702385cdd214a6fef4dc6d55284657de902d0d9d1de050dfad15bc6f91c5`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 937.8 KB (937842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3314c1071254b28a0a521e3fa90ec43b146ed5ae7d66debe2901c91cad958ea7`  
		Last Modified: Wed, 05 Jun 2024 04:45:01 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48284f6c8a0c7f8c517fe535f95e38595fd80d0145d6a0845f05932bb1b959fd`  
		Last Modified: Wed, 05 Jun 2024 04:45:47 GMT  
		Size: 665.1 MB (665134032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4beecff366ba038a147495b319d5ac261dd810f34be094949254a0380ee8665`  
		Last Modified: Wed, 05 Jun 2024 04:45:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2251face004d78d2c656061b24045054e380b5f25a8cfcb176fd7e769193b`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1832473980e8699d416b37a01176cf2ac88e702e12c59a68f38301734ea5a8`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27df547176ae8dee54df2b0c34f33df77e77b0666c4c5aaa6fcff65952ba6c0`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26ea295d184fce055cd028b0466ec5507b48b2370e6c3cd9b522c5b6199cd98`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d13cf202de00b888fd4a0c3b2efbb326bd9a957e10354cde05171ca878bff62`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.6.2`

```console
$ docker pull couchbase@sha256:cc9e0ecdbef303d65f0a6d9baa6afa52eb687dbc6b3b512f1950a2a6a324fa55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:1c9b750e63714c46b6b7f348eaee231aaf029e5eaee68b30589bf333dad0410e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.4 MB (735358640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b206bc7556eeb26682217bb56b71146f685efd7580c68336196ef1b6d5491`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:15:47 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 05:15:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 05:15:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:16:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 05:16:47 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Sat, 20 Jul 2024 01:19:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Sat, 20 Jul 2024 01:19:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Sat, 20 Jul 2024 01:19:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 20 Jul 2024 01:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 20 Jul 2024 01:19:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 20 Jul 2024 01:21:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 20 Jul 2024 01:21:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 20 Jul 2024 01:21:07 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Sat, 20 Jul 2024 01:21:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Sat, 20 Jul 2024 01:21:07 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 20 Jul 2024 01:21:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 20 Jul 2024 01:21:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 20 Jul 2024 01:21:09 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Sat, 20 Jul 2024 01:21:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 20 Jul 2024 01:21:09 GMT
CMD ["couchbase-server"]
# Sat, 20 Jul 2024 01:21:09 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 20 Jul 2024 01:21:09 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2034c2147aa55eac433cfa8e83637c42989b33107ea886069ff5b5d5bee96e59`  
		Last Modified: Wed, 05 Jun 2024 05:27:56 GMT  
		Size: 6.2 MB (6186275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fad3b9e423454fa6e83992e4bbe4c11eaf6c1ae328dca66778e3f76a9ec96a`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 1.1 MB (1092231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cab928b74c7c94295c373baf7e0f4a062dd7bdd13e23bfc52b8a1cb283d363`  
		Last Modified: Sat, 20 Jul 2024 01:23:03 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a11b8f14d478376110dc1bc23628bff92308435d082183388f48b81adcd54e`  
		Last Modified: Sat, 20 Jul 2024 01:24:07 GMT  
		Size: 699.5 MB (699490903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e90f1615b4a2d03bf03b2cad1e6bc587e747ff49bae9edbcf7420f76b739625`  
		Last Modified: Sat, 20 Jul 2024 01:23:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac67f396ab12439cf7c494ab03b8a184e94689f41300b00241cfca0eeac9607`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ed228e2b9049986c163409cfd08f01cefc598d6a7c232b1d009f44d7649bc1`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293eb32a691d34e751a005ecef52eb064deed8308a9fe8a8edcc2d445766cb13`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3327d1197126a1bcc2ee7df413bac8d3b01b10731932e553505bcbb4f7ed25df`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d634d5aa8dba461c3661c5d1e2057356a761556dfe52ef0e17dfb59517a66a`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:bee661151f53113263132ea13ea17d3c5f839b5e0805cdc511e482e7c4fdf290
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707786526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a44dec6ca8568d26a6e7a004c1615b7e4c393d79993610dfe7e7cfcaf595f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:29 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 04:37:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 04:37:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:37:51 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 04:38:14 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Sat, 20 Jul 2024 01:50:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Sat, 20 Jul 2024 01:50:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Sat, 20 Jul 2024 01:50:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 20 Jul 2024 01:50:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 20 Jul 2024 01:50:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 20 Jul 2024 01:51:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 20 Jul 2024 01:52:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 20 Jul 2024 01:52:03 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Sat, 20 Jul 2024 01:52:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Sat, 20 Jul 2024 01:52:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 20 Jul 2024 01:52:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 20 Jul 2024 01:52:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 20 Jul 2024 01:52:04 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Sat, 20 Jul 2024 01:52:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 20 Jul 2024 01:52:05 GMT
CMD ["couchbase-server"]
# Sat, 20 Jul 2024 01:52:05 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 20 Jul 2024 01:52:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd764ccf72f3934668b26d77c587c626d519a4000fe05b91cd9adbd69046e17`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 6.0 MB (6027453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f702385cdd214a6fef4dc6d55284657de902d0d9d1de050dfad15bc6f91c5`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 937.8 KB (937842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a01210cf437bd96d8ddb4ae98ed12e2598e6661482b39e98b288ef23b0f646`  
		Last Modified: Sat, 20 Jul 2024 01:53:29 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43b1d78f25447a10511981612d08371f853a8d92b1dd7d85f2a28cc45f76545`  
		Last Modified: Sat, 20 Jul 2024 01:54:16 GMT  
		Size: 673.6 MB (673610965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69f5cd08cd5e013914d939b40d4f7914b9ba0f315bf47d06188df3eb9f0ad8e`  
		Last Modified: Sat, 20 Jul 2024 01:53:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b0e46255bdd75f55954f8c73cc606a39fadc550c56a8ec0d114320d078182b`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 821.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367087c5664dbde36d013211e42341b868aae61e64f5d574fe88885daf2f09c6`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f89a0c293002313d3d9d0c4fb3e7cc2c363cc8ca3b1d802652f9b4a9aaf7a7`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfadc3bf51c177d39f86456f65656f00dba5469dbf1c655e5c55b256fef46456`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18b30d001d3cbbbd7cd8d21d2cb8c637e452c7cd136b12968539382c34a86a3`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.6.3`

```console
$ docker pull couchbase@sha256:dff8011f5ed177b35ca5f916a51d97c1c7c0c53aa2013988d83f1e52171ac934
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:15d79ad96890fbfb17a36dd0e36575763251246c94becd76fe056ba96c7325e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.9 MB (768925234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3a46a56717114c7d9a9e75ba5538403252161f66fe571bae33d58c09c49fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181cf9a43df8c5e399e6d27dc51b550cb7eef1030eb4a23e9f2f1afc4fad47f7`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 39.3 MB (39276283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a57105c51c8a53b98e917c2a49922367ac246740ec2c4e5cb12c63f7618cbf`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 926.1 KB (926064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289ce120bf8531c16bb73d516193c2f95d5195d73ffb2bc4161ac2a689e7b85`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d3be05b1124e4858d82f0dbf1835540b90859cd9a894e529eae5a96ced26b6`  
		Last Modified: Tue, 12 Nov 2024 00:57:33 GMT  
		Size: 699.2 MB (699182015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20c0f01b24c1dd797d45570d12038d45ea57c1ffa8455ed3b675d7cbe161415`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cb7effd6ff13e9221825c975693a2f7eaeb5eb2f265f68bfd029cd2bdf5597`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d50fafe6355c5d292618c4baa5ae1347782aa58b113f23cf81498296d6a063`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcccada2863443a2551bf883c46696463ef77ea948fd074b08889a9aca0fd53`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786b1974142cdacd50c61e47beb3bb57acbaa3a705b0ed5d6ff920a6dcc3c546`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6a45fae918ae9c11f313b88bf4891ad8aa6f31fbe5a86006ef9240c17ca2b4`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:75d8f31d7368d637a7e098f38e21b5b272747d82b4935da1fac0749e4079419d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b568b81538ac5613e925c3341db97a3e720df08305bb0dee448cfeddedd53278`

```dockerfile
```

-	Layers:
	-	`sha256:680d4d9b916a40a0d91194e0fb7dbefd7e698c3ed2567bd465065af663466647`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:e946c69bd434360dff17a1ae8c0aab63a7f317a29cf2f27127791e9a4eecfb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.3 MB (740282679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3851b9155496fe9af8cbc67ff23e4caffbd71871440a790f482c22ba9dc111a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9837b35b89321c86b62c4addb2275efc6de452946a2230ae527a93ebaf64cbe6`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 38.9 MB (38853543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fd330817e32cf64f5305421981635c23024aced95a96800b8b6ce2fb23e74`  
		Last Modified: Tue, 12 Nov 2024 01:14:05 GMT  
		Size: 770.5 KB (770459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d108e111e1445face871399f66a53e0b609b5ff77408a902bba19fac2c77d02`  
		Last Modified: Tue, 12 Nov 2024 01:14:04 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de71da94bf9d6e25f0e91a9daf9bcf94b199bac819f65b6a29e61f77169cb6`  
		Last Modified: Tue, 12 Nov 2024 01:14:18 GMT  
		Size: 673.3 MB (673295157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d99b296f051c9dc747c85dd25c8159a417848e04e40d834b284f8df97c87ee`  
		Last Modified: Tue, 12 Nov 2024 01:14:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59d212c610c18199191dbe112705bc49d5e2e984b6fb9d07b247fc49c3ce0e3`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfb7bdaffda0c2da7179426e577d7b60142ebb643e96480fd11a5f01f4d7d36`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec9e5848ef97d3adba7c6d08916d14fa24da401e5b27cedac89051fc43c3b3`  
		Last Modified: Tue, 12 Nov 2024 01:14:07 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdb3085b85319798414ae6966fdd5ae53da24afd01358f25793b83d7b452e08`  
		Last Modified: Tue, 12 Nov 2024 01:14:07 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61fd3b1b4b3694f62f5143556d788d1c795cdbac69b5109a7bdb516dd57f20`  
		Last Modified: Tue, 12 Nov 2024 01:14:08 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:1f527e11d9d65304110978d5ef93ff51e65d7817c1cf1acb3db44025bbb39e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b35e309505303c360e78d5104f12aa63359e7bc911244e4ffa3d7de76652a`

```dockerfile
```

-	Layers:
	-	`sha256:c326186959e6a2fff0a42329d862b28666f28c789c125277ea53350eb9dc99f2`  
		Last Modified: Tue, 12 Nov 2024 01:14:04 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.4`

```console
$ docker pull couchbase@sha256:1712f7ea984a17e98422d23cad535a24251fc59726720a535786ea4386dfae77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:bb46e6473d51c1301c9e223d3b2a0f8bf9fda28282c59e1db26db3730d6cab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771640031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ce6132cdb3fa96f599f385750800b1b5373663d2fee48a3c63a8d979f66cc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e4c8297c01db11c191858fd6cf8a7511d64a9118a1c1c750d681e3841e7f3`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 39.3 MB (39298708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce06b3288eb688faca7cdc69d231f81faaa16e369004bfaef06068b9687c27a`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 926.1 KB (926065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ee6a894c26a477744c2bc2b3101e65176887db8b0aeb5cf047c5884101d455`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7451ade6546d4e3b9d7953419d27c746ce6b0e9f23a891197a416e9a34cf29`  
		Last Modified: Wed, 11 Dec 2024 20:31:24 GMT  
		Size: 701.9 MB (701874383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac90a5eb80de27a57eeff0fead5cf60c6a688e1e8ab5d0510560b51277ea74a`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e05105422fbe68ce9e63c322db62cb0c03c6d6ce8d543b5923087760b80230`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b19bb06f3c79a6921855e7577dfa4a8a2ee0dbfef49e3ef3d13eb64eb62ac6`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b714361da7137396fe322b09fc0e45fedcb305b31525630b48039fbf83e968c`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785dba9ba6eea486f48865f659aa8f43797dd9892579171a4220ee34e9c387d3`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02364dd300798b3a2cdffb4fd4c9996710276b95ddd51cd92bf0bdb976c03`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:e875371520bedaa2baffb1beeea80adefa9df8a91ab6f12b0f01cc032977ad47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d8101bc5a78ebb73c600b37b58d257e800de5275e2f26524dff7688415b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:5951a1e0fc56cf41e206b54e13f281427ce397d604402be27b44f6c0664377aa`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:51890184c7f5923841b5d2667eaac8968a0bb450d93b8e377e98f09867f21012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742534627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37c525e8fa9c00cf8205958c87d66908faf2e0ddb4182a09a3a6dddce05f1a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0584481da729d18de66076f7754e37c2bbc39cbf05bd725b8aa1ebf12e1429a`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 38.8 MB (38844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9437b11152e6789daaee1b8b2816829ecec5fe6f7b7e66d2b57cf0a8fb340f5`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 770.4 KB (770448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b80241375276135ce691e34844832bbc260efe1e17f69b3f6c0c63a909cf8`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3461cd28120e1f6e3a2a5d1632a4c0b55c34c9f983e76358764a1c2ef23dd3`  
		Last Modified: Wed, 11 Dec 2024 20:35:36 GMT  
		Size: 675.6 MB (675556548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9a2303e4b89e2749df948d7b77b504b000b4b505078adcfb37a62dcd836a2`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacce055b74872fa011424cec1d27c67e1a1e63bd686fd81dc6f607572c5a6bf`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a8748af089af62557555c76fee8ee17283476c34a1a2719fce6c853545f9a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fd38386fb9ec7054edc75e6910d24e7f2828b2898eba07f0ab18f31df677a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae18f583723b3303d32822f4967c9220fefebebdca459e5cbccd3efd1a0b5a6f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c5cb759bf8528349b284da7a8f8e541fdda4bec66b63b16482c7eca1d329f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:38911045564e44eee162d11ab29804f5a2411172e6c55fc0959d3046d87c3e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d54da9ce17575a870692837ab8c7c5ee9b37c2595580d3efb48953b68c80e`

```dockerfile
```

-	Layers:
	-	`sha256:f05cbd60b6824e37fba0b063111378fdd30aa399b050e17cc9fbeb37de5ea28d`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:7.6.5`

```console
$ docker pull couchbase@sha256:2c1ec01cdf6cb2142bd8219ae191a7b039e7353d51868e9bf6807d3ec629750d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:7.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:63f655af7ae0c05f2203a89c3fc69a2949d9520ecc0c2c7f3a5eac67fe3b42cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771497798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ff576beaa9240c61d927b9f6b849effcdabc46db8e282dba8242ca9518196c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d270795631b0971893631768750b0de304a12febfacf7fe0f5a4026c2bcee`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 39.3 MB (39295602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823613d607305acd8ae1edbe587b8c02e78f5ccadbde27cceb19e9ca344727ea`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 926.5 KB (926524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094dda71641f1d4026536ee278a8e30040c669f8fe866519481429eaf49bd7c2`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16402788a89907ea531377d4ef06e2abce136164be8157a9ea4e5f85d75088a6`  
		Last Modified: Tue, 04 Feb 2025 04:40:49 GMT  
		Size: 701.7 MB (701734548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b036622c75a24cfcdf9837c93c85234d5a7abe5628cc827b9cd6227cb751153`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a6250533cf535ddd828f6c6b9098c419c49b7aaa8a8d20619c0a0a8fd2cf4`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ce9448d874ff987bdfd7c3eb61b0a3fd48a7d9dfc73a4ecb99a46c8fda6b3`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a64793937a5d8f5271e6c9668665f540a585508cd26f87995abc41c780b75f6`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2efc41046c96b788cd55290db4fbdca5f07e793a1c512c07551de0c4c054171`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133bd02127032cb69c9e3d1edc362a235641ced952a6514fc2064d45de5923eb`  
		Last Modified: Tue, 04 Feb 2025 04:40:41 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:1c58771043610f9f7b53d2114524e952b057ff7e333e968f157547738b7d886d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f10f1cba8a84ccf9a7fc46cdb25a026072283227dde939d3074c2a30c6a8d`

```dockerfile
```

-	Layers:
	-	`sha256:c9e7ab4d81fb834f5dc73ec294ac450a891102f0d8660cbc47a86c6b53eaffeb`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:7.6.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:01cd206baf811b7c051add20ba17fd65586880b7f4862f0a1dfb5b6a21d5c589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742447958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1965fc289bc7e8b1ccfd9c91807bc41920dc3a95fb840b6b459970c7f945e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdc8d5137de9b565226c43a7234b3a6c27a1db780f35bfb41835c032e3f0dac`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 38.8 MB (38848133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb760e4a8859fed7ea1ffc0434cb9d7221983c1e7efc0bbd8f5223856b23d88`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 770.6 KB (770599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b2abc5868f013566f52b890cdc23967bd9e3246ecc8f1b03a1df1d61cdf694`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f5541d9510754a013a5e7e9cc8f454cbe88f0cca06483cf149711cdaef9df`  
		Last Modified: Tue, 04 Feb 2025 09:11:36 GMT  
		Size: 675.5 MB (675465854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492712947a194f44ae4209e9b72d225e60a228f99e2084ca0d5d02e04de9c0b`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e9dedebddf045d0236ed469d0738d1235e288322c1bca4bf8eeff31e5f91e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826709d0a5dd4d6b8755a04ad9bbde9d326c46ab5182d72c6355ad570c65161`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8913eb3415b49bb55568876ad7d0116762d5da14c2fd273d230e8050e208f8`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e4197ded4c4f2c842e12f696ef2adf5c2cb5dad09acb59c9ddcc22fc5d9899`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583501de5e5975a56e3649e4bf4a9149362cd124cd76d1e410c99c1f336a23e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:c329bd890bdbe161653f6aace193fa1c12282fb7a55b5a91baac38f7e4486284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d614bfe2b9ebd8292abeba1a210ffd7d6ecf27eb571f7bc8d4803b675c1d5`

```dockerfile
```

-	Layers:
	-	`sha256:22fa9afc58162c8f930c3aaca635a2f04c41f5834052bbc2339f77df9789772a`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community`

```console
$ docker pull couchbase@sha256:f1adb86d7cbd80d8dbacd3f07fc0889e04dc066f482c074c699916257df8452a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:734d65f9237d4b450de5ae67135b4eaeac9b93fb732d523091821d9ca990c7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396856400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0728fa92614e27d1fff830a23e35aa4b80767586c029d7108aa0a9467f4529b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b733c0871caa9a475d215b92cbe37a613e1fcdbccb1b7bcc3afcae3a5f468a`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 6.2 MB (6203660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62305e070fed67cd0548459a868e5951da2c6de93092828d660433a17b16029`  
		Last Modified: Tue, 12 Nov 2024 00:56:46 GMT  
		Size: 864.1 KB (864119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21607cc5c773a16308ddb3a486d8f3323e7334271486a1a796f4995653967743`  
		Last Modified: Tue, 12 Nov 2024 00:56:45 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fddb1102a33b33a1703a410e4440b66334d248a5a0d1881f003b071c88854f`  
		Last Modified: Tue, 12 Nov 2024 00:56:59 GMT  
		Size: 362.3 MB (362272565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43b327ae54827ef79a854d0a745bd151ce3bcdf468be38c080542ecd06f9e0e`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746b2dd4b873da687238d40aae68b28b0be0378fa18f57b28c4e2d323b5ae335`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105130c90e1d7094a2b5da46bc7354108466818317ece4ad1b3f061e7f4d98e4`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f530646a8ed8e8a11335816a224f1c34c924412c2827d05cf0680ed20f6df772`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c81daafc67e7c37c3bfb30cb021ef86ea144942d2f49695f289245d3d56003`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce18c6e915edfcaa8eccbe37468315666964179ac85f90a9e1103a5369545b3`  
		Last Modified: Tue, 12 Nov 2024 00:56:49 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community` - unknown; unknown

```console
$ docker pull couchbase@sha256:306b63aef21099f06466ca02a915a2a140a989f4f0d35142bdbf51889b538348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec4fb915b799a8c6c78cb52d58c21e6cef7f08666cd2ab17479a19e63a08210`

```dockerfile
```

-	Layers:
	-	`sha256:2ec97e150fe65dd5e37aae67664b9a278c0a3f27f53ca4d4d430ebc3c55f6aca`  
		Last Modified: Tue, 12 Nov 2024 00:56:45 GMT  
		Size: 35.8 KB (35802 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:58b172719e2896d56371c0979b68d1a939bee50519877c374e334841b3cf36ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374267184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad90b83dc7735a300f107f9fa8dc1db852f0286d864bc835fd2f46f8f0fbd2e0`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2d226b8a2a5bed7e39fdd186b0130b1e137e9c1e042bebfd75a673998138b6`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 6.0 MB (6041697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39acfedf2947d1ad202b22f7276f9292046ade1b3bf08392056597fb098b4415`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 711.5 KB (711511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba88b570ce0d0123eb3ccdb4b164753247a71923e6815f043d834e220033c51b`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07042fae3f2858dcdd21687a650931f8a79d20eb8103bd8dc990443220c333e`  
		Last Modified: Tue, 12 Nov 2024 01:18:31 GMT  
		Size: 341.5 MB (341535132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f38b13293c7d7844aeb9cfcf70a63d5eaca157977303e09697bf020b7cacfe9`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07a6d2c9db9ce42ca8d4e4b31c35d7e5826f362d895f6167ebd7049c6ca2aa`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc516eae03b66fcc21e81d3d956f7a7886fd0bfe3b3d1b5cc6dfd7dc584987c`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897ed6965fec2096defec1cd8db1ce5070bebe67e8fbda48d0d4e705ccc052b2`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7086d6272eff2099f81d5daea3de53060873ab4e43d02d5754ac0bba56512bf4`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535d59683aff16aebf534a487ac4324548dd435638c4ddc7e63d4764ab571a83`  
		Last Modified: Tue, 12 Nov 2024 01:18:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community` - unknown; unknown

```console
$ docker pull couchbase@sha256:ca6a7c009639b29a6e72fccae3f2a6f7084dae7d09ad263d10c8bd5d66c9f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f2bf5ae98b097b085ec5d5701d85cf57d63ace6314c139bd04c073e1d70c43`

```dockerfile
```

-	Layers:
	-	`sha256:22722e4310d9de112ec3a5fbc00a7349c38061faab4b2422942248924a9977bb`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 36.0 KB (35987 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.2.0`

```console
$ docker pull couchbase@sha256:580ef32893ec74eb070d59f0e267bf9069ffadaaccd175a09a650f275e3e8f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:d581a356ec8e5a4edd58086fcfff60c3bcbf57f629dc3cb3e92ccc17537ebf80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.1 MB (357144300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f69d43f1cb82c428ca8a164618cb9e0dd9dc0c3eb67d8a7047b5fe4488a8090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:54:54 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Aug 2023 02:54:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Aug 2023 02:54:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 02:55:09 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Aug 2023 02:55:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 03 Aug 2023 02:56:33 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 03 Aug 2023 02:56:33 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 03 Aug 2023 02:56:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Aug 2023 02:56:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Aug 2023 02:57:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 02:57:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Aug 2023 02:57:17 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Aug 2023 02:57:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Aug 2023 02:57:18 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Aug 2023 02:57:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Aug 2023 02:57:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Aug 2023 02:57:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Aug 2023 02:57:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Aug 2023 02:57:19 GMT
CMD ["couchbase-server"]
# Thu, 03 Aug 2023 02:57:19 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 03 Aug 2023 02:57:19 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35618df5c9a71269b91577e6aea59155f8edb63501d542ce129979a4d9e328b`  
		Last Modified: Thu, 03 Aug 2023 03:03:49 GMT  
		Size: 6.3 MB (6285930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e41c93bd38e3d7fdf86eadfe0151f9734ceff7e79a5a6145bcd35f946ae28`  
		Last Modified: Thu, 03 Aug 2023 03:05:01 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5632644e8d86888dbc0c089ef9a799b763decf6608e7dcbe3bed9799557579ac`  
		Last Modified: Thu, 03 Aug 2023 03:05:37 GMT  
		Size: 322.3 MB (322273343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4602f313633c16d97e25528f307259b5e8f021aed28d78fadc1fdb06be7a7057`  
		Last Modified: Thu, 03 Aug 2023 03:05:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1717e0b83c6b95798f94427c6e9bf582eaaa8162d027849f4675e20b7dd666e1`  
		Last Modified: Thu, 03 Aug 2023 03:04:59 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651857319e9313aaa090d5a37fa79092c6c6d6461a31ba2d732eb3a23946681b`  
		Last Modified: Thu, 03 Aug 2023 03:04:59 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56226190e7500bbbcd87a52b1b4e832f0f16ddcd23445515d1ec9fe0ad2d3452`  
		Last Modified: Thu, 03 Aug 2023 03:04:59 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df454e98a14bbc6d686c397cd8f0a91f0027d67e7823342e372c81d08fc1560f`  
		Last Modified: Thu, 03 Aug 2023 03:04:59 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e9de64bb6b795340dccecdff38f79aa00f6e42552836bb675503ed427b3272`  
		Last Modified: Thu, 03 Aug 2023 03:04:59 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:768fb3231cda398b6037ef94711baf3cbf63e042e255460a324d2f3cfa512316
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335640659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d238841d3f4a0cc6037724bbfff2ccbaf4ff8eaa0b51c09b60fd362b71936077`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:13:43 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Aug 2023 01:13:43 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Aug 2023 01:13:43 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 01:14:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Aug 2023 01:14:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 03 Aug 2023 01:15:21 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb
# Thu, 03 Aug 2023 01:15:21 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 03 Aug 2023 01:15:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Aug 2023 01:15:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Aug 2023 01:15:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=0877ec5c4109992fc2186ecf6153d7f30a24be7f6559133c855ecff77b9b2363            ;;          'amd64')            CB_SHA256=6c07122d9e28c0679c012cba73c28df76a74424cf206fedf42c7e18fa640b6b1            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 01:16:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Aug 2023 01:16:02 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Aug 2023 01:16:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Aug 2023 01:16:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:16:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Aug 2023 01:16:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Aug 2023 01:16:04 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Aug 2023 01:16:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Aug 2023 01:16:04 GMT
CMD ["couchbase-server"]
# Thu, 03 Aug 2023 01:16:04 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 03 Aug 2023 01:16:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad91e7dfaee3352f726a7133ee4af8e38e1f989f4a537f0618abd00bb4c784e`  
		Last Modified: Thu, 03 Aug 2023 01:18:32 GMT  
		Size: 6.1 MB (6110566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefecead7df3f5aa37a70d9e442ce43ad22c79b54655c79940ea2f69d65bb966`  
		Last Modified: Thu, 03 Aug 2023 01:19:30 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc1584daf4c996a64d74df8ed87fcc8e727950c3418a5986323ef83ad48bf1c`  
		Last Modified: Thu, 03 Aug 2023 01:19:58 GMT  
		Size: 302.3 MB (302325147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc35ac731662e27039bf03d8847fec34e4e2b4f3c62194c0611961fa00780413`  
		Last Modified: Thu, 03 Aug 2023 01:19:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e908fc65253bcbf3d19eb2d9ebf53b2a914b27175b4e37ee8e22c78c75d77990`  
		Last Modified: Thu, 03 Aug 2023 01:19:28 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111e60bd32f1d333e21bab75e6996d2da9892b0d2ab926fd5d3c09ec4a8f2eb1`  
		Last Modified: Thu, 03 Aug 2023 01:19:28 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179c85844312c438aa86f9adbfed86fdf551537dae841c3d6f111d881cf2d03c`  
		Last Modified: Thu, 03 Aug 2023 01:19:28 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552fc9f0b9bb5b50a7e0458e44a9c9f31b57468a1ac1fb634923a74964cc1fb`  
		Last Modified: Thu, 03 Aug 2023 01:19:29 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93fa8bb145c1ea2655271e27a35fbe2897a1db63a9f0ae20e169c93682689cf`  
		Last Modified: Thu, 03 Aug 2023 01:19:28 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.2.2`

```console
$ docker pull couchbase@sha256:595e16d459c3cbd3c1ce3cb485ef153e280ad21dd849a9dfd282a3c8d4208539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:62f151dadf2fd6337e92793113a0e35cb20aba626d1a3eb362fa7d2915ef133c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361639829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb146e4290888fe5f9fbbe09acf4533435e461e2540c433a8e62ba41e067864`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:25:59 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 10:26:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 10:26:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:26:18 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 10:27:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Sat, 16 Dec 2023 10:27:53 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 10:27:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 10:27:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 10:27:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 10:28:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:28:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 10:28:32 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 10:28:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 10:28:33 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 10:28:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 10:28:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 10:28:34 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 10:28:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 10:28:34 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 10:28:34 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 10:28:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78735bf4de6f426e7422bf3d534899d82db0f0d2d66034d6db341ce8d26f0b2`  
		Last Modified: Sat, 16 Dec 2023 10:35:19 GMT  
		Size: 6.3 MB (6286008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c3a9d3cb6c526925edd4e69fa9d0990cb8cecddf132fcf4f86f9536a56db67`  
		Last Modified: Sat, 16 Dec 2023 10:36:28 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef661a7a9296aac37cd7bf10d5a50280d8ee10c386944e4599279a5db3b0354`  
		Last Modified: Sat, 16 Dec 2023 10:37:04 GMT  
		Size: 326.8 MB (326765439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53d388f93f0ad0ea8c540b7ed3761f85e7917e2406ab4ef76f7253b9e755230`  
		Last Modified: Sat, 16 Dec 2023 10:36:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bb942f563d81c6d8b5f0476d611d0a79c83b3fb438dca2973f744ce7fca4f6`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0faf6729f915640d095fab3205ee40f6fd399158209063aba0ac8cf2546db8f`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd2f79c6cafef10a2535b7521673f3d89c42ee1d0a13134621f916775ad8d3d`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a42de1c1afb3a842f4ae40b286db8faa306721a1de89c7b755451e90e0df411`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aabf49d9c8c2cc3e7859716d2c0e97d4cad160b60232995aab7c94aff88e1ac`  
		Last Modified: Sat, 16 Dec 2023 10:36:26 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:0e71cd9041434b67a8ed669b2ba28e7e22cd516c9fadef397e9aa662e83b265e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338249089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a16d4915eeab0c1d4bb08cfd5a32d421146915aae8ffa984a7977a96a9301f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:54:01 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 09:54:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 09:54:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:54:19 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 09:55:39 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Sat, 16 Dec 2023 09:55:39 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 09:55:39 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 09:55:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 09:55:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 09:56:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=15e8e8185882210ea02ad83e3667714cce16293afad29506adf07131d684f2db            ;;          'amd64')            CB_SHA256=71bd7359e07810726c3f2735e71aa2a41e6da0865407d407bd666a3d123fa5dc            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 09:56:20 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 09:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 09:56:20 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 09:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 09:56:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 09:56:21 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 09:56:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 09:56:21 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 09:56:21 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 09:56:21 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a83d6afdb30f174382ab5039378b0bae25520129e600a54c8d3a1ee404eeae`  
		Last Modified: Sat, 16 Dec 2023 09:58:48 GMT  
		Size: 6.1 MB (6109493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9cfa47d30bfa7e8ca05f5797557a777657738f99ee228681baa7829b81743d`  
		Last Modified: Sat, 16 Dec 2023 09:59:43 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560066726de56cdbf85086fa375e8aaa3490ad7ec7b2d726168e914f159e9f0d`  
		Last Modified: Sat, 16 Dec 2023 10:00:10 GMT  
		Size: 304.9 MB (304932093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9868a5a67ca556a81eca3a8b8a376b854253e6990f23e0a1bd4f723bb3215f`  
		Last Modified: Sat, 16 Dec 2023 09:59:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2edb90f91027b3900421acd294554fa85c09bc64743aa6bd7060540ab6fe16`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2528581d204a073bc6362932f258b934d85fddd27aecd90eff2639b09ff29429`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1f3846ba9dc058b43529d7eda2a6aec9e2b0e8d3ab840b432a8b2e6aa11b57`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b305cff2a968879e35a48bd10b29792fe4c5629da0039c610ad86d19fce9b36`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f339cd1b5b19f55445503e45222e6ee3317c30590b15ab5560d90e34b81a63bd`  
		Last Modified: Sat, 16 Dec 2023 09:59:41 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:d11bf54e681306bb46c892aa587a2d7005eb4f0865d2f50ecf4d1f1269935a07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:25c1a39c2c8ccaf5c62795f6dd12aaece6917c525b947df0bb7e9194b9a6646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364888406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d643c72b83d8e2584ca061927edb83473099ec79136161b1ad70b62314822b32`
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
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
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
	-	`sha256:1249f821f7cc033833e49bccee2b7e3ab0ce3e339b0f8a6d8b572ad7b14bb9a7`  
		Last Modified: Tue, 12 Nov 2024 00:57:19 GMT  
		Size: 6.3 MB (6299169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73a9107d36a345fcb6cfae794e4f7b9b725a40316513d0c069df3904e1076f6`  
		Last Modified: Tue, 12 Nov 2024 00:57:18 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ce8de9a95b31a3a4ccdf80d3c544a6f82cca983645911a87d8f093385cde9`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 331.1 MB (331073871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552b6419f103c9228fc0d828d34336fe1f6dd4b7fdd88b69279b876ded02822e`  
		Last Modified: Tue, 12 Nov 2024 00:57:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9430f310a775f4143ef2c28f618b6135eebdc3e5a41478ab1ff73577291a02ef`  
		Last Modified: Tue, 12 Nov 2024 00:57:19 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45825920c7cc2223a1ccf5209c5b14eb7093f11436a929d818f1f6fbc7e566c`  
		Last Modified: Tue, 12 Nov 2024 00:57:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913574a0bf2ab74f73adc3b1a2b812c78a2cb37a7666ad18441c8359e19590fc`  
		Last Modified: Tue, 12 Nov 2024 00:57:20 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c2e751e345d362ad129af7c338f7fc75acc0a3e67ec3a955dd2a4dcd2366f`  
		Last Modified: Tue, 12 Nov 2024 00:57:21 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137158146c83890791c53f554fa1c73f9de0bde771c5fbc3f2867bff9a9550f9`  
		Last Modified: Tue, 12 Nov 2024 00:57:21 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:31f7220e99398dbd08300a471e4dbcba1f52909eef49529f43ab0fce530ca06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f2844420556df11febba9e496df8f473c36d07e513c08b5a3651d0dc3a806c`

```dockerfile
```

-	Layers:
	-	`sha256:213753f0bbe49850ddeff4494ec08e34a9d7f0fc31cb26b310c0deaa1ecb3820`  
		Last Modified: Tue, 12 Nov 2024 00:57:18 GMT  
		Size: 31.5 KB (31500 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:0601e812e45f7c556dabb6ba9a246d00c6f1f220a33a05bba08f1f1ead5af6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344968826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45191f1f54e7e792276513dc3abbe9bcfef9673cd557b38d6cc160a0f2d34c43`
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
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Mon, 18 Mar 2024 15:52:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 18 Mar 2024 15:52:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Mon, 18 Mar 2024 15:52:02 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
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
	-	`sha256:a0a87bfd0a7181920474e87c7920879cc89e906ca81559bad045f9294c33d7d0`  
		Last Modified: Tue, 12 Nov 2024 01:22:56 GMT  
		Size: 6.1 MB (6128843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b1a14c7dd6c90b90d1abaf9287cfd7d2b79bad7e250fdec20e18521b55cccd`  
		Last Modified: Tue, 12 Nov 2024 01:22:55 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64baeab963456e940d34f69de18e2781940319ee2dafdd23ff36de78a23a22`  
		Last Modified: Tue, 12 Nov 2024 01:23:03 GMT  
		Size: 312.9 MB (312861847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b10af300674dbd4168b82a862df679d8dbb579c01f6cc075ad4aa28551c19cd`  
		Last Modified: Tue, 12 Nov 2024 01:22:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186d2adce589e4cf8ac6c070aa6ee61e5eb541419746737ac3cd48fc799eb36`  
		Last Modified: Tue, 12 Nov 2024 01:22:56 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20636096e3990aab6dacf5e9273bcaccb11db9586ab25dfea2654f3b136f644e`  
		Last Modified: Tue, 12 Nov 2024 01:22:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e9d6d9e2e7c426ba012bfd436979f3e6e671ba39bda68dd9f6afddc014679`  
		Last Modified: Tue, 12 Nov 2024 01:22:57 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876f5593ec9b92ce6ae6002908a906a71c2838037b13a91c4b9b783fc7b47f34`  
		Last Modified: Tue, 12 Nov 2024 01:22:57 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41887c42971b90c60bd0e3b23b4110464c025f2962d76ec7b892b0cc8312ce`  
		Last Modified: Tue, 12 Nov 2024 01:22:57 GMT  
		Size: 869.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.2.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:2f148f15afc46d18e37f6e34c00346b4a026f65aa4de9a9dfc5beefa7d50c884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 KB (31658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbd53f0b4cc44d7189d302fd986468a42e942990d798485674874fff6950c95`

```dockerfile
```

-	Layers:
	-	`sha256:a4215aaf563e48f52f620526422120bffa2d27f162e61b24631fa1b67351473b`  
		Last Modified: Tue, 12 Nov 2024 01:22:55 GMT  
		Size: 31.7 KB (31658 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:community-7.6.0`

```console
$ docker pull couchbase@sha256:832d250e1cd75acd01f5e43c18ba6c15b5174fc0a30a7907c78e082448e72e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:e0c129ffe83caf88b65856924df986d1d7020e1d6069f88d99e721686683b04c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385907515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb7dc467d604bb03472d808d0cc5f5df9f600d0b373b01aed2e9a07b6dc6766`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:47:13 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 06 Mar 2024 05:47:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 06 Mar 2024 05:47:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 19:53:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Mon, 25 Mar 2024 19:54:15 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Mon, 25 Mar 2024 19:54:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 19:55:38 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 19:55:38 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 19:55:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 19:55:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 25 Mar 2024 19:56:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 19:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 25 Mar 2024 19:56:20 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 25 Mar 2024 19:56:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Mon, 25 Mar 2024 19:56:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 25 Mar 2024 19:56:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 25 Mar 2024 19:56:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 25 Mar 2024 19:56:22 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Mon, 25 Mar 2024 19:56:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:56:22 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 19:56:22 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Mon, 25 Mar 2024 19:56:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c70b701cc06e2eb6819cce35006c4488c4b5a0d155a9907f97b364b735c9098`  
		Last Modified: Mon, 25 Mar 2024 19:56:58 GMT  
		Size: 6.2 MB (6186179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70ffc4db4d8f1e8937df0d6247cb7bf8ba89311ba720503180a95df5a30247d`  
		Last Modified: Mon, 25 Mar 2024 19:56:57 GMT  
		Size: 1.1 MB (1092117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc0df43d6e4177fb7c57981fdd82e188c3f9a14cd4f3b24b0fa74ecf0bae334`  
		Last Modified: Mon, 25 Mar 2024 19:58:18 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876e375c7009d56f1178d7f5dea8108549a1f030aa591abd732e2b1005c4e81e`  
		Last Modified: Mon, 25 Mar 2024 19:58:58 GMT  
		Size: 350.0 MB (350040146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f979870401be09f76688aed95fdc4d461af1da4c77498b6e24d38e2e1ca26ec`  
		Last Modified: Mon, 25 Mar 2024 19:58:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e345b4a3f68a3d55d398ade31b1f664812916931de12f11f4899646b68a07fb`  
		Last Modified: Mon, 25 Mar 2024 19:58:16 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e2bfea730443c545b7326c38213af51a981d7eac0280669bfa252471e2269`  
		Last Modified: Mon, 25 Mar 2024 19:58:16 GMT  
		Size: 728.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf54e9ea8cc5a792a1b09d602afe3def10300a74c9489e56bc624235044b7432`  
		Last Modified: Mon, 25 Mar 2024 19:58:16 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3072a8ec22232c6618c16e1677c280b0b38a3e6b8924f9dea0b75514e474c357`  
		Last Modified: Mon, 25 Mar 2024 19:58:16 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42812bbaa172d4dc231689ff70a65eb17c34ee6b84041c30d5be3aa8085c3484`  
		Last Modified: Mon, 25 Mar 2024 19:58:16 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9b1f40438e4e4294eb17b374df592e00b91fe2dc88153e3a5d2b0e48ddd61d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367742948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200878411ffd29b0eaa92135fb098108b92d1dd6eb3f53ae6cfa413fdc13e8b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:53:20 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 06 Mar 2024 03:53:20 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 06 Mar 2024 03:53:20 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 20:09:44 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Mon, 25 Mar 2024 20:10:37 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Mon, 25 Mar 2024 20:10:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 20:12:06 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 20:12:07 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 20:12:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 20:12:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 25 Mar 2024 20:12:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=9fee2723a019157fa6b696d5bfc011440ae96347430087f67c67a73afc1a2518            ;;          'amd64')            CB_SHA256=b6b86779b16bc5c83e86220f40c8e230cf9650f0a7deb7e190997a93d9a50316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 20:12:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 25 Mar 2024 20:12:52 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 25 Mar 2024 20:12:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Mon, 25 Mar 2024 20:12:52 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 25 Mar 2024 20:12:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 25 Mar 2024 20:12:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 25 Mar 2024 20:12:53 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Mon, 25 Mar 2024 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:12:53 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 20:12:53 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Mon, 25 Mar 2024 20:12:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a70596a0a7145916afe9432e93cb09ff5afcb23b36d2e34b6ae25193d2b9ba`  
		Last Modified: Mon, 25 Mar 2024 20:13:26 GMT  
		Size: 6.0 MB (6027552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fd1b0caa23b4cff84ef14dd8c48fb56d2da767b34c863298692c154ab1491b`  
		Last Modified: Mon, 25 Mar 2024 20:13:25 GMT  
		Size: 937.9 KB (937892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97733cbaef74a8ca102460bcedb2b338bcab748eb1459b5d96ea959b8a02ef86`  
		Last Modified: Mon, 25 Mar 2024 20:14:31 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0ef3cc13677d772de2fd9e78a88ba7d8253bb1ec59709fa892d2f783c67959`  
		Last Modified: Mon, 25 Mar 2024 20:15:07 GMT  
		Size: 333.6 MB (333568452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5907ce06f39671a160eacf865a228ee6933b79dc21f17450361f3c8b0f222970`  
		Last Modified: Mon, 25 Mar 2024 20:14:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d380908297a1216e3810e750663db0f431bf98786abdab7a7b7ad92ea9ee5b28`  
		Last Modified: Mon, 25 Mar 2024 20:14:29 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b400bcc09cfc9efdeb3cd65a4f91ebf5ed1b7b9b5f0310a0be898ece21a8791b`  
		Last Modified: Mon, 25 Mar 2024 20:14:29 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d625160c44ae39a233aff7b0439bb25ce675eee4a90961e571c40e0ecf20b1`  
		Last Modified: Mon, 25 Mar 2024 20:14:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847f136b1ba18ba1680cd4fdc51908b4c982abd4a8766e9b26aefa31cc493750`  
		Last Modified: Mon, 25 Mar 2024 20:14:29 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f761b3d2c980f05e9950faa9fca623494ba591202137c585206db85c4895e610`  
		Last Modified: Mon, 25 Mar 2024 20:14:29 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.6.1`

```console
$ docker pull couchbase@sha256:5bf1add5ba0fdbec7a4203e7a874be67e38bf1c8db809e6f717e7167a4f01539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:7684cfd8e7c6aa8a516969af03e4d1ffa6931cb85b16ff4a89623088837d2657
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385922840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471d17d5315021b1bd6cd8040fdc565b6b5be15f2faa17848c571436eec140a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:15:47 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 05:15:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 05:15:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:16:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 05:16:47 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 05 Jun 2024 05:16:48 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 05 Jun 2024 05:18:26 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Wed, 05 Jun 2024 05:18:26 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 05 Jun 2024 05:18:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 05 Jun 2024 05:18:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 05 Jun 2024 05:19:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:19:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 05 Jun 2024 05:19:16 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 05 Jun 2024 05:19:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 05 Jun 2024 05:19:17 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 05 Jun 2024 05:19:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 05 Jun 2024 05:19:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 05 Jun 2024 05:19:18 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 05 Jun 2024 05:19:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Jun 2024 05:19:19 GMT
CMD ["couchbase-server"]
# Wed, 05 Jun 2024 05:19:19 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 05 Jun 2024 05:19:19 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2034c2147aa55eac433cfa8e83637c42989b33107ea886069ff5b5d5bee96e59`  
		Last Modified: Wed, 05 Jun 2024 05:27:56 GMT  
		Size: 6.2 MB (6186275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fad3b9e423454fa6e83992e4bbe4c11eaf6c1ae328dca66778e3f76a9ec96a`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 1.1 MB (1092231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490b97b0876ce979dcd457e0c551460f89a4556cbe3fa406c2937d3a69350d55`  
		Last Modified: Wed, 05 Jun 2024 05:29:13 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c387e64f9e1f7cdecf41c4ac99615334b909fca4cd6eaf7556b1e4e3430e84f8`  
		Last Modified: Wed, 05 Jun 2024 05:29:55 GMT  
		Size: 350.1 MB (350055409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38786f2881acb91bac12cc96f1f7c1d7eb35551ed7e5a2baeba209439e4ae703`  
		Last Modified: Wed, 05 Jun 2024 05:29:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80808e5e50be027bf98e0d0068abdd390ea9d6569a8eb202ad14a56a511bb347`  
		Last Modified: Wed, 05 Jun 2024 05:29:11 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5782fa3da1ba255b9602b1e0139dac1f8308d88771ea518475ca44b7ae41fa5`  
		Last Modified: Wed, 05 Jun 2024 05:29:12 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29281af3a156b69a21fa155e44f6c50f6750e338310186296e4c2154ff2a2852`  
		Last Modified: Wed, 05 Jun 2024 05:29:12 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dc97dba9e3e547e68a711e9fc3bad05bb44bfae8a588f16ecb4ac90e2e0309`  
		Last Modified: Wed, 05 Jun 2024 05:29:12 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33396e3e3579a4fbd04b2c5822f26ecaa7305c65f162e1e2502449539c6d3f7`  
		Last Modified: Wed, 05 Jun 2024 05:29:11 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:2be3c5ba73e82a4b1739ca406bd053eec943493368a62a0995d9bba98a1db7cf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367767340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dfbc211dd2edce6764465a16728bab406aa9334c84826c140c11cbd43913c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:29 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 04:37:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 04:37:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:37:51 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 04:38:14 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 05 Jun 2024 04:38:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 05 Jun 2024 04:39:37 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Wed, 05 Jun 2024 04:39:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 05 Jun 2024 04:39:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 05 Jun 2024 04:39:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 05 Jun 2024 04:40:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:40:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 05 Jun 2024 04:40:20 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 05 Jun 2024 04:40:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 05 Jun 2024 04:40:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 05 Jun 2024 04:40:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 05 Jun 2024 04:40:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 05 Jun 2024 04:40:22 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 05 Jun 2024 04:40:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Jun 2024 04:40:22 GMT
CMD ["couchbase-server"]
# Wed, 05 Jun 2024 04:40:22 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 05 Jun 2024 04:40:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd764ccf72f3934668b26d77c587c626d519a4000fe05b91cd9adbd69046e17`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 6.0 MB (6027453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f702385cdd214a6fef4dc6d55284657de902d0d9d1de050dfad15bc6f91c5`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 937.8 KB (937842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec852e05ea831d02413b93c7081bcb8279c8e70f14070d30aa61576e05631ca`  
		Last Modified: Wed, 05 Jun 2024 04:46:03 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fd32ac0634ad5c87f6865eb7a6f8a74df8acad2c6e60829b789cb613539bd`  
		Last Modified: Wed, 05 Jun 2024 04:46:31 GMT  
		Size: 333.6 MB (333592107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edf1ad5ed8ff634b215ce4d3ac9c3e51d0d834c53a7af9a84ae908c69e26188`  
		Last Modified: Wed, 05 Jun 2024 04:46:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cd3808a7ffdf654bacb9142e367521850e6e394b936940dec92d3c0598bff`  
		Last Modified: Wed, 05 Jun 2024 04:46:01 GMT  
		Size: 661.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d1080b0a5f39f76f19c5eb502795e0cbe0b6b760e9d891caa72e729e99ecc3`  
		Last Modified: Wed, 05 Jun 2024 04:46:01 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9c7b62f1829e2b90e6cbd7580f28ae7dd6923189675b45e33e33bcfc1a1f17`  
		Last Modified: Wed, 05 Jun 2024 04:46:01 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d72e25efc655dc3effad25b37740c81745869389a8c816e73b4fe5f06f900b`  
		Last Modified: Wed, 05 Jun 2024 04:46:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcd152a4ec228b7465f4a8956b5022ba3147b614b94d16a53afbe3de8378bd`  
		Last Modified: Wed, 05 Jun 2024 04:46:01 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.6.2`

```console
$ docker pull couchbase@sha256:f1adb86d7cbd80d8dbacd3f07fc0889e04dc066f482c074c699916257df8452a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:community-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:734d65f9237d4b450de5ae67135b4eaeac9b93fb732d523091821d9ca990c7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396856400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0728fa92614e27d1fff830a23e35aa4b80767586c029d7108aa0a9467f4529b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b733c0871caa9a475d215b92cbe37a613e1fcdbccb1b7bcc3afcae3a5f468a`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 6.2 MB (6203660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62305e070fed67cd0548459a868e5951da2c6de93092828d660433a17b16029`  
		Last Modified: Tue, 12 Nov 2024 00:56:46 GMT  
		Size: 864.1 KB (864119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21607cc5c773a16308ddb3a486d8f3323e7334271486a1a796f4995653967743`  
		Last Modified: Tue, 12 Nov 2024 00:56:45 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fddb1102a33b33a1703a410e4440b66334d248a5a0d1881f003b071c88854f`  
		Last Modified: Tue, 12 Nov 2024 00:56:59 GMT  
		Size: 362.3 MB (362272565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43b327ae54827ef79a854d0a745bd151ce3bcdf468be38c080542ecd06f9e0e`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746b2dd4b873da687238d40aae68b28b0be0378fa18f57b28c4e2d323b5ae335`  
		Last Modified: Tue, 12 Nov 2024 00:56:47 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105130c90e1d7094a2b5da46bc7354108466818317ece4ad1b3f061e7f4d98e4`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f530646a8ed8e8a11335816a224f1c34c924412c2827d05cf0680ed20f6df772`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c81daafc67e7c37c3bfb30cb021ef86ea144942d2f49695f289245d3d56003`  
		Last Modified: Tue, 12 Nov 2024 00:56:48 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce18c6e915edfcaa8eccbe37468315666964179ac85f90a9e1103a5369545b3`  
		Last Modified: Tue, 12 Nov 2024 00:56:49 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:306b63aef21099f06466ca02a915a2a140a989f4f0d35142bdbf51889b538348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec4fb915b799a8c6c78cb52d58c21e6cef7f08666cd2ab17479a19e63a08210`

```dockerfile
```

-	Layers:
	-	`sha256:2ec97e150fe65dd5e37aae67664b9a278c0a3f27f53ca4d4d430ebc3c55f6aca`  
		Last Modified: Tue, 12 Nov 2024 00:56:45 GMT  
		Size: 35.8 KB (35802 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:community-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:58b172719e2896d56371c0979b68d1a939bee50519877c374e334841b3cf36ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374267184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad90b83dc7735a300f107f9fa8dc1db852f0286d864bc835fd2f46f8f0fbd2e0`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2d226b8a2a5bed7e39fdd186b0130b1e137e9c1e042bebfd75a673998138b6`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 6.0 MB (6041697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39acfedf2947d1ad202b22f7276f9292046ade1b3bf08392056597fb098b4415`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 711.5 KB (711511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba88b570ce0d0123eb3ccdb4b164753247a71923e6815f043d834e220033c51b`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07042fae3f2858dcdd21687a650931f8a79d20eb8103bd8dc990443220c333e`  
		Last Modified: Tue, 12 Nov 2024 01:18:31 GMT  
		Size: 341.5 MB (341535132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f38b13293c7d7844aeb9cfcf70a63d5eaca157977303e09697bf020b7cacfe9`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07a6d2c9db9ce42ca8d4e4b31c35d7e5826f362d895f6167ebd7049c6ca2aa`  
		Last Modified: Tue, 12 Nov 2024 01:18:25 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc516eae03b66fcc21e81d3d956f7a7886fd0bfe3b3d1b5cc6dfd7dc584987c`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897ed6965fec2096defec1cd8db1ce5070bebe67e8fbda48d0d4e705ccc052b2`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7086d6272eff2099f81d5daea3de53060873ab4e43d02d5754ac0bba56512bf4`  
		Last Modified: Tue, 12 Nov 2024 01:18:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535d59683aff16aebf534a487ac4324548dd435638c4ddc7e63d4764ab571a83`  
		Last Modified: Tue, 12 Nov 2024 01:18:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:community-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:ca6a7c009639b29a6e72fccae3f2a6f7084dae7d09ad263d10c8bd5d66c9f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f2bf5ae98b097b085ec5d5701d85cf57d63ace6314c139bd04c073e1d70c43`

```dockerfile
```

-	Layers:
	-	`sha256:22722e4310d9de112ec3a5fbc00a7349c38061faab4b2422942248924a9977bb`  
		Last Modified: Tue, 12 Nov 2024 01:18:24 GMT  
		Size: 36.0 KB (35987 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:2c1ec01cdf6cb2142bd8219ae191a7b039e7353d51868e9bf6807d3ec629750d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:63f655af7ae0c05f2203a89c3fc69a2949d9520ecc0c2c7f3a5eac67fe3b42cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771497798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ff576beaa9240c61d927b9f6b849effcdabc46db8e282dba8242ca9518196c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d270795631b0971893631768750b0de304a12febfacf7fe0f5a4026c2bcee`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 39.3 MB (39295602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823613d607305acd8ae1edbe587b8c02e78f5ccadbde27cceb19e9ca344727ea`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 926.5 KB (926524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094dda71641f1d4026536ee278a8e30040c669f8fe866519481429eaf49bd7c2`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16402788a89907ea531377d4ef06e2abce136164be8157a9ea4e5f85d75088a6`  
		Last Modified: Tue, 04 Feb 2025 04:40:49 GMT  
		Size: 701.7 MB (701734548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b036622c75a24cfcdf9837c93c85234d5a7abe5628cc827b9cd6227cb751153`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a6250533cf535ddd828f6c6b9098c419c49b7aaa8a8d20619c0a0a8fd2cf4`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ce9448d874ff987bdfd7c3eb61b0a3fd48a7d9dfc73a4ecb99a46c8fda6b3`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a64793937a5d8f5271e6c9668665f540a585508cd26f87995abc41c780b75f6`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2efc41046c96b788cd55290db4fbdca5f07e793a1c512c07551de0c4c054171`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133bd02127032cb69c9e3d1edc362a235641ced952a6514fc2064d45de5923eb`  
		Last Modified: Tue, 04 Feb 2025 04:40:41 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:1c58771043610f9f7b53d2114524e952b057ff7e333e968f157547738b7d886d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f10f1cba8a84ccf9a7fc46cdb25a026072283227dde939d3074c2a30c6a8d`

```dockerfile
```

-	Layers:
	-	`sha256:c9e7ab4d81fb834f5dc73ec294ac450a891102f0d8660cbc47a86c6b53eaffeb`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:01cd206baf811b7c051add20ba17fd65586880b7f4862f0a1dfb5b6a21d5c589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742447958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1965fc289bc7e8b1ccfd9c91807bc41920dc3a95fb840b6b459970c7f945e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdc8d5137de9b565226c43a7234b3a6c27a1db780f35bfb41835c032e3f0dac`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 38.8 MB (38848133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb760e4a8859fed7ea1ffc0434cb9d7221983c1e7efc0bbd8f5223856b23d88`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 770.6 KB (770599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b2abc5868f013566f52b890cdc23967bd9e3246ecc8f1b03a1df1d61cdf694`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f5541d9510754a013a5e7e9cc8f454cbe88f0cca06483cf149711cdaef9df`  
		Last Modified: Tue, 04 Feb 2025 09:11:36 GMT  
		Size: 675.5 MB (675465854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492712947a194f44ae4209e9b72d225e60a228f99e2084ca0d5d02e04de9c0b`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e9dedebddf045d0236ed469d0738d1235e288322c1bca4bf8eeff31e5f91e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826709d0a5dd4d6b8755a04ad9bbde9d326c46ab5182d72c6355ad570c65161`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8913eb3415b49bb55568876ad7d0116762d5da14c2fd273d230e8050e208f8`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e4197ded4c4f2c842e12f696ef2adf5c2cb5dad09acb59c9ddcc22fc5d9899`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583501de5e5975a56e3649e4bf4a9149362cd124cd76d1e410c99c1f336a23e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise` - unknown; unknown

```console
$ docker pull couchbase@sha256:c329bd890bdbe161653f6aace193fa1c12282fb7a55b5a91baac38f7e4486284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d614bfe2b9ebd8292abeba1a210ffd7d6ecf27eb571f7bc8d4803b675c1d5`

```dockerfile
```

-	Layers:
	-	`sha256:22fa9afc58162c8f930c3aaca635a2f04c41f5834052bbc2339f77df9789772a`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.2.0`

```console
$ docker pull couchbase@sha256:76114e559a863fde21c7b327ac82c3b5e265599e259ea8731f3c739c42e65464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.2.0` - linux; amd64

```console
$ docker pull couchbase@sha256:772a2c8fcc3e4a65e410053e5b4f1a4c5349da0ccb78de4d458cf91e49719263
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.7 MB (663685101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232147af3c363497c044401c3a221e39f18ad490a26bf4efc84e5e972db019c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:54:54 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Aug 2023 02:54:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Aug 2023 02:54:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 02:55:09 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Aug 2023 02:55:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 03 Aug 2023 02:55:10 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 03 Aug 2023 02:55:10 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 03 Aug 2023 02:55:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Aug 2023 02:55:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Aug 2023 02:56:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 02:56:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Aug 2023 02:56:26 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Aug 2023 02:56:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Aug 2023 02:56:26 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Aug 2023 02:56:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Aug 2023 02:56:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Aug 2023 02:56:27 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Aug 2023 02:56:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Aug 2023 02:56:28 GMT
CMD ["couchbase-server"]
# Thu, 03 Aug 2023 02:56:28 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 03 Aug 2023 02:56:28 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35618df5c9a71269b91577e6aea59155f8edb63501d542ce129979a4d9e328b`  
		Last Modified: Thu, 03 Aug 2023 03:03:49 GMT  
		Size: 6.3 MB (6285930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76951ffea2eb9305de925d27044022b82719478ca00eb5b6aa7c90bef872ed3a`  
		Last Modified: Thu, 03 Aug 2023 03:03:47 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91aeb93d2aa72ad20c4cf699740572ef7fd37fa590584cbbb57e54731b7b6cad`  
		Last Modified: Thu, 03 Aug 2023 03:04:45 GMT  
		Size: 628.8 MB (628814146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d05cef67ec666d42e81e534724fed4d45134c72ee363e7a29f01a2ce99df6f`  
		Last Modified: Thu, 03 Aug 2023 03:03:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f693b82a631465ff6992c15eb0c719a8520cd5aea5e5b792f56780e5198372`  
		Last Modified: Thu, 03 Aug 2023 03:03:46 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9f16769ccd60bfc6c37bac170d94eaea8450f86e7037af4bbdd76ffd32dd9c`  
		Last Modified: Thu, 03 Aug 2023 03:03:45 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610602c4cf5517d76cf7f4d8e9441310dbd2ba991dc2a93f94bb0c791e5ba0b3`  
		Last Modified: Thu, 03 Aug 2023 03:03:45 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18677c045c6414523bb2312b313c88a51526e6a391a04e30d03d247b089d724`  
		Last Modified: Thu, 03 Aug 2023 03:03:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0adce102afa0b1f44d32dfba2af0957cf3eee275bade93e91635ab108fe7a9`  
		Last Modified: Thu, 03 Aug 2023 03:03:46 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.2.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:191e40485c3d7a0404733af87322a7b02149d074bf1adc03eb8949e17aa62ebd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 MB (636755632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0b7899f3ccdee4d8441e1232f6633f1a2d9b4ae1c6c28580194d087884f836`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:13:43 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 03 Aug 2023 01:13:43 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 03 Aug 2023 01:13:43 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 01:14:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 03 Aug 2023 01:14:02 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0
# Thu, 03 Aug 2023 01:14:02 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb
# Thu, 03 Aug 2023 01:14:02 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 03 Aug 2023 01:14:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 03 Aug 2023 01:14:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 03 Aug 2023 01:15:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=b44a4d8e577613ad027dbac9830e6123deb7bda22facefe687d6b6e98c86ac66            ;;          'amd64')            CB_SHA256=2fd31b46a6df5ed9c85d3a6cadfb0214e3f928c14ff0b03e6a24652700128328            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 03 Aug 2023 01:15:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 03 Aug 2023 01:15:13 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 03 Aug 2023 01:15:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 03 Aug 2023 01:15:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 03 Aug 2023 01:15:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 03 Aug 2023 01:15:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 03 Aug 2023 01:15:15 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 03 Aug 2023 01:15:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Aug 2023 01:15:15 GMT
CMD ["couchbase-server"]
# Thu, 03 Aug 2023 01:15:15 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 03 Aug 2023 01:15:15 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad91e7dfaee3352f726a7133ee4af8e38e1f989f4a537f0618abd00bb4c784e`  
		Last Modified: Thu, 03 Aug 2023 01:18:32 GMT  
		Size: 6.1 MB (6110566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d117fae1bda3d1ce14ae0cf3990cf2156ac7e81f990b54bc4ae483f50d6a6e`  
		Last Modified: Thu, 03 Aug 2023 01:18:31 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96d8d44e8dd52499dbe81834a7c9b340f54094d3b65d3b4c324924c8a48d350`  
		Last Modified: Thu, 03 Aug 2023 01:19:14 GMT  
		Size: 603.4 MB (603440121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742a874d02c82e1540e5b6c7ff63495b2312be683041805df65174a1a9bd9b9b`  
		Last Modified: Thu, 03 Aug 2023 01:18:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ac7f9d2f4e2ad03a33ad57c9287d472fc372ac96ed3c4e908b2f0e2245e36`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4430dfb88cb992b7c4d808078a7d23f2ff4883b459d0b099adf44f58e3145cb0`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e93e4ab3785185d50863b20c222c5bb80dd625a42cd01491ff351314eb78f2`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59147a009b35da6ae2cd75b9fc14052375adb5467ab8c193ba79f63cfae342a6`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083a640e5a13d39b2c983bb586c2fcd1283a577da7c1c718d014d05e5a281a10`  
		Last Modified: Thu, 03 Aug 2023 01:18:29 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.2.2`

```console
$ docker pull couchbase@sha256:fdd84aed2ea79384a0223080651ca06ac2c9a137b149725a5c7d9bdbbb2f789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.2.2` - linux; amd64

```console
$ docker pull couchbase@sha256:16ea62e32f96fa27d0e1fc3ab84e0877f0fa19d0ea0baf494de98793de087e1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.9 MB (668875225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2894333b48a5b7ef3bd9fea7da57f98a57c056f7562411034712619b2378121`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 07:34:46 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 13 Oct 2023 07:34:46 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 13 Oct 2023 07:34:46 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 07:35:15 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 13 Oct 2023 07:35:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 13 Oct 2023 07:35:16 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Fri, 13 Oct 2023 07:35:16 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 13 Oct 2023 07:35:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 13 Oct 2023 07:35:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 13 Oct 2023 07:36:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 07:36:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 13 Oct 2023 07:36:46 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 13 Oct 2023 07:36:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 13 Oct 2023 07:36:46 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 13 Oct 2023 07:36:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 13 Oct 2023 07:36:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 13 Oct 2023 07:36:47 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 13 Oct 2023 07:36:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 07:36:48 GMT
CMD ["couchbase-server"]
# Fri, 13 Oct 2023 07:36:48 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 13 Oct 2023 07:36:48 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f74dd8ee7b698aa30f6021db1eba8fe81ac68ece2c5829894a3fcc95667e11`  
		Last Modified: Fri, 13 Oct 2023 07:45:16 GMT  
		Size: 6.3 MB (6285994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f719fafe0b994fb15b24cf6d3c25952e43fb9aea27536d12b441fff0590cfe`  
		Last Modified: Fri, 13 Oct 2023 07:45:15 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1b00b6ed63000d00ec4f85352eb288d152551dbfeaf88a9551ab3c5394829`  
		Last Modified: Fri, 13 Oct 2023 07:46:14 GMT  
		Size: 634.0 MB (634004190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97b4d65bdddc8424ef131ab99944ee044d73a4a75838eb33141954066697655`  
		Last Modified: Fri, 13 Oct 2023 07:45:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f621a143a41ed5304d93bf556dd005d9a5a37bee913adb6c51fa73a5ac847d1d`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 742.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6593905d712fac24f86d21544b6e259bfc0f04d60bce8a754a2d4a48b3c4e2fb`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e73873d14d11576c1686a77f0f248a99a7ad8da429f5b36a48a67d27ae21f6`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a445bbeb8054941d3516c04c3749ab81421520836941fff2a7399a985bb96fbd`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3ab2ca4efb0b01347210fb5176c132ba36a49db49a24fcb317837ef70b8f5`  
		Last Modified: Fri, 13 Oct 2023 07:45:13 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.2.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6b388f27b914f0f9f57b843c2675f084727dcfd42f4771653d4e92f25100cbf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 MB (640369682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a94a2ed1d241646d5e83ef4b6aab188551f2293767f606b3912ff7bc99816c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 03:56:50 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 13 Oct 2023 03:56:50 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 13 Oct 2023 03:56:50 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 03:57:08 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Fri, 13 Oct 2023 03:57:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2
# Fri, 13 Oct 2023 03:57:09 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb
# Fri, 13 Oct 2023 03:57:09 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 13 Oct 2023 03:57:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 13 Oct 2023 03:57:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 13 Oct 2023 03:58:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=73d9cb6389a878c83da2b697d8e3d5574f8249e689933139278dd27106d3edbf            ;;          'amd64')            CB_SHA256=992bd6628e0b415a5fb47152845cdba412e0d2081eb250ce8a6e32edd0ca3152            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Fri, 13 Oct 2023 03:58:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 13 Oct 2023 03:58:21 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 13 Oct 2023 03:58:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 13 Oct 2023 03:58:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 13 Oct 2023 03:58:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 13 Oct 2023 03:58:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Fri, 13 Oct 2023 03:58:22 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 13 Oct 2023 03:58:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Oct 2023 03:58:23 GMT
CMD ["couchbase-server"]
# Fri, 13 Oct 2023 03:58:23 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Fri, 13 Oct 2023 03:58:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e1c15a1b1f2e05138fe2b49be3e2f9ea9a9dcd2a096c2ee69d1636a18082ef`  
		Last Modified: Fri, 13 Oct 2023 04:01:39 GMT  
		Size: 6.1 MB (6109875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650354a58c417d4e2144895bce1598e3e897806b813a323182f8bb387e41615d`  
		Last Modified: Fri, 13 Oct 2023 04:01:39 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c375bb8cb7f5c39c87b4b30e1dc5a9b80ff1c0e7f607c7404b29655c522aa`  
		Last Modified: Fri, 13 Oct 2023 04:02:22 GMT  
		Size: 607.1 MB (607055943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf3a287bfa03cf1499527ebd79713fc030bb3f840e6312e5179bf53bc59c6b7`  
		Last Modified: Fri, 13 Oct 2023 04:01:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14c1cfa00c110bdc0b4e6f78bc70bb4ea6c7885140339b4a4ef4a30f3ec8090`  
		Last Modified: Fri, 13 Oct 2023 04:01:37 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c96446b8555fe77fd9136bd14317211f48d02ebe24313effe313e888069b16`  
		Last Modified: Fri, 13 Oct 2023 04:01:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd91b09193923acf20558fcedeeaa0f1ea5a19816b3f9aa659876e5e5fb3a731`  
		Last Modified: Fri, 13 Oct 2023 04:01:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26a88b5a9cfb6a0b6cb06b081ce695e444891ab3b656672021f981c386354de`  
		Last Modified: Fri, 13 Oct 2023 04:01:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6beda31d1c3b875888f514a497d0d74b03676af327382f13bbddf8a03dd0afef`  
		Last Modified: Fri, 13 Oct 2023 04:01:36 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.2.3`

```console
$ docker pull couchbase@sha256:daea166ce4cf8c1b2472d3cfbd0fa6675f33f23eec4ed1e9ee6f66d5ebe40610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.2.3` - linux; amd64

```console
$ docker pull couchbase@sha256:18415c4cbdb61fc0da3c58eead4d78525dff2ee655155109aa61cde2bdb92faf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.0 MB (670029391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbb0f5f6965e30ec7917749c4de1fab9b1e5e297d971c35bef9eeb725426a81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:25:59 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 10:26:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 10:26:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:26:18 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 10:26:18 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 10:26:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 10:26:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 10:27:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 10:27:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 10:27:40 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 10:27:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 10:27:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 10:27:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 10:27:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 10:27:42 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 10:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 10:27:42 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 10:27:42 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 10:27:42 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78735bf4de6f426e7422bf3d534899d82db0f0d2d66034d6db341ce8d26f0b2`  
		Last Modified: Sat, 16 Dec 2023 10:35:19 GMT  
		Size: 6.3 MB (6286008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de84f8aa811274c19311a984e5405ac2a61a5227477fe24ec3fbe305f97cf89`  
		Last Modified: Sat, 16 Dec 2023 10:35:17 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e041a4b9d588c08b72d8f7f657e4ce93467fcd9cc539126b43484ab1fe9e28`  
		Last Modified: Sat, 16 Dec 2023 10:36:12 GMT  
		Size: 635.2 MB (635154999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9164d43e9daf583b22402ce0651a77e6c21552b2521860a0d998cf102362612`  
		Last Modified: Sat, 16 Dec 2023 10:35:17 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2b90a6de88b7882e89a2584cb53f3c93dcca0c1eb69ad8f184163e59380e33`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ec37b4f6e10362278fd677e1e15d6f434617739b005fdbcccae021278f3701`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4513a22f09dd3d7fe1df2c2a9a17deb0aab7d12e935ebfa6df33c1c2fffa049b`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98488eff588073c8b3ca3cbdb24074de5ad27a496b39903482f0b4dacd8b898`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804c21d7cb8de5ef4419d5b801ab528eeb39863ae8cce22b694174a8f3185fdb`  
		Last Modified: Sat, 16 Dec 2023 10:35:15 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.2.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:9070a162a941ab9d43e2f8b0d361a4e7f5aec53ee89cfdf26c5860e1893e7370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.4 MB (641439491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c85bcaca8610743429a4a9374dadd7fc73deebb41fa34f63dad4d4c4d74b1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:54:01 GMT
LABEL maintainer=docker@couchbase.com
# Sat, 16 Dec 2023 09:54:01 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Sat, 16 Dec 2023 09:54:01 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:54:19 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Sat, 16 Dec 2023 09:54:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3
# Sat, 16 Dec 2023 09:54:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb
# Sat, 16 Dec 2023 09:54:20 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 16 Dec 2023 09:54:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 16 Dec 2023 09:54:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 16 Dec 2023 09:55:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1ca43fd4d5c7d390974ba5ae0465875b4c42687dd497ceadb2ef6816585e3ec7            ;;          'amd64')            CB_SHA256=941ad294cc93102b655290701e4f6f6c653c146dc525ade7c734047b3797e316            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 16 Dec 2023 09:55:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 16 Dec 2023 09:55:27 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Sat, 16 Dec 2023 09:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Sat, 16 Dec 2023 09:55:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 16 Dec 2023 09:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 16 Dec 2023 09:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.3-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.3 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 16 Dec 2023 09:55:29 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Sat, 16 Dec 2023 09:55:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Dec 2023 09:55:29 GMT
CMD ["couchbase-server"]
# Sat, 16 Dec 2023 09:55:29 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 16 Dec 2023 09:55:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a83d6afdb30f174382ab5039378b0bae25520129e600a54c8d3a1ee404eeae`  
		Last Modified: Sat, 16 Dec 2023 09:58:48 GMT  
		Size: 6.1 MB (6109493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a955fe360ffe527e18bb09ebf93804eed1ffda89965d306366b2a5ac16cf6d9a`  
		Last Modified: Sat, 16 Dec 2023 09:58:47 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911e51334194534bc793dd194873bc3795c3971d6a92ed68ac67b61a2d242f35`  
		Last Modified: Sat, 16 Dec 2023 09:59:28 GMT  
		Size: 608.1 MB (608122491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8a7f3860597d49bff454f019588b40bea00ae01a7969f22ecb8b92b6c3f361`  
		Last Modified: Sat, 16 Dec 2023 09:58:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1084ffb17cf83af9888747528711823416c81e65d2ef29a3d48f161727879ec6`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ca2c8f48efc6c50ae6e750a7a8540fa98baa2c39790395af00ffa6c21ac99c`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbd4a2f5d8034e2b86a45be911af0069430b9f298f1ed28722a6253273645ac`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5dfa9429a7aa09076fada3bf7151afedd3bba71e3b44d043918ac62ca95cdc0`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd10be5c4525a4962ee0d31225e6c568a680f6f9a75d03c13715f122c850b4ef`  
		Last Modified: Sat, 16 Dec 2023 09:58:45 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.2.4`

```console
$ docker pull couchbase@sha256:c2f921c253e8ff868e96b0afc535fb611473c3c7b3c0381d8d717b638a162de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:396086ccc8a180fb085b73d57cb26ff80f1768078e01ae3f0741731282eee134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.8 MB (640753927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2265daaa10bfb096cc2b697863cfd7d91dd051b1cd3e35be666e7514fa9609`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 04:39:56 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 04:39:56 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 04:39:56 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:43:43 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 04:43:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Tue, 16 Apr 2024 04:43:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 04:43:44 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 04:43:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 04:43:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 04:44:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 04:45:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 04:45:03 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 04:45:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 04:45:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 04:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 04:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 04:45:05 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 04:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 04:45:05 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 04:45:05 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 04:45:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2539cc6714d28ae08856da9a1375e679890fea343b120abb8b5ad0d44be436`  
		Last Modified: Tue, 16 Apr 2024 04:53:50 GMT  
		Size: 6.3 MB (6286645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f13bf02912f439e34bca8c94fcdad907768c193ca0d2d336e45368f629d1f`  
		Last Modified: Tue, 16 Apr 2024 04:53:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd5306cc5ca74bf36574560ae5d4db54aa59f87af511c9f111195d7e2a318e7`  
		Last Modified: Tue, 16 Apr 2024 04:54:47 GMT  
		Size: 605.9 MB (605878411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35aeb2a5afb5a5a671b91d4b5cb8c2b9033df03be8719eb6c9cfa2786e474174`  
		Last Modified: Tue, 16 Apr 2024 04:53:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd8c73c7c23291ecc35c4cc14b9d15e7acdc482c416e66bbdb3f3c5ccea2d1`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1d59efddd5be2f0b371bd100c7245d9e9adb335846af64aaa6be03f9be0fba`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af74b4d7fa4a71ae091abe170e37cd1ecbb5372620506ca2863fbfdc039e50b7`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d9a7ddcb35252a922bd19ca94bce025a15ef7cd76ef40a5e8220eae923e393`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876d28a90fc70e06bc6fa398052a97d4922897452aa8a2db1367a31e0bd30d12`  
		Last Modified: Tue, 16 Apr 2024 04:53:47 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:cb0d3bcfc90b44709a057ae5bfd66b0556f610286a773e575c0d134549120780
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.9 MB (615930332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ae52aa3b8d05afcbedea1f7290dcb7035f0cc3ab2dcded9802fe5ccc9b2a7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:18:54 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 16 Apr 2024 03:18:54 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 16 Apr 2024 03:18:54 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:22:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Tue, 16 Apr 2024 03:22:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Tue, 16 Apr 2024 03:22:22 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb
# Tue, 16 Apr 2024 03:22:22 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 16 Apr 2024 03:22:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 16 Apr 2024 03:22:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 16 Apr 2024 03:23:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c675d9e2a355cca833c9c12f85585e92a4d1cd95858d79e958b507f9ba1a4349            ;;          'amd64')            CB_SHA256=0f5edf6c011df25e172ae54c6bbe5f83be6a3c24e4e23b25e77d5079262c30ca            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Tue, 16 Apr 2024 03:23:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Tue, 16 Apr 2024 03:23:31 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Tue, 16 Apr 2024 03:23:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Tue, 16 Apr 2024 03:23:32 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 16 Apr 2024 03:23:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 16 Apr 2024 03:23:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Tue, 16 Apr 2024 03:23:33 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Tue, 16 Apr 2024 03:23:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 03:23:33 GMT
CMD ["couchbase-server"]
# Tue, 16 Apr 2024 03:23:33 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Tue, 16 Apr 2024 03:23:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63a620f1ecf9579c760cf290f09f23af0305d47d3bb6f3cbcaf31145979bb8`  
		Last Modified: Tue, 16 Apr 2024 03:28:32 GMT  
		Size: 6.1 MB (6110804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db1cb36f52f81614935cd6dd44cf22439186895e6198859fe1cc7c5a1298fc`  
		Last Modified: Tue, 16 Apr 2024 03:28:31 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05138313d3eff50a8b91f16c8d6df5b9e8bd313609e8dc9ee886f240c2db999c`  
		Last Modified: Tue, 16 Apr 2024 03:29:12 GMT  
		Size: 582.6 MB (582610179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcd6463ec7d5ad156ca56e4589e735be34e7c909ac5f6763b320d95137492e5`  
		Last Modified: Tue, 16 Apr 2024 03:28:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1817853d4050bddeff14bb376210616831126c8952f52082f5e29ba8d14ba739`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a91053c9390921bef945eb15171ed04baf15fb026992c2380e2109150a5893f`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174697aa7f6bc87a5ca9ef758d5d25554ee48c62d2bbcdd61a800bcffcc5075`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae688037262871a8b79a71a738f292d3fad93887fae54bdcea5e0f7f203db735`  
		Last Modified: Tue, 16 Apr 2024 03:28:30 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d11b91b7e0e5f4ea147d1df339cdf3a3c1521d6f7eacc39abcc58a7cafabf62`  
		Last Modified: Tue, 16 Apr 2024 03:28:29 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.2.5`

```console
$ docker pull couchbase@sha256:3bb926a13a9d46fd8a44bfe42625f610bc3a10f8657b3886b5f22604bb8cb681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:fc54d3c6ed5ff6293e3f24ce44ea715749b9c4b604b88074e9dc2faba6ad6383
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644241117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf1d526853d30263ae34dd0d990eec906e7d37e795a07b63fee79eaff9d8f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:22:12 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 16 Oct 2024 02:22:12 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 16 Oct 2024 02:22:12 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:22:28 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 16 Oct 2024 02:22:55 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 16 Oct 2024 02:24:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Wed, 16 Oct 2024 02:24:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Wed, 16 Oct 2024 02:24:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 16 Oct 2024 02:24:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 16 Oct 2024 02:24:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 16 Oct 2024 02:25:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 02:25:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 16 Oct 2024 02:25:35 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Wed, 16 Oct 2024 02:25:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 16 Oct 2024 02:25:35 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 16 Oct 2024 02:25:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 16 Oct 2024 02:25:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 16 Oct 2024 02:25:37 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 16 Oct 2024 02:25:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 02:25:37 GMT
CMD ["couchbase-server"]
# Wed, 16 Oct 2024 02:25:37 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 16 Oct 2024 02:25:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a75f1093d68c4a4df16d8da90c0a7fa5de10d215bc15c4dfb921639b3da9d`  
		Last Modified: Wed, 16 Oct 2024 02:32:33 GMT  
		Size: 6.2 MB (6204670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805b2d185509813a24f9505cb9d5a616a84d04580eaea45ae3f2e4d2afdf5757`  
		Last Modified: Wed, 16 Oct 2024 02:32:32 GMT  
		Size: 1.1 MB (1092446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6687ab00d3b506b39a9a5bd5fb095e14dcc2bd3de974060420f4c06f980c7060`  
		Last Modified: Wed, 16 Oct 2024 02:33:24 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c200ff7db29f8e412443beae9a0010823c2bbac99d7f416179bd22952a8712`  
		Last Modified: Wed, 16 Oct 2024 02:34:19 GMT  
		Size: 608.4 MB (608355047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b8428bcb6049e629792216a6372f3053c6a9486d34cf2dd303ad962797c863`  
		Last Modified: Wed, 16 Oct 2024 02:33:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1deea5194a5cc887c2f95bec477c12d05e59a44faa83c99bfbb8cb772cb99a8`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 821.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8c44ef19e976a6de5a58b04610dc15b5c36dc79d8dc63821e6c7ffccec1ffd`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2259fd86f971d980baf3cc55cdd8d1f43a264352ee6ad57885b6aaf07e8c38`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6c315b3ac4fea94dfe8a835e58497f65bc961a0bf1e4d8c3e75ebc4947976`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d0dccfb2833e2b58b4ff5d17a6554065b98640ee30e4cfb2ed2989a6060218`  
		Last Modified: Wed, 16 Oct 2024 02:33:22 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:66b3fdd690d608ffbe551dcdd5e1c9e9cb92ed55fc0f0ee3f2a95c6af2732833
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619821330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d12fe4f829d544aeca6ae2616502b9a918de98fe99b3e06fb39504ca672fff6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 00:58:37 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 16 Oct 2024 00:58:38 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 16 Oct 2024 00:58:38 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 00:59:12 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 16 Oct 2024 01:00:25 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 16 Oct 2024 01:01:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Wed, 16 Oct 2024 01:01:31 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Wed, 16 Oct 2024 01:01:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 16 Oct 2024 01:01:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 16 Oct 2024 01:01:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 16 Oct 2024 01:02:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 16 Oct 2024 01:02:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 16 Oct 2024 01:02:45 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Wed, 16 Oct 2024 01:02:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 16 Oct 2024 01:02:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 16 Oct 2024 01:02:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 16 Oct 2024 01:02:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 16 Oct 2024 01:02:46 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 16 Oct 2024 01:02:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 01:02:47 GMT
CMD ["couchbase-server"]
# Wed, 16 Oct 2024 01:02:47 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 16 Oct 2024 01:02:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:963ceec6c2ca13b343a25d3157e3e30ffa80fc297ad5e3f78d8f43087427b2d3`  
		Last Modified: Sat, 12 Oct 2024 07:30:30 GMT  
		Size: 27.2 MB (27204259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78e6f6941d8212e81ac25e018b1ead37c0c44c9ed155d6f48148bda886de531`  
		Last Modified: Wed, 16 Oct 2024 01:06:15 GMT  
		Size: 6.0 MB (6041871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc7c114f093f2a5b8b90e9f681ab5cbe80a551963e43c9758c3323999f692b6`  
		Last Modified: Wed, 16 Oct 2024 01:06:13 GMT  
		Size: 938.0 KB (938015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fc261a6e4a2cc3d68c2b67288a62a642ecbb69f1c9c7c7cbbf5f85dd93e262`  
		Last Modified: Wed, 16 Oct 2024 01:06:54 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caa32686ca5cae50370a02f540cc662ec955316c99c3c4dd48c8e6bce2a762a`  
		Last Modified: Wed, 16 Oct 2024 01:07:37 GMT  
		Size: 585.6 MB (585632177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5b14238faa625d7777e9bff471bcefde1e58938085005ddab026ab2ddc8b6d`  
		Last Modified: Wed, 16 Oct 2024 01:06:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013f7d889ea6ddd3e81ee17b06ef00e086b5184ca20a951e2be005b66ee663d9`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49592155f8ad68ac3353dae4f34310ac1a5ecd89bf00292588e8f8cfbe856975`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3116ffaf5958283ea6802017ee637c1a401a136fca83b56a181436ed395d95`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3443a0240c8bbe3ecb1731a12727cd6c8d4f69244e9ab032e7837700726678fe`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40c2c4a5f84e8e3299bba0c8142bf84898cd1a4c529250e1b6b57438a88aaeb`  
		Last Modified: Wed, 16 Oct 2024 01:06:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.2.6`

```console
$ docker pull couchbase@sha256:1dac0baa8d3aa50c8805d470251e7e7439b788dc65352a89b081946e8206ab91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.2.6` - linux; amd64

```console
$ docker pull couchbase@sha256:4b58e0f8320f4bcaa514e02825a9f8b5e9b0db273b3aede57566531df5be959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650159192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d483933a28486d97ddc44bbaa28bdf7ea70d9a3e4b677f7db49bd7c65ca6db17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bce8dc623fb4f3b3e2f2cc90f532dac81793aacbfd9a8bc34c7f272703f7a04`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 6.2 MB (6203640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19b7a1a5cddb1dd4cc46227271aebc5b7e04e4a597533097f72215b6de729a9`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 864.1 KB (864102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254b5ffe8533432799b56c6292c531117f209ee875676174e3188c2cd6b67c76`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e6bd39cd5ff83a20414e99f19041663a8313b4e0b5b69f78776e581d85181`  
		Last Modified: Tue, 12 Nov 2024 00:58:21 GMT  
		Size: 615.6 MB (615575393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d278f5fbb4ee15892c99cac6533847d979ee97e0e2b63098ca5edd4b181b0df`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833d0cc313a835e05978d3a22e3dde75ae46d8d17a0e7db6fcdf13ed201b50cf`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159862f14c611065e1095187d03c984757591a20abe4438321678feb502d9abe`  
		Last Modified: Tue, 12 Nov 2024 00:58:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8028c515492bf94343b675e5ffdf634023b92257b9ce84725ae8c515f7db4283`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e6789d74bcbcf727c3b7a0b84ec13e12667d062fba4be39233407cc8ae5477`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ece909dec61e564cba6a304fe5fb8d33cb6caee4a492b8a6f3007f86f3044`  
		Last Modified: Tue, 12 Nov 2024 00:58:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:07b7ddfcbbc6654d535c6f8e3aa740fc5686593c93e326761d5ca322ef7e456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 KB (35805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6d9fe49c4d25b47cb627b75fba8083241e331d3cb80a914c8c43703509d432`

```dockerfile
```

-	Layers:
	-	`sha256:34e1cbdcc69402662d39f078751cc241871754e7f67167f99131512e449d1730`  
		Last Modified: Tue, 12 Nov 2024 00:58:12 GMT  
		Size: 35.8 KB (35805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.2.6` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:7d6e356fbf2f30d7ae3b911cf30a838def123ad5cdc478f4c28ffc70e29b7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.1 MB (625088287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5969a5713480f17d7527249193f24bb3bc7ac4993aaab6b130a8b41df733d931`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Tue, 17 Sep 2024 23:15:04 GMT
ARG RELEASE
# Tue, 17 Sep 2024 23:15:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 17 Sep 2024 23:15:04 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 23:15:04 GMT
LABEL maintainer=docker@couchbase.com
# Tue, 17 Sep 2024 23:15:04 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb
# Tue, 17 Sep 2024 23:15:04 GMT
ARG CB_SKIP_CHECKSUM=false
# Tue, 17 Sep 2024 23:15:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=a5f0e4c2bc8bc38a4001818ebe7ebd12ca028876204f37f04b6a95b487bbf114            ;;          'amd64')            CB_SHA256=eb8da18cee68a94b9c300a86c2ceafe2d9e651e237dc0013d002f308659c6645            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.6 CB_PACKAGE=couchbase-server-enterprise_7.2.6-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
COPY scripts/entrypoint.sh / # buildkit
# Tue, 17 Sep 2024 23:15:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Sep 2024 23:15:04 GMT
CMD ["couchbase-server"]
# Tue, 17 Sep 2024 23:15:04 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Tue, 17 Sep 2024 23:15:04 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c396dd29f50bcc388cd0a519fac3f34e943a627c9613af69542b47bc466da9`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 6.0 MB (6041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d496ab92773d4bdd2c16f3738ba1c83e773a36e0751d0d35726afa7c5a8e82f`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 711.5 KB (711539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c75c5ebbbf48135024eccbbe96b521716a04200202d2875050b09064894d0`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319800ef44742b499fcfbc93d09de12fea172ea219d05d004f91261026c1c30`  
		Last Modified: Tue, 12 Nov 2024 01:21:19 GMT  
		Size: 592.4 MB (592356189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4482d826458e6222a04fe76268240d36790979884f96d96bb5b497326d52182`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4274ccec6ea478230d9bcca8679cdf9aa16736185b4f153f0a55f9c0eb9d8681`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 815.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925dc1477caa9acc381dcf8926803bf1a1cdf324feebd4f41c09da0839e0645`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4336c388f739dae1fd4292ccdf7c2ff11aadc5007eae6d45c269546dc0aba440`  
		Last Modified: Tue, 12 Nov 2024 01:21:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365adc0efea529df15fec109eb02b13100a35d2ce7f790c19926d9dcebcb9b88`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f473ad2dfa83535574df9224f6c6e39650fac01ba4b6f717dfeb0cf4dbfb5f1`  
		Last Modified: Tue, 12 Nov 2024 01:21:06 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.2.6` - unknown; unknown

```console
$ docker pull couchbase@sha256:d6a3d2e1a5b12207764e6ba8007e41e07ca6c779a070cfd4927bc79370c17581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 KB (35990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c65b08c9d54fe98556a645b20872297f9b7901d89dac7dad2fc39816b1d9f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3800b8a1e257590c56d807e081dc422f2914c16ec2c2f9193abd124d3ef823d`  
		Last Modified: Tue, 12 Nov 2024 01:21:04 GMT  
		Size: 36.0 KB (35990 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.0`

```console
$ docker pull couchbase@sha256:2725d8a339831cecaf28f124bd52b5bc8c323b184e1f47f4ef474c489a83c068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:3e7eb016088f1a7b3fc28f014cfed0c7a49248fc4df1d64853d95b3a4ebb8c90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726110733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc41528b1bb6a83d70e8c361a27276e926cd9886b5c961aec69183db1bb1fcaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:47:13 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 06 Mar 2024 05:47:13 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 06 Mar 2024 05:47:13 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 19:53:22 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Mon, 25 Mar 2024 19:54:15 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Mon, 25 Mar 2024 19:54:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 19:54:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 19:54:15 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 19:54:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 19:54:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 25 Mar 2024 19:55:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 19:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 25 Mar 2024 19:55:28 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 25 Mar 2024 19:55:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Mon, 25 Mar 2024 19:55:29 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 25 Mar 2024 19:55:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 25 Mar 2024 19:55:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 25 Mar 2024 19:55:30 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Mon, 25 Mar 2024 19:55:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:55:30 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 19:55:30 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Mon, 25 Mar 2024 19:55:30 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c70b701cc06e2eb6819cce35006c4488c4b5a0d155a9907f97b364b735c9098`  
		Last Modified: Mon, 25 Mar 2024 19:56:58 GMT  
		Size: 6.2 MB (6186179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70ffc4db4d8f1e8937df0d6247cb7bf8ba89311ba720503180a95df5a30247d`  
		Last Modified: Mon, 25 Mar 2024 19:56:57 GMT  
		Size: 1.1 MB (1092117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee74925a0aa53f2d73d2c7fc78af3699f5651b3ca9b135328e03a0b7577c43ec`  
		Last Modified: Mon, 25 Mar 2024 19:56:57 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c4c1c484fc891727c034f8b70547c5e102d96a8e9cd13db032d64c4634ca72`  
		Last Modified: Mon, 25 Mar 2024 19:58:00 GMT  
		Size: 690.2 MB (690243366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369dc8e57ef9e2847ed34d7d3ee11cd3d0a00276bc9938672f32d7afb847e8c6`  
		Last Modified: Mon, 25 Mar 2024 19:56:56 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851a17038a0d8e533365e5b0c9e79226d09554b437bbffdf78257ced2a79fe5d`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b5b586db13e1fa4863a831ff0fbdd0fc317f569e4afd2604b430b4943c5200`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f17e26a77d2b5883a2e5b33b7afc581f8964a019e6a9376acf78aa2ee43e91b`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf97f95dfae3eee59e488fd9e998a534c8a2b44bd885abe3fedfc9fcda4029a4`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7265d35ae73387cce84e60c7a510283337094849bb5fdc29cf028b890a6df136`  
		Last Modified: Mon, 25 Mar 2024 19:56:54 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.6.0` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:3000e1f9550ce49e8a6c1456ac0293937040b1daaea08edd7f33ed9176f3b299
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699275743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ac23c76f00b8455293f0a75f1509e3b356118a0d0676a861203149a2a364ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:53:20 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 06 Mar 2024 03:53:20 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 06 Mar 2024 03:53:20 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 20:09:44 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Mon, 25 Mar 2024 20:10:37 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Mon, 25 Mar 2024 20:10:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0
# Mon, 25 Mar 2024 20:10:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb
# Mon, 25 Mar 2024 20:10:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Mon, 25 Mar 2024 20:10:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 25 Mar 2024 20:10:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 25 Mar 2024 20:11:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=1512430a602c67d53886502d758bf95b25b9faab066d08292a8eb496e9c08492            ;;          'amd64')            CB_SHA256=fe94419fff0c1b9176292b44ab8715fd0e8e48872e76330cc6ec6f3fa07b3966            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 25 Mar 2024 20:11:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 25 Mar 2024 20:11:54 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 25 Mar 2024 20:11:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Mon, 25 Mar 2024 20:11:54 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 25 Mar 2024 20:11:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 25 Mar 2024 20:11:55 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.0-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.0 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 25 Mar 2024 20:11:55 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Mon, 25 Mar 2024 20:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:11:55 GMT
CMD ["couchbase-server"]
# Mon, 25 Mar 2024 20:11:56 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Mon, 25 Mar 2024 20:11:56 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a70596a0a7145916afe9432e93cb09ff5afcb23b36d2e34b6ae25193d2b9ba`  
		Last Modified: Mon, 25 Mar 2024 20:13:26 GMT  
		Size: 6.0 MB (6027552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fd1b0caa23b4cff84ef14dd8c48fb56d2da767b34c863298692c154ab1491b`  
		Last Modified: Mon, 25 Mar 2024 20:13:25 GMT  
		Size: 937.9 KB (937892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693ceb773c091ecfd338ecd6a6b79478c857d06f64a6ec17b9ea49e1d38b6c6d`  
		Last Modified: Mon, 25 Mar 2024 20:13:24 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3e601f979953f24e1506ac87152e038abcb9cbeb0dcde753ed118cfcadbd24`  
		Last Modified: Mon, 25 Mar 2024 20:14:10 GMT  
		Size: 665.1 MB (665101253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c5b66cf8d66e5bcbd3b0df24be085b898261b8f24885de27db8a30638a9c2a`  
		Last Modified: Mon, 25 Mar 2024 20:13:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c757f4a852e02ada3140a9b176e07176090aebcf58e90b290e73e587d4f30813`  
		Last Modified: Mon, 25 Mar 2024 20:13:23 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cbd7bbb21b3cf07ea9ce9c584d8b81b4c2444125654d925b2f11ba57596293`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e271cc0ba7958e06e2093df6eb127abf059d11f021c8a7c1000d6a889fb59e95`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bb590d20c882bb9af049fa740a4b7abc4803a3b74998c74e8545660c5220f1`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af65230ed87acd09c4aff658c30d964a4425be9c0c32cca852947de5cd1b141`  
		Last Modified: Mon, 25 Mar 2024 20:13:22 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.6.1`

```console
$ docker pull couchbase@sha256:fd94ce4abaaccaa55d9d45ed1dd18bcbe1b30ca2bf72a1bb7c9f8d3008b7aeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:337482c7db431e6b0bbf13e4dc584bb9928274dfa25ee632425e03f653f4e9e2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726129645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58c10fdcacdbe999cd31c8759e946000814c67ff84ba2cc1607ea6de22c4dc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:15:47 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 05:15:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 05:15:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:16:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 05:16:47 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 05 Jun 2024 05:16:48 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 05 Jun 2024 05:16:48 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Wed, 05 Jun 2024 05:16:48 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 05 Jun 2024 05:16:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 05 Jun 2024 05:16:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 05 Jun 2024 05:18:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:18:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 05 Jun 2024 05:18:18 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 05 Jun 2024 05:18:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 05 Jun 2024 05:18:18 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 05 Jun 2024 05:18:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 05 Jun 2024 05:18:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 05 Jun 2024 05:18:20 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 05 Jun 2024 05:18:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Jun 2024 05:18:20 GMT
CMD ["couchbase-server"]
# Wed, 05 Jun 2024 05:18:20 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 05 Jun 2024 05:18:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2034c2147aa55eac433cfa8e83637c42989b33107ea886069ff5b5d5bee96e59`  
		Last Modified: Wed, 05 Jun 2024 05:27:56 GMT  
		Size: 6.2 MB (6186275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fad3b9e423454fa6e83992e4bbe4c11eaf6c1ae328dca66778e3f76a9ec96a`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 1.1 MB (1092231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9a5d6a077730b14f7c41ecb61f99276201c4c689a2baf803fb12894796dea6`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a09216a074eec63c6df1993ccb5c47953902be8a97fd75bfc59fa8e13bfbabc`  
		Last Modified: Wed, 05 Jun 2024 05:28:58 GMT  
		Size: 690.3 MB (690262214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a40c2f022aa56d900d4bc4fd4a1ca0c62d493b5dced90011ac4d96e322a0a9`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4646d6b8dfa5bd18b9f17d46ecef0bceb8ad3b40a1d94128f7aca1a43fddf235`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fd883698752db7f3b1c10957ecde555282507023af3a6f712bb63d7b3ff041`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead79c6ba554441124b1fe3780c322a8f07a3e706ce44323b1db3e56644b775a`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2763561b33b75afc5ebcf03fc296efe76c59df84d299cd5616f3cb1b36be5cc`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43b51fcbc7a8324004e7cf52e5784f6f8d8b49a4e913b8046ff525a8dc4ff48`  
		Last Modified: Wed, 05 Jun 2024 05:27:53 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:65eafe602fc11638ccf500d3d984bb166a2b8835da7982f82f384c6ec20d2a36
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.3 MB (699309271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee32de1bac9dde7d88abb9936a34068ed6a1c47644a9483379fae04da3f41dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:29 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 04:37:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 04:37:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:37:51 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 04:38:14 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Wed, 05 Jun 2024 04:38:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Wed, 05 Jun 2024 04:38:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Wed, 05 Jun 2024 04:38:15 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 05 Jun 2024 04:38:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 05 Jun 2024 04:38:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 05 Jun 2024 04:39:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:39:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 05 Jun 2024 04:39:30 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 05 Jun 2024 04:39:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Wed, 05 Jun 2024 04:39:30 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 05 Jun 2024 04:39:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 05 Jun 2024 04:39:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 05 Jun 2024 04:39:31 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Wed, 05 Jun 2024 04:39:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 05 Jun 2024 04:39:32 GMT
CMD ["couchbase-server"]
# Wed, 05 Jun 2024 04:39:32 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Wed, 05 Jun 2024 04:39:32 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd764ccf72f3934668b26d77c587c626d519a4000fe05b91cd9adbd69046e17`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 6.0 MB (6027453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f702385cdd214a6fef4dc6d55284657de902d0d9d1de050dfad15bc6f91c5`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 937.8 KB (937842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3314c1071254b28a0a521e3fa90ec43b146ed5ae7d66debe2901c91cad958ea7`  
		Last Modified: Wed, 05 Jun 2024 04:45:01 GMT  
		Size: 1.8 KB (1840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48284f6c8a0c7f8c517fe535f95e38595fd80d0145d6a0845f05932bb1b959fd`  
		Last Modified: Wed, 05 Jun 2024 04:45:47 GMT  
		Size: 665.1 MB (665134032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4beecff366ba038a147495b319d5ac261dd810f34be094949254a0380ee8665`  
		Last Modified: Wed, 05 Jun 2024 04:45:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2251face004d78d2c656061b24045054e380b5f25a8cfcb176fd7e769193b`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1832473980e8699d416b37a01176cf2ac88e702e12c59a68f38301734ea5a8`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27df547176ae8dee54df2b0c34f33df77e77b0666c4c5aaa6fcff65952ba6c0`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26ea295d184fce055cd028b0466ec5507b48b2370e6c3cd9b522c5b6199cd98`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d13cf202de00b888fd4a0c3b2efbb326bd9a957e10354cde05171ca878bff62`  
		Last Modified: Wed, 05 Jun 2024 04:44:59 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.6.2`

```console
$ docker pull couchbase@sha256:cc9e0ecdbef303d65f0a6d9baa6afa52eb687dbc6b3b512f1950a2a6a324fa55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:1c9b750e63714c46b6b7f348eaee231aaf029e5eaee68b30589bf333dad0410e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.4 MB (735358640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b206bc7556eeb26682217bb56b71146f685efd7580c68336196ef1b6d5491`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:15:47 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 05:15:47 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 05:15:47 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 05:16:01 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 05:16:47 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Sat, 20 Jul 2024 01:19:28 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Sat, 20 Jul 2024 01:19:28 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Sat, 20 Jul 2024 01:19:28 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 20 Jul 2024 01:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 20 Jul 2024 01:19:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 20 Jul 2024 01:21:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 20 Jul 2024 01:21:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 20 Jul 2024 01:21:07 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Sat, 20 Jul 2024 01:21:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Sat, 20 Jul 2024 01:21:07 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 20 Jul 2024 01:21:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 20 Jul 2024 01:21:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 20 Jul 2024 01:21:09 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Sat, 20 Jul 2024 01:21:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 20 Jul 2024 01:21:09 GMT
CMD ["couchbase-server"]
# Sat, 20 Jul 2024 01:21:09 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 20 Jul 2024 01:21:09 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2034c2147aa55eac433cfa8e83637c42989b33107ea886069ff5b5d5bee96e59`  
		Last Modified: Wed, 05 Jun 2024 05:27:56 GMT  
		Size: 6.2 MB (6186275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fad3b9e423454fa6e83992e4bbe4c11eaf6c1ae328dca66778e3f76a9ec96a`  
		Last Modified: Wed, 05 Jun 2024 05:27:55 GMT  
		Size: 1.1 MB (1092231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cab928b74c7c94295c373baf7e0f4a062dd7bdd13e23bfc52b8a1cb283d363`  
		Last Modified: Sat, 20 Jul 2024 01:23:03 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a11b8f14d478376110dc1bc23628bff92308435d082183388f48b81adcd54e`  
		Last Modified: Sat, 20 Jul 2024 01:24:07 GMT  
		Size: 699.5 MB (699490903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e90f1615b4a2d03bf03b2cad1e6bc587e747ff49bae9edbcf7420f76b739625`  
		Last Modified: Sat, 20 Jul 2024 01:23:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac67f396ab12439cf7c494ab03b8a184e94689f41300b00241cfca0eeac9607`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 820.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ed228e2b9049986c163409cfd08f01cefc598d6a7c232b1d009f44d7649bc1`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293eb32a691d34e751a005ecef52eb064deed8308a9fe8a8edcc2d445766cb13`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3327d1197126a1bcc2ee7df413bac8d3b01b10731932e553505bcbb4f7ed25df`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d634d5aa8dba461c3661c5d1e2057356a761556dfe52ef0e17dfb59517a66a`  
		Last Modified: Sat, 20 Jul 2024 01:23:01 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:bee661151f53113263132ea13ea17d3c5f839b5e0805cdc511e482e7c4fdf290
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707786526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a44dec6ca8568d26a6e7a004c1615b7e4c393d79993610dfe7e7cfcaf595f3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 04:37:29 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 05 Jun 2024 04:37:29 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 05 Jun 2024 04:37:29 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 05 Jun 2024 04:37:51 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Wed, 05 Jun 2024 04:38:14 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Sat, 20 Jul 2024 01:50:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Sat, 20 Jul 2024 01:50:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Sat, 20 Jul 2024 01:50:37 GMT
ARG CB_SKIP_CHECKSUM=false
# Sat, 20 Jul 2024 01:50:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Sat, 20 Jul 2024 01:50:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Sat, 20 Jul 2024 01:51:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Sat, 20 Jul 2024 01:52:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Sat, 20 Jul 2024 01:52:03 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Sat, 20 Jul 2024 01:52:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Sat, 20 Jul 2024 01:52:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Sat, 20 Jul 2024 01:52:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Sat, 20 Jul 2024 01:52:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Sat, 20 Jul 2024 01:52:04 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Sat, 20 Jul 2024 01:52:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 20 Jul 2024 01:52:05 GMT
CMD ["couchbase-server"]
# Sat, 20 Jul 2024 01:52:05 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Sat, 20 Jul 2024 01:52:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd764ccf72f3934668b26d77c587c626d519a4000fe05b91cd9adbd69046e17`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 6.0 MB (6027453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f702385cdd214a6fef4dc6d55284657de902d0d9d1de050dfad15bc6f91c5`  
		Last Modified: Wed, 05 Jun 2024 04:45:02 GMT  
		Size: 937.8 KB (937842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a01210cf437bd96d8ddb4ae98ed12e2598e6661482b39e98b288ef23b0f646`  
		Last Modified: Sat, 20 Jul 2024 01:53:29 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43b1d78f25447a10511981612d08371f853a8d92b1dd7d85f2a28cc45f76545`  
		Last Modified: Sat, 20 Jul 2024 01:54:16 GMT  
		Size: 673.6 MB (673610965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69f5cd08cd5e013914d939b40d4f7914b9ba0f315bf47d06188df3eb9f0ad8e`  
		Last Modified: Sat, 20 Jul 2024 01:53:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b0e46255bdd75f55954f8c73cc606a39fadc550c56a8ec0d114320d078182b`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 821.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367087c5664dbde36d013211e42341b868aae61e64f5d574fe88885daf2f09c6`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f89a0c293002313d3d9d0c4fb3e7cc2c363cc8ca3b1d802652f9b4a9aaf7a7`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfadc3bf51c177d39f86456f65656f00dba5469dbf1c655e5c55b256fef46456`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18b30d001d3cbbbd7cd8d21d2cb8c637e452c7cd136b12968539382c34a86a3`  
		Last Modified: Sat, 20 Jul 2024 01:53:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.6.3`

```console
$ docker pull couchbase@sha256:dff8011f5ed177b35ca5f916a51d97c1c7c0c53aa2013988d83f1e52171ac934
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.3` - linux; amd64

```console
$ docker pull couchbase@sha256:15d79ad96890fbfb17a36dd0e36575763251246c94becd76fe056ba96c7325e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **768.9 MB (768925234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3a46a56717114c7d9a9e75ba5538403252161f66fe571bae33d58c09c49fd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181cf9a43df8c5e399e6d27dc51b550cb7eef1030eb4a23e9f2f1afc4fad47f7`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 39.3 MB (39276283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a57105c51c8a53b98e917c2a49922367ac246740ec2c4e5cb12c63f7618cbf`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 926.1 KB (926064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289ce120bf8531c16bb73d516193c2f95d5195d73ffb2bc4161ac2a689e7b85`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d3be05b1124e4858d82f0dbf1835540b90859cd9a894e529eae5a96ced26b6`  
		Last Modified: Tue, 12 Nov 2024 00:57:33 GMT  
		Size: 699.2 MB (699182015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20c0f01b24c1dd797d45570d12038d45ea57c1ffa8455ed3b675d7cbe161415`  
		Last Modified: Tue, 12 Nov 2024 00:57:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cb7effd6ff13e9221825c975693a2f7eaeb5eb2f265f68bfd029cd2bdf5597`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d50fafe6355c5d292618c4baa5ae1347782aa58b113f23cf81498296d6a063`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcccada2863443a2551bf883c46696463ef77ea948fd074b08889a9aca0fd53`  
		Last Modified: Tue, 12 Nov 2024 00:57:25 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786b1974142cdacd50c61e47beb3bb57acbaa3a705b0ed5d6ff920a6dcc3c546`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6a45fae918ae9c11f313b88bf4891ad8aa6f31fbe5a86006ef9240c17ca2b4`  
		Last Modified: Tue, 12 Nov 2024 00:57:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:75d8f31d7368d637a7e098f38e21b5b272747d82b4935da1fac0749e4079419d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b568b81538ac5613e925c3341db97a3e720df08305bb0dee448cfeddedd53278`

```dockerfile
```

-	Layers:
	-	`sha256:680d4d9b916a40a0d91194e0fb7dbefd7e698c3ed2567bd465065af663466647`  
		Last Modified: Tue, 12 Nov 2024 00:57:23 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.3` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:e946c69bd434360dff17a1ae8c0aab63a7f317a29cf2f27127791e9a4eecfb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **740.3 MB (740282679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3851b9155496fe9af8cbc67ff23e4caffbd71871440a790f482c22ba9dc111a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 30 Aug 2024 20:05:06 GMT
ARG RELEASE
# Fri, 30 Aug 2024 20:05:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 Aug 2024 20:05:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["/bin/bash"]
# Fri, 30 Aug 2024 20:05:06 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 30 Aug 2024 20:05:06 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb
# Fri, 30 Aug 2024 20:05:06 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 30 Aug 2024 20:05:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=24c783f316cb6cb368da2a80d657a652b1efb4d03e30b8ea540481008cf68191            ;;          'amd64')            CB_SHA256=882df2178c657ddbfdc7e532d32252ee5367403b0472aec2699433634a98b88c            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.3 CB_PACKAGE=couchbase-server-enterprise_7.6.3-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 30 Aug 2024 20:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Aug 2024 20:05:06 GMT
CMD ["couchbase-server"]
# Fri, 30 Aug 2024 20:05:06 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 30 Aug 2024 20:05:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9837b35b89321c86b62c4addb2275efc6de452946a2230ae527a93ebaf64cbe6`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 38.9 MB (38853543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fd330817e32cf64f5305421981635c23024aced95a96800b8b6ce2fb23e74`  
		Last Modified: Tue, 12 Nov 2024 01:14:05 GMT  
		Size: 770.5 KB (770459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d108e111e1445face871399f66a53e0b609b5ff77408a902bba19fac2c77d02`  
		Last Modified: Tue, 12 Nov 2024 01:14:04 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de71da94bf9d6e25f0e91a9daf9bcf94b199bac819f65b6a29e61f77169cb6`  
		Last Modified: Tue, 12 Nov 2024 01:14:18 GMT  
		Size: 673.3 MB (673295157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d99b296f051c9dc747c85dd25c8159a417848e04e40d834b284f8df97c87ee`  
		Last Modified: Tue, 12 Nov 2024 01:14:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59d212c610c18199191dbe112705bc49d5e2e984b6fb9d07b247fc49c3ce0e3`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfb7bdaffda0c2da7179426e577d7b60142ebb643e96480fd11a5f01f4d7d36`  
		Last Modified: Tue, 12 Nov 2024 01:14:06 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfec9e5848ef97d3adba7c6d08916d14fa24da401e5b27cedac89051fc43c3b3`  
		Last Modified: Tue, 12 Nov 2024 01:14:07 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdb3085b85319798414ae6966fdd5ae53da24afd01358f25793b83d7b452e08`  
		Last Modified: Tue, 12 Nov 2024 01:14:07 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61fd3b1b4b3694f62f5143556d788d1c795cdbac69b5109a7bdb516dd57f20`  
		Last Modified: Tue, 12 Nov 2024 01:14:08 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.3` - unknown; unknown

```console
$ docker pull couchbase@sha256:1f527e11d9d65304110978d5ef93ff51e65d7817c1cf1acb3db44025bbb39e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b35e309505303c360e78d5104f12aa63359e7bc911244e4ffa3d7de76652a`

```dockerfile
```

-	Layers:
	-	`sha256:c326186959e6a2fff0a42329d862b28666f28c789c125277ea53350eb9dc99f2`  
		Last Modified: Tue, 12 Nov 2024 01:14:04 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.4`

```console
$ docker pull couchbase@sha256:1712f7ea984a17e98422d23cad535a24251fc59726720a535786ea4386dfae77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:bb46e6473d51c1301c9e223d3b2a0f8bf9fda28282c59e1db26db3730d6cab57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.6 MB (771640031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ce6132cdb3fa96f599f385750800b1b5373663d2fee48a3c63a8d979f66cc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e4c8297c01db11c191858fd6cf8a7511d64a9118a1c1c750d681e3841e7f3`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 39.3 MB (39298708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce06b3288eb688faca7cdc69d231f81faaa16e369004bfaef06068b9687c27a`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 926.1 KB (926065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ee6a894c26a477744c2bc2b3101e65176887db8b0aeb5cf047c5884101d455`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7451ade6546d4e3b9d7953419d27c746ce6b0e9f23a891197a416e9a34cf29`  
		Last Modified: Wed, 11 Dec 2024 20:31:24 GMT  
		Size: 701.9 MB (701874383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac90a5eb80de27a57eeff0fead5cf60c6a688e1e8ab5d0510560b51277ea74a`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e05105422fbe68ce9e63c322db62cb0c03c6d6ce8d543b5923087760b80230`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b19bb06f3c79a6921855e7577dfa4a8a2ee0dbfef49e3ef3d13eb64eb62ac6`  
		Last Modified: Wed, 11 Dec 2024 20:31:15 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b714361da7137396fe322b09fc0e45fedcb305b31525630b48039fbf83e968c`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785dba9ba6eea486f48865f659aa8f43797dd9892579171a4220ee34e9c387d3`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02364dd300798b3a2cdffb4fd4c9996710276b95ddd51cd92bf0bdb976c03`  
		Last Modified: Wed, 11 Dec 2024 20:31:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:e875371520bedaa2baffb1beeea80adefa9df8a91ab6f12b0f01cc032977ad47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d8101bc5a78ebb73c600b37b58d257e800de5275e2f26524dff7688415b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:5951a1e0fc56cf41e206b54e13f281427ce397d604402be27b44f6c0664377aa`  
		Last Modified: Wed, 11 Dec 2024 20:31:14 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:51890184c7f5923841b5d2667eaac8968a0bb450d93b8e377e98f09867f21012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.5 MB (742534627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37c525e8fa9c00cf8205958c87d66908faf2e0ddb4182a09a3a6dddce05f1a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Dec 2024 01:31:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 11 Dec 2024 01:31:34 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb
# Wed, 11 Dec 2024 01:31:34 GMT
ARG CB_SKIP_CHECKSUM=false
# Wed, 11 Dec 2024 01:31:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=362376a07ccdc1d604ef2d48229d853bed9340dbd033abd8a0174819dfa76b6e            ;;          'amd64')            CB_SHA256=9616bba1b213231493b4d17ed677f0dc26575e0d7f09234e6d4a6e0f6b1358ad            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.4 CB_PACKAGE=couchbase-server-enterprise_7.6.4-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
COPY scripts/entrypoint.sh / # buildkit
# Wed, 11 Dec 2024 01:31:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Dec 2024 01:31:34 GMT
CMD ["couchbase-server"]
# Wed, 11 Dec 2024 01:31:34 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Wed, 11 Dec 2024 01:31:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0584481da729d18de66076f7754e37c2bbc39cbf05bd725b8aa1ebf12e1429a`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 38.8 MB (38844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9437b11152e6789daaee1b8b2816829ecec5fe6f7b7e66d2b57cf0a8fb340f5`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 770.4 KB (770448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b80241375276135ce691e34844832bbc260efe1e17f69b3f6c0c63a909cf8`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3461cd28120e1f6e3a2a5d1632a4c0b55c34c9f983e76358764a1c2ef23dd3`  
		Last Modified: Wed, 11 Dec 2024 20:35:36 GMT  
		Size: 675.6 MB (675556548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9a2303e4b89e2749df948d7b77b504b000b4b505078adcfb37a62dcd836a2`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacce055b74872fa011424cec1d27c67e1a1e63bd686fd81dc6f607572c5a6bf`  
		Last Modified: Wed, 11 Dec 2024 20:35:23 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560a8748af089af62557555c76fee8ee17283476c34a1a2719fce6c853545f9a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fd38386fb9ec7054edc75e6910d24e7f2828b2898eba07f0ab18f31df677a`  
		Last Modified: Wed, 11 Dec 2024 20:35:24 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae18f583723b3303d32822f4967c9220fefebebdca459e5cbccd3efd1a0b5a6f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c5cb759bf8528349b284da7a8f8e541fdda4bec66b63b16482c7eca1d329f`  
		Last Modified: Wed, 11 Dec 2024 20:35:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.4` - unknown; unknown

```console
$ docker pull couchbase@sha256:38911045564e44eee162d11ab29804f5a2411172e6c55fc0959d3046d87c3e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d54da9ce17575a870692837ab8c7c5ee9b37c2595580d3efb48953b68c80e`

```dockerfile
```

-	Layers:
	-	`sha256:f05cbd60b6824e37fba0b063111378fdd30aa399b050e17cc9fbeb37de5ea28d`  
		Last Modified: Wed, 11 Dec 2024 20:35:22 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:enterprise-7.6.5`

```console
$ docker pull couchbase@sha256:2c1ec01cdf6cb2142bd8219ae191a7b039e7353d51868e9bf6807d3ec629750d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:63f655af7ae0c05f2203a89c3fc69a2949d9520ecc0c2c7f3a5eac67fe3b42cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771497798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ff576beaa9240c61d927b9f6b849effcdabc46db8e282dba8242ca9518196c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d270795631b0971893631768750b0de304a12febfacf7fe0f5a4026c2bcee`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 39.3 MB (39295602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823613d607305acd8ae1edbe587b8c02e78f5ccadbde27cceb19e9ca344727ea`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 926.5 KB (926524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094dda71641f1d4026536ee278a8e30040c669f8fe866519481429eaf49bd7c2`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16402788a89907ea531377d4ef06e2abce136164be8157a9ea4e5f85d75088a6`  
		Last Modified: Tue, 04 Feb 2025 04:40:49 GMT  
		Size: 701.7 MB (701734548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b036622c75a24cfcdf9837c93c85234d5a7abe5628cc827b9cd6227cb751153`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a6250533cf535ddd828f6c6b9098c419c49b7aaa8a8d20619c0a0a8fd2cf4`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ce9448d874ff987bdfd7c3eb61b0a3fd48a7d9dfc73a4ecb99a46c8fda6b3`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a64793937a5d8f5271e6c9668665f540a585508cd26f87995abc41c780b75f6`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2efc41046c96b788cd55290db4fbdca5f07e793a1c512c07551de0c4c054171`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133bd02127032cb69c9e3d1edc362a235641ced952a6514fc2064d45de5923eb`  
		Last Modified: Tue, 04 Feb 2025 04:40:41 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:1c58771043610f9f7b53d2114524e952b057ff7e333e968f157547738b7d886d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f10f1cba8a84ccf9a7fc46cdb25a026072283227dde939d3074c2a30c6a8d`

```dockerfile
```

-	Layers:
	-	`sha256:c9e7ab4d81fb834f5dc73ec294ac450a891102f0d8660cbc47a86c6b53eaffeb`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:01cd206baf811b7c051add20ba17fd65586880b7f4862f0a1dfb5b6a21d5c589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742447958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1965fc289bc7e8b1ccfd9c91807bc41920dc3a95fb840b6b459970c7f945e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdc8d5137de9b565226c43a7234b3a6c27a1db780f35bfb41835c032e3f0dac`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 38.8 MB (38848133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb760e4a8859fed7ea1ffc0434cb9d7221983c1e7efc0bbd8f5223856b23d88`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 770.6 KB (770599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b2abc5868f013566f52b890cdc23967bd9e3246ecc8f1b03a1df1d61cdf694`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f5541d9510754a013a5e7e9cc8f454cbe88f0cca06483cf149711cdaef9df`  
		Last Modified: Tue, 04 Feb 2025 09:11:36 GMT  
		Size: 675.5 MB (675465854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492712947a194f44ae4209e9b72d225e60a228f99e2084ca0d5d02e04de9c0b`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e9dedebddf045d0236ed469d0738d1235e288322c1bca4bf8eeff31e5f91e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826709d0a5dd4d6b8755a04ad9bbde9d326c46ab5182d72c6355ad570c65161`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8913eb3415b49bb55568876ad7d0116762d5da14c2fd273d230e8050e208f8`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e4197ded4c4f2c842e12f696ef2adf5c2cb5dad09acb59c9ddcc22fc5d9899`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583501de5e5975a56e3649e4bf4a9149362cd124cd76d1e410c99c1f336a23e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.5` - unknown; unknown

```console
$ docker pull couchbase@sha256:c329bd890bdbe161653f6aace193fa1c12282fb7a55b5a91baac38f7e4486284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d614bfe2b9ebd8292abeba1a210ffd7d6ecf27eb571f7bc8d4803b675c1d5`

```dockerfile
```

-	Layers:
	-	`sha256:22fa9afc58162c8f930c3aaca635a2f04c41f5834052bbc2339f77df9789772a`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:2c1ec01cdf6cb2142bd8219ae191a7b039e7353d51868e9bf6807d3ec629750d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:63f655af7ae0c05f2203a89c3fc69a2949d9520ecc0c2c7f3a5eac67fe3b42cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **771.5 MB (771497798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ff576beaa9240c61d927b9f6b849effcdabc46db8e282dba8242ca9518196c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d270795631b0971893631768750b0de304a12febfacf7fe0f5a4026c2bcee`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 39.3 MB (39295602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823613d607305acd8ae1edbe587b8c02e78f5ccadbde27cceb19e9ca344727ea`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 926.5 KB (926524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094dda71641f1d4026536ee278a8e30040c669f8fe866519481429eaf49bd7c2`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16402788a89907ea531377d4ef06e2abce136164be8157a9ea4e5f85d75088a6`  
		Last Modified: Tue, 04 Feb 2025 04:40:49 GMT  
		Size: 701.7 MB (701734548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b036622c75a24cfcdf9837c93c85234d5a7abe5628cc827b9cd6227cb751153`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5a6250533cf535ddd828f6c6b9098c419c49b7aaa8a8d20619c0a0a8fd2cf4`  
		Last Modified: Tue, 04 Feb 2025 04:40:39 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095ce9448d874ff987bdfd7c3eb61b0a3fd48a7d9dfc73a4ecb99a46c8fda6b3`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a64793937a5d8f5271e6c9668665f540a585508cd26f87995abc41c780b75f6`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2efc41046c96b788cd55290db4fbdca5f07e793a1c512c07551de0c4c054171`  
		Last Modified: Tue, 04 Feb 2025 04:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133bd02127032cb69c9e3d1edc362a235641ced952a6514fc2064d45de5923eb`  
		Last Modified: Tue, 04 Feb 2025 04:40:41 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:1c58771043610f9f7b53d2114524e952b057ff7e333e968f157547738b7d886d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f10f1cba8a84ccf9a7fc46cdb25a026072283227dde939d3074c2a30c6a8d`

```dockerfile
```

-	Layers:
	-	`sha256:c9e7ab4d81fb834f5dc73ec294ac450a891102f0d8660cbc47a86c6b53eaffeb`  
		Last Modified: Tue, 04 Feb 2025 04:40:38 GMT  
		Size: 36.4 KB (36432 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:latest` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:01cd206baf811b7c051add20ba17fd65586880b7f4862f0a1dfb5b6a21d5c589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 MB (742447958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1965fc289bc7e8b1ccfd9c91807bc41920dc3a95fb840b6b459970c7f945e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 24 Jan 2025 19:07:53 GMT
ARG RELEASE
# Fri, 24 Jan 2025 19:07:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 24 Jan 2025 19:07:53 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 19:07:53 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 24 Jan 2025 19:07:53 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb
# Fri, 24 Jan 2025 19:07:53 GMT
ARG CB_SKIP_CHECKSUM=false
# Fri, 24 Jan 2025 19:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d162fb1d2e7acf151fdbf302c80f79622b7df67bf27ab85d83c40cc7e82a2ad1            ;;          'amd64')            CB_SHA256=9c2f2a01cecf862c210af5a7bfe38fd71fe087c52e1cc168119d34bf7aa79761            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.5 CB_PACKAGE=couchbase-server-enterprise_7.6.5-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
COPY scripts/entrypoint.sh / # buildkit
# Fri, 24 Jan 2025 19:07:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 19:07:53 GMT
CMD ["couchbase-server"]
# Fri, 24 Jan 2025 19:07:53 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Fri, 24 Jan 2025 19:07:53 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdc8d5137de9b565226c43a7234b3a6c27a1db780f35bfb41835c032e3f0dac`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 38.8 MB (38848133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb760e4a8859fed7ea1ffc0434cb9d7221983c1e7efc0bbd8f5223856b23d88`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 770.6 KB (770599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b2abc5868f013566f52b890cdc23967bd9e3246ecc8f1b03a1df1d61cdf694`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 2.0 KB (1994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f5541d9510754a013a5e7e9cc8f454cbe88f0cca06483cf149711cdaef9df`  
		Last Modified: Tue, 04 Feb 2025 09:11:36 GMT  
		Size: 675.5 MB (675465854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492712947a194f44ae4209e9b72d225e60a228f99e2084ca0d5d02e04de9c0b`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e9dedebddf045d0236ed469d0738d1235e288322c1bca4bf8eeff31e5f91e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:22 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d826709d0a5dd4d6b8755a04ad9bbde9d326c46ab5182d72c6355ad570c65161`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8913eb3415b49bb55568876ad7d0116762d5da14c2fd273d230e8050e208f8`  
		Last Modified: Tue, 04 Feb 2025 09:11:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e4197ded4c4f2c842e12f696ef2adf5c2cb5dad09acb59c9ddcc22fc5d9899`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583501de5e5975a56e3649e4bf4a9149362cd124cd76d1e410c99c1f336a23e7`  
		Last Modified: Tue, 04 Feb 2025 09:11:24 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:latest` - unknown; unknown

```console
$ docker pull couchbase@sha256:c329bd890bdbe161653f6aace193fa1c12282fb7a55b5a91baac38f7e4486284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829d614bfe2b9ebd8292abeba1a210ffd7d6ecf27eb571f7bc8d4803b675c1d5`

```dockerfile
```

-	Layers:
	-	`sha256:22fa9afc58162c8f930c3aaca635a2f04c41f5834052bbc2339f77df9789772a`  
		Last Modified: Tue, 04 Feb 2025 09:11:21 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json
