## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:2b22e8275494c15f5e570059d6e2af32e8df31b7f59c40a914aa7950ee14d83b
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
$ docker pull buildpack-deps@sha256:f140e1bca21188a15222c6d0b4f97749b9d8673e42c0409d9b1f1013ab148b2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37672729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2817be03fccdc1b5159deb073cda1c678a46d11880c3acc0553d04ade510398a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f1668d3645729ae45f8050cfcb2a85fa59293b2179fee5ecc56693f1ffdc90`  
		Last Modified: Tue, 02 May 2023 23:44:26 GMT  
		Size: 10.2 MB (10190664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dfe2cb51267bca20f5f9e0132bcec7faf309651dd623c63011e5a1b2ee4adef1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35415473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2073db234c0b66d4f52fd4b7608602ac6f46b52bcde4c9e2c2fd0f00935c6059`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e55f5249b8525f144077fbb31a4099933acecd00e0a8d0080df9d62254b716e`  
		Last Modified: Tue, 02 May 2023 23:42:50 GMT  
		Size: 9.5 MB (9524222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3c54974fca8d55cc2aae0bf59aaf13d1492ee8fab8fc7afc6758ca10a9901bc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36909668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8f78b7034cdd7b9e8c7a44a1c482fb47fc143533f941369a3d0387c98fd411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:24:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a211e249366d1e9c621cfbb98a45087c7ca76b4539f9bc7d9068b701a8054585`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 6.6 MB (6604111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99e3413cacb724e75738256d7ae34f43ccb93122964be0ea699ffcc780ae6d`  
		Last Modified: Tue, 18 Apr 2023 01:35:19 GMT  
		Size: 3.6 MB (3603384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a173db92e12ea4bc7ab8861dc75b1d01163b4169bf587bcbdf056ceceef84f9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44213227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa7da5a02e3ed5cc84aef25afdec00f9462f210848b3903b605466dcbf679da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:45:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:46:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978ddb6b21e3fea6c8cb5970d8cd307a6ec15ef6b639b994cfdebe9384ef6e24`  
		Last Modified: Tue, 18 Apr 2023 01:03:02 GMT  
		Size: 7.8 MB (7751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54556acf1bc962b10d66a29a9198cf3876dbc10be5d5899d89ee4ee01770250e`  
		Last Modified: Tue, 18 Apr 2023 01:03:01 GMT  
		Size: 4.4 MB (4362837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a9a30abdb96a71c9bfe40e06305587f2453f48e6826253c2346f68c867918c49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36122431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d179c68254fd9641c116296236caf4426c7b9a75a4eef7ff30749528c41b419`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded2cd498871df7ac556305ff379ade5376ed441cad7f51cf98b4867ac750d39`  
		Last Modified: Tue, 18 Apr 2023 01:14:11 GMT  
		Size: 6.5 MB (6467769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5cee9d25bba89e9b965d2fee1419c9d544d12c148be50fd20849d7f808bde1`  
		Last Modified: Tue, 18 Apr 2023 01:14:10 GMT  
		Size: 3.6 MB (3625375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
