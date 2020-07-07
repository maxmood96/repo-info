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
