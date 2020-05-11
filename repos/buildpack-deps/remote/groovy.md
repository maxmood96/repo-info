## `buildpack-deps:groovy`

```console
$ docker pull buildpack-deps@sha256:1fe14f3035c8b93806cdaf079a5646c5b6463cacda1a725e24d530f975824a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0b8a41b3636523af47fe1bb0c860d000ffd19e4bb6931559aa6972313f8f2ed9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (237967149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a23207b45a22e7c07fe8821f411ee6ceaa8e57e475b6c410bfbf2708b3b9c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 18:42:49 GMT
ADD file:0a4786f61369ab8311ad73df0425a325cc7095cd1d2a955a27c759d6e77320b9 in / 
# Wed, 06 May 2020 18:42:49 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 18:42:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 18:42:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 18:42:51 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:21:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 11 May 2020 18:22:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:24:47 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4278c4af5b59c968c977e7ebe9d86416b17eb5328985758690e3d3eac8aaa3f4`  
		Last Modified: Wed, 06 May 2020 16:10:34 GMT  
		Size: 28.2 MB (28171554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05b16b3cc63a06490c0e17d7ce09fb81e50884605c98e94db4883e63d9de811`  
		Last Modified: Wed, 06 May 2020 18:43:26 GMT  
		Size: 31.8 KB (31801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3e637c5311a8a3018cf95f210e8f2a56ee3d14c6bbae422d6349d7b93c466e`  
		Last Modified: Wed, 06 May 2020 18:43:25 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2eb2835f6239dd2e96e96b24f169df777bafb9ad56d18129da631d47d0d1a62`  
		Last Modified: Wed, 06 May 2020 18:43:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcd31e5147b6e6e3e0bc52a304cbc500bfca7c1f2eb804b29f376b9fee98148`  
		Last Modified: Mon, 11 May 2020 18:25:36 GMT  
		Size: 6.9 MB (6859390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae361abb991a333032309434504cb932f8c23f767ee99a2cf2dca31ad0a5c66f`  
		Last Modified: Mon, 11 May 2020 18:25:35 GMT  
		Size: 3.8 MB (3801124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c6ebf940958fd34abcaa57540c221c18bb78bbbf7175bd0f5930f2421eca4f`  
		Last Modified: Mon, 11 May 2020 18:25:52 GMT  
		Size: 63.0 MB (62986024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2fe6a2875c0d7b788071e63a1eb6c7cae286edb90949599cded65d9d34e454`  
		Last Modified: Mon, 11 May 2020 18:26:21 GMT  
		Size: 136.1 MB (136116249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0965c86bf715427ba822d57697802bc7ab2458d95373e4936ac9507ffda0482b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228232852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe9061fb76b2e815e1fe5fa1fd2d6b8f210a8b1bba660cf8ee9779ea60705be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 18:58:02 GMT
ADD file:10718d520403d7b501162166c0d6cc2e6ef14d44aa2908a8e5e6d2c5c618af04 in / 
# Wed, 06 May 2020 18:58:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 18:58:09 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 18:58:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 18:58:12 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:42:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:42:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 11 May 2020 18:43:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:45:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f943d186ebac43c150ac4989818a14f554333749a7ee7c2ffb497356702be370`  
		Last Modified: Wed, 06 May 2020 18:59:27 GMT  
		Size: 26.8 MB (26777518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e815d4dd81b12774fdad087103b1e7ea9ab7a4797013201dc39e59d9191719c3`  
		Last Modified: Wed, 06 May 2020 18:59:20 GMT  
		Size: 31.8 KB (31797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202efd9452c4c247573837e755a3b4dd3d388dcbc12b436862e2401e799a0880`  
		Last Modified: Wed, 06 May 2020 18:59:20 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d13f8c7592c93d54371297aa250ee2e54a4fb7c78bbf0ba95655b7a88cc39`  
		Last Modified: Wed, 06 May 2020 18:59:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84e8785bc94e26b33169918a85a90213bdba70b26f5b3acbbc0888a45b6d4d`  
		Last Modified: Mon, 11 May 2020 18:46:21 GMT  
		Size: 6.7 MB (6723107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33521a12fb9e6fe69f0b65b956711c6ebd884efe082d09f48615c9f45e845658`  
		Last Modified: Mon, 11 May 2020 18:46:20 GMT  
		Size: 3.8 MB (3774287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20fd3e9733ec8b191a7cd2b5953f394022ba27edc2f47f11bf8e8cdb5bbf371`  
		Last Modified: Mon, 11 May 2020 18:46:45 GMT  
		Size: 63.0 MB (63032272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d6abb2f09a85ff44711650d87fd9270c41fd999d20f44d219321b88c990d62`  
		Last Modified: Mon, 11 May 2020 18:47:26 GMT  
		Size: 127.9 MB (127892836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:36a112c2b018d4bfa83e3349bf9fc01b2676fef4873c5e308d2fbe411de9f9b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261640780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8581d9cb4849e9a89a598676a5b07ee5aceb54e0c091a808c3a62483c667f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 18:53:34 GMT
ADD file:38bef3b89ab78f35a240c77d3bfd2424cfe83a3bf6c80a86755d0757378faac3 in / 
# Wed, 06 May 2020 18:53:42 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 18:53:46 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 18:53:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 18:53:53 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:20:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:20:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 11 May 2020 18:24:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:31:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d4b677207667f6a9c31fb95628b1688e43185c1e68507b8ce69c6f753fa6ba0b`  
		Last Modified: Wed, 06 May 2020 18:55:08 GMT  
		Size: 32.8 MB (32830571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a7e3233f42ddeee42ce7307c2f23c2e22479c24ac6391bebc3673d1acedd3e`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 31.6 KB (31614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f21b6f278fbf61dc1503c0ae1118b76024acb128bddbbd2588268e7b0649f91`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a08354d087a0cd2da0584d4775ad4cd0dc224a90d08ba7bdb69f3617e83688e`  
		Last Modified: Wed, 06 May 2020 18:55:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9641d94e47a948c31373f5d11e71cf0507deb3964f344b8bdb7f49293f8aeb`  
		Last Modified: Mon, 11 May 2020 18:33:19 GMT  
		Size: 7.8 MB (7813663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a3e6208b1cfd7270677514d1f2db85afab8cf34dfb830c72dd011bd388c59`  
		Last Modified: Mon, 11 May 2020 18:33:18 GMT  
		Size: 4.7 MB (4701080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22253cdb40902ecc0b1f5770fd187606bf265971c911aa33a44804223204708f`  
		Last Modified: Mon, 11 May 2020 18:34:41 GMT  
		Size: 71.9 MB (71927870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61627b7c0fab769de69f7f35131b0ab7c787aa5502a2de53e3e8574be4a08871`  
		Last Modified: Mon, 11 May 2020 18:36:36 GMT  
		Size: 144.3 MB (144334944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:154723bd74c63411cf9d33c522a9727d145f9cbc01ca3307bd9162e739fac24d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223722407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0314501f5e302e0ad4eeda83702f784776500f61d00a79fa5177bc37b4f82c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 06 May 2020 19:11:33 GMT
ADD file:18b80c063e2b39052a6f2524611163983a5b6c8e1528240afb20fc3b41886101 in / 
# Wed, 06 May 2020 19:11:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 06 May 2020 19:11:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 06 May 2020 19:11:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 06 May 2020 19:11:41 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2020 18:43:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:44:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 11 May 2020 18:45:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 11 May 2020 18:46:31 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8ed64b725cc4ff032cc93a2ea3abdb156d4ad0bd348733dd539bad2cac6bbed4`  
		Last Modified: Wed, 06 May 2020 19:12:19 GMT  
		Size: 26.9 MB (26896707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19c313a26839bd4356dfd3e27dbe2c5a6987cabd276b1be0796a0a4f11ee03f`  
		Last Modified: Wed, 06 May 2020 19:12:16 GMT  
		Size: 32.5 KB (32456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80258349596dcffe60b09a96aa544fb2e8e215f2bf5f84b131d5a9be69df01e8`  
		Last Modified: Wed, 06 May 2020 19:12:21 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213a1263d4ddd1b0655fdd29fbcd9a8bbe45007f72b6e9b37a3b0e770423cdf`  
		Last Modified: Wed, 06 May 2020 19:12:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e0df22201c8478d4407b1096292794871599aa21ad630b45d6ede37b0dae4e`  
		Last Modified: Mon, 11 May 2020 18:47:41 GMT  
		Size: 6.5 MB (6548064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cdd7894b14e9dee6298a895f30b09c83ce10efb5bf2ef94966eee2b9d495a0`  
		Last Modified: Mon, 11 May 2020 18:47:41 GMT  
		Size: 3.8 MB (3795522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253d089777b2e8e500acc9b4f9c4149b4a50a57fe8c80bf3017844af7d5b8031`  
		Last Modified: Mon, 11 May 2020 18:47:56 GMT  
		Size: 62.8 MB (62761515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099dc1d98c1afcb4231f710162a5e8765034e6d0554d8594726a12c1428c465b`  
		Last Modified: Mon, 11 May 2020 18:48:18 GMT  
		Size: 123.7 MB (123687109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
