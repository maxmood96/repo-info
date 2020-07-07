<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.5.1`](#couchbase651)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.5.1`](#couchbasecommunity-651)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.5.0`](#couchbaseenterprise-650)
-	[`couchbase:enterprise-6.5.1`](#couchbaseenterprise-651)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.5.1`

```console
$ docker pull couchbase@sha256:00512a2c71734c56e9d030d4f597c6492c23dce53a67af9e0b7fedf6a62124c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.5.1` - linux; amd64

```console
$ docker pull couchbase@sha256:a46ea3d6665ebd05bb0e69d573cccf15ea8f9dae61d5b09432b8138c5023d3c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515338711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8558296d6ab2cd70f82d248d092cfd414508bc35ac6957f370e2b30af1a8542`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:05:48 GMT
ARG CB_VERSION=6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66
# Tue, 07 Jul 2020 00:05:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:05:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:06:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:06:44 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:06:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:06:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:06:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:06:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:06:46 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:06:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:06:47 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:06:47 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:06:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ea011ae57cb06279eae6675423177a2de8d465637ef6509d65650ea69c5c8c`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2674567f79a2dd39fe8337f2828752cbf1b1877f3f9a359d0def3efe07a3ba80`  
		Last Modified: Tue, 07 Jul 2020 00:10:13 GMT  
		Size: 465.0 MB (465013145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b8605d612679f4e85e472820876451131383ae9b3db814068b2c5b26fe622f`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb8ebc86176e4d41a3dc0b70e4d8a46d2cebe65b686aa25b86e8b1b64b3aa5a`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33546706af73de9efb3cd7944da396e6caf2145aab8950980d8cacdef14dd525`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e850ef94972bc259aef0c336964ec90cb3827c50aff2ead3a0d4bca430a545fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff30952419971219f8991def47d455efbe53e64a56a261d485290a23c8f1e3fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 118.1 KB (118068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042d7117c7d6000c005d2cb0d0748a4d7397e42d52de8aa974accf0e139a9e0`  
		Last Modified: Tue, 07 Jul 2020 00:09:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:ad1fb4ecc05a946c7daa2fb8195d755d80f560efb5a894f87bef43d4905a6009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:2a72ed4cd149339b2abea5d6e942f74ddb9fee08d24f29f6ec9c6c0017efff0a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367316836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1447078b431571a3a963078dc5f935363ab87da0e51b5fdc3e6a6fad8e9b8bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:05:48 GMT
ARG CB_VERSION=6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Tue, 07 Jul 2020 00:08:15 GMT
ARG CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:08:16 GMT
ARG CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7
# Tue, 07 Jul 2020 00:08:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:08:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:08:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:09:00 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:09:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:09:01 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:09:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:09:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:09:02 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:09:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:09:03 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:09:03 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:09:03 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6430c537c9d9402277ec1ea2bef64d8fa70554fe380c4693d06d4f9c1bac14`  
		Last Modified: Tue, 07 Jul 2020 00:11:30 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a863251f3793d0dcd43c1ab640f3869f5c9c7cbc802683a5fc7fc5fb68a7fa`  
		Last Modified: Tue, 07 Jul 2020 00:12:10 GMT  
		Size: 317.0 MB (316991267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cd04e4ec3fa8e4bed5ad0a85154b5677cb1e4cd998d499bbbb3440a62cbe5`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794ae268873f00024a92032669c2632765f5d8652171d3aef1ba0d34b99ba785`  
		Last Modified: Tue, 07 Jul 2020 00:11:28 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037088a1c52a9b20783c8399d0e0724822bdf694a6f850cb6e74bd5c4872466c`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5087ce2ab30725ba61cec52d1ce39eabebf1ca3b38b0ac56e19043d78ec9a`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d596f5542dc4cadb1b934d4c65974bff73f3f3b88853a6fda69b7c612d2c0`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 118.1 KB (118067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484a36cec155ad683fff11ead3af2d4fba1127f16f0ec17822d0bb6539686a86`  
		Last Modified: Tue, 07 Jul 2020 00:11:28 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.5.1`

```console
$ docker pull couchbase@sha256:ad1fb4ecc05a946c7daa2fb8195d755d80f560efb5a894f87bef43d4905a6009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.5.1` - linux; amd64

```console
$ docker pull couchbase@sha256:2a72ed4cd149339b2abea5d6e942f74ddb9fee08d24f29f6ec9c6c0017efff0a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367316836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1447078b431571a3a963078dc5f935363ab87da0e51b5fdc3e6a6fad8e9b8bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:05:48 GMT
ARG CB_VERSION=6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Tue, 07 Jul 2020 00:08:15 GMT
ARG CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:08:16 GMT
ARG CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7
# Tue, 07 Jul 2020 00:08:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:08:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:08:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:09:00 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:09:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:09:01 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:09:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:09:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=baf65fb9cbcec87783d4e9c3ec067143a42cdeef13a884e1f917e8d2f14044b7 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:09:02 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:09:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:09:03 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:09:03 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:09:03 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6430c537c9d9402277ec1ea2bef64d8fa70554fe380c4693d06d4f9c1bac14`  
		Last Modified: Tue, 07 Jul 2020 00:11:30 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a863251f3793d0dcd43c1ab640f3869f5c9c7cbc802683a5fc7fc5fb68a7fa`  
		Last Modified: Tue, 07 Jul 2020 00:12:10 GMT  
		Size: 317.0 MB (316991267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613cd04e4ec3fa8e4bed5ad0a85154b5677cb1e4cd998d499bbbb3440a62cbe5`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794ae268873f00024a92032669c2632765f5d8652171d3aef1ba0d34b99ba785`  
		Last Modified: Tue, 07 Jul 2020 00:11:28 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037088a1c52a9b20783c8399d0e0724822bdf694a6f850cb6e74bd5c4872466c`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5087ce2ab30725ba61cec52d1ce39eabebf1ca3b38b0ac56e19043d78ec9a`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d596f5542dc4cadb1b934d4c65974bff73f3f3b88853a6fda69b7c612d2c0`  
		Last Modified: Tue, 07 Jul 2020 00:11:29 GMT  
		Size: 118.1 KB (118067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484a36cec155ad683fff11ead3af2d4fba1127f16f0ec17822d0bb6539686a86`  
		Last Modified: Tue, 07 Jul 2020 00:11:28 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:00512a2c71734c56e9d030d4f597c6492c23dce53a67af9e0b7fedf6a62124c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:a46ea3d6665ebd05bb0e69d573cccf15ea8f9dae61d5b09432b8138c5023d3c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515338711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8558296d6ab2cd70f82d248d092cfd414508bc35ac6957f370e2b30af1a8542`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:05:48 GMT
ARG CB_VERSION=6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66
# Tue, 07 Jul 2020 00:05:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:05:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:06:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:06:44 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:06:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:06:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:06:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:06:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:06:46 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:06:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:06:47 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:06:47 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:06:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ea011ae57cb06279eae6675423177a2de8d465637ef6509d65650ea69c5c8c`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2674567f79a2dd39fe8337f2828752cbf1b1877f3f9a359d0def3efe07a3ba80`  
		Last Modified: Tue, 07 Jul 2020 00:10:13 GMT  
		Size: 465.0 MB (465013145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b8605d612679f4e85e472820876451131383ae9b3db814068b2c5b26fe622f`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb8ebc86176e4d41a3dc0b70e4d8a46d2cebe65b686aa25b86e8b1b64b3aa5a`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33546706af73de9efb3cd7944da396e6caf2145aab8950980d8cacdef14dd525`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e850ef94972bc259aef0c336964ec90cb3827c50aff2ead3a0d4bca430a545fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff30952419971219f8991def47d455efbe53e64a56a261d485290a23c8f1e3fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 118.1 KB (118068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042d7117c7d6000c005d2cb0d0748a4d7397e42d52de8aa974accf0e139a9e0`  
		Last Modified: Tue, 07 Jul 2020 00:09:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.5.0`

```console
$ docker pull couchbase@sha256:73e45c99ba508e96d4ebfbe2ace4293713e2e60e3d5826d5dd76a43657123999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.5.0` - linux; amd64

```console
$ docker pull couchbase@sha256:3542f842e1e10f642d4521ab1bb32727de126a76559a07b8914be3bc0675471c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.1 MB (556131264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbacc9bbf56e9a18c8db2e01a554183c422d227d589004d8bfdea36c5222d5f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:06:59 GMT
ARG CB_VERSION=6.5.0
# Tue, 07 Jul 2020 00:06:59 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0
# Tue, 07 Jul 2020 00:06:59 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:07:00 GMT
ARG CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b
# Tue, 07 Jul 2020 00:07:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:07:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:08:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:08:05 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:08:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:08:06 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:08:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:08:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=5505c6bb026090dae7351e9d83caeab00437f19e48e826afd4cb6bafc484cd2b CB_VERSION=6.5.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:08:07 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:08:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:08:08 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:08:08 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:08:08 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f9c1b74d6b117b1e79352ee9544f0e1a8a8366e3ea91f70aadffa5971f7f5a`  
		Last Modified: Tue, 07 Jul 2020 00:10:25 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ab8168793703e3e669e2469ca7cdcc44726dac99c23b5c5a1da090900c9bd5`  
		Last Modified: Tue, 07 Jul 2020 00:11:24 GMT  
		Size: 505.8 MB (505805698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9335099703fa59686c3bc36fb231ee971d775c70fda9f48a6b4a37f60ebd0da0`  
		Last Modified: Tue, 07 Jul 2020 00:10:25 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7321a92efe02496bab93ce5245d0b58e2cd44e29249e64e7fa7786b29c079279`  
		Last Modified: Tue, 07 Jul 2020 00:10:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de550baef662e5cd241881f87275ee76fc3436e061652d2d30d8df471fc6374`  
		Last Modified: Tue, 07 Jul 2020 00:10:24 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18418b3061cb5e859c026d7d0afcf2039bd4a418d4654c23850c57696a1f159`  
		Last Modified: Tue, 07 Jul 2020 00:10:24 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76a970e9336fd97f29176e60cc4c30262aad30592eab29b5d9fd19aadff35cb`  
		Last Modified: Tue, 07 Jul 2020 00:10:24 GMT  
		Size: 118.1 KB (118067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b16da61a835d72d9a075c728929c9009e469dd2e423285d2abf625bd7cfe31`  
		Last Modified: Tue, 07 Jul 2020 00:10:24 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.5.1`

```console
$ docker pull couchbase@sha256:00512a2c71734c56e9d030d4f597c6492c23dce53a67af9e0b7fedf6a62124c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.5.1` - linux; amd64

```console
$ docker pull couchbase@sha256:a46ea3d6665ebd05bb0e69d573cccf15ea8f9dae61d5b09432b8138c5023d3c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515338711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8558296d6ab2cd70f82d248d092cfd414508bc35ac6957f370e2b30af1a8542`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:05:48 GMT
ARG CB_VERSION=6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66
# Tue, 07 Jul 2020 00:05:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:05:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:06:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:06:44 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:06:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:06:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:06:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:06:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:06:46 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:06:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:06:47 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:06:47 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:06:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ea011ae57cb06279eae6675423177a2de8d465637ef6509d65650ea69c5c8c`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2674567f79a2dd39fe8337f2828752cbf1b1877f3f9a359d0def3efe07a3ba80`  
		Last Modified: Tue, 07 Jul 2020 00:10:13 GMT  
		Size: 465.0 MB (465013145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b8605d612679f4e85e472820876451131383ae9b3db814068b2c5b26fe622f`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb8ebc86176e4d41a3dc0b70e4d8a46d2cebe65b686aa25b86e8b1b64b3aa5a`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33546706af73de9efb3cd7944da396e6caf2145aab8950980d8cacdef14dd525`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e850ef94972bc259aef0c336964ec90cb3827c50aff2ead3a0d4bca430a545fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff30952419971219f8991def47d455efbe53e64a56a261d485290a23c8f1e3fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 118.1 KB (118068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042d7117c7d6000c005d2cb0d0748a4d7397e42d52de8aa974accf0e139a9e0`  
		Last Modified: Tue, 07 Jul 2020 00:09:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:00512a2c71734c56e9d030d4f597c6492c23dce53a67af9e0b7fedf6a62124c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:a46ea3d6665ebd05bb0e69d573cccf15ea8f9dae61d5b09432b8138c5023d3c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.3 MB (515338711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8558296d6ab2cd70f82d248d092cfd414508bc35ac6957f370e2b30af1a8542`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jul 2020 21:57:02 GMT
ADD file:47805a69cb7dd669e357d291ce27735c2d514348468b2d3e69c66161a4f80abd in / 
# Mon, 06 Jul 2020 21:57:03 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 21:57:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:57:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:57:05 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:05:29 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 07 Jul 2020 00:05:48 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 07 Jul 2020 00:05:48 GMT
ARG CB_VERSION=6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb
# Tue, 07 Jul 2020 00:05:49 GMT
ARG CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66
# Tue, 07 Jul 2020 00:05:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 07 Jul 2020 00:05:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 07 Jul 2020 00:06:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 07 Jul 2020 00:06:44 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 07 Jul 2020 00:06:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chown -R couchbase:couchbase /etc/service
# Tue, 07 Jul 2020 00:06:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 07 Jul 2020 00:06:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 07 Jul 2020 00:06:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=80427193137e5cb5a4795b2675b1c450c1af8cf1a5c634d917f6c416f2047e66 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 07 Jul 2020 00:06:46 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 07 Jul 2020 00:06:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Jul 2020 00:06:47 GMT
CMD ["couchbase-server"]
# Tue, 07 Jul 2020 00:06:47 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 07 Jul 2020 00:06:47 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:6aa38bd67045d3ed7e7a73ca42e06fadbfd139a26693bf2dc8b9ccc318d87c3c`  
		Last Modified: Sat, 20 Jun 2020 13:20:13 GMT  
		Size: 44.4 MB (44374155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981ae4862c056451e69578c614f07a5b552995d3fc1cf17d5dc78a26e8455d5a`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bad8949dcb16a7693551042e056cef1e767ac0a23625a2eb9ae33ac44ac80f9`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9461589e708efab1c30577ec50f06db05714523e2976c7da421b0b418312e0`  
		Last Modified: Mon, 06 Jul 2020 21:57:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebedec0f7e959d19fb95ec05e13ccabd602c2e061c9aa8f416ccdacf87cb13e`  
		Last Modified: Tue, 07 Jul 2020 00:09:19 GMT  
		Size: 5.8 MB (5827589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ea011ae57cb06279eae6675423177a2de8d465637ef6509d65650ea69c5c8c`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2674567f79a2dd39fe8337f2828752cbf1b1877f3f9a359d0def3efe07a3ba80`  
		Last Modified: Tue, 07 Jul 2020 00:10:13 GMT  
		Size: 465.0 MB (465013145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b8605d612679f4e85e472820876451131383ae9b3db814068b2c5b26fe622f`  
		Last Modified: Tue, 07 Jul 2020 00:09:16 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb8ebc86176e4d41a3dc0b70e4d8a46d2cebe65b686aa25b86e8b1b64b3aa5a`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33546706af73de9efb3cd7944da396e6caf2145aab8950980d8cacdef14dd525`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e850ef94972bc259aef0c336964ec90cb3827c50aff2ead3a0d4bca430a545fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff30952419971219f8991def47d455efbe53e64a56a261d485290a23c8f1e3fd`  
		Last Modified: Tue, 07 Jul 2020 00:09:15 GMT  
		Size: 118.1 KB (118068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6042d7117c7d6000c005d2cb0d0748a4d7397e42d52de8aa974accf0e139a9e0`  
		Last Modified: Tue, 07 Jul 2020 00:09:14 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
