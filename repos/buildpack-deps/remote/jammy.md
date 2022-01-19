## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:e30ae59c3627a67b1755ad2fe9167b801e58dbcc811999dc1489e32258d110c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:90f14998f18831bf31772b3329583ba8195b78c112ff61e4a455ba3fad7b93e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252270654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c44d01f9225c8fd20dceec804bd5c6a79997cf9a364ca59c29b43042664a9fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:53 GMT
ADD file:7fa9713fdcdef2552cd85dc53d57c2f444a09798fd2254d68f2f955cc1114ab7 in / 
# Fri, 07 Jan 2022 02:25:53 GMT
CMD ["bash"]
# Wed, 19 Jan 2022 20:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:25:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 19 Jan 2022 20:26:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:30:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25f4cd1d54a5120c409f812234ad6f2266a5ae22fe0cf58c3ffab80bedc4368c`  
		Last Modified: Fri, 07 Jan 2022 02:27:47 GMT  
		Size: 30.5 MB (30501041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6311ad417ef23361fb71080ea7fad77c8b9a37aa95089e986c3044e64d70bd`  
		Last Modified: Wed, 19 Jan 2022 20:31:55 GMT  
		Size: 3.8 MB (3816208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e4beb01c08f1a271fb7ca3ff2994f6f2beab96b23bd9c983f4729f3159f082`  
		Last Modified: Wed, 19 Jan 2022 20:31:55 GMT  
		Size: 3.6 MB (3563299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176a62698817879a5fa8670c465f6e4835be3313ff44d1fa93027ff7320c86b2`  
		Last Modified: Wed, 19 Jan 2022 20:32:14 GMT  
		Size: 41.2 MB (41189960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e738a20424d0ac31404749814e3650e2fcae0105cf36fb78c488a3f9b1245ea7`  
		Last Modified: Wed, 19 Jan 2022 20:32:49 GMT  
		Size: 173.2 MB (173200146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:67d47b5485749fbfffb5cf32d7fa48e22b40e19087a1939bc657140446c9426f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (219039048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd33fead91d34eb5b94e2fd2204b3bc0d694771acab77441236929efc3bfbca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:27:32 GMT
ADD file:8718f314f447f7d0c389825500d5ceb026028c337363ef130cdcf6125750046e in / 
# Fri, 07 Jan 2022 02:27:33 GMT
CMD ["bash"]
# Wed, 19 Jan 2022 20:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:02:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 19 Jan 2022 20:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:05:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:152d82d6f338fbb1e956a78af2d045c6fc15f4c5352ab546d88118f037a1a4e5`  
		Last Modified: Fri, 07 Jan 2022 02:32:16 GMT  
		Size: 27.6 MB (27564608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c52570a8f7aa86b8f432cd77ef9b8392b52570c37d9f4e1e8ca35387813c57`  
		Last Modified: Wed, 19 Jan 2022 20:12:40 GMT  
		Size: 3.6 MB (3564776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888582659393511a7d76d42aeefc827d2c6d3738c7de8cb6c17fd00110a94b7b`  
		Last Modified: Wed, 19 Jan 2022 20:12:39 GMT  
		Size: 3.7 MB (3729934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e70dda0e64068714bdb2b8fda6094f05fece909d0cf5bf1741d49507ebf25b`  
		Last Modified: Wed, 19 Jan 2022 20:13:21 GMT  
		Size: 43.0 MB (42964376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9acb7f9ace03e99b3bfd29faf61f8ccc262b6591907c8e3d0fb4edaa88c7675`  
		Last Modified: Wed, 19 Jan 2022 20:14:56 GMT  
		Size: 141.2 MB (141215354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:67392c231dc4596b600839c1ea85754634cc99b03a3daf72bd7135757b6f76cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244031517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d3317028d07cc2dcd0b58273af68de611be2df6ceb2b6252155fad2c1257cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:54:09 GMT
ADD file:d75d592836ef38b5620858a3eb1666af50f390695066b7b3432f365e1cc3a56b in / 
# Fri, 07 Jan 2022 01:54:10 GMT
CMD ["bash"]
# Wed, 19 Jan 2022 20:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 19 Jan 2022 20:46:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:47:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9ca93140713b0208e2ea5b1925e67a506893717f9d1ff5aa2097ad25d2ffd59`  
		Last Modified: Fri, 07 Jan 2022 01:56:30 GMT  
		Size: 28.9 MB (28921769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ac17a8576102f02f0d17e513cce60acefa1f17b22cea0405764106868d3056`  
		Last Modified: Wed, 19 Jan 2022 20:50:35 GMT  
		Size: 3.8 MB (3789818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af662860a905155ab4657cd4cf774cd0e5915df27adfaf7f4be2c0d4ff646d9b`  
		Last Modified: Wed, 19 Jan 2022 20:50:34 GMT  
		Size: 3.3 MB (3324301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab1fb77fb60b28a1d9c76f07bef60c207a15a1658ee7cb16de7a78e26cd0a4d`  
		Last Modified: Wed, 19 Jan 2022 20:50:52 GMT  
		Size: 41.0 MB (40951139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdaf1f2a2033dc7920ccedd29617f176faa043c14368d1ebea5c134e9c4be92`  
		Last Modified: Wed, 19 Jan 2022 20:51:26 GMT  
		Size: 167.0 MB (167044490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:61a1660cc802e6a9e79326781f370974b34af90b8e349f34d92081354f431ab6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227137085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce9acbaf1c65a76c4e04175e4a07ce2030478b0d596c914d078d729e85e519a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:53 GMT
ADD file:63122dcff09feadc66081fd2b45b3e3de924cf0f111e8515c56594154aabde6e in / 
# Fri, 07 Jan 2022 01:42:56 GMT
CMD ["bash"]
# Wed, 19 Jan 2022 20:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:44:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 19 Jan 2022 20:44:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Jan 2022 20:45:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a0ea954c58d9a01dec91e416a4d333a9fcdca5f2b6512986d1201c7c1763d0b2`  
		Last Modified: Fri, 07 Jan 2022 01:44:50 GMT  
		Size: 29.4 MB (29387057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1266489e4c7f83a842b01329c1954a145ad0287c7254077a9e2b5a6cd40f23`  
		Last Modified: Wed, 19 Jan 2022 20:48:57 GMT  
		Size: 3.8 MB (3815886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f52b0bde0d9ad7fbf84d609e08896778b79c7669c58fb4d0a8fb13a62a526e`  
		Last Modified: Wed, 19 Jan 2022 20:48:57 GMT  
		Size: 3.5 MB (3475100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306ddfd86db03196f7854d02de8dcabfb988e5cdbd7f3b37bede49a98316a9b`  
		Last Modified: Wed, 19 Jan 2022 20:49:13 GMT  
		Size: 40.8 MB (40818719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cd568e0786a779f546a48ca222fd195a1cabbbcc1d3e17376dc6d7ac96cf41`  
		Last Modified: Wed, 19 Jan 2022 20:49:37 GMT  
		Size: 149.6 MB (149640323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
