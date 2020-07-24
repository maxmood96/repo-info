## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:6ddf6ef256597493dd4da342aeb793caf916001b6eb3e6656539e06939cab227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:be69a80b63a3f577986c38e9bc32761c6e52bf2141e404a4beb2c765216aa7c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237171725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe181d17dfd97963486ce9757495a42efcdcb083a0d5a76a31d664f00a7861a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:32 GMT
ADD file:65a1cc50a9867c153deb3bed36d9d51d469fb123df6ee0ba31e01646edf1a1c4 in / 
# Fri, 24 Jul 2020 14:38:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 14:59:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:59:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Jul 2020 15:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:01:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ff22d22a8554f746f90a78b501da38d56a46f2ddba0dfec8b260aebaa61b3ba`  
		Last Modified: Mon, 20 Jul 2020 15:20:12 GMT  
		Size: 28.6 MB (28557306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb79d19722c46b9c0829811d7a5a0ae82c8771ab7f2f68e7d3a3ed6bd5d5d0`  
		Last Modified: Fri, 24 Jul 2020 14:39:29 GMT  
		Size: 32.3 KB (32320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323d0d660b6a7da8df08a01dbc7250f38cfa2161db00c7c27c0b20be07a8236a`  
		Last Modified: Fri, 24 Jul 2020 14:39:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f616834fd07522cbfd33f0dfa848903599320b5c7191b59fe9aa7562f956a1`  
		Last Modified: Fri, 24 Jul 2020 14:39:29 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d46447739d2619447d72b412a47f550173d1fcc69c94dcc4bb2d1df4443a`  
		Last Modified: Fri, 24 Jul 2020 15:09:41 GMT  
		Size: 6.9 MB (6860878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66fb5ee47e01d585299d8ccc7ae78e598e30aa17e45bfbf62a04678c6eec158`  
		Last Modified: Fri, 24 Jul 2020 15:09:41 GMT  
		Size: 3.6 MB (3566147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f871d6e87730e51cd523dc94917c24ffe4ffaeb3ea1843591d4f67b2885740c9`  
		Last Modified: Fri, 24 Jul 2020 15:10:00 GMT  
		Size: 60.6 MB (60550814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc995ad24c36d98acdedfe59398f21e4a462dfeb1b39134e511ae9b8a6dd555`  
		Last Modified: Fri, 24 Jul 2020 15:10:33 GMT  
		Size: 137.6 MB (137603247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:28c1991dedf3acc2acc6e6d54e14aed6154ab30ef4995355b1f16f21bb1710bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205941472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0cf7b96448a740fe94dac8030aabff52beebe291311500e3ffae5c4c88c1f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:06:12 GMT
ADD file:bcba01fb27d025c2931e46af0b091f98e743ab46eaa1d2d2dd38e6aeb9706267 in / 
# Fri, 24 Jul 2020 16:06:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:06:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:06:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:06:55 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 17:57:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 17:58:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Jul 2020 18:00:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:02:53 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:86924fd76ad7a77a1ec54ad07fdb4d2d51c12b6070f2dfe92dbf92e3f99702d7`  
		Last Modified: Mon, 20 Jul 2020 15:50:15 GMT  
		Size: 24.0 MB (24034159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e967235e6adc918de90ffb2d143fb1ad2659c63f6c0c8a9c70c8e08bff13917`  
		Last Modified: Fri, 24 Jul 2020 16:14:35 GMT  
		Size: 32.3 KB (32349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabf100c8ea14f6342f16b9b10cb81a1355aa9a9d6b8f607c04119c9790f1a51`  
		Last Modified: Fri, 24 Jul 2020 16:14:35 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344cec738d225bc4e9abb563b22a040685352088e9d588d910c09039fa47ac35`  
		Last Modified: Fri, 24 Jul 2020 16:14:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7289da11e3a62aa99da074c382eccf3812167072a3147d29bceb7d45b9e22bfe`  
		Last Modified: Fri, 24 Jul 2020 18:15:03 GMT  
		Size: 5.9 MB (5854937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf7a75afc7720477d11fa4f5187fac976ace930e6e54b4bbbf0d2f9e91ec168`  
		Last Modified: Fri, 24 Jul 2020 18:15:02 GMT  
		Size: 3.0 MB (3044526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c17470ee08bc2ebbb57b9bbb05ab4978e3e329ede7dc1f14bbf02bb9ce6880`  
		Last Modified: Fri, 24 Jul 2020 18:15:34 GMT  
		Size: 55.2 MB (55247686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11096f9a5021b2d53fa98d84ff50cf7a15365fd10bc507dbb2637ec89a3139bc`  
		Last Modified: Fri, 24 Jul 2020 18:16:19 GMT  
		Size: 117.7 MB (117726777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:db383d6f79a6a323ed2713421a2ef27cdf848b212211b148f2002a37d918e731
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227270159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347fe6099f5801fd562fc8f469fec7e9975525dc353004620f56d38e7302a12f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:24:06 GMT
ADD file:26bd57f1dbcfd1a91715cc84cf0f221783655f16bbb7a912aaf20507cc252535 in / 
# Fri, 24 Jul 2020 16:24:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:24:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:24:39 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:24:44 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:44:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:44:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Jul 2020 18:45:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:47:12 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3583fd5e2faf2976fb6333a3a15414f2708dc284c018a672e37112326bc7b7a1`  
		Last Modified: Mon, 20 Jul 2020 15:50:10 GMT  
		Size: 27.2 MB (27159444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2d9e0aed378588f59f8f4276e70ea379b773d7d6507046cd7a044601499785`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 32.3 KB (32333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4a6dca9e536449681a937b8f49022cb56b230e352da8aed9b616fadb14dc30`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d9e98650a6106452fc9e640abe8929399fa4f7a0d3ef58a593e8d68cdf3a6`  
		Last Modified: Fri, 24 Jul 2020 16:27:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeed9dbc01b0e52ebfe80653b8e979e38d89a69f4b3258533876dc5e7a813d49`  
		Last Modified: Fri, 24 Jul 2020 18:55:33 GMT  
		Size: 6.7 MB (6723815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a10d149805dec546848f6a96c2d1c33138a98cf04721779fe6dba30942e590`  
		Last Modified: Fri, 24 Jul 2020 18:55:32 GMT  
		Size: 3.5 MB (3541722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eff3caf55da596ec45ce32cf006a8020c7ca96400f390d8817a904a575f82b5`  
		Last Modified: Fri, 24 Jul 2020 18:56:01 GMT  
		Size: 60.6 MB (60597005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356bbb58d059646cedaa694b27ef1dc6683fa085ce4ed373439f31a94a30256a`  
		Last Modified: Fri, 24 Jul 2020 18:56:46 GMT  
		Size: 129.2 MB (129214805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0069585bf04ffefd64a0e1b6fdcaa914450da2ca9131c5f0cdda06e8857536fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260773432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5464d223a4d634757cd7803ba2f26ed4c379eedd5d75cf4fe59712af16b6bfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:35:30 GMT
ADD file:fec1d8aac4ab3a3c2326e15808c04b0df4c06c2c4e66d3f34e3e31d3408fd793 in / 
# Fri, 24 Jul 2020 14:35:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:36:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:36:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:36:43 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:02:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:03:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Jul 2020 18:10:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:27:31 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4739cd2f4f486596c583c79f6033f1a9dee019389d512603609494678c8ccd53`  
		Last Modified: Mon, 20 Jul 2020 15:51:10 GMT  
		Size: 33.3 MB (33279182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f57f5c67707a22a55ae858c6c54f236321b919889f34c321e1a3cc35b9a7988`  
		Last Modified: Fri, 24 Jul 2020 14:42:20 GMT  
		Size: 32.2 KB (32166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169b0395dde9514c1a521632a61afda1494fe836f816badcab196bd067b4891c`  
		Last Modified: Fri, 24 Jul 2020 14:42:20 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b459fe5e4dff59e4cc2b4b5207df42a369d6f0ac774f26c55184b3ccd491996`  
		Last Modified: Fri, 24 Jul 2020 14:42:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595dfa7aa2023f65b441c28c9412f7ceaefa19a7a2dd3fb399a6ae5ee57937b6`  
		Last Modified: Fri, 24 Jul 2020 19:15:09 GMT  
		Size: 7.8 MB (7813527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8940bf8a991181bc1642a5f54b6d000b8b1a466c7edb85172bb5e9e361766449`  
		Last Modified: Fri, 24 Jul 2020 19:15:04 GMT  
		Size: 4.4 MB (4399121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d101b17ef943c6c1b34f096b192971235fd78ba6d787fe3c9ba518fb3961282e`  
		Last Modified: Fri, 24 Jul 2020 19:16:46 GMT  
		Size: 69.3 MB (69335201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21528dc07fc12b435c276fae6f9ef021639edeacca4f6f17080ca04d4279e556`  
		Last Modified: Fri, 24 Jul 2020 19:19:38 GMT  
		Size: 145.9 MB (145913193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a9029b023c95d9607fdff7644dea0d4bef501db02157ea7bb437926d164232b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223073043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef27f82e196560991d47067edd888c8f70faa11fb2e3e384e74db346cb2078`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:44:16 GMT
ADD file:6c803b66511ab9cbe066bf89c4d7eb4d7ee4e5a277c36a87dcf63834e18fcfb6 in / 
# Fri, 24 Jul 2020 14:44:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:28 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:49:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:49:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Jul 2020 15:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:50:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:72b8403ae854f945520d1213c568e1b3edf3c0c608fa66780ac822be2ce76657`  
		Last Modified: Mon, 20 Jul 2020 15:56:17 GMT  
		Size: 27.3 MB (27268775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824bb95b6ed456a4fb312de39690e22ca2dac1131067ef2e32679e61e1bf4e76`  
		Last Modified: Fri, 24 Jul 2020 14:45:44 GMT  
		Size: 33.0 KB (32965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daf151e726997888df7ebd2403777ed7675e924280e5e5a4180528029a48c0c`  
		Last Modified: Fri, 24 Jul 2020 14:45:44 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72590bfaf79d6d4e391712b6a34001678f6d42795816fc127ce10762be56d826`  
		Last Modified: Fri, 24 Jul 2020 14:45:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8809e9c24249f66aea9c398f5c4e43e6d5c0243cb7f6818d030b8e5675628f`  
		Last Modified: Fri, 24 Jul 2020 16:48:09 GMT  
		Size: 6.5 MB (6547419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199a56b507f027b721456ac4740386c62ee5b62db119c97efceaa98c29a840f8`  
		Last Modified: Fri, 24 Jul 2020 16:48:09 GMT  
		Size: 3.6 MB (3563215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34993824137bbd369ad9cb673e5aa8850702c9f93e3634f2559daf5a93130b6`  
		Last Modified: Fri, 24 Jul 2020 16:48:34 GMT  
		Size: 60.3 MB (60314839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fe0b9f3f45beebd5f7da4560d6f70d2388b9dc6fc70894019182e0f3a2941b`  
		Last Modified: Fri, 24 Jul 2020 16:48:59 GMT  
		Size: 125.3 MB (125344795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
