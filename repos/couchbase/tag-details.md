<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:7.0.5`](#couchbase705)
-	[`couchbase:7.1.6`](#couchbase716)
-	[`couchbase:7.2.5`](#couchbase725)
-	[`couchbase:7.6.1`](#couchbase761)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-7.0.2`](#couchbasecommunity-702)
-	[`couchbase:community-7.1.1`](#couchbasecommunity-711)
-	[`couchbase:community-7.2.4`](#couchbasecommunity-724)
-	[`couchbase:community-7.6.1`](#couchbasecommunity-761)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-7.0.5`](#couchbaseenterprise-705)
-	[`couchbase:enterprise-7.1.6`](#couchbaseenterprise-716)
-	[`couchbase:enterprise-7.2.5`](#couchbaseenterprise-725)
-	[`couchbase:enterprise-7.6.1`](#couchbaseenterprise-761)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:7.0.5`

```console
$ docker pull couchbase@sha256:1d82ee796db11b14e6d837d342e75feace2e3bd6606054a5bcbdf106d1a9c11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:7.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:2bbb398e1612cb653c96ea62884e7428fcee41b996692cb68d0c240f18928bf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.7 MB (616705759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90d9a632b7eb69380052b904a26d1d199135be14929e4f8c5a1e828f4405df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:57 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:56:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:56:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:57:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:57:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:57:52 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:57:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:57:52 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:57:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:57:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:57:53 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 May 2024 00:57:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:57:53 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:57:54 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:57:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8dd6aa076fe85827f46df8b7cf6f7bc1b849b0804a4bd22f27595cf982cfe`  
		Last Modified: Thu, 02 May 2024 01:03:05 GMT  
		Size: 6.3 MB (6286683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6d34b916b8f08df67bc384a8fb7a359a8b85bbaebd957a41dd74df8ced176e`  
		Last Modified: Thu, 02 May 2024 01:05:45 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ef2633700e8cad97ea2e148fca2ff1417373f7791e163d0a2d1f02f1d037e`  
		Last Modified: Thu, 02 May 2024 01:06:40 GMT  
		Size: 581.8 MB (581830398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0baf1edf757ddcc50711b161c3fae17e13996a416b264c8998d053aac9d48043`  
		Last Modified: Thu, 02 May 2024 01:05:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465ec6219d975fe2e0e263ef0966bb2ba8eef4c5a8fd41ce646600609f74112`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 748.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a868467492ba046b788aa80921321d9dcd93e8fc026a3f008bc369a85d45c`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f228ba0e4b631d523777873e40af72dab2b3b776a6407fc60560c81b8e4524`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946479679eab4d19ba434606dbd72d26a9923cb20306a9fec16da09e07f7aab1`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ec88b827f3572e810554ca084cd32895104f028c8de24d2fa831861bc1606`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.1.6`

```console
$ docker pull couchbase@sha256:161f9cf82cf82938abc7eb3a8e5b173c4b510610cfd71e2447bf33c30c5337ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:87e8cb2589b75cb82bb43f4c31766f1b040e2e67a75344ffa24dc76bb3496952
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.0 MB (652023721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc58fecfec0a8dbdf036476b9a70d6da5266b1ef9966b68c9d9fcbf0f83b948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:57 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:53:57 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Thu, 02 May 2024 00:53:57 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:53:57 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:53:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:53:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:55:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:55:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:55:21 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:55:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:55:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:55:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:55:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:55:23 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 May 2024 00:55:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:55:23 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:55:23 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:55:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8dd6aa076fe85827f46df8b7cf6f7bc1b849b0804a4bd22f27595cf982cfe`  
		Last Modified: Thu, 02 May 2024 01:03:05 GMT  
		Size: 6.3 MB (6286683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c43fa9aebf73a4de5e8b208d659747cdcdbfa8528591a1158421364c049df`  
		Last Modified: Thu, 02 May 2024 01:03:55 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176b0250db94f20b5965d13ae83f0688f1778a6ad4e7226db3e0f507e906c260`  
		Last Modified: Thu, 02 May 2024 01:04:50 GMT  
		Size: 617.1 MB (617148379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6b3a143c9c8313585c28b4872f75ea144f02bc07a783edc5ad7af680390d8`  
		Last Modified: Thu, 02 May 2024 01:03:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b91b42a5d344a76df2aa58f98990c869d04775f59b75accf04c8cf78425c5`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed19e1f6275e70e29da75160b6c0b60cf534459826df7add422361171b21013`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962ae7b4cdf5d4f8cefc69fcf3cee7693c706bdb58b08ac79368149b9cc800f5`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417e301262691fe9e7681dd421f6dd26d30d22fcc701d36cba6e29163a01be60`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fbca79eaad8b6f442d83ecabc7927434c12023de5263cb04796f0f8c1aa764`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.1.6` - linux; arm64 variant v8

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

## `couchbase:7.2.5`

```console
$ docker pull couchbase@sha256:743df47b52499d3bbbc135206e73b0aa595ed0322af91f890844530d85c6f8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:5fb1362830f2325705d347714617b9059f3762c98ad29f18f572476eb6850154
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644222563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526a686305444f9add31d141101e54f1f516a32501ede0bdfc3c3624f2ac51f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:51:08 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 02 May 2024 00:51:08 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:51:08 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:51:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:51:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:52:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:52:35 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:52:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:52:35 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:52:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:52:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:52:36 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:52:37 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:52:37 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:52:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fe1c8b264cce2a50cc2191a2a9a0b46743e4cbabc88c479376b3247c059b6`  
		Last Modified: Thu, 02 May 2024 01:01:56 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0786a827daa92e8f4ce28d3d0a3d70bfd5a93d12265501e6be9f62d16523ec`  
		Last Modified: Thu, 02 May 2024 01:02:52 GMT  
		Size: 608.4 MB (608354761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e3957b7555f2824be552831594321a893f9ac15fdec2484d1a92bb9a6d7309`  
		Last Modified: Thu, 02 May 2024 01:01:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6eca6e5b1f4d707198d97e747e5b2999d32f68e3330f8d3775f5bfad517e6`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9769fba8498429c111618a0b374867db0bcf3c07ef45c7ddfc87ff7cb2fa55aa`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b03c0f90253f7678d63197b3eb322b982ccc9d401b04cdf3e6eb92a7a4a1e2`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9225831271d5fef37f84f86781a8d35c221cfc050797350df6703e5815305fb3`  
		Last Modified: Thu, 02 May 2024 01:01:55 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e1ad589e668767251fd832e69fab89fdd1c4e4e8bd86e4b4b474ef970fd0f5`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:d3493adad0fbf5d323ebef4b9cce2b8a0a2aab9477a0cdc297f60d9cb532cc6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624269628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5472f0e24a9896338d922653cb92f39f9fe82508e1d3b76d9c3cb3d5205bf394`
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
# Thu, 25 Apr 2024 22:16:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 25 Apr 2024 22:16:18 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:16:18 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:16:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:16:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:17:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:17:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:17:12 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:17:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 22:17:13 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:17:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:17:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:17:14 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 22:17:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:17:14 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:17:14 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:17:14 GMT
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
	-	`sha256:13db1ba8ebb56791def7856b054fc58ab79100e2f7a25a5cabd5b18e72b54c20`  
		Last Modified: Thu, 25 Apr 2024 22:22:33 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e862e6c4fa7ce264e48e374cff2ff9eea9cad2861a5dd2e3c56048cbec3c8379`  
		Last Modified: Thu, 25 Apr 2024 22:23:14 GMT  
		Size: 585.6 MB (585633478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eebc4e958ba7ee39b88d44f0c2090d6454b3e4ee31cc52c2b7cf7753ae7203`  
		Last Modified: Thu, 25 Apr 2024 22:22:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a4b79491d157e91840b9b55c3c2aef862c10cf00250d29890bbb62cd7b6b08`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c9e9265bb76033f6f99ea9a2457563de7d03104c219929d9fa993e6ddeeba`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d358891ae505783b80e36aa12656118d60a9372697e209ae9edb16c4734735fb`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae3cdabb3317dd841dbe1e010374157443facde122dce578a5fe2d476781da0`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d1f78b9579aaf82a0879b4292093bd0d926d91c898abaacbb75515df16bc61`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.6.1`

```console
$ docker pull couchbase@sha256:8e26bc262eaf275ed690771e18d8f9fc74038a07348a9d5323bed4bfd28587e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:38835bf458d2e4cbd9f33bb5c83768f4b12a7a470472edafdc643b9846d355af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726131042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d2f219d1990a6054fe0461254d93ab09c4de6a2c28b013a0a02aac64574937`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:48:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:48:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:49:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:50:04 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:50:05 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:50:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:50:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:50:06 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:50:06 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:50:06 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:50:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07fe4b96ebd53fc3177bbf4e5dcd74de712e50af605f6cbe8e48cad098c2fa`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adbfd73fa263a825a5def76dbc07197afe07ec32046b17c124f323bea98d0ee`  
		Last Modified: Thu, 02 May 2024 01:00:42 GMT  
		Size: 690.3 MB (690263558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c902ef1c5b4700dd341c615e618428862dd09dba615028cdca3e1841622a3816`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cbd88266449594d449d3df784af9591bf9351ccead74fd9345562589878a01`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cb0fd953e14ef6bbcbf0065d63ccb47148e6fca30503a87f24a5e3d94820bf`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6db8ad5983e9cd0c5dfadb622d344e2a132668224b5d8ed85dce1c9b040faa`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269009594dc83f4f03ca1aab7f093cd70c34740c69bf51229f1ba64413d7184f`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2c6152d311d556d65512c14aae0a8bb0a02794fcf473ed63128c8fd9879173`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:7.6.1` - linux; arm64 variant v8

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

## `couchbase:community`

```console
$ docker pull couchbase@sha256:815a8fd0928c1f90bf50f121ea0a6fe959b368dde3ff1b0ecdffb0617664587d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:4409fe452bd0f09896bd643caa9348866efd7f16ef836400659259ded14a5ed3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385922911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4538475c73a983b81e32ca06d3eb5eaa96366a7e2c714e0e43fb050ff8266`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 02 May 2024 00:50:09 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:50:09 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:50:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:50:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:50:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:51:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:51:03 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:51:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:51:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:51:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:51:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:51:04 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:51:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:51:05 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:51:05 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:51:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1d895a9ccd79723ef218e92013b7c859cd0865602175c42c022764100e5977`  
		Last Modified: Thu, 02 May 2024 01:01:04 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775fab3933551288582afd00398e97e1bdb9496370e3b3c75ea1433da7bda763`  
		Last Modified: Thu, 02 May 2024 01:01:45 GMT  
		Size: 350.1 MB (350055423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95877db3c84c262e34faa0f16c49fbfba8fed61aeeb6ccae3e33735ccfd4d4a4`  
		Last Modified: Thu, 02 May 2024 01:01:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d957d3d8d22f60e326004c752faa6491e43fa8d295797720b9675d0325526bd`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01941898c6c7ff68d1d84b666c2f14d7cd3e0e8ba03a37742e21cf2ef85b2401`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f9fb8b3c3bc5b068d20ef75e05b7b53e716c109f6e337287acec0118ed4d7`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81eb65fd47d5c3b74f15fe23baddabfb2a570037ffa02fc8ebad5f323e02cb3`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdb282a11f2bc3cfc146242214db5695bbaa2a8d33f2de4213485adf890e22e`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:321081682d2dd3f30da647bfe29f8bdf5f2bb8cac70eb943236676293c8e0a39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372228414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2362af7280346c95a45d90d3ee7a7df4a12c612bc2318550ac84027de2ba94`
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
# Thu, 25 Apr 2024 22:15:20 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:15:20 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:15:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:15:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:16:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:16:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:16:09 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:16:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 22:16:10 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:16:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:16:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:16:11 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 22:16:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:16:11 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:16:11 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:16:11 GMT
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
	-	`sha256:8769e56c204167d9ec3e325378c22e88c63856fade0dbe4546fa3615c1e71625`  
		Last Modified: Thu, 25 Apr 2024 22:21:52 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5077d86e8a7a20418cd1313df06633a780c74ca0a6d16a4d5010deeefb9fb4`  
		Last Modified: Thu, 25 Apr 2024 22:22:21 GMT  
		Size: 333.6 MB (333592572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8cb4e2838abe8fe39f0bfcc2d4b22a7973b53519b4408acee6dff04016142`  
		Last Modified: Thu, 25 Apr 2024 22:21:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8563c40799b6df0e79a999ec46577596e49668b0331c327a604f1a969d628a4b`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8284de8fcd6f329d99b4012f148ec7e2c53eb2f93a4d9452b58af4d2df5c7961`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 728.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d400ca417a38741016ae22d6e3c335083f8c3a96e0400eb9b3a0ba7336808b0a`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a26477ca3cecf08c0a8bb6e8c837ae05f7af46c5624adde141fc8ed3d779fa`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801a691cd9dc3a030d7ed3df0c19c8b6ce0767512ad0a273c7ad90e74d798879`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:94ec213bb8690e8dc1efed21c32911e7116681752a39a25763daba89e8feec74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:fefa8d1b7dd1019f6b2db7719b83fb7fe60a91c73779bab432cdf52117310c70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429074721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5b53b30df9d465757e1a0a515f1fc73c9b6d37c749e043f9ce317d92d304c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:58:10 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:58:11 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_VERSION=7.0.2
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Thu, 02 May 2024 00:58:11 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Thu, 02 May 2024 00:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:58:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:59:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:59:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:59:06 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:59:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:59:07 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:59:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:59:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 02 May 2024 00:59:08 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 02 May 2024 00:59:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:59:08 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:59:08 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 02 May 2024 00:59:08 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc08d610d2fa548b2b67f737eb36eb283b7a2036afd9bd8d675db8705ba5514`  
		Last Modified: Thu, 02 May 2024 01:06:58 GMT  
		Size: 6.3 MB (6294092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de60ba1b6ccd1ce3f3ff96e2a41cfc090d97f782b61218cc775301c8c4b4d99f`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f10bb3daeb5a6b113a8214c83805f64efabc07aca5743e14fe8837b6988cdc`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1347e5c62c081c8cd54911af7fd643da1463ff4b65e6b13485ecc6f7bdd12a09`  
		Last Modified: Thu, 02 May 2024 01:07:39 GMT  
		Size: 394.1 MB (394062349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cc9db2b286e5a9540143ac7b3eca23ca07bf5eecd386b37e1c76f768e5ef7c`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058b92e31e463d1a4b138ea5f407f2757a78fcacb3d6d26c06b938cd7f1396d2`  
		Last Modified: Thu, 02 May 2024 01:06:55 GMT  
		Size: 599.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8633306ca2854151ccb05471c0b7c2c209241dd568b380ce1f3631cd55397c0`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14958626f7ccbe1614865656aaaf5ecccf87a473969285ef1aea1f2d0a383e2`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910a83ab8115602a23df858681e3f0021dbcbb2f014556b9de04f8d21369508c`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec969ed0b52b873d757f261655524f971a4e7e5c17738a867d85886d44be9ad`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 129.5 KB (129508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec4b5adc5b2aa8268ac9bdc8bea5ea45ceb745e97f93fe7803e735089fe3fd3`  
		Last Modified: Thu, 02 May 2024 01:06:53 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.1.1`

```console
$ docker pull couchbase@sha256:c3f49e0a974513f0bdd22765e86ed0e5b3ea4ecd6e0b192085217ea86f2d3cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.1.1` - linux; amd64

```console
$ docker pull couchbase@sha256:3008b471d354c54d9e1dc59da2060dac2db71ac75f70d2691a7319b11d7e8807
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.7 MB (346675397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c75429f3e8264653493a835a1992c25c45c2ac1c0e25ce0326f1b4f16f05a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:57 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:55:36 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Thu, 02 May 2024 00:55:36 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:55:36 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:55:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:55:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:56:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:56:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:56:22 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:56:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:56:23 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:56:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:56:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:56:24 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 May 2024 00:56:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:56:24 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:56:24 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 02 May 2024 00:56:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8dd6aa076fe85827f46df8b7cf6f7bc1b849b0804a4bd22f27595cf982cfe`  
		Last Modified: Thu, 02 May 2024 01:03:05 GMT  
		Size: 6.3 MB (6286683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac700a840423b948d3c2d56d4b2768bd0ce8deb895d07858cacbda08097edc3`  
		Last Modified: Thu, 02 May 2024 01:05:01 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d27757e1ee766eee3709753ea431f9d7cc82cdcb7a40df6c0205673fee0882`  
		Last Modified: Thu, 02 May 2024 01:05:36 GMT  
		Size: 311.8 MB (311800048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50d5e46cfa4294776e677f7f988f7267befcac09bb0bd6a6101bb338043e8c4`  
		Last Modified: Thu, 02 May 2024 01:05:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ef5a04eeb107878827151d8405efb78fd72df69ae043814ab0034ec44275e0`  
		Last Modified: Thu, 02 May 2024 01:04:59 GMT  
		Size: 739.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a19ac800098f7300496a1f373a045223e01b5ddbab1970b6fa7f8c38af5a3a`  
		Last Modified: Thu, 02 May 2024 01:04:59 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf249ee296b645032851b321a699ee2146e7aea67d6e9ef8967c81fa807e8ba`  
		Last Modified: Thu, 02 May 2024 01:04:59 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c150cc99c67a011b1d6334c38e161eba132c0d584089a6a9af12ba74f38d4c`  
		Last Modified: Thu, 02 May 2024 01:04:59 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81ddcd785f628de0d9f97f19fd60d057584a65eed0d98fafb5558f90f70aac3`  
		Last Modified: Thu, 02 May 2024 01:04:59 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.1.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:4459d72ebb55b26681a8734dc67e13878e8ad87fc10dcc02fe156d4abc213651
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327350360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5161b6d1590874806fff96c9d9f4bc3bf11f81ddeb6a2f248e7e3f07d2991b`
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
# Thu, 25 Apr 2024 22:19:48 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1
# Thu, 25 Apr 2024 22:19:48 GMT
ARG CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:19:48 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:19:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:19:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:20:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=275a0bb41d81920e9948fc05f736eef753179f698a04609eb8fe617d0fe55b8b            ;;          'amd64')            CB_SHA256=2fa47dc00f6d85aad5298149bb52450cc98c2c1e18eb54ab8ed45346c24a9403            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:20:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:20:29 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:20:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 25 Apr 2024 22:20:30 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:20:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:20:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.1.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:20:31 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 25 Apr 2024 22:20:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:20:31 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:20:31 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 25 Apr 2024 22:20:31 GMT
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
	-	`sha256:ec0de0cc0c2b704eeeca14d03692602909b397cb69e5029ebe445998c8c68c6e`  
		Last Modified: Thu, 25 Apr 2024 22:24:51 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d912f3773aa0c4a5d6d21593e27407c0c047f94d3ad34cafb05a786e6c2a5c5`  
		Last Modified: Thu, 25 Apr 2024 22:25:16 GMT  
		Size: 294.0 MB (294027237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab92b8ba87eca29301269f72132a51a7449b7273bb5254767681413db9d7cf`  
		Last Modified: Thu, 25 Apr 2024 22:24:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080d59de1d4383700ac7a9639c8b001e13076400082a73e70535e7da223cdc85`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 740.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807864382c6ed15f1b063929e7dd898190bda4b8098394257f9317ec2787e4a3`  
		Last Modified: Thu, 25 Apr 2024 22:24:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac52b84909c20a845c227cb379122907cd93b233bc56917e10adbb701dc91e8`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700dfafa8122fc14bde9c3dc2827bc9ed7b82f45fde5265ff053ddccd4978ab`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee965786d39c13834357c7c597216fd3d4033231e7036d4db35a5d4159b4c1`  
		Last Modified: Thu, 25 Apr 2024 22:24:49 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.2.4`

```console
$ docker pull couchbase@sha256:ac9b63fbfa48e4dc0711dcd108ccea9415d1679894a5b5530aae598e22774453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.2.4` - linux; amd64

```console
$ docker pull couchbase@sha256:17eae305c2df6eb111bef0fb8a0bcd7195609492c04a25d8e2c2ccdceee4bb5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366178850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321fcefc2565f64e35a20447b14d15f71235ac9d3c1ecf39131f7964ed846bd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:57 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:52:57 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 02 May 2024 00:52:58 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:52:58 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:52:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:52:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:53:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:53:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:53:49 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:53:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:53:50 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:53:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:53:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:53:51 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 May 2024 00:53:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:53:51 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:53:51 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:53:51 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8dd6aa076fe85827f46df8b7cf6f7bc1b849b0804a4bd22f27595cf982cfe`  
		Last Modified: Thu, 02 May 2024 01:03:05 GMT  
		Size: 6.3 MB (6286683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b8f7a018d846c72bff254f148f3d9385d3265b2b7667e2571370c3886f8d1c`  
		Last Modified: Thu, 02 May 2024 01:03:03 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5032c9742ff624376ca7a290579ab0e72dc7cfb2902653ba72368c838542e881`  
		Last Modified: Thu, 02 May 2024 01:03:42 GMT  
		Size: 331.3 MB (331303499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92d947a16d69ff06e7d7f3854a51b6772f89c186e856d7d183443cada3cf515`  
		Last Modified: Thu, 02 May 2024 01:03:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc0dc23492d0cdb83d79b615ca2faeb18666a16fb1ceb73114aad7bd1c87d9d`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881cf5ab867f00075d058ea49cfbd1c4621399c7d0941edab77c165e9802e3aa`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bdf67406549d428ee8055a70abb8b9640918329ed9b6a144ba7a102b5e9c1c`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37229c0ded9e5f371cdbda1d0f510e70ea9a308f60e64075cdc8b40b2309b7c1`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8887bffb1c0d0e424d77c77bf7fe2195f0fe9bc9221da146c38356c7d55f99`  
		Last Modified: Thu, 02 May 2024 01:03:01 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.2.4` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:6fb3e3f26d0c44be19c4a06b8875ba7e5f751da9955efb7ff90118c934dfca43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346405276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fe4fb9ced9c98750469a71c3347991d4a6cf16c15da2f17058c9bbcafcb8f6`
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
# Thu, 25 Apr 2024 22:17:35 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4
# Thu, 25 Apr 2024 22:17:35 GMT
ARG CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:17:35 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:17:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:17:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:18:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=58d7299088933bb866af1faa917236abf226ef2c0cdbfaf789de124984f7a018            ;;          'amd64')            CB_SHA256=94ffff0e3f7d0b4dc5c227815ca76c3300d39cae491085f01ff8dbfa5bd98054            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:18:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:18:17 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:18:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 25 Apr 2024 22:18:18 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:18:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:18:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.2.4-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.4 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:18:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 25 Apr 2024 22:18:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:18:19 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:18:19 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:18:19 GMT
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
	-	`sha256:f6d3cadef398b30067970c4a9a98a9d25cb43ce59648df37c6f4f2628d420c51`  
		Last Modified: Thu, 25 Apr 2024 22:23:24 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9e72fd37f317985fbd2e50e39f4178e7c7073946b823d91a71d8e211e516c7`  
		Last Modified: Thu, 25 Apr 2024 22:23:51 GMT  
		Size: 313.1 MB (313082150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c859515bbe31c894885dbcbe8da04cd4db5e5ad50eb5fa8732030e0d6190e5a`  
		Last Modified: Thu, 25 Apr 2024 22:23:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9002c48188cc168da831617d05893204c46f5701644faf776aa74d04d802e2`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d2c686ffc07fa68487a93eb51eca25c8e817f3edfdca5bfc41bcc9e9750afd`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004c86d977cffc1ef2c3d0d31ba81f3d3667820838817476bf5a427bedefd1a`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e53aa1fb690498ac8a56d7a7dabd020013cd971d20e45ac0164c7c7a8543278`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329ae614dc0c88662e80836a8e7525b3206b2f0ad196b425c4400e84c7f0fd5a`  
		Last Modified: Thu, 25 Apr 2024 22:23:22 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.6.1`

```console
$ docker pull couchbase@sha256:815a8fd0928c1f90bf50f121ea0a6fe959b368dde3ff1b0ecdffb0617664587d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:community-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:4409fe452bd0f09896bd643caa9348866efd7f16ef836400659259ded14a5ed3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385922911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba4538475c73a983b81e32ca06d3eb5eaa96366a7e2c714e0e43fb050ff8266`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 02 May 2024 00:50:09 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:50:09 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:50:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:50:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:50:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:51:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:51:03 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:51:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:51:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:51:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:51:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:51:04 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:51:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:51:05 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:51:05 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:51:05 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1d895a9ccd79723ef218e92013b7c859cd0865602175c42c022764100e5977`  
		Last Modified: Thu, 02 May 2024 01:01:04 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775fab3933551288582afd00398e97e1bdb9496370e3b3c75ea1433da7bda763`  
		Last Modified: Thu, 02 May 2024 01:01:45 GMT  
		Size: 350.1 MB (350055423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95877db3c84c262e34faa0f16c49fbfba8fed61aeeb6ccae3e33735ccfd4d4a4`  
		Last Modified: Thu, 02 May 2024 01:01:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d957d3d8d22f60e326004c752faa6491e43fa8d295797720b9675d0325526bd`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01941898c6c7ff68d1d84b666c2f14d7cd3e0e8ba03a37742e21cf2ef85b2401`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42f9fb8b3c3bc5b068d20ef75e05b7b53e716c109f6e337287acec0118ed4d7`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81eb65fd47d5c3b74f15fe23baddabfb2a570037ffa02fc8ebad5f323e02cb3`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdb282a11f2bc3cfc146242214db5695bbaa2a8d33f2de4213485adf890e22e`  
		Last Modified: Thu, 02 May 2024 01:01:02 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:community-7.6.1` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:321081682d2dd3f30da647bfe29f8bdf5f2bb8cac70eb943236676293c8e0a39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372228414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2362af7280346c95a45d90d3ee7a7df4a12c612bc2318550ac84027de2ba94`
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
# Thu, 25 Apr 2024 22:15:20 GMT
ARG CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:15:20 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:15:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:15:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:16:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=abfd2a4d57c930be72d501af1e54612e06d9a73faf948df549c342252f1d3e49            ;;          'amd64')            CB_SHA256=c1e48a4175ed7f82532a1b2b858f0c2af08752ab83b4d084cb16d59f52437a82            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:16:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:16:09 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:16:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 22:16:10 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:16:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:16:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:16:11 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 22:16:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:16:11 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:16:11 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:16:11 GMT
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
	-	`sha256:8769e56c204167d9ec3e325378c22e88c63856fade0dbe4546fa3615c1e71625`  
		Last Modified: Thu, 25 Apr 2024 22:21:52 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5077d86e8a7a20418cd1313df06633a780c74ca0a6d16a4d5010deeefb9fb4`  
		Last Modified: Thu, 25 Apr 2024 22:22:21 GMT  
		Size: 333.6 MB (333592572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8cb4e2838abe8fe39f0bfcc2d4b22a7973b53519b4408acee6dff04016142`  
		Last Modified: Thu, 25 Apr 2024 22:21:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8563c40799b6df0e79a999ec46577596e49668b0331c327a604f1a969d628a4b`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8284de8fcd6f329d99b4012f148ec7e2c53eb2f93a4d9452b58af4d2df5c7961`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 728.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d400ca417a38741016ae22d6e3c335083f8c3a96e0400eb9b3a0ba7336808b0a`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a26477ca3cecf08c0a8bb6e8c837ae05f7af46c5624adde141fc8ed3d779fa`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801a691cd9dc3a030d7ed3df0c19c8b6ce0767512ad0a273c7ad90e74d798879`  
		Last Modified: Thu, 25 Apr 2024 22:21:50 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:8e26bc262eaf275ed690771e18d8f9fc74038a07348a9d5323bed4bfd28587e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:38835bf458d2e4cbd9f33bb5c83768f4b12a7a470472edafdc643b9846d355af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726131042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d2f219d1990a6054fe0461254d93ab09c4de6a2c28b013a0a02aac64574937`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:48:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:48:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:49:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:50:04 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:50:05 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:50:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:50:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:50:06 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:50:06 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:50:06 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:50:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07fe4b96ebd53fc3177bbf4e5dcd74de712e50af605f6cbe8e48cad098c2fa`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adbfd73fa263a825a5def76dbc07197afe07ec32046b17c124f323bea98d0ee`  
		Last Modified: Thu, 02 May 2024 01:00:42 GMT  
		Size: 690.3 MB (690263558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c902ef1c5b4700dd341c615e618428862dd09dba615028cdca3e1841622a3816`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cbd88266449594d449d3df784af9591bf9351ccead74fd9345562589878a01`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cb0fd953e14ef6bbcbf0065d63ccb47148e6fca30503a87f24a5e3d94820bf`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6db8ad5983e9cd0c5dfadb622d344e2a132668224b5d8ed85dce1c9b040faa`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269009594dc83f4f03ca1aab7f093cd70c34740c69bf51229f1ba64413d7184f`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2c6152d311d556d65512c14aae0a8bb0a02794fcf473ed63128c8fd9879173`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise` - linux; arm64 variant v8

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

## `couchbase:enterprise-7.0.5`

```console
$ docker pull couchbase@sha256:1d82ee796db11b14e6d837d342e75feace2e3bd6606054a5bcbdf106d1a9c11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:2bbb398e1612cb653c96ea62884e7428fcee41b996692cb68d0c240f18928bf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.7 MB (616705759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90d9a632b7eb69380052b904a26d1d199135be14929e4f8c5a1e828f4405df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:57 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea
# Thu, 02 May 2024 00:56:35 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:56:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:56:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:57:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:57:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:57:52 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:57:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:57:52 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:57:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:57:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.5 CB_SHA256=9a5ea4e5ec6e9af81b39d1e04b135fd5e8ce13a64cd9c8d587fe3e906c17cdea CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:57:53 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 May 2024 00:57:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:57:53 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:57:54 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:57:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8dd6aa076fe85827f46df8b7cf6f7bc1b849b0804a4bd22f27595cf982cfe`  
		Last Modified: Thu, 02 May 2024 01:03:05 GMT  
		Size: 6.3 MB (6286683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6d34b916b8f08df67bc384a8fb7a359a8b85bbaebd957a41dd74df8ced176e`  
		Last Modified: Thu, 02 May 2024 01:05:45 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ef2633700e8cad97ea2e148fca2ff1417373f7791e163d0a2d1f02f1d037e`  
		Last Modified: Thu, 02 May 2024 01:06:40 GMT  
		Size: 581.8 MB (581830398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0baf1edf757ddcc50711b161c3fae17e13996a416b264c8998d053aac9d48043`  
		Last Modified: Thu, 02 May 2024 01:05:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465ec6219d975fe2e0e263ef0966bb2ba8eef4c5a8fd41ce646600609f74112`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 748.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a868467492ba046b788aa80921321d9dcd93e8fc026a3f008bc369a85d45c`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f228ba0e4b631d523777873e40af72dab2b3b776a6407fc60560c81b8e4524`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946479679eab4d19ba434606dbd72d26a9923cb20306a9fec16da09e07f7aab1`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5ec88b827f3572e810554ca084cd32895104f028c8de24d2fa831861bc1606`  
		Last Modified: Thu, 02 May 2024 01:05:43 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.1.6`

```console
$ docker pull couchbase@sha256:161f9cf82cf82938abc7eb3a8e5b173c4b510610cfd71e2447bf33c30c5337ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.1.6` - linux; amd64

```console
$ docker pull couchbase@sha256:87e8cb2589b75cb82bb43f4c31766f1b040e2e67a75344ffa24dc76bb3496952
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.0 MB (652023721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc58fecfec0a8dbdf036476b9a70d6da5266b1ef9966b68c9d9fcbf0f83b948`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:57 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:53:57 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6
# Thu, 02 May 2024 00:53:57 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:53:57 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:53:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:53:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:55:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=d4462e7228c372f761bd83f96fa63a7211544df885c2d2e065202ff663dad6f9            ;;          'amd64')            CB_SHA256=abf410a1f97dd14171cd260d4abb853be003db5ec0a44c8324c846068eb90ce7            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:55:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:55:21 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:55:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 02 May 2024 00:55:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:55:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:55:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.6-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.6 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:55:23 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Thu, 02 May 2024 00:55:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:55:23 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:55:23 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:55:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d8dd6aa076fe85827f46df8b7cf6f7bc1b849b0804a4bd22f27595cf982cfe`  
		Last Modified: Thu, 02 May 2024 01:03:05 GMT  
		Size: 6.3 MB (6286683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c43fa9aebf73a4de5e8b208d659747cdcdbfa8528591a1158421364c049df`  
		Last Modified: Thu, 02 May 2024 01:03:55 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176b0250db94f20b5965d13ae83f0688f1778a6ad4e7226db3e0f507e906c260`  
		Last Modified: Thu, 02 May 2024 01:04:50 GMT  
		Size: 617.1 MB (617148379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6b3a143c9c8313585c28b4872f75ea144f02bc07a783edc5ad7af680390d8`  
		Last Modified: Thu, 02 May 2024 01:03:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b91b42a5d344a76df2aa58f98990c869d04775f59b75accf04c8cf78425c5`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed19e1f6275e70e29da75160b6c0b60cf534459826df7add422361171b21013`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962ae7b4cdf5d4f8cefc69fcf3cee7693c706bdb58b08ac79368149b9cc800f5`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417e301262691fe9e7681dd421f6dd26d30d22fcc701d36cba6e29163a01be60`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fbca79eaad8b6f442d83ecabc7927434c12023de5263cb04796f0f8c1aa764`  
		Last Modified: Thu, 02 May 2024 01:03:53 GMT  
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

## `couchbase:enterprise-7.2.5`

```console
$ docker pull couchbase@sha256:743df47b52499d3bbbc135206e73b0aa595ed0322af91f890844530d85c6f8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.2.5` - linux; amd64

```console
$ docker pull couchbase@sha256:5fb1362830f2325705d347714617b9059f3762c98ad29f18f572476eb6850154
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.2 MB (644222563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526a686305444f9add31d141101e54f1f516a32501ede0bdfc3c3624f2ac51f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:51:08 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 02 May 2024 00:51:08 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:51:08 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:51:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:51:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:52:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:52:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:52:35 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:52:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:52:35 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:52:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:52:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:52:36 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:52:37 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:52:37 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:52:37 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fe1c8b264cce2a50cc2191a2a9a0b46743e4cbabc88c479376b3247c059b6`  
		Last Modified: Thu, 02 May 2024 01:01:56 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0786a827daa92e8f4ce28d3d0a3d70bfd5a93d12265501e6be9f62d16523ec`  
		Last Modified: Thu, 02 May 2024 01:02:52 GMT  
		Size: 608.4 MB (608354761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e3957b7555f2824be552831594321a893f9ac15fdec2484d1a92bb9a6d7309`  
		Last Modified: Thu, 02 May 2024 01:01:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe6eca6e5b1f4d707198d97e747e5b2999d32f68e3330f8d3775f5bfad517e6`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9769fba8498429c111618a0b374867db0bcf3c07ef45c7ddfc87ff7cb2fa55aa`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b03c0f90253f7678d63197b3eb322b982ccc9d401b04cdf3e6eb92a7a4a1e2`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9225831271d5fef37f84f86781a8d35c221cfc050797350df6703e5815305fb3`  
		Last Modified: Thu, 02 May 2024 01:01:55 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e1ad589e668767251fd832e69fab89fdd1c4e4e8bd86e4b4b474ef970fd0f5`  
		Last Modified: Thu, 02 May 2024 01:01:54 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.2.5` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:d3493adad0fbf5d323ebef4b9cce2b8a0a2aab9477a0cdc297f60d9cb532cc6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624269628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5472f0e24a9896338d922653cb92f39f9fe82508e1d3b76d9c3cb3d5205bf394`
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
# Thu, 25 Apr 2024 22:16:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5
# Thu, 25 Apr 2024 22:16:18 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb
# Thu, 25 Apr 2024 22:16:18 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 25 Apr 2024 22:16:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 25 Apr 2024 22:16:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 25 Apr 2024 22:17:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=843d8aba87fa4740ff53d739f0b535a828a9f43a5276a0ec59c467f617e639df            ;;          'amd64')            CB_SHA256=f428b2ff390dd0421c12742aea0cacf9ebb63160d3c485ffec928997dc55a0cd            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 25 Apr 2024 22:17:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 25 Apr 2024 22:17:12 GMT
COPY file:3f4db0c2408bbc86ac8a83dadde3cc570eac180b99cd0ad6333dd7e75e14324c in /etc/service/couchbase-server/run 
# Thu, 25 Apr 2024 22:17:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 25 Apr 2024 22:17:13 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 25 Apr 2024 22:17:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 25 Apr 2024 22:17:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.2.5-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.2.5 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 25 Apr 2024 22:17:14 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 25 Apr 2024 22:17:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Apr 2024 22:17:14 GMT
CMD ["couchbase-server"]
# Thu, 25 Apr 2024 22:17:14 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 25 Apr 2024 22:17:14 GMT
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
	-	`sha256:13db1ba8ebb56791def7856b054fc58ab79100e2f7a25a5cabd5b18e72b54c20`  
		Last Modified: Thu, 25 Apr 2024 22:22:33 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e862e6c4fa7ce264e48e374cff2ff9eea9cad2861a5dd2e3c56048cbec3c8379`  
		Last Modified: Thu, 25 Apr 2024 22:23:14 GMT  
		Size: 585.6 MB (585633478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eebc4e958ba7ee39b88d44f0c2090d6454b3e4ee31cc52c2b7cf7753ae7203`  
		Last Modified: Thu, 25 Apr 2024 22:22:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a4b79491d157e91840b9b55c3c2aef862c10cf00250d29890bbb62cd7b6b08`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751c9e9265bb76033f6f99ea9a2457563de7d03104c219929d9fa993e6ddeeba`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d358891ae505783b80e36aa12656118d60a9372697e209ae9edb16c4734735fb`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae3cdabb3317dd841dbe1e010374157443facde122dce578a5fe2d476781da0`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d1f78b9579aaf82a0879b4292093bd0d926d91c898abaacbb75515df16bc61`  
		Last Modified: Thu, 25 Apr 2024 22:22:31 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.6.1`

```console
$ docker pull couchbase@sha256:8e26bc262eaf275ed690771e18d8f9fc74038a07348a9d5323bed4bfd28587e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:enterprise-7.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:38835bf458d2e4cbd9f33bb5c83768f4b12a7a470472edafdc643b9846d355af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726131042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d2f219d1990a6054fe0461254d93ab09c4de6a2c28b013a0a02aac64574937`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:48:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:48:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:49:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:50:04 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:50:05 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:50:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:50:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:50:06 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:50:06 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:50:06 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:50:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07fe4b96ebd53fc3177bbf4e5dcd74de712e50af605f6cbe8e48cad098c2fa`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adbfd73fa263a825a5def76dbc07197afe07ec32046b17c124f323bea98d0ee`  
		Last Modified: Thu, 02 May 2024 01:00:42 GMT  
		Size: 690.3 MB (690263558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c902ef1c5b4700dd341c615e618428862dd09dba615028cdca3e1841622a3816`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cbd88266449594d449d3df784af9591bf9351ccead74fd9345562589878a01`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cb0fd953e14ef6bbcbf0065d63ccb47148e6fca30503a87f24a5e3d94820bf`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6db8ad5983e9cd0c5dfadb622d344e2a132668224b5d8ed85dce1c9b040faa`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269009594dc83f4f03ca1aab7f093cd70c34740c69bf51229f1ba64413d7184f`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2c6152d311d556d65512c14aae0a8bb0a02794fcf473ed63128c8fd9879173`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchbase:enterprise-7.6.1` - linux; arm64 variant v8

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

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:8e26bc262eaf275ed690771e18d8f9fc74038a07348a9d5323bed4bfd28587e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:38835bf458d2e4cbd9f33bb5c83768f4b12a7a470472edafdc643b9846d355af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726131042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d2f219d1990a6054fe0461254d93ab09c4de6a2c28b013a0a02aac64574937`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 00:47:00 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 02 May 2024 00:47:00 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 02 May 2024 00:47:00 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:47:26 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND}
# Thu, 02 May 2024 00:48:31 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb
# Thu, 02 May 2024 00:48:31 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 02 May 2024 00:48:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 02 May 2024 00:48:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 02 May 2024 00:49:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=785f9d1f17ce6cde779f361adf0a0ed5f0bdaa78a1a4ab1c70b289d109b59709            ;;          'amd64')            CB_SHA256=12f1a671c28f12d946b9f39fb5cf7fe7c32e51fe30e0045d423b25627367be54            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 02 May 2024 00:50:04 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Thu, 02 May 2024 00:50:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise
# Thu, 02 May 2024 00:50:05 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 02 May 2024 00:50:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 02 May 2024 00:50:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.6.1-linux_@@ARCH@@.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.1 CB_SKIP_CHECKSUM=false CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Thu, 02 May 2024 00:50:06 GMT
COPY file:d33fbbdd0ce895d4e271d6bb86ac8fd83524ba267b4e2af7a862d4d466a732ba in / 
# Thu, 02 May 2024 00:50:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 May 2024 00:50:06 GMT
CMD ["couchbase-server"]
# Thu, 02 May 2024 00:50:06 GMT
EXPOSE 11207 11210 11280 18091 18092 18093 18094 18095 18096 18097 8091 8092 8093 8094 8095 8096 8097 9123
# Thu, 02 May 2024 00:50:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7039ce94a84a2dc1844011699cb97eb389dbf5833291fa86485ee87ca34b97`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 6.2 MB (6186248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12776822fa74481fc3ed725566afbd9a2d7ef07c65ce69d9316c541e6ddd625`  
		Last Modified: Thu, 02 May 2024 00:59:39 GMT  
		Size: 1.1 MB (1092194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07fe4b96ebd53fc3177bbf4e5dcd74de712e50af605f6cbe8e48cad098c2fa`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adbfd73fa263a825a5def76dbc07197afe07ec32046b17c124f323bea98d0ee`  
		Last Modified: Thu, 02 May 2024 01:00:42 GMT  
		Size: 690.3 MB (690263558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c902ef1c5b4700dd341c615e618428862dd09dba615028cdca3e1841622a3816`  
		Last Modified: Thu, 02 May 2024 00:59:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cbd88266449594d449d3df784af9591bf9351ccead74fd9345562589878a01`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cb0fd953e14ef6bbcbf0065d63ccb47148e6fca30503a87f24a5e3d94820bf`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6db8ad5983e9cd0c5dfadb622d344e2a132668224b5d8ed85dce1c9b040faa`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269009594dc83f4f03ca1aab7f093cd70c34740c69bf51229f1ba64413d7184f`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2c6152d311d556d65512c14aae0a8bb0a02794fcf473ed63128c8fd9879173`  
		Last Modified: Thu, 02 May 2024 00:59:36 GMT  
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
