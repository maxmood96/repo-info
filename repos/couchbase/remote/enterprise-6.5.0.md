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
