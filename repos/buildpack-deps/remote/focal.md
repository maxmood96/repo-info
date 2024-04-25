## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:85a77e15b5d114adc8f6f28dad0f48834893e6f186deddb18e6b5b3511d73866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:19d9b8554978e3023cec8db6ab773019f8aebad7fe2070d89006270fc99d227b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251106019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c7d74bf2c6b369f1eb7256e94d459aed0cb3de2dd184a6cbe0c800f794796f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:23:31 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:23:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:23:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:23:33 GMT
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
# Wed, 17 Apr 2024 18:23:33 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:18:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:19:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:22:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:60cc0dcff74033c96380df2ca2f1381aa68602df27d53aa1bbf2bbe4ba703158`  
		Last Modified: Wed, 17 Apr 2024 23:03:46 GMT  
		Size: 28.6 MB (28584597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72898805f20ab903dcade318c35ce3fe3649171ca4591d6dd905b862b99e0218`  
		Last Modified: Thu, 25 Apr 2024 21:42:45 GMT  
		Size: 11.1 MB (11131301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc13b1b2b919d0130bb947cef1aaaeda4aceea279cfe77098959ea1e2023efd`  
		Last Modified: Thu, 25 Apr 2024 21:43:03 GMT  
		Size: 60.9 MB (60906197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975c081e57fc27d0af1e2c9b587e8b2683d31ed290ec7d542eacadb9920290cf`  
		Last Modified: Thu, 25 Apr 2024 21:43:31 GMT  
		Size: 150.5 MB (150483924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c6fb118925d1c1eebeddae297a6ceaedb329d074372e7ae634589f09faea191c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216609526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e90dbc182f7f1a58a2ea422ca79f6307f1854e5395b2cc58806f56f04cd6811`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:28 GMT
ADD file:648705eca6ad0949d4722f06be77e38518c38195f6aa605ceb301e2b576583a6 in / 
# Wed, 17 Apr 2024 17:58:29 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:37:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:39:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:46:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43be25f0e2861789d9988ebf21e9e09ed9fc29e4a0a9fcff186988c12198eb72`  
		Last Modified: Thu, 25 Apr 2024 20:32:27 GMT  
		Size: 24.6 MB (24603299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9044ae288fe4194a15be798aa70686b6f183eb9d530926a75da5b2ddbc42d4c4`  
		Last Modified: Thu, 25 Apr 2024 21:19:19 GMT  
		Size: 9.6 MB (9604714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa851e24240da4f8e0925938c1badc8113043c77e5aae5a2b08f4fda3e0e7bb`  
		Last Modified: Thu, 25 Apr 2024 21:19:39 GMT  
		Size: 55.9 MB (55867722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053f55b8a0f6d32f86da008006ba0350c82d973d43360c20cf2da3564d2edaa0`  
		Last Modified: Thu, 25 Apr 2024 21:20:07 GMT  
		Size: 126.5 MB (126533791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dc01c22b0876ba44f21ba0ab856959da377715a9df8e2c0983bd0b0a348e6fb3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240485623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164869e4b36ec2af96e6a72425ebb48be64401da7c1d840664424414ea54db13`
-	Default Command: `["\/bin\/bash"]`

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
# Thu, 25 Apr 2024 21:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:14:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11686d3c3279d285321ad7d2bd863c8436ee583c2e454390121bee791f83f4f0`  
		Last Modified: Fri, 19 Apr 2024 07:58:29 GMT  
		Size: 27.2 MB (27207009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5121d4c393eb5fe2720dbbf8d8e07f41ab2ebf3e52aa43d3b7d9b59526edddf9`  
		Last Modified: Thu, 25 Apr 2024 21:45:10 GMT  
		Size: 11.0 MB (10983849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fe9691435ff49a6b18c6e8e505338c686a3c0f56c374d0c9f3b2120419dac6`  
		Last Modified: Thu, 25 Apr 2024 21:45:27 GMT  
		Size: 61.1 MB (61050201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cdf6ca7c54699f1c623254e7128b127daea3ae229231debd357c4fce2cb5f0`  
		Last Modified: Thu, 25 Apr 2024 21:45:49 GMT  
		Size: 141.2 MB (141244564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:17869d942039561e51709932f926668513d24a34e77e676883511de60985b17d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275638664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09987955d69d4710093ac9d4d21dac137770b3d7889fdcc6394322c222394bc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 17:58:26 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:58:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:58:26 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 17:58:30 GMT
ADD file:4b03eaec2f51a953c9ccc0a67500331d1c8e8184b6aabb40b8b988151cae02a7 in / 
# Wed, 17 Apr 2024 17:58:30 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:09:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:20:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f8bb14c4f706bfa46117251c6dad75ca75486672a0d08c838c1c4b8ef608aad`  
		Last Modified: Thu, 25 Apr 2024 20:52:39 GMT  
		Size: 33.3 MB (33315776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a4182c29400d6c1f4a95c25230c42d16d826e7916918afbfd612a8e7f30fdc`  
		Last Modified: Thu, 25 Apr 2024 22:04:18 GMT  
		Size: 12.9 MB (12940407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5250b0da18672ce303cb6d2b5b26bcc675548bf927e7ab099d1d95d85744be`  
		Last Modified: Thu, 25 Apr 2024 22:04:38 GMT  
		Size: 69.6 MB (69639656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c8907639b08d3b968fe0d58a5ffb8413fc7b7eb385f4d816e9b0061c4b47b9`  
		Last Modified: Thu, 25 Apr 2024 22:05:11 GMT  
		Size: 159.7 MB (159742825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4ab24d9b51f01bc62bf7374b22b4f37c3760bcebfbc061d32f70b421bd02019d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231062086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bff7c4e59dd830b22cfb2dc33e487ee9542a40adc9d66549a9e3893b2e568c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Apr 2024 18:38:36 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:38:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:38:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Apr 2024 18:38:40 GMT
ADD file:da0ff0dbc934fe8a302da2a67ea8c5ff869d6bfdd919e1e1956c06f0cf34caf5 in / 
# Wed, 17 Apr 2024 18:38:40 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:08:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:16:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0820294584b3892c5ee83c185febb4613e73d261e74e3fa651fbe35b0f997d0`  
		Last Modified: Thu, 25 Apr 2024 20:57:22 GMT  
		Size: 27.0 MB (27013669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f56ea049cf49cc715420b456371bc4769d7d37f5acaa9056f27fdb87c24713f`  
		Last Modified: Thu, 25 Apr 2024 20:57:21 GMT  
		Size: 10.7 MB (10690122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d79eaa04d8e6c5fd7ecf572a1bf445c11c214f114b4684d9e62a30871216fe`  
		Last Modified: Thu, 25 Apr 2024 20:57:39 GMT  
		Size: 60.3 MB (60318190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182187ba9322f230de6d0f55ce410f8e3ff9e9b6e3640b826a34183cfa7bfaee`  
		Last Modified: Thu, 25 Apr 2024 20:58:06 GMT  
		Size: 133.0 MB (133040105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
