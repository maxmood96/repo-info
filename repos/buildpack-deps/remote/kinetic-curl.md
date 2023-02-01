## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:23564de567f054c26eda9eaf44dc3976fd8f6f810f52c1349f9096514d278621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:aee83996c48b86aeb5b790a31fe66a215e9925a3476a210d23b74f1ed7217bc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37878994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154ba55bc0e297c9fb12b70cceafd72e5fb510e6be0838aeac5e673ba3eb83b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:52:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:62a5d402f83137154c8e54f4f370e9f9f70b5a6892f6ec8cc2fae7be0fd8ae91`  
		Last Modified: Tue, 31 Jan 2023 18:03:39 GMT  
		Size: 27.5 MB (27479169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242f8f31e97bc8f200f610260668952e0a909150c1e95f494e3165edd6a4e74d`  
		Last Modified: Tue, 31 Jan 2023 18:03:36 GMT  
		Size: 6.8 MB (6764654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddf4e3936d1208458d4e3e5395b8b86da6f3f7ef3b30242decd50ee0403f1e9`  
		Last Modified: Tue, 31 Jan 2023 18:03:35 GMT  
		Size: 3.6 MB (3635171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a00e7f2caaf7a80d3ff855871cfb9a73dbc6b81ee23f46c7946598e61761415b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35627603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06b8b48a09e857ec43c808693fed0bc4a960da257fe2898ddb6e5a123e5e3dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:02:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:02:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3689a8df2bef3da04eb6dd3992a8a12da08076bfc3b502ebfd175c90d3befc1a`  
		Last Modified: Tue, 31 Jan 2023 18:17:39 GMT  
		Size: 25.9 MB (25892003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fd827b5dcd49a319ffaf18db83f4d8e6234d1a0a5ca59247e525d46959e950`  
		Last Modified: Tue, 31 Jan 2023 18:17:35 GMT  
		Size: 5.9 MB (5935215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c4c2c8c1755f8908e4f7f6c8064b5226752b53649ff4a6117d436f2601c4ab`  
		Last Modified: Tue, 31 Jan 2023 18:17:35 GMT  
		Size: 3.8 MB (3800385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:459333d1097d8ab2a535f9c41fd9eff41b7f5820d2c47c0d962e093657486976
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36897627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f0ccf2c259d8726bab173cdcb0552efa2ef70239be80ab1d4ec8c83bd6a86e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:18 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:18 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:20 GMT
ADD file:f61617371f6963c6be2852e2b94d04e8507feb8f77e3484c94aa8b9d0ac67f76 in / 
# Thu, 26 Jan 2023 12:08:20 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:24:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:44d97c2a5ae0fb5d56de8a6242583e80e9265c58a742eb1e52d40264d9f034e9`  
		Last Modified: Tue, 31 Jan 2023 18:35:38 GMT  
		Size: 26.7 MB (26699721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3b285ead03b32399f7eb21eb63769c45b64c8b1731dfc244904cc2e9a8262a`  
		Last Modified: Tue, 31 Jan 2023 18:35:35 GMT  
		Size: 6.6 MB (6595500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855afc623fecc9cad347ac6e791b5bb08dd8331201f22400b2764672b1e9a48c`  
		Last Modified: Tue, 31 Jan 2023 18:35:35 GMT  
		Size: 3.6 MB (3602406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:055376708ea1867e94b93cf561f8cef6c53ee9ef58b8b61cd47ead6df152da8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44214075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6297083ca03c278a01cf0c0652d9765e62bcb400e73228e55692cf5c25319c77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:59:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6a06c15ccb04b9b73efad888bdc885d26bd74537d9322b6629f3b3ef906c0756`  
		Last Modified: Tue, 31 Jan 2023 18:18:11 GMT  
		Size: 32.1 MB (32109752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ee7c83faf85e0ce7383151d494b3fbc177d548f264c95b2dcbf49dca2d06d2`  
		Last Modified: Tue, 31 Jan 2023 18:18:05 GMT  
		Size: 7.7 MB (7741886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e688b449cdca40b587631310483952ae87bf319f0b7d13251a6a085f60c05db4`  
		Last Modified: Tue, 31 Jan 2023 18:18:04 GMT  
		Size: 4.4 MB (4362437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:832891dce637dd6a45a4d5349c2792f04ad3f518c1596702561171552b5eb5fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36112516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4326242fb08207106428f6944530b3e0d79c30fcfb112b958bcf78cf90ad2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 12:08:47 GMT
ARG RELEASE
# Thu, 26 Jan 2023 12:08:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 12:08:48 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 12:08:50 GMT
ADD file:a83afd93816f868be76d243df85b87a66b39d5ef0497c3cb8d0bba2bd4a27c40 in / 
# Thu, 26 Jan 2023 12:08:50 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:45:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:45:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a5bec5e5b1f8afd82addaa8ef129ee5026d804c474c34ca3e565dfa18fa5f877`  
		Last Modified: Tue, 31 Jan 2023 17:56:19 GMT  
		Size: 26.0 MB (26029773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888884268a5ab3f78486597366fa902253286ebe039958a9950d8ab78853d5c5`  
		Last Modified: Tue, 31 Jan 2023 17:56:16 GMT  
		Size: 6.5 MB (6457669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7aa7ab93554822a6ee5149dc403f0ba1aa47ed227911574510630a9383bf8f`  
		Last Modified: Tue, 31 Jan 2023 17:56:16 GMT  
		Size: 3.6 MB (3625074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
