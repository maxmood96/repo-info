<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.5`](#couchbase605)
-	[`couchbase:6.6.1`](#couchbase661)
-	[`couchbase:7.0.0-beta`](#couchbase700-beta)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.0-beta`](#couchbasecommunity-700-beta)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.5`](#couchbaseenterprise-605)
-	[`couchbase:enterprise-6.6.1`](#couchbaseenterprise-661)
-	[`couchbase:enterprise-7.0.0-beta`](#couchbaseenterprise-700-beta)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.5`

```console
$ docker pull couchbase@sha256:518d939db1b7aeb3ba35bd967c58fe79e8b9491e51dfbfd96a181de7577a6670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:665afb55b0c91ddabcf0e8badba0163dc971452bdcbece94e2bd7fccf457b143
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.0 MB (481042612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa58b0dace013adb2608824255c2d84ab06d1346455890215c5e9129f2dd4bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:12:05 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:12:07 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_VERSION=6.0.5
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a
# Thu, 21 Jan 2021 08:12:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:12:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:12:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:12:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:12:57 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:12:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:12:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:12:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:13:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:13:01 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:13:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:13:01 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:13:01 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:13:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca990adc1b7f73c4f8065a18dd12b134b9c8027cabdb9f99fd222413221f0e3`  
		Last Modified: Thu, 21 Jan 2021 08:18:44 GMT  
		Size: 14.3 MB (14311792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1fa59f2b88fd7e407119bafaa30702f3159a50bcbba1a4268e14934e189558`  
		Last Modified: Thu, 21 Jan 2021 08:18:39 GMT  
		Size: 2.1 KB (2073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94213fdcb82847117c08a250f705e5b83a6f9d400e9cc50ef1ef0fb4e7690ac`  
		Last Modified: Thu, 21 Jan 2021 08:19:29 GMT  
		Size: 420.6 MB (420641935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9210fbe2501f1b0c0e4d750805eaf10fb0738c6204b87ea70fd3fe6704d7f6`  
		Last Modified: Thu, 21 Jan 2021 08:18:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f0a4a6e34d6a68f75fd859d23071d281cf75e379b8aeabf309385363fe246`  
		Last Modified: Thu, 21 Jan 2021 08:18:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0defd54281e80a16b9cec6054f29075e29fee17bc711832381363132d1494ff3`  
		Last Modified: Thu, 21 Jan 2021 08:18:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810a014f170d98767a3f8265bf545c104ac56a0399f3c59c0437cf8dacc353bc`  
		Last Modified: Thu, 21 Jan 2021 08:18:36 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785ca61252fc0dd56057218327246b036d1f63817786f335a4693659715620f9`  
		Last Modified: Thu, 21 Jan 2021 08:18:36 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a71f10158af8c705e2d95a02e194850a438b0d154a6b374b038c816fb7a8a3d`  
		Last Modified: Thu, 21 Jan 2021 08:18:38 GMT  
		Size: 120.6 KB (120599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e096983578a2a5faf7c1dc22d459d0cd4bddcd650e3ac54a9d7479ae86733a0d`  
		Last Modified: Thu, 21 Jan 2021 08:18:36 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.6.1`

```console
$ docker pull couchbase@sha256:8a0bc6ad73b5eff52b094e0f59a6f0b8adb35e7a527b2248d950c4238a1f669c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:980ea727964bbba97ae1ff953b00b115f7250b442d7de9b4da37b5f36c215c62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544428626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a2e9a583022cd20ff9124b1932bb9f8bdab6f81b83ef6d023c668b14bfe66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:09:18 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:09:19 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_VERSION=6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:09:20 GMT
ARG CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9
# Thu, 21 Jan 2021 08:09:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:09:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:10:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:10:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:10:21 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:10:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:10:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:10:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:10:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:10:24 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:10:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:10:25 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:10:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:10:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f637e8d8fd3a8af409688314ce45335bbe0cd39a99fb995180ace08b1ee3f429`  
		Last Modified: Thu, 21 Jan 2021 08:16:21 GMT  
		Size: 5.8 MB (5840064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19d0547a7d9c15a315e7734bcfb1f2c660f1ef0de74dd376c474957d5233ed0`  
		Last Modified: Thu, 21 Jan 2021 08:16:18 GMT  
		Size: 2.1 KB (2072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46afd66269256f287828136b42271b8d8e632259a709d50efeed3e10ffd976`  
		Last Modified: Thu, 21 Jan 2021 08:17:19 GMT  
		Size: 492.5 MB (492502200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd481437c5458144fa54b40e4252921fcaf7ead0e743a13f72ca9ab2c9bc2a`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030e43d181141e4a7a947dfb094dc7b4326e3af7869b9f2537aa4a8f9ace325`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1052706563146cd4cc4810eccce97bc50a925dcb9386dfbf5ae79632d949fc7`  
		Last Modified: Thu, 21 Jan 2021 08:16:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab398a3c21f9447e1b5d15e92f5b6a2e061525597f4d18fe44a1a0188067310`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5905df6369e77fad5b7e7a5f2e8a8e1d83c2f6805dd653f6e1a44f293bb554c`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1575ba367cde5884383b921f9ea272d75c045997d5454c29916c8e97eebae034`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db1033b73fbe7789a655b6cc51d7888f75df57f84ad00ca2bba3f4cf884ac3`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.0.0-beta`

```console
$ docker pull couchbase@sha256:137ed4d0ab3e8b48cf52210e606c35c7078ae2304d0b17133834cf6685673118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:f290418dfbb8bb18a93d80c56a4d8cf335e706059c812c19febdd34ae3be9d2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.8 MB (625802888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81229b5e7efae08fe2f497e3c2b04607daf4c65c7dec622871c7faedcb8efe16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:55:03 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 04 Mar 2021 03:55:22 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Mar 2021 03:55:23 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7
# Thu, 04 Mar 2021 03:55:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 04 Mar 2021 03:55:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 04 Mar 2021 03:56:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 04 Mar 2021 03:56:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 04 Mar 2021 03:56:37 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 04 Mar 2021 03:56:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Thu, 04 Mar 2021 03:56:38 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 04 Mar 2021 03:56:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 04 Mar 2021 03:56:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 04 Mar 2021 03:56:44 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 04 Mar 2021 03:56:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Mar 2021 03:56:48 GMT
CMD ["couchbase-server"]
# Thu, 04 Mar 2021 03:56:50 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 04 Mar 2021 03:56:51 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9554fabf446c196bafd3140fe0a097c18e9f37bbaf3cb5b15933313d851455`  
		Last Modified: Thu, 04 Mar 2021 03:58:33 GMT  
		Size: 6.3 MB (6270368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35028997dc022a748113806b8b124d8026bb6fe05278a69d0f4f0015edeff0`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52190f9432bfa5f86fec6d84560c1a00e635b5c4ddc357b392b848c487beda70`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca17a6d8691d6dbce05c5597a9a28cf7b262d4b7325449276fb701547c000cc4`  
		Last Modified: Thu, 04 Mar 2021 03:59:48 GMT  
		Size: 590.8 MB (590833622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93fbbd8f703d2cfcb1671d66ef027c3240a241ad815629bf8c14ac1b802c913`  
		Last Modified: Thu, 04 Mar 2021 03:58:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3946a6540abba50167ad3a92f2b7f6ecfd217411c45916a3b67b91f125db6d83`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b315bdf4bd4b1f1d06ee10a1b91fce631147bdc93d1f26ff637cf2ef909d0f`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbb6f862af83ce02eefe8125adc2d8904d375a7051c7d5250c4c38b24731639`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6a68f582c55860429b87c573a4af0d426d9353679344cb622a391dede7d8be`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f908e76063212315e2474fa92c7bdfc210219a6fa9017f3dcca5673f1da86`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0288da769d9f7bb0a120492f2bc134aa57056f9e563ef3563434c2cf5edffb2f`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:93f1cea7179efde8932f265a7ebc8bc2f03105f12cab872da79c05c723a738cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:af374096873a6bb15a40e0ebecaef4a1c5a7c30d24a57fb93afa943b1facd2c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371499367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3664a45f58939c2d5de81046aa79f5e5ffcee3ae89e4482d76d7acbfa810b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:09:18 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:09:19 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_VERSION=6.6.0
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e
# Thu, 21 Jan 2021 08:10:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:10:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:11:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:11:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:11:27 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:11:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:11:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:11:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:11:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:11:30 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:11:30 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:11:31 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:11:31 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f637e8d8fd3a8af409688314ce45335bbe0cd39a99fb995180ace08b1ee3f429`  
		Last Modified: Thu, 21 Jan 2021 08:16:21 GMT  
		Size: 5.8 MB (5840064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683580b86dd631ba8a80569913bbe6184224a29c9a824dc554d0ce25c8d61e0d`  
		Last Modified: Thu, 21 Jan 2021 08:17:33 GMT  
		Size: 2.1 KB (2073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0d24dad4cf9c8adc6743942e76dd208ef196ba376a9dd665cc45a3502b5fdf`  
		Last Modified: Thu, 21 Jan 2021 08:18:16 GMT  
		Size: 319.6 MB (319572942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ca2d76ef97156c0803a0266e739fcd6b2b63b807c0e4a2c5b7ec7c84025132`  
		Last Modified: Thu, 21 Jan 2021 08:17:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361265e2f4fc8a564543cda01f2f6b63c96c60e5fb3cc679cbe1df4e7dc6dc98`  
		Last Modified: Thu, 21 Jan 2021 08:17:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbf41debb2660eb80b3b76c45d9b58f9ae04c9549eb8f76a3187970ec0e30b3`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9664fe5cec72cf7fa6c18112609705ddb261a514388116d8e37df2118a835`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88710f42f376fd0326b8f54154fcb85f36f0b02688eab22f40e8d53b7da52760`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9895962c5436f2180dcff44943ba7ac818c84697ba2584c742b4f676c56d4db`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 118.1 KB (118073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85f7c340f5382d3e3b5727a432066989161d05fdf2edc5ee11f28b9ab9ee8df`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:93f1cea7179efde8932f265a7ebc8bc2f03105f12cab872da79c05c723a738cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:af374096873a6bb15a40e0ebecaef4a1c5a7c30d24a57fb93afa943b1facd2c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371499367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3664a45f58939c2d5de81046aa79f5e5ffcee3ae89e4482d76d7acbfa810b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:09:18 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:09:19 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_VERSION=6.6.0
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:10:39 GMT
ARG CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e
# Thu, 21 Jan 2021 08:10:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:10:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:11:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:11:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:11:27 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:11:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:11:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:11:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:11:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=19ba0f8ac60fd63226c45674c3d113a91a0e9168787b38df59fec5e98d11257e CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:11:30 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:11:30 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:11:31 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:11:31 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f637e8d8fd3a8af409688314ce45335bbe0cd39a99fb995180ace08b1ee3f429`  
		Last Modified: Thu, 21 Jan 2021 08:16:21 GMT  
		Size: 5.8 MB (5840064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683580b86dd631ba8a80569913bbe6184224a29c9a824dc554d0ce25c8d61e0d`  
		Last Modified: Thu, 21 Jan 2021 08:17:33 GMT  
		Size: 2.1 KB (2073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0d24dad4cf9c8adc6743942e76dd208ef196ba376a9dd665cc45a3502b5fdf`  
		Last Modified: Thu, 21 Jan 2021 08:18:16 GMT  
		Size: 319.6 MB (319572942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ca2d76ef97156c0803a0266e739fcd6b2b63b807c0e4a2c5b7ec7c84025132`  
		Last Modified: Thu, 21 Jan 2021 08:17:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361265e2f4fc8a564543cda01f2f6b63c96c60e5fb3cc679cbe1df4e7dc6dc98`  
		Last Modified: Thu, 21 Jan 2021 08:17:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbf41debb2660eb80b3b76c45d9b58f9ae04c9549eb8f76a3187970ec0e30b3`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f9664fe5cec72cf7fa6c18112609705ddb261a514388116d8e37df2118a835`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88710f42f376fd0326b8f54154fcb85f36f0b02688eab22f40e8d53b7da52760`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9895962c5436f2180dcff44943ba7ac818c84697ba2584c742b4f676c56d4db`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 118.1 KB (118073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85f7c340f5382d3e3b5727a432066989161d05fdf2edc5ee11f28b9ab9ee8df`  
		Last Modified: Thu, 21 Jan 2021 08:17:31 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.0-beta`

```console
$ docker pull couchbase@sha256:a2bc32811725b7fe540f5642d53d748a79c1dc6553c94cfbf3293b432a87b1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:85faac87565b6a7df0ca725d5dc45ba970242ed74c41ff8fdbaa20ff66de0584
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431741040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed049ca0440cb6b0a8291d4acba995fae9f9c60f7bb0e450b402834f961f07f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:55:03 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 04 Mar 2021 03:55:22 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Mar 2021 03:55:23 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 04 Mar 2021 03:57:05 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 04 Mar 2021 03:57:05 GMT
ARG CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991
# Thu, 04 Mar 2021 03:57:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 04 Mar 2021 03:57:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 04 Mar 2021 03:57:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 04 Mar 2021 03:57:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 04 Mar 2021 03:57:57 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 04 Mar 2021 03:57:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Thu, 04 Mar 2021 03:57:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 04 Mar 2021 03:57:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 04 Mar 2021 03:58:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=5ea728ef6c8ba24a63cfd04cd459a3dccc5ae5dcdabf352ac9ee5c1f9526f991 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 04 Mar 2021 03:58:01 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 04 Mar 2021 03:58:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Mar 2021 03:58:01 GMT
CMD ["couchbase-server"]
# Thu, 04 Mar 2021 03:58:01 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 04 Mar 2021 03:58:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9554fabf446c196bafd3140fe0a097c18e9f37bbaf3cb5b15933313d851455`  
		Last Modified: Thu, 04 Mar 2021 03:58:33 GMT  
		Size: 6.3 MB (6270368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35028997dc022a748113806b8b124d8026bb6fe05278a69d0f4f0015edeff0`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac97cfd68ae5267152e20902e4cc08fa0717ad00023059759d04a81af279fde5`  
		Last Modified: Thu, 04 Mar 2021 03:59:58 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a132f9a6b823c1a7298bc813eefe6858742665e722f384cc106b9ced210549ec`  
		Last Modified: Thu, 04 Mar 2021 04:00:50 GMT  
		Size: 396.8 MB (396771769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bb4ac087debbc196fe9531123ae5cfaa58f0abbd4923fbb9f506201178363d`  
		Last Modified: Thu, 04 Mar 2021 03:59:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3b1e50b5d32bdb9a826a6da1fc2a553db224cab0f088fc3e096b7f3c5e1395`  
		Last Modified: Thu, 04 Mar 2021 03:59:57 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127f54f45844b254ee4b8a4496a68364e81866eff9002bd3a65f6b224409d48`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211844bc0f5dfba158ec00b9c77f62f911b2d0a6b18c75d7f68dcead78c56672`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f31c9d95a167db27a0c5180e439073278e0717592c2cc9ad0567bc98bfaed9`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f9621f558fe62fdc941b899732dd67a87a527511c095c3bd3805d166580598`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 125.9 KB (125893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b80e85638811db6df49794e05278d4a21ad0d91cd6d5f33ac225b54570e247`  
		Last Modified: Thu, 04 Mar 2021 03:59:56 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:8a0bc6ad73b5eff52b094e0f59a6f0b8adb35e7a527b2248d950c4238a1f669c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:980ea727964bbba97ae1ff953b00b115f7250b442d7de9b4da37b5f36c215c62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544428626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a2e9a583022cd20ff9124b1932bb9f8bdab6f81b83ef6d023c668b14bfe66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:09:18 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:09:19 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_VERSION=6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:09:20 GMT
ARG CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9
# Thu, 21 Jan 2021 08:09:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:09:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:10:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:10:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:10:21 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:10:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:10:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:10:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:10:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:10:24 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:10:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:10:25 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:10:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:10:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f637e8d8fd3a8af409688314ce45335bbe0cd39a99fb995180ace08b1ee3f429`  
		Last Modified: Thu, 21 Jan 2021 08:16:21 GMT  
		Size: 5.8 MB (5840064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19d0547a7d9c15a315e7734bcfb1f2c660f1ef0de74dd376c474957d5233ed0`  
		Last Modified: Thu, 21 Jan 2021 08:16:18 GMT  
		Size: 2.1 KB (2072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46afd66269256f287828136b42271b8d8e632259a709d50efeed3e10ffd976`  
		Last Modified: Thu, 21 Jan 2021 08:17:19 GMT  
		Size: 492.5 MB (492502200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd481437c5458144fa54b40e4252921fcaf7ead0e743a13f72ca9ab2c9bc2a`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030e43d181141e4a7a947dfb094dc7b4326e3af7869b9f2537aa4a8f9ace325`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1052706563146cd4cc4810eccce97bc50a925dcb9386dfbf5ae79632d949fc7`  
		Last Modified: Thu, 21 Jan 2021 08:16:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab398a3c21f9447e1b5d15e92f5b6a2e061525597f4d18fe44a1a0188067310`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5905df6369e77fad5b7e7a5f2e8a8e1d83c2f6805dd653f6e1a44f293bb554c`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1575ba367cde5884383b921f9ea272d75c045997d5454c29916c8e97eebae034`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db1033b73fbe7789a655b6cc51d7888f75df57f84ad00ca2bba3f4cf884ac3`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:518d939db1b7aeb3ba35bd967c58fe79e8b9491e51dfbfd96a181de7577a6670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:665afb55b0c91ddabcf0e8badba0163dc971452bdcbece94e2bd7fccf457b143
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.0 MB (481042612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa58b0dace013adb2608824255c2d84ab06d1346455890215c5e9129f2dd4bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:12:05 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:12:07 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_VERSION=6.0.5
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:12:07 GMT
ARG CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a
# Thu, 21 Jan 2021 08:12:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:12:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:12:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:12:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:12:57 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:12:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:12:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:12:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:13:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=3227bd9bf04affeea6c567a9e87cde585d2d49e5548b95204ffbda7dea8d451a CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:13:01 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:13:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:13:01 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:13:01 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:13:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca990adc1b7f73c4f8065a18dd12b134b9c8027cabdb9f99fd222413221f0e3`  
		Last Modified: Thu, 21 Jan 2021 08:18:44 GMT  
		Size: 14.3 MB (14311792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1fa59f2b88fd7e407119bafaa30702f3159a50bcbba1a4268e14934e189558`  
		Last Modified: Thu, 21 Jan 2021 08:18:39 GMT  
		Size: 2.1 KB (2073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94213fdcb82847117c08a250f705e5b83a6f9d400e9cc50ef1ef0fb4e7690ac`  
		Last Modified: Thu, 21 Jan 2021 08:19:29 GMT  
		Size: 420.6 MB (420641935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9210fbe2501f1b0c0e4d750805eaf10fb0738c6204b87ea70fd3fe6704d7f6`  
		Last Modified: Thu, 21 Jan 2021 08:18:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89f0a4a6e34d6a68f75fd859d23071d281cf75e379b8aeabf309385363fe246`  
		Last Modified: Thu, 21 Jan 2021 08:18:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0defd54281e80a16b9cec6054f29075e29fee17bc711832381363132d1494ff3`  
		Last Modified: Thu, 21 Jan 2021 08:18:38 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810a014f170d98767a3f8265bf545c104ac56a0399f3c59c0437cf8dacc353bc`  
		Last Modified: Thu, 21 Jan 2021 08:18:36 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785ca61252fc0dd56057218327246b036d1f63817786f335a4693659715620f9`  
		Last Modified: Thu, 21 Jan 2021 08:18:36 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a71f10158af8c705e2d95a02e194850a438b0d154a6b374b038c816fb7a8a3d`  
		Last Modified: Thu, 21 Jan 2021 08:18:38 GMT  
		Size: 120.6 KB (120599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e096983578a2a5faf7c1dc22d459d0cd4bddcd650e3ac54a9d7479ae86733a0d`  
		Last Modified: Thu, 21 Jan 2021 08:18:36 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.6.1`

```console
$ docker pull couchbase@sha256:8a0bc6ad73b5eff52b094e0f59a6f0b8adb35e7a527b2248d950c4238a1f669c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:980ea727964bbba97ae1ff953b00b115f7250b442d7de9b4da37b5f36c215c62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544428626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a2e9a583022cd20ff9124b1932bb9f8bdab6f81b83ef6d023c668b14bfe66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:09:18 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:09:19 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_VERSION=6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:09:20 GMT
ARG CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9
# Thu, 21 Jan 2021 08:09:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:09:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:10:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:10:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:10:21 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:10:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:10:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:10:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:10:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:10:24 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:10:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:10:25 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:10:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:10:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f637e8d8fd3a8af409688314ce45335bbe0cd39a99fb995180ace08b1ee3f429`  
		Last Modified: Thu, 21 Jan 2021 08:16:21 GMT  
		Size: 5.8 MB (5840064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19d0547a7d9c15a315e7734bcfb1f2c660f1ef0de74dd376c474957d5233ed0`  
		Last Modified: Thu, 21 Jan 2021 08:16:18 GMT  
		Size: 2.1 KB (2072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46afd66269256f287828136b42271b8d8e632259a709d50efeed3e10ffd976`  
		Last Modified: Thu, 21 Jan 2021 08:17:19 GMT  
		Size: 492.5 MB (492502200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd481437c5458144fa54b40e4252921fcaf7ead0e743a13f72ca9ab2c9bc2a`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030e43d181141e4a7a947dfb094dc7b4326e3af7869b9f2537aa4a8f9ace325`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1052706563146cd4cc4810eccce97bc50a925dcb9386dfbf5ae79632d949fc7`  
		Last Modified: Thu, 21 Jan 2021 08:16:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab398a3c21f9447e1b5d15e92f5b6a2e061525597f4d18fe44a1a0188067310`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5905df6369e77fad5b7e7a5f2e8a8e1d83c2f6805dd653f6e1a44f293bb554c`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1575ba367cde5884383b921f9ea272d75c045997d5454c29916c8e97eebae034`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db1033b73fbe7789a655b6cc51d7888f75df57f84ad00ca2bba3f4cf884ac3`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.0-beta`

```console
$ docker pull couchbase@sha256:137ed4d0ab3e8b48cf52210e606c35c7078ae2304d0b17133834cf6685673118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:f290418dfbb8bb18a93d80c56a4d8cf335e706059c812c19febdd34ae3be9d2c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.8 MB (625802888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81229b5e7efae08fe2f497e3c2b04607daf4c65c7dec622871c7faedcb8efe16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 03:55:03 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 04 Mar 2021 03:55:22 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Mar 2021 03:55:23 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 04 Mar 2021 03:55:23 GMT
ARG CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7
# Thu, 04 Mar 2021 03:55:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 04 Mar 2021 03:55:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 04 Mar 2021 03:56:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 04 Mar 2021 03:56:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 04 Mar 2021 03:56:37 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 04 Mar 2021 03:56:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Thu, 04 Mar 2021 03:56:38 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 04 Mar 2021 03:56:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 04 Mar 2021 03:56:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=611b7fad89d6be1bef93dff7635fa2cc861f433568b738b5423dd08c862aaaa7 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 04 Mar 2021 03:56:44 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 04 Mar 2021 03:56:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Mar 2021 03:56:48 GMT
CMD ["couchbase-server"]
# Thu, 04 Mar 2021 03:56:50 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 04 Mar 2021 03:56:51 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9554fabf446c196bafd3140fe0a097c18e9f37bbaf3cb5b15933313d851455`  
		Last Modified: Thu, 04 Mar 2021 03:58:33 GMT  
		Size: 6.3 MB (6270368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35028997dc022a748113806b8b124d8026bb6fe05278a69d0f4f0015edeff0`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52190f9432bfa5f86fec6d84560c1a00e635b5c4ddc357b392b848c487beda70`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca17a6d8691d6dbce05c5597a9a28cf7b262d4b7325449276fb701547c000cc4`  
		Last Modified: Thu, 04 Mar 2021 03:59:48 GMT  
		Size: 590.8 MB (590833622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93fbbd8f703d2cfcb1671d66ef027c3240a241ad815629bf8c14ac1b802c913`  
		Last Modified: Thu, 04 Mar 2021 03:58:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3946a6540abba50167ad3a92f2b7f6ecfd217411c45916a3b67b91f125db6d83`  
		Last Modified: Thu, 04 Mar 2021 03:58:31 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b315bdf4bd4b1f1d06ee10a1b91fce631147bdc93d1f26ff637cf2ef909d0f`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbb6f862af83ce02eefe8125adc2d8904d375a7051c7d5250c4c38b24731639`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6a68f582c55860429b87c573a4af0d426d9353679344cb622a391dede7d8be`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f908e76063212315e2474fa92c7bdfc210219a6fa9017f3dcca5673f1da86`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0288da769d9f7bb0a120492f2bc134aa57056f9e563ef3563434c2cf5edffb2f`  
		Last Modified: Thu, 04 Mar 2021 03:58:30 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:8a0bc6ad73b5eff52b094e0f59a6f0b8adb35e7a527b2248d950c4238a1f669c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:980ea727964bbba97ae1ff953b00b115f7250b442d7de9b4da37b5f36c215c62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.4 MB (544428626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a2e9a583022cd20ff9124b1932bb9f8bdab6f81b83ef6d023c668b14bfe66f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:08:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 21 Jan 2021 08:09:18 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 21 Jan 2021 08:09:19 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_VERSION=6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1
# Thu, 21 Jan 2021 08:09:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb
# Thu, 21 Jan 2021 08:09:20 GMT
ARG CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9
# Thu, 21 Jan 2021 08:09:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 21 Jan 2021 08:09:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 21 Jan 2021 08:10:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 21 Jan 2021 08:10:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 21 Jan 2021 08:10:21 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 21 Jan 2021 08:10:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chown -R couchbase:couchbase /etc/service
# Thu, 21 Jan 2021 08:10:22 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 21 Jan 2021 08:10:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 21 Jan 2021 08:10:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=247ed50de608c5fa121e4f2749d710e94c370e75c599f51e12e24b2910c6d9c9 CB_VERSION=6.6.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 21 Jan 2021 08:10:24 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 21 Jan 2021 08:10:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Jan 2021 08:10:25 GMT
CMD ["couchbase-server"]
# Thu, 21 Jan 2021 08:10:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 21 Jan 2021 08:10:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f637e8d8fd3a8af409688314ce45335bbe0cd39a99fb995180ace08b1ee3f429`  
		Last Modified: Thu, 21 Jan 2021 08:16:21 GMT  
		Size: 5.8 MB (5840064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19d0547a7d9c15a315e7734bcfb1f2c660f1ef0de74dd376c474957d5233ed0`  
		Last Modified: Thu, 21 Jan 2021 08:16:18 GMT  
		Size: 2.1 KB (2072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46afd66269256f287828136b42271b8d8e632259a709d50efeed3e10ffd976`  
		Last Modified: Thu, 21 Jan 2021 08:17:19 GMT  
		Size: 492.5 MB (492502200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd481437c5458144fa54b40e4252921fcaf7ead0e743a13f72ca9ab2c9bc2a`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030e43d181141e4a7a947dfb094dc7b4326e3af7869b9f2537aa4a8f9ace325`  
		Last Modified: Thu, 21 Jan 2021 08:16:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1052706563146cd4cc4810eccce97bc50a925dcb9386dfbf5ae79632d949fc7`  
		Last Modified: Thu, 21 Jan 2021 08:16:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab398a3c21f9447e1b5d15e92f5b6a2e061525597f4d18fe44a1a0188067310`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5905df6369e77fad5b7e7a5f2e8a8e1d83c2f6805dd653f6e1a44f293bb554c`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1575ba367cde5884383b921f9ea272d75c045997d5454c29916c8e97eebae034`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 118.1 KB (118074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1db1033b73fbe7789a655b6cc51d7888f75df57f84ad00ca2bba3f4cf884ac3`  
		Last Modified: Thu, 21 Jan 2021 08:16:15 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
