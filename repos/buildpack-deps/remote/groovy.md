## `buildpack-deps:groovy`

```console
$ docker pull buildpack-deps@sha256:809308b484357061c659749cad159b14febdd48285c215c6d02c5d418b53f151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1e34730d0a550f41d2feaa453eb656a6de0d622dfa132ef96127818fd03db774
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244551245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a14461d832f5045285939ca3ba06f6461510e40fe18a96b754fc23ae44634b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 17:32:46 GMT
ADD file:6099585856c27a9f8dd40d7e679184a6d1bb58133acf73d5d3c9904932def005 in / 
# Fri, 23 Oct 2020 17:32:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 17:32:47 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 17:32:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 17:32:48 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 18:01:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:01:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Oct 2020 18:02:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 18:03:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a14fb4cd302ea60d4b208f17bb50098b52a17183a2137c08299a3b915d7cbae`  
		Last Modified: Fri, 23 Oct 2020 17:33:40 GMT  
		Size: 31.3 MB (31337938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b1fecc905c746712dc231f73c5d630927892af991ce140673eb77dd9b697cd`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac8019c9736cea870759cf87bf752344fd3fb2dbf7a3921e9c60e140213900`  
		Last Modified: Fri, 23 Oct 2020 17:33:35 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b137add616873c756cd3a60d7de3e8ac2ad471a32a8d7e7fba112082ac32f5`  
		Last Modified: Fri, 23 Oct 2020 18:08:23 GMT  
		Size: 4.5 MB (4515029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9baeffa76ee358acf2e9423b3bd03ff13ef4361cda101c57242f87268fc7e`  
		Last Modified: Fri, 23 Oct 2020 18:08:24 GMT  
		Size: 3.6 MB (3587545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9a37c16661daea48912319bcac62ebc465498b050a168b140e35fdedb5ab5e`  
		Last Modified: Fri, 23 Oct 2020 18:08:42 GMT  
		Size: 55.0 MB (55013337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b4316385454a48bc9998e88339aef9ecbe25ba68206d852d936820329727c4`  
		Last Modified: Fri, 23 Oct 2020 18:09:19 GMT  
		Size: 150.1 MB (150096389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:34afc1ba5c29024124f3fd4b43884f892679ce394a5e13b994e31d5167f62ffd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208984438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21dcfa2a71e5887a35038f01008ddaa090b70a1579fc9b10465395e959a26c58`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 23:00:02 GMT
ADD file:064c9cf96cc5a27a93d36df3f2590769d18b7ce2870d6fcfc9dc92137a6565b7 in / 
# Wed, 25 Nov 2020 23:00:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 23:00:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 23:00:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 23:00:10 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:47:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:47:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 25 Nov 2020 23:48:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:49:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf5d881b2b889e71fd32d9e0c3ba5c6da794e6e5afa2741a16d3fc09ae7beffc`  
		Last Modified: Wed, 25 Nov 2020 23:02:13 GMT  
		Size: 26.3 MB (26295207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb07a3af272cbbfd1fcc64d017f4fc7bae62fcb025cda21f621f2476bbf4589`  
		Last Modified: Wed, 25 Nov 2020 23:02:06 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2bd357c5c9ebe614fe49e864454ee6c2cc7bb576066d0d514483aed112ff05`  
		Last Modified: Wed, 25 Nov 2020 23:02:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7207a53d4c4a7708ce000c577926f3beb0dec788c12fd3fe7d2faf6d7c5633fd`  
		Last Modified: Wed, 25 Nov 2020 23:58:22 GMT  
		Size: 4.0 MB (3950065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f30892035840669548f54d04602e990b76625a1a2877362fc8aae8d308b813`  
		Last Modified: Wed, 25 Nov 2020 23:58:22 GMT  
		Size: 3.1 MB (3061644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bf5fecc9648611de357827499d0fea054889f033af4a041e40f9e309f3f255`  
		Last Modified: Wed, 25 Nov 2020 23:58:45 GMT  
		Size: 49.9 MB (49893435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cabe2dee5955453db3dec6439065915a1b7b7ac6ae96024767d9ee8afbc2b0e`  
		Last Modified: Wed, 25 Nov 2020 23:59:26 GMT  
		Size: 125.8 MB (125783051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d48bcafc9edbc5267851fcd826de0d4e24782d0626d2e54ac85efa36dd882b92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235595598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233fe2f1b42ee494f2bfdd18d74e8c9c3a1ed6cd043db32b141a8e547a0ac82a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:43:30 GMT
ADD file:64620b7461f90248a314404599b9aa3b9b592786bcc8ed2cae9df8a7e1f15304 in / 
# Wed, 25 Nov 2020 22:43:33 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:43:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:43:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:43:38 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:08:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:08:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 25 Nov 2020 23:09:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:11:17 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2769ac0e7b9ff64f87f3db82269939c4119f3e9b548bf84e398e068642e07624`  
		Last Modified: Wed, 25 Nov 2020 22:45:16 GMT  
		Size: 29.9 MB (29882425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b76975e3e10573aec5f323bc1d6dbc76af857b1dc3289a68a449dfb881dc2b6`  
		Last Modified: Wed, 25 Nov 2020 22:45:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958ead7f79658868738b309ef9d34e12c738ee519ace595275e35b3c7ea3a5c2`  
		Last Modified: Wed, 25 Nov 2020 22:45:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4213aae5ba683b357424fa2bea5c4e52825e7ea9b8b005dce568bef39c53401`  
		Last Modified: Wed, 25 Nov 2020 23:17:14 GMT  
		Size: 4.5 MB (4489528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9734172f17eb676dad8b6e9ebb6a0b12a5d362962c46d5b7b796b8f63ac368`  
		Last Modified: Wed, 25 Nov 2020 23:17:14 GMT  
		Size: 3.6 MB (3573150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6da05b8b22cb5bc57d1162c5d9dc236f726b3ee89478da5b4c2635637535cdc`  
		Last Modified: Wed, 25 Nov 2020 23:17:36 GMT  
		Size: 55.1 MB (55052055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f0a32f6561ef83b8d4ed0e208ffb49d9e889bce76e92f454fbdd701a8917e1`  
		Last Modified: Wed, 25 Nov 2020 23:18:18 GMT  
		Size: 142.6 MB (142597405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:070dbbb34edb8f8c268f004c967f4bcf2c58801f64b140c2a3a91e2279f0efba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267996240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1cc9291baec34d8ecf8022a78de79a14ec6a34ee5753052baebea29b9a9e1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Oct 2020 19:27:22 GMT
ADD file:3cceb8288ea4091c4fb6670e395f7391741cb6aaa44a1f5e6a2085df56ecba62 in / 
# Fri, 23 Oct 2020 19:27:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Oct 2020 19:28:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Oct 2020 19:28:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Oct 2020 19:28:47 GMT
CMD ["/bin/bash"]
# Fri, 23 Oct 2020 21:04:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 21:05:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Oct 2020 21:08:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Oct 2020 21:22:43 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a69afe95a22d68414fa1ac1b89258d7d482624063e15ae9202ea3fa7649709e8`  
		Last Modified: Fri, 23 Oct 2020 19:32:07 GMT  
		Size: 36.5 MB (36548485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80643583a935ac0edf00defeb0107c6483073a7c2dddd14e5dfad2a4699b178`  
		Last Modified: Fri, 23 Oct 2020 19:31:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49aeb38173a94db987f5d84e1a11177492fa369f214626d961156443b10f1571`  
		Last Modified: Fri, 23 Oct 2020 19:31:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26244204f484bf82c80adec639263fb4afb37e1c8a6aa041874a008251bea4a8`  
		Last Modified: Fri, 23 Oct 2020 21:53:01 GMT  
		Size: 5.2 MB (5151374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49940bb5dd8a122a071e1056de6bba9d7dd55b97adf0d169cae103878e2835b0`  
		Last Modified: Fri, 23 Oct 2020 21:53:02 GMT  
		Size: 4.4 MB (4448921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b559aff162e623b8c5c2f5c17cc7dc95a2aeadae10e202c846b2474689237193`  
		Last Modified: Fri, 23 Oct 2020 21:53:32 GMT  
		Size: 63.4 MB (63438147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd4b64f263542b44dc6249296cc9e51d096cd88374e78b4a81bda828cfc5031`  
		Last Modified: Fri, 23 Oct 2020 21:54:24 GMT  
		Size: 158.4 MB (158408272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e32825840c30c060e1f7f0832cfa0441fb3f2cf3f7efc6984dc0866b1290652
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238729271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187e645cd60442eaf1d59200d7846df4b824e7e018931843969592078dcc4f85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:45:41 GMT
ADD file:af8181cb78887aa9e6aa7f7b33a8ef7b76b74cabc09f582883a8d3111c0fe9e9 in / 
# Wed, 25 Nov 2020 22:45:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:45:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:45:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:45:53 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:55:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 25 Nov 2020 23:56:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:58:38 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:abd4319bb36506beca49a36e3151713760b1b1a72286ebd52ed6a0f8b037ef26`  
		Last Modified: Wed, 25 Nov 2020 22:47:37 GMT  
		Size: 31.5 MB (31461133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13be14e62d3b49d67b17ae821b83ac4bdfd2186f11cceaa27ea603582a04e6e6`  
		Last Modified: Wed, 25 Nov 2020 22:47:34 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285f4745ab7467cbae8d29dc6729e2735cabc05177631c8eb03cfafa79c8bd58`  
		Last Modified: Wed, 25 Nov 2020 22:47:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eeebe396cfa22cf2fc2d0fd92c9dec59dbd2fe7726de52a00e2a081efc99c7b`  
		Last Modified: Thu, 26 Nov 2020 00:05:58 GMT  
		Size: 4.7 MB (4710202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd121be9c3aab14266f8b8785c0d3afe9508806816108bbdbc9185d242c3bae`  
		Last Modified: Thu, 26 Nov 2020 00:05:59 GMT  
		Size: 3.6 MB (3582006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3e22f68e0daff7ad9503beb8eb7ec02a8db63ea4fe21d25aa0a196c75535e1`  
		Last Modified: Thu, 26 Nov 2020 00:06:15 GMT  
		Size: 55.2 MB (55194507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c43c7ce5d3996f30dcf2264d68d909624bdaa96830087cb729e13f469d0fc7b`  
		Last Modified: Thu, 26 Nov 2020 00:06:43 GMT  
		Size: 143.8 MB (143780391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
