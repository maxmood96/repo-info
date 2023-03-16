## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:65a0bbd7cf7563e35126397be974565c3e38662313ebdd0abb231da6075fc920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c4824dc0e30a785dd034a6ba5ded770e6f50c8bd8d9075e44a4bd853b3877215
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39944587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5caab55bf6d1a9670b35b8708c155221d41b0494671f44dce30a46726e341d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:25:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:25:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b7d3f3b016944c7eeeee37880c5c274cfc06cccd337b282c382d036852f921`  
		Last Modified: Thu, 02 Mar 2023 03:43:00 GMT  
		Size: 7.7 MB (7739318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7712ac161458ffa37dfe485734ac5bfbc45c78512bfc1bca4479eb5b6f2aa64e`  
		Last Modified: Thu, 02 Mar 2023 03:43:00 GMT  
		Size: 3.6 MB (3627267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1e8bc526fbffc69c9d0e626081bc81793a560032e1e3c4d3a449f5a60672d96f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34417103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33bbc0c141172ce22bf7cf86bda316933123e335366e1ea9deba8bd6b964d00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:48:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:48:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47332fc42b573d4baf56c0357c8403f43cd7e32995cd91e98f1b63904c165edc`  
		Last Modified: Thu, 16 Mar 2023 04:08:41 GMT  
		Size: 6.7 MB (6726111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae7608366f198edf1178000bf5d347ad633c37686847555ad129799eb689113`  
		Last Modified: Thu, 16 Mar 2023 04:08:41 GMT  
		Size: 3.1 MB (3104510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ffc84a0fcbb9d176e50ebb0222e5eeb290a58fb42bf38dc74b182632e8e2e222
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38415735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8c193e0e6515f7fb45285ce5e80b324f558869d3e85d6ccb9c186b56de169b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada92025b6d5b0737643d0b1828f2344b2cdb92c860a121d471b8f0c87875d0c`  
		Last Modified: Thu, 16 Mar 2023 04:22:35 GMT  
		Size: 7.6 MB (7602314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1d3bbdc78821c82e7efb7e6b25412a925801281a52d89ff278c1440c1682f2`  
		Last Modified: Thu, 16 Mar 2023 04:22:35 GMT  
		Size: 3.6 MB (3617260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6bcb7bbe9e71ec3bf79e404b8dca4821d0a8a8d3e0ba52087d4db6b77cfa2e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46480053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2030d035639fd89c4173ce60293f8f470778669b33f7cb717d29c96ea46f603`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:14 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:14 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:39:17 GMT
ADD file:e8eae0af07e662df38a5b691d04648b4fc72382b6918877da22520ed4d01c3a6 in / 
# Wed, 08 Mar 2023 04:39:17 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:15:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 03:16:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:35c7876eb976fb68d0f3bf24f227b6220a73f879e77ad564d913af35104da2eb`  
		Last Modified: Thu, 16 Mar 2023 01:58:06 GMT  
		Size: 33.3 MB (33300378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6346be203b914f77b544d394d2d63c301d06a7b8926cd30449cdb5a3046edc`  
		Last Modified: Thu, 16 Mar 2023 03:49:06 GMT  
		Size: 8.7 MB (8692841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabdc66fc416ff468476139eca7bc89d467220b030d725d5715d0f79364e4c8`  
		Last Modified: Thu, 16 Mar 2023 03:49:04 GMT  
		Size: 4.5 MB (4486834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1c1099e10a2fe4905babce95ad918aafac037e6865e1dd2de6bebf8c1b1b282f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37937503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e125599525fdd8c0449dd97ad937ff4d8e51359718898ac7bf028fcc1e0ef9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:58 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:42:00 GMT
ADD file:4463dafd3352de8c5ff87090e2f30be9bdffc3fa9d84e27b13e2364d856f82e9 in / 
# Wed, 08 Mar 2023 04:42:00 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:46:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:46:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:422c367cdac1ee2f6bd9ea546c8e5a643af0847a822d04ba202af409973273ad`  
		Last Modified: Thu, 16 Mar 2023 01:40:19 GMT  
		Size: 27.0 MB (27016120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a483453055472ff48de1fd6d705ef6ead7ebb9e0846c4954ba91b6fb7660d5`  
		Last Modified: Thu, 16 Mar 2023 02:01:49 GMT  
		Size: 7.4 MB (7379309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5348a385bccd245fea6b55ab45b16d2bd72f5a321f2339d63941b14ea5af141e`  
		Last Modified: Thu, 16 Mar 2023 02:01:49 GMT  
		Size: 3.5 MB (3542074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
