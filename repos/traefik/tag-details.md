<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.34`](#traefik1734)
-	[`traefik:1.7.34-alpine`](#traefik1734-alpine)
-	[`traefik:1.7.34-windowsservercore-1809`](#traefik1734-windowsservercore-1809)
-	[`traefik:2.9`](#traefik29)
-	[`traefik:2.9-windowsservercore-1809`](#traefik29-windowsservercore-1809)
-	[`traefik:2.9.4`](#traefik294)
-	[`traefik:2.9.4-windowsservercore-1809`](#traefik294-windowsservercore-1809)
-	[`traefik:banon`](#traefikbanon)
-	[`traefik:banon-windowsservercore-1809`](#traefikbanon-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v1.7.34`](#traefikv1734)
-	[`traefik:v1.7.34-alpine`](#traefikv1734-alpine)
-	[`traefik:v1.7.34-windowsservercore-1809`](#traefikv1734-windowsservercore-1809)
-	[`traefik:v2.9`](#traefikv29)
-	[`traefik:v2.9-windowsservercore-1809`](#traefikv29-windowsservercore-1809)
-	[`traefik:v2.9.4`](#traefikv294)
-	[`traefik:v2.9.4-windowsservercore-1809`](#traefikv294-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:74c0df9a0b72ee3ccfeff333a8a2ede28c27d539918dcbcf04c523b3c88c533e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:9248f7f17d44a02872613d652aff91856f928ebc400d037cd3439731da4cecbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22605595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dd394242b858ec3a77eec6506ea614377091f1904f704d3412983c1be8c0cd`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 07 Oct 2022 04:21:34 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 07 Oct 2022 04:21:35 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 07 Oct 2022 04:21:35 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:35 GMT
VOLUME [/tmp]
# Fri, 07 Oct 2022 04:21:35 GMT
ENTRYPOINT ["/traefik"]
# Fri, 07 Oct 2022 04:21:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa79c7609bd35acb6baeec95c0534de9f28c053bb3b54b53c4831b70e4a2b6e2`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 320.1 KB (320103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b58027c881a56cde12f5ad6ba79f399d338b083423a96ae8fdb32a53f55af9`  
		Last Modified: Fri, 07 Oct 2022 04:22:44 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84aae39edfd57a3d7eb7d5f3506e471031166e65d061c8be54fca77258b6140c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b13bdeaf794060f706e8061be10b71e7ef64882356982de89daec674fe698c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 08 Oct 2022 03:58:30 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 08 Oct 2022 03:58:31 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Sat, 08 Oct 2022 03:58:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Sat, 08 Oct 2022 03:58:33 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:33 GMT
VOLUME [/tmp]
# Sat, 08 Oct 2022 03:58:33 GMT
ENTRYPOINT ["/traefik"]
# Sat, 08 Oct 2022 03:58:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:480f18b6c0179f0ed54861403bbe3503ed26203a6307b30978f4edb95c7a1f03`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 123.5 KB (123539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e3fa745c422a0bf87c538e124bc46e1c0a2c2fd0c50501c4e558da00084fc`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 320.1 KB (320098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115198abd673e94528474879115112ca2bd769da4a9f7c9cce6302d59f3d456`  
		Last Modified: Sat, 08 Oct 2022 04:00:21 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:998889d8da01c621040b155856bb41038aa1a65896c86abb4915d9e7710a07eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20574991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71027e8a7dfc0095b24f9fbbf590702387cb0bbb08c7da94646dea0044028799`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 27 Oct 2022 23:00:59 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Thu, 27 Oct 2022 23:01:00 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 27 Oct 2022 23:01:00 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:01:00 GMT
VOLUME [/tmp]
# Thu, 27 Oct 2022 23:01:00 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 23:01:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dcf3621c695e89e69ec66c2e79a79a8b1c5cc7d4b33794c23f40dd4e1c589a`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 320.1 KB (320107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a1a0cc2676bf63edfe4593a0283c5204b2434451e09da0f8acc781f6c031b`  
		Last Modified: Thu, 27 Oct 2022 23:02:03 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:2069e9421447a979d3b452395bb820361c08d83de00c636e0ab2ac0603e104e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26fa7cd56b81852ea9f61e45df0913aab21313dc3ceeab8a893916893b533054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25662747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d7c99e10d8ab1a83a9b8ae9755e9912e39a2a9e52da6ce6de8defc71809bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 04:21:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 04:21:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 04:21:27 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:21:28 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 04:21:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02345b26a3d377d58f815ff68ead6a7dd73b699f6c32431c8d20e8f089729c37`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 672.8 KB (672839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedb3d96d801ee542c140b3c61969835a610feec705ca8958b056cca584fce66`  
		Last Modified: Fri, 07 Oct 2022 04:22:23 GMT  
		Size: 22.2 MB (22162052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4889541507d1292f1cc22ab716fe900b3cf01a14362a5fe85f91fbf67a75cee`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:852bfc774229c23356a5d820bf44f86881baa8514ad6e2f20ab62c4e403de23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eefd9c077e3966c82a20fb7d97684c827cc1e65d9c63684ebe18c8076247c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:17 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:22 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:22 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:22 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ced22cf89095c1fa196cdfa7a81f1e06c58396cba3d7aba02c0a0dc15a9091`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 677.6 KB (677556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8c7574d9711fae322abb656d8f6b17662f5f2c4d353b09a116a83bc9fa751a`  
		Last Modified: Sat, 08 Oct 2022 03:59:54 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8974f171927f790c59d4a52f62af80705a746cc0c5e97fbecdc3f03b5e801d17`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:aa2581cd19c9cedc7889a4f8694169cb5337d5cfc77b67e6c6b7e68a6a7c406f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23527803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc42e10eb1bc021727b03128a3ffa88509d49ffda91826e320ce7c000951b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:54 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:54 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:55 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcac61fa6de5b9a13a488b720a6192d410da114e28e9622be993368cd7e6f14e`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 673.9 KB (673910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5d651501b15cd983c2bec1ab8a076859c15803a1b03dff828baf0f1a6a83a8`  
		Last Modified: Thu, 27 Oct 2022 23:01:45 GMT  
		Size: 20.1 MB (20131372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f40d2b1f6b02b45c16a9fa54fd5fbd5d2062d79f726fbd3909b52c2c0c399`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2b98a6729f6acb261b00df5cd442aeba121553d307a2bf4c556b0f2d6db5b1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:71ad6a0260772b709548bedfb9d634d97cd28a14fca877bdb6297a9ffd43bb99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734015671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b09c2bb205d96b067404adfd97994511716618d40107644629870147cba58b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 18:17:51 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 12 Oct 2022 18:17:52 GMT
EXPOSE 80
# Wed, 12 Oct 2022 18:17:53 GMT
ENTRYPOINT ["/traefik"]
# Wed, 12 Oct 2022 18:17:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c05aa1874a2d976a43b6d2c3a71b81f3a4f594a5d048a192a33debac9dae8a`  
		Last Modified: Wed, 12 Oct 2022 18:18:48 GMT  
		Size: 22.8 MB (22846075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af5a81401a21645a0408443fe991fd9df7a3f84fdb3bb206fe094dac1fdd6cd`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b38614dda35cd6fd3ea0a8beb5c6dba618af1103fde9a7404ce5720b6c170b`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8152802c5fefe99fcf75179a44df9139a1474ab34a433c273d27152ef4f836d9`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34`

```console
$ docker pull traefik@sha256:74c0df9a0b72ee3ccfeff333a8a2ede28c27d539918dcbcf04c523b3c88c533e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:9248f7f17d44a02872613d652aff91856f928ebc400d037cd3439731da4cecbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22605595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dd394242b858ec3a77eec6506ea614377091f1904f704d3412983c1be8c0cd`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 07 Oct 2022 04:21:34 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 07 Oct 2022 04:21:35 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 07 Oct 2022 04:21:35 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:35 GMT
VOLUME [/tmp]
# Fri, 07 Oct 2022 04:21:35 GMT
ENTRYPOINT ["/traefik"]
# Fri, 07 Oct 2022 04:21:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa79c7609bd35acb6baeec95c0534de9f28c053bb3b54b53c4831b70e4a2b6e2`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 320.1 KB (320103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b58027c881a56cde12f5ad6ba79f399d338b083423a96ae8fdb32a53f55af9`  
		Last Modified: Fri, 07 Oct 2022 04:22:44 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84aae39edfd57a3d7eb7d5f3506e471031166e65d061c8be54fca77258b6140c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b13bdeaf794060f706e8061be10b71e7ef64882356982de89daec674fe698c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 08 Oct 2022 03:58:30 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 08 Oct 2022 03:58:31 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Sat, 08 Oct 2022 03:58:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Sat, 08 Oct 2022 03:58:33 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:33 GMT
VOLUME [/tmp]
# Sat, 08 Oct 2022 03:58:33 GMT
ENTRYPOINT ["/traefik"]
# Sat, 08 Oct 2022 03:58:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:480f18b6c0179f0ed54861403bbe3503ed26203a6307b30978f4edb95c7a1f03`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 123.5 KB (123539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e3fa745c422a0bf87c538e124bc46e1c0a2c2fd0c50501c4e558da00084fc`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 320.1 KB (320098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115198abd673e94528474879115112ca2bd769da4a9f7c9cce6302d59f3d456`  
		Last Modified: Sat, 08 Oct 2022 04:00:21 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:998889d8da01c621040b155856bb41038aa1a65896c86abb4915d9e7710a07eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20574991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71027e8a7dfc0095b24f9fbbf590702387cb0bbb08c7da94646dea0044028799`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 27 Oct 2022 23:00:59 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Thu, 27 Oct 2022 23:01:00 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 27 Oct 2022 23:01:00 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:01:00 GMT
VOLUME [/tmp]
# Thu, 27 Oct 2022 23:01:00 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 23:01:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dcf3621c695e89e69ec66c2e79a79a8b1c5cc7d4b33794c23f40dd4e1c589a`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 320.1 KB (320107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a1a0cc2676bf63edfe4593a0283c5204b2434451e09da0f8acc781f6c031b`  
		Last Modified: Thu, 27 Oct 2022 23:02:03 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-alpine`

```console
$ docker pull traefik@sha256:2069e9421447a979d3b452395bb820361c08d83de00c636e0ab2ac0603e104e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26fa7cd56b81852ea9f61e45df0913aab21313dc3ceeab8a893916893b533054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25662747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d7c99e10d8ab1a83a9b8ae9755e9912e39a2a9e52da6ce6de8defc71809bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 04:21:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 04:21:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 04:21:27 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:21:28 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 04:21:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02345b26a3d377d58f815ff68ead6a7dd73b699f6c32431c8d20e8f089729c37`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 672.8 KB (672839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedb3d96d801ee542c140b3c61969835a610feec705ca8958b056cca584fce66`  
		Last Modified: Fri, 07 Oct 2022 04:22:23 GMT  
		Size: 22.2 MB (22162052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4889541507d1292f1cc22ab716fe900b3cf01a14362a5fe85f91fbf67a75cee`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:852bfc774229c23356a5d820bf44f86881baa8514ad6e2f20ab62c4e403de23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eefd9c077e3966c82a20fb7d97684c827cc1e65d9c63684ebe18c8076247c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:17 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:22 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:22 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:22 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ced22cf89095c1fa196cdfa7a81f1e06c58396cba3d7aba02c0a0dc15a9091`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 677.6 KB (677556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8c7574d9711fae322abb656d8f6b17662f5f2c4d353b09a116a83bc9fa751a`  
		Last Modified: Sat, 08 Oct 2022 03:59:54 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8974f171927f790c59d4a52f62af80705a746cc0c5e97fbecdc3f03b5e801d17`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:aa2581cd19c9cedc7889a4f8694169cb5337d5cfc77b67e6c6b7e68a6a7c406f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23527803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc42e10eb1bc021727b03128a3ffa88509d49ffda91826e320ce7c000951b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:54 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:54 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:55 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcac61fa6de5b9a13a488b720a6192d410da114e28e9622be993368cd7e6f14e`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 673.9 KB (673910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5d651501b15cd983c2bec1ab8a076859c15803a1b03dff828baf0f1a6a83a8`  
		Last Modified: Thu, 27 Oct 2022 23:01:45 GMT  
		Size: 20.1 MB (20131372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f40d2b1f6b02b45c16a9fa54fd5fbd5d2062d79f726fbd3909b52c2c0c399`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2b98a6729f6acb261b00df5cd442aeba121553d307a2bf4c556b0f2d6db5b1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:1.7.34-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:71ad6a0260772b709548bedfb9d634d97cd28a14fca877bdb6297a9ffd43bb99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734015671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b09c2bb205d96b067404adfd97994511716618d40107644629870147cba58b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 18:17:51 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 12 Oct 2022 18:17:52 GMT
EXPOSE 80
# Wed, 12 Oct 2022 18:17:53 GMT
ENTRYPOINT ["/traefik"]
# Wed, 12 Oct 2022 18:17:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c05aa1874a2d976a43b6d2c3a71b81f3a4f594a5d048a192a33debac9dae8a`  
		Last Modified: Wed, 12 Oct 2022 18:18:48 GMT  
		Size: 22.8 MB (22846075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af5a81401a21645a0408443fe991fd9df7a3f84fdb3bb206fe094dac1fdd6cd`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b38614dda35cd6fd3ea0a8beb5c6dba618af1103fde9a7404ce5720b6c170b`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8152802c5fefe99fcf75179a44df9139a1474ab34a433c273d27152ef4f836d9`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9`

```console
$ docker pull traefik@sha256:b8112aeedf7d261afeeb615d6105984fb4997cff6e0bd8ef9d26341061decffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.9` - linux; amd64

```console
$ docker pull traefik@sha256:710a1be6c3f4e92ac1894c482d64eaeda5b13b5e416ea46a050358b6367ba984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38656611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288889429becfa205fc2887f5b51e8b53d3c32021b7614d350ff54ce88bbd4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:14 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 22:48:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 22:48:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 22:48:41 GMT
EXPOSE 80
# Thu, 27 Oct 2022 22:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 22:48:41 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 22:48:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b4fe8af5e2bd23c9c1a5303b1d320706bc52330058f23c4725df3dadc9cad`  
		Last Modified: Fri, 07 Oct 2022 04:21:55 GMT  
		Size: 673.4 KB (673371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea834e28da0cc4373c270d8a30b17cf4ff012e37b544c8c2a768f43492997ce1`  
		Last Modified: Thu, 27 Oct 2022 22:49:12 GMT  
		Size: 35.2 MB (35159359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5c503d34f7e88b95c5930e79a6bc440d0f9291c825dac16a714a283db65f1`  
		Last Modified: Thu, 27 Oct 2022 22:49:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5f6d8279305cd2439d2ba817891d2f0b6a39a82788cbd8cb70c78cd82e7d71f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31534845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9591f270234191e2457e5ef20e4c9fba74a47169cdb284f6851628341227f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:03 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:08 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:08 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb1837b21ae6f7a69dfce3afba31ef5efecb4def0a933320f1a3913f37eccf`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 677.7 KB (677723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6e95c457c38e18b852bac8b792c9541e77b70517d2a1abe199891c65133ad`  
		Last Modified: Sat, 08 Oct 2022 03:59:25 GMT  
		Size: 28.2 MB (28225628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27574205390cbb62143d6e41ff14490c4edde087ebfaca66345274206956b9b`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8d7e8847186424c52dca377c7f1d088cf0cba624540ef52ff5618febeae0cd76
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35654345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5a2180dc152f67cb26ec8323b70df284053260a6c2635ca3b02855c8c8308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:47 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:47 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419a1f6cc11ff80386f709f63fad8effa6eddf857f09bbdc097ba541fa4bc4a`  
		Last Modified: Thu, 27 Oct 2022 23:01:21 GMT  
		Size: 673.9 KB (673921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47af98fda9734fb5896c0e9b8fbf61a78b7ffa698a1a48893f6630dc21b8861`  
		Last Modified: Thu, 27 Oct 2022 23:01:24 GMT  
		Size: 32.3 MB (32261617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5637806f38472ff253adaf5a6ae5f23fa72be14a95dc14e5206b20acfb25eb8`  
		Last Modified: Thu, 27 Oct 2022 23:01:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.9` - linux; s390x

```console
$ docker pull traefik@sha256:86ff93cc178de9b8f86436b83bc6e896c65edb55cda098b94882253afdd3eb1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32112411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0174719729d126f9205e2bd2f9d55bdd430ac98c573cb2f2b92d2e5c12bcf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 09:57:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 09:57:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 09:57:11 GMT
EXPOSE 80
# Fri, 07 Oct 2022 09:57:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 09:57:12 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 09:57:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cdf710f5b7ee39c5124c50c753228dc9b8b1c1c0a1a38f1413487548565445c3`  
		Last Modified: Tue, 09 Aug 2022 17:42:56 GMT  
		Size: 2.6 MB (2606087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1ec6f28225d3ff13bc2defe049a19ceecab6d949a0e69884c44e7e28279b`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 677.5 KB (677512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1d229f8b015fe7609ece81d9725b607d8ca5314d0f08667adfd7c13a5d5daf`  
		Last Modified: Fri, 07 Oct 2022 09:57:46 GMT  
		Size: 28.8 MB (28828444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd924ce12d473d0268c58ca23de4965014be194f51da2ab5fa66fbb94384d8e5`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:49dcb74f197aadf03edc59303f9936b06ce3be7e947c74607eaaeb3b6344fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:2.9-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:6207a4986cc11e02da65392bfd152733786b87c433a09241a7d5fec2d8988c0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809165937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0500e1f3123ac9672f2d965c2271d84c4d18d4338fb7e9bd81661a0f8588843a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Oct 2022 21:26:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 27 Oct 2022 21:26:17 GMT
EXPOSE 80
# Thu, 27 Oct 2022 21:26:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 21:26:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807f285722ea86cc3d70eac642b38577e2a9058a8e6b90c49dbd064fea4997a`  
		Last Modified: Thu, 27 Oct 2022 21:26:53 GMT  
		Size: 35.7 MB (35661956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332f98b1e5522f72374c2b31a9ebe3adf1feb1b779a72319c0913b32671e42bb`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee544e98bde8d908e40e363c1800ca618bfab13e2ca6ff3a13dcd48d101fa51`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13601bc1cce5482abf666b88a9b7183ff6260c56ebb72603196aab3f51565a0`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9.4`

```console
$ docker pull traefik@sha256:eb15c134829bd8d68eb86fb967acb3a29c594dd7c53a081668a4cc667020ee41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `traefik:2.9.4` - linux; amd64

```console
$ docker pull traefik@sha256:710a1be6c3f4e92ac1894c482d64eaeda5b13b5e416ea46a050358b6367ba984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38656611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288889429becfa205fc2887f5b51e8b53d3c32021b7614d350ff54ce88bbd4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:14 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 22:48:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 22:48:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 22:48:41 GMT
EXPOSE 80
# Thu, 27 Oct 2022 22:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 22:48:41 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 22:48:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b4fe8af5e2bd23c9c1a5303b1d320706bc52330058f23c4725df3dadc9cad`  
		Last Modified: Fri, 07 Oct 2022 04:21:55 GMT  
		Size: 673.4 KB (673371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea834e28da0cc4373c270d8a30b17cf4ff012e37b544c8c2a768f43492997ce1`  
		Last Modified: Thu, 27 Oct 2022 22:49:12 GMT  
		Size: 35.2 MB (35159359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5c503d34f7e88b95c5930e79a6bc440d0f9291c825dac16a714a283db65f1`  
		Last Modified: Thu, 27 Oct 2022 22:49:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.9.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8d7e8847186424c52dca377c7f1d088cf0cba624540ef52ff5618febeae0cd76
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35654345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5a2180dc152f67cb26ec8323b70df284053260a6c2635ca3b02855c8c8308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:47 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:47 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419a1f6cc11ff80386f709f63fad8effa6eddf857f09bbdc097ba541fa4bc4a`  
		Last Modified: Thu, 27 Oct 2022 23:01:21 GMT  
		Size: 673.9 KB (673921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47af98fda9734fb5896c0e9b8fbf61a78b7ffa698a1a48893f6630dc21b8861`  
		Last Modified: Thu, 27 Oct 2022 23:01:24 GMT  
		Size: 32.3 MB (32261617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5637806f38472ff253adaf5a6ae5f23fa72be14a95dc14e5206b20acfb25eb8`  
		Last Modified: Thu, 27 Oct 2022 23:01:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:49dcb74f197aadf03edc59303f9936b06ce3be7e947c74607eaaeb3b6344fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:2.9.4-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:6207a4986cc11e02da65392bfd152733786b87c433a09241a7d5fec2d8988c0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809165937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0500e1f3123ac9672f2d965c2271d84c4d18d4338fb7e9bd81661a0f8588843a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Oct 2022 21:26:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 27 Oct 2022 21:26:17 GMT
EXPOSE 80
# Thu, 27 Oct 2022 21:26:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 21:26:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807f285722ea86cc3d70eac642b38577e2a9058a8e6b90c49dbd064fea4997a`  
		Last Modified: Thu, 27 Oct 2022 21:26:53 GMT  
		Size: 35.7 MB (35661956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332f98b1e5522f72374c2b31a9ebe3adf1feb1b779a72319c0913b32671e42bb`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee544e98bde8d908e40e363c1800ca618bfab13e2ca6ff3a13dcd48d101fa51`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13601bc1cce5482abf666b88a9b7183ff6260c56ebb72603196aab3f51565a0`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:banon`

```console
$ docker pull traefik@sha256:b8112aeedf7d261afeeb615d6105984fb4997cff6e0bd8ef9d26341061decffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:banon` - linux; amd64

```console
$ docker pull traefik@sha256:710a1be6c3f4e92ac1894c482d64eaeda5b13b5e416ea46a050358b6367ba984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38656611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288889429becfa205fc2887f5b51e8b53d3c32021b7614d350ff54ce88bbd4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:14 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 22:48:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 22:48:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 22:48:41 GMT
EXPOSE 80
# Thu, 27 Oct 2022 22:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 22:48:41 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 22:48:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b4fe8af5e2bd23c9c1a5303b1d320706bc52330058f23c4725df3dadc9cad`  
		Last Modified: Fri, 07 Oct 2022 04:21:55 GMT  
		Size: 673.4 KB (673371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea834e28da0cc4373c270d8a30b17cf4ff012e37b544c8c2a768f43492997ce1`  
		Last Modified: Thu, 27 Oct 2022 22:49:12 GMT  
		Size: 35.2 MB (35159359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5c503d34f7e88b95c5930e79a6bc440d0f9291c825dac16a714a283db65f1`  
		Last Modified: Thu, 27 Oct 2022 22:49:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5f6d8279305cd2439d2ba817891d2f0b6a39a82788cbd8cb70c78cd82e7d71f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31534845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9591f270234191e2457e5ef20e4c9fba74a47169cdb284f6851628341227f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:03 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:08 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:08 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb1837b21ae6f7a69dfce3afba31ef5efecb4def0a933320f1a3913f37eccf`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 677.7 KB (677723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6e95c457c38e18b852bac8b792c9541e77b70517d2a1abe199891c65133ad`  
		Last Modified: Sat, 08 Oct 2022 03:59:25 GMT  
		Size: 28.2 MB (28225628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27574205390cbb62143d6e41ff14490c4edde087ebfaca66345274206956b9b`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8d7e8847186424c52dca377c7f1d088cf0cba624540ef52ff5618febeae0cd76
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35654345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5a2180dc152f67cb26ec8323b70df284053260a6c2635ca3b02855c8c8308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:47 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:47 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419a1f6cc11ff80386f709f63fad8effa6eddf857f09bbdc097ba541fa4bc4a`  
		Last Modified: Thu, 27 Oct 2022 23:01:21 GMT  
		Size: 673.9 KB (673921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47af98fda9734fb5896c0e9b8fbf61a78b7ffa698a1a48893f6630dc21b8861`  
		Last Modified: Thu, 27 Oct 2022 23:01:24 GMT  
		Size: 32.3 MB (32261617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5637806f38472ff253adaf5a6ae5f23fa72be14a95dc14e5206b20acfb25eb8`  
		Last Modified: Thu, 27 Oct 2022 23:01:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; s390x

```console
$ docker pull traefik@sha256:86ff93cc178de9b8f86436b83bc6e896c65edb55cda098b94882253afdd3eb1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32112411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0174719729d126f9205e2bd2f9d55bdd430ac98c573cb2f2b92d2e5c12bcf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 09:57:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 09:57:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 09:57:11 GMT
EXPOSE 80
# Fri, 07 Oct 2022 09:57:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 09:57:12 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 09:57:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cdf710f5b7ee39c5124c50c753228dc9b8b1c1c0a1a38f1413487548565445c3`  
		Last Modified: Tue, 09 Aug 2022 17:42:56 GMT  
		Size: 2.6 MB (2606087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1ec6f28225d3ff13bc2defe049a19ceecab6d949a0e69884c44e7e28279b`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 677.5 KB (677512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1d229f8b015fe7609ece81d9725b607d8ca5314d0f08667adfd7c13a5d5daf`  
		Last Modified: Fri, 07 Oct 2022 09:57:46 GMT  
		Size: 28.8 MB (28828444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd924ce12d473d0268c58ca23de4965014be194f51da2ab5fa66fbb94384d8e5`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:banon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:49dcb74f197aadf03edc59303f9936b06ce3be7e947c74607eaaeb3b6344fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:banon-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:6207a4986cc11e02da65392bfd152733786b87c433a09241a7d5fec2d8988c0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809165937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0500e1f3123ac9672f2d965c2271d84c4d18d4338fb7e9bd81661a0f8588843a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Oct 2022 21:26:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 27 Oct 2022 21:26:17 GMT
EXPOSE 80
# Thu, 27 Oct 2022 21:26:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 21:26:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807f285722ea86cc3d70eac642b38577e2a9058a8e6b90c49dbd064fea4997a`  
		Last Modified: Thu, 27 Oct 2022 21:26:53 GMT  
		Size: 35.7 MB (35661956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332f98b1e5522f72374c2b31a9ebe3adf1feb1b779a72319c0913b32671e42bb`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee544e98bde8d908e40e363c1800ca618bfab13e2ca6ff3a13dcd48d101fa51`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13601bc1cce5482abf666b88a9b7183ff6260c56ebb72603196aab3f51565a0`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:b8112aeedf7d261afeeb615d6105984fb4997cff6e0bd8ef9d26341061decffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:710a1be6c3f4e92ac1894c482d64eaeda5b13b5e416ea46a050358b6367ba984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38656611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288889429becfa205fc2887f5b51e8b53d3c32021b7614d350ff54ce88bbd4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:14 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 22:48:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 22:48:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 22:48:41 GMT
EXPOSE 80
# Thu, 27 Oct 2022 22:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 22:48:41 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 22:48:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b4fe8af5e2bd23c9c1a5303b1d320706bc52330058f23c4725df3dadc9cad`  
		Last Modified: Fri, 07 Oct 2022 04:21:55 GMT  
		Size: 673.4 KB (673371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea834e28da0cc4373c270d8a30b17cf4ff012e37b544c8c2a768f43492997ce1`  
		Last Modified: Thu, 27 Oct 2022 22:49:12 GMT  
		Size: 35.2 MB (35159359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5c503d34f7e88b95c5930e79a6bc440d0f9291c825dac16a714a283db65f1`  
		Last Modified: Thu, 27 Oct 2022 22:49:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5f6d8279305cd2439d2ba817891d2f0b6a39a82788cbd8cb70c78cd82e7d71f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31534845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9591f270234191e2457e5ef20e4c9fba74a47169cdb284f6851628341227f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:03 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:08 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:08 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb1837b21ae6f7a69dfce3afba31ef5efecb4def0a933320f1a3913f37eccf`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 677.7 KB (677723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6e95c457c38e18b852bac8b792c9541e77b70517d2a1abe199891c65133ad`  
		Last Modified: Sat, 08 Oct 2022 03:59:25 GMT  
		Size: 28.2 MB (28225628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27574205390cbb62143d6e41ff14490c4edde087ebfaca66345274206956b9b`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8d7e8847186424c52dca377c7f1d088cf0cba624540ef52ff5618febeae0cd76
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35654345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5a2180dc152f67cb26ec8323b70df284053260a6c2635ca3b02855c8c8308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:47 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:47 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419a1f6cc11ff80386f709f63fad8effa6eddf857f09bbdc097ba541fa4bc4a`  
		Last Modified: Thu, 27 Oct 2022 23:01:21 GMT  
		Size: 673.9 KB (673921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47af98fda9734fb5896c0e9b8fbf61a78b7ffa698a1a48893f6630dc21b8861`  
		Last Modified: Thu, 27 Oct 2022 23:01:24 GMT  
		Size: 32.3 MB (32261617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5637806f38472ff253adaf5a6ae5f23fa72be14a95dc14e5206b20acfb25eb8`  
		Last Modified: Thu, 27 Oct 2022 23:01:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:86ff93cc178de9b8f86436b83bc6e896c65edb55cda098b94882253afdd3eb1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32112411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0174719729d126f9205e2bd2f9d55bdd430ac98c573cb2f2b92d2e5c12bcf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 09:57:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 09:57:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 09:57:11 GMT
EXPOSE 80
# Fri, 07 Oct 2022 09:57:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 09:57:12 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 09:57:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cdf710f5b7ee39c5124c50c753228dc9b8b1c1c0a1a38f1413487548565445c3`  
		Last Modified: Tue, 09 Aug 2022 17:42:56 GMT  
		Size: 2.6 MB (2606087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1ec6f28225d3ff13bc2defe049a19ceecab6d949a0e69884c44e7e28279b`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 677.5 KB (677512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1d229f8b015fe7609ece81d9725b607d8ca5314d0f08667adfd7c13a5d5daf`  
		Last Modified: Fri, 07 Oct 2022 09:57:46 GMT  
		Size: 28.8 MB (28828444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd924ce12d473d0268c58ca23de4965014be194f51da2ab5fa66fbb94384d8e5`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:74c0df9a0b72ee3ccfeff333a8a2ede28c27d539918dcbcf04c523b3c88c533e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:9248f7f17d44a02872613d652aff91856f928ebc400d037cd3439731da4cecbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22605595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dd394242b858ec3a77eec6506ea614377091f1904f704d3412983c1be8c0cd`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 07 Oct 2022 04:21:34 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 07 Oct 2022 04:21:35 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 07 Oct 2022 04:21:35 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:35 GMT
VOLUME [/tmp]
# Fri, 07 Oct 2022 04:21:35 GMT
ENTRYPOINT ["/traefik"]
# Fri, 07 Oct 2022 04:21:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa79c7609bd35acb6baeec95c0534de9f28c053bb3b54b53c4831b70e4a2b6e2`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 320.1 KB (320103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b58027c881a56cde12f5ad6ba79f399d338b083423a96ae8fdb32a53f55af9`  
		Last Modified: Fri, 07 Oct 2022 04:22:44 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84aae39edfd57a3d7eb7d5f3506e471031166e65d061c8be54fca77258b6140c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b13bdeaf794060f706e8061be10b71e7ef64882356982de89daec674fe698c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 08 Oct 2022 03:58:30 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 08 Oct 2022 03:58:31 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Sat, 08 Oct 2022 03:58:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Sat, 08 Oct 2022 03:58:33 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:33 GMT
VOLUME [/tmp]
# Sat, 08 Oct 2022 03:58:33 GMT
ENTRYPOINT ["/traefik"]
# Sat, 08 Oct 2022 03:58:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:480f18b6c0179f0ed54861403bbe3503ed26203a6307b30978f4edb95c7a1f03`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 123.5 KB (123539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e3fa745c422a0bf87c538e124bc46e1c0a2c2fd0c50501c4e558da00084fc`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 320.1 KB (320098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115198abd673e94528474879115112ca2bd769da4a9f7c9cce6302d59f3d456`  
		Last Modified: Sat, 08 Oct 2022 04:00:21 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:998889d8da01c621040b155856bb41038aa1a65896c86abb4915d9e7710a07eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20574991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71027e8a7dfc0095b24f9fbbf590702387cb0bbb08c7da94646dea0044028799`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 27 Oct 2022 23:00:59 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Thu, 27 Oct 2022 23:01:00 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 27 Oct 2022 23:01:00 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:01:00 GMT
VOLUME [/tmp]
# Thu, 27 Oct 2022 23:01:00 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 23:01:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dcf3621c695e89e69ec66c2e79a79a8b1c5cc7d4b33794c23f40dd4e1c589a`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 320.1 KB (320107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a1a0cc2676bf63edfe4593a0283c5204b2434451e09da0f8acc781f6c031b`  
		Last Modified: Thu, 27 Oct 2022 23:02:03 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:2069e9421447a979d3b452395bb820361c08d83de00c636e0ab2ac0603e104e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26fa7cd56b81852ea9f61e45df0913aab21313dc3ceeab8a893916893b533054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25662747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d7c99e10d8ab1a83a9b8ae9755e9912e39a2a9e52da6ce6de8defc71809bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 04:21:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 04:21:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 04:21:27 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:21:28 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 04:21:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02345b26a3d377d58f815ff68ead6a7dd73b699f6c32431c8d20e8f089729c37`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 672.8 KB (672839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedb3d96d801ee542c140b3c61969835a610feec705ca8958b056cca584fce66`  
		Last Modified: Fri, 07 Oct 2022 04:22:23 GMT  
		Size: 22.2 MB (22162052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4889541507d1292f1cc22ab716fe900b3cf01a14362a5fe85f91fbf67a75cee`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:852bfc774229c23356a5d820bf44f86881baa8514ad6e2f20ab62c4e403de23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eefd9c077e3966c82a20fb7d97684c827cc1e65d9c63684ebe18c8076247c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:17 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:22 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:22 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:22 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ced22cf89095c1fa196cdfa7a81f1e06c58396cba3d7aba02c0a0dc15a9091`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 677.6 KB (677556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8c7574d9711fae322abb656d8f6b17662f5f2c4d353b09a116a83bc9fa751a`  
		Last Modified: Sat, 08 Oct 2022 03:59:54 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8974f171927f790c59d4a52f62af80705a746cc0c5e97fbecdc3f03b5e801d17`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:aa2581cd19c9cedc7889a4f8694169cb5337d5cfc77b67e6c6b7e68a6a7c406f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23527803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc42e10eb1bc021727b03128a3ffa88509d49ffda91826e320ce7c000951b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:54 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:54 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:55 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcac61fa6de5b9a13a488b720a6192d410da114e28e9622be993368cd7e6f14e`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 673.9 KB (673910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5d651501b15cd983c2bec1ab8a076859c15803a1b03dff828baf0f1a6a83a8`  
		Last Modified: Thu, 27 Oct 2022 23:01:45 GMT  
		Size: 20.1 MB (20131372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f40d2b1f6b02b45c16a9fa54fd5fbd5d2062d79f726fbd3909b52c2c0c399`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2b98a6729f6acb261b00df5cd442aeba121553d307a2bf4c556b0f2d6db5b1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:71ad6a0260772b709548bedfb9d634d97cd28a14fca877bdb6297a9ffd43bb99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734015671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b09c2bb205d96b067404adfd97994511716618d40107644629870147cba58b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 18:17:51 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 12 Oct 2022 18:17:52 GMT
EXPOSE 80
# Wed, 12 Oct 2022 18:17:53 GMT
ENTRYPOINT ["/traefik"]
# Wed, 12 Oct 2022 18:17:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c05aa1874a2d976a43b6d2c3a71b81f3a4f594a5d048a192a33debac9dae8a`  
		Last Modified: Wed, 12 Oct 2022 18:18:48 GMT  
		Size: 22.8 MB (22846075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af5a81401a21645a0408443fe991fd9df7a3f84fdb3bb206fe094dac1fdd6cd`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b38614dda35cd6fd3ea0a8beb5c6dba618af1103fde9a7404ce5720b6c170b`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8152802c5fefe99fcf75179a44df9139a1474ab34a433c273d27152ef4f836d9`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:74c0df9a0b72ee3ccfeff333a8a2ede28c27d539918dcbcf04c523b3c88c533e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:9248f7f17d44a02872613d652aff91856f928ebc400d037cd3439731da4cecbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22605595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dd394242b858ec3a77eec6506ea614377091f1904f704d3412983c1be8c0cd`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 07 Oct 2022 04:21:34 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 07 Oct 2022 04:21:35 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 07 Oct 2022 04:21:35 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:35 GMT
VOLUME [/tmp]
# Fri, 07 Oct 2022 04:21:35 GMT
ENTRYPOINT ["/traefik"]
# Fri, 07 Oct 2022 04:21:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa79c7609bd35acb6baeec95c0534de9f28c053bb3b54b53c4831b70e4a2b6e2`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 320.1 KB (320103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b58027c881a56cde12f5ad6ba79f399d338b083423a96ae8fdb32a53f55af9`  
		Last Modified: Fri, 07 Oct 2022 04:22:44 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84aae39edfd57a3d7eb7d5f3506e471031166e65d061c8be54fca77258b6140c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b13bdeaf794060f706e8061be10b71e7ef64882356982de89daec674fe698c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 08 Oct 2022 03:58:30 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 08 Oct 2022 03:58:31 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Sat, 08 Oct 2022 03:58:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Sat, 08 Oct 2022 03:58:33 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:33 GMT
VOLUME [/tmp]
# Sat, 08 Oct 2022 03:58:33 GMT
ENTRYPOINT ["/traefik"]
# Sat, 08 Oct 2022 03:58:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:480f18b6c0179f0ed54861403bbe3503ed26203a6307b30978f4edb95c7a1f03`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 123.5 KB (123539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e3fa745c422a0bf87c538e124bc46e1c0a2c2fd0c50501c4e558da00084fc`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 320.1 KB (320098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115198abd673e94528474879115112ca2bd769da4a9f7c9cce6302d59f3d456`  
		Last Modified: Sat, 08 Oct 2022 04:00:21 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:998889d8da01c621040b155856bb41038aa1a65896c86abb4915d9e7710a07eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20574991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71027e8a7dfc0095b24f9fbbf590702387cb0bbb08c7da94646dea0044028799`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 27 Oct 2022 23:00:59 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Thu, 27 Oct 2022 23:01:00 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 27 Oct 2022 23:01:00 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:01:00 GMT
VOLUME [/tmp]
# Thu, 27 Oct 2022 23:01:00 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 23:01:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dcf3621c695e89e69ec66c2e79a79a8b1c5cc7d4b33794c23f40dd4e1c589a`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 320.1 KB (320107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a1a0cc2676bf63edfe4593a0283c5204b2434451e09da0f8acc781f6c031b`  
		Last Modified: Thu, 27 Oct 2022 23:02:03 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:2069e9421447a979d3b452395bb820361c08d83de00c636e0ab2ac0603e104e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26fa7cd56b81852ea9f61e45df0913aab21313dc3ceeab8a893916893b533054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25662747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d7c99e10d8ab1a83a9b8ae9755e9912e39a2a9e52da6ce6de8defc71809bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 04:21:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 04:21:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 04:21:27 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:21:28 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 04:21:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02345b26a3d377d58f815ff68ead6a7dd73b699f6c32431c8d20e8f089729c37`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 672.8 KB (672839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedb3d96d801ee542c140b3c61969835a610feec705ca8958b056cca584fce66`  
		Last Modified: Fri, 07 Oct 2022 04:22:23 GMT  
		Size: 22.2 MB (22162052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4889541507d1292f1cc22ab716fe900b3cf01a14362a5fe85f91fbf67a75cee`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:852bfc774229c23356a5d820bf44f86881baa8514ad6e2f20ab62c4e403de23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eefd9c077e3966c82a20fb7d97684c827cc1e65d9c63684ebe18c8076247c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:17 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:22 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:22 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:22 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ced22cf89095c1fa196cdfa7a81f1e06c58396cba3d7aba02c0a0dc15a9091`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 677.6 KB (677556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8c7574d9711fae322abb656d8f6b17662f5f2c4d353b09a116a83bc9fa751a`  
		Last Modified: Sat, 08 Oct 2022 03:59:54 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8974f171927f790c59d4a52f62af80705a746cc0c5e97fbecdc3f03b5e801d17`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:aa2581cd19c9cedc7889a4f8694169cb5337d5cfc77b67e6c6b7e68a6a7c406f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23527803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc42e10eb1bc021727b03128a3ffa88509d49ffda91826e320ce7c000951b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:54 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:54 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:55 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcac61fa6de5b9a13a488b720a6192d410da114e28e9622be993368cd7e6f14e`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 673.9 KB (673910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5d651501b15cd983c2bec1ab8a076859c15803a1b03dff828baf0f1a6a83a8`  
		Last Modified: Thu, 27 Oct 2022 23:01:45 GMT  
		Size: 20.1 MB (20131372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f40d2b1f6b02b45c16a9fa54fd5fbd5d2062d79f726fbd3909b52c2c0c399`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2b98a6729f6acb261b00df5cd442aeba121553d307a2bf4c556b0f2d6db5b1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:71ad6a0260772b709548bedfb9d634d97cd28a14fca877bdb6297a9ffd43bb99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734015671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b09c2bb205d96b067404adfd97994511716618d40107644629870147cba58b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 18:17:51 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 12 Oct 2022 18:17:52 GMT
EXPOSE 80
# Wed, 12 Oct 2022 18:17:53 GMT
ENTRYPOINT ["/traefik"]
# Wed, 12 Oct 2022 18:17:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c05aa1874a2d976a43b6d2c3a71b81f3a4f594a5d048a192a33debac9dae8a`  
		Last Modified: Wed, 12 Oct 2022 18:18:48 GMT  
		Size: 22.8 MB (22846075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af5a81401a21645a0408443fe991fd9df7a3f84fdb3bb206fe094dac1fdd6cd`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b38614dda35cd6fd3ea0a8beb5c6dba618af1103fde9a7404ce5720b6c170b`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8152802c5fefe99fcf75179a44df9139a1474ab34a433c273d27152ef4f836d9`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34`

```console
$ docker pull traefik@sha256:74c0df9a0b72ee3ccfeff333a8a2ede28c27d539918dcbcf04c523b3c88c533e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:9248f7f17d44a02872613d652aff91856f928ebc400d037cd3439731da4cecbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22605595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dd394242b858ec3a77eec6506ea614377091f1904f704d3412983c1be8c0cd`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 07 Oct 2022 04:21:34 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 07 Oct 2022 04:21:35 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 07 Oct 2022 04:21:35 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:35 GMT
VOLUME [/tmp]
# Fri, 07 Oct 2022 04:21:35 GMT
ENTRYPOINT ["/traefik"]
# Fri, 07 Oct 2022 04:21:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa79c7609bd35acb6baeec95c0534de9f28c053bb3b54b53c4831b70e4a2b6e2`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 320.1 KB (320103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b58027c881a56cde12f5ad6ba79f399d338b083423a96ae8fdb32a53f55af9`  
		Last Modified: Fri, 07 Oct 2022 04:22:44 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84aae39edfd57a3d7eb7d5f3506e471031166e65d061c8be54fca77258b6140c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b13bdeaf794060f706e8061be10b71e7ef64882356982de89daec674fe698c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 08 Oct 2022 03:58:30 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 08 Oct 2022 03:58:31 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Sat, 08 Oct 2022 03:58:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Sat, 08 Oct 2022 03:58:33 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:33 GMT
VOLUME [/tmp]
# Sat, 08 Oct 2022 03:58:33 GMT
ENTRYPOINT ["/traefik"]
# Sat, 08 Oct 2022 03:58:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:480f18b6c0179f0ed54861403bbe3503ed26203a6307b30978f4edb95c7a1f03`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 123.5 KB (123539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e3fa745c422a0bf87c538e124bc46e1c0a2c2fd0c50501c4e558da00084fc`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 320.1 KB (320098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115198abd673e94528474879115112ca2bd769da4a9f7c9cce6302d59f3d456`  
		Last Modified: Sat, 08 Oct 2022 04:00:21 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:998889d8da01c621040b155856bb41038aa1a65896c86abb4915d9e7710a07eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20574991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71027e8a7dfc0095b24f9fbbf590702387cb0bbb08c7da94646dea0044028799`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 27 Oct 2022 23:00:59 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Thu, 27 Oct 2022 23:01:00 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 27 Oct 2022 23:01:00 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:01:00 GMT
VOLUME [/tmp]
# Thu, 27 Oct 2022 23:01:00 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 23:01:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2dcf3621c695e89e69ec66c2e79a79a8b1c5cc7d4b33794c23f40dd4e1c589a`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 320.1 KB (320107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a1a0cc2676bf63edfe4593a0283c5204b2434451e09da0f8acc781f6c031b`  
		Last Modified: Thu, 27 Oct 2022 23:02:03 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-alpine`

```console
$ docker pull traefik@sha256:2069e9421447a979d3b452395bb820361c08d83de00c636e0ab2ac0603e104e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26fa7cd56b81852ea9f61e45df0913aab21313dc3ceeab8a893916893b533054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25662747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d7c99e10d8ab1a83a9b8ae9755e9912e39a2a9e52da6ce6de8defc71809bd8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:23 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 04:21:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 04:21:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 04:21:27 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 04:21:28 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 04:21:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02345b26a3d377d58f815ff68ead6a7dd73b699f6c32431c8d20e8f089729c37`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 672.8 KB (672839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedb3d96d801ee542c140b3c61969835a610feec705ca8958b056cca584fce66`  
		Last Modified: Fri, 07 Oct 2022 04:22:23 GMT  
		Size: 22.2 MB (22162052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4889541507d1292f1cc22ab716fe900b3cf01a14362a5fe85f91fbf67a75cee`  
		Last Modified: Fri, 07 Oct 2022 04:22:19 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:852bfc774229c23356a5d820bf44f86881baa8514ad6e2f20ab62c4e403de23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8eefd9c077e3966c82a20fb7d97684c827cc1e65d9c63684ebe18c8076247c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:17 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:22 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:22 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:22 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ced22cf89095c1fa196cdfa7a81f1e06c58396cba3d7aba02c0a0dc15a9091`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 677.6 KB (677556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8c7574d9711fae322abb656d8f6b17662f5f2c4d353b09a116a83bc9fa751a`  
		Last Modified: Sat, 08 Oct 2022 03:59:54 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8974f171927f790c59d4a52f62af80705a746cc0c5e97fbecdc3f03b5e801d17`  
		Last Modified: Sat, 08 Oct 2022 03:59:50 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:aa2581cd19c9cedc7889a4f8694169cb5337d5cfc77b67e6c6b7e68a6a7c406f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23527803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc42e10eb1bc021727b03128a3ffa88509d49ffda91826e320ce7c000951b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:54 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:54 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:55 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcac61fa6de5b9a13a488b720a6192d410da114e28e9622be993368cd7e6f14e`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 673.9 KB (673910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5d651501b15cd983c2bec1ab8a076859c15803a1b03dff828baf0f1a6a83a8`  
		Last Modified: Thu, 27 Oct 2022 23:01:45 GMT  
		Size: 20.1 MB (20131372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14f40d2b1f6b02b45c16a9fa54fd5fbd5d2062d79f726fbd3909b52c2c0c399`  
		Last Modified: Thu, 27 Oct 2022 23:01:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2b98a6729f6acb261b00df5cd442aeba121553d307a2bf4c556b0f2d6db5b1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:v1.7.34-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:71ad6a0260772b709548bedfb9d634d97cd28a14fca877bdb6297a9ffd43bb99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734015671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b09c2bb205d96b067404adfd97994511716618d40107644629870147cba58b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 18:17:51 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 12 Oct 2022 18:17:52 GMT
EXPOSE 80
# Wed, 12 Oct 2022 18:17:53 GMT
ENTRYPOINT ["/traefik"]
# Wed, 12 Oct 2022 18:17:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c05aa1874a2d976a43b6d2c3a71b81f3a4f594a5d048a192a33debac9dae8a`  
		Last Modified: Wed, 12 Oct 2022 18:18:48 GMT  
		Size: 22.8 MB (22846075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af5a81401a21645a0408443fe991fd9df7a3f84fdb3bb206fe094dac1fdd6cd`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b38614dda35cd6fd3ea0a8beb5c6dba618af1103fde9a7404ce5720b6c170b`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8152802c5fefe99fcf75179a44df9139a1474ab34a433c273d27152ef4f836d9`  
		Last Modified: Wed, 12 Oct 2022 18:18:43 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9`

```console
$ docker pull traefik@sha256:b8112aeedf7d261afeeb615d6105984fb4997cff6e0bd8ef9d26341061decffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.9` - linux; amd64

```console
$ docker pull traefik@sha256:710a1be6c3f4e92ac1894c482d64eaeda5b13b5e416ea46a050358b6367ba984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38656611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288889429becfa205fc2887f5b51e8b53d3c32021b7614d350ff54ce88bbd4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:14 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 22:48:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 22:48:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 22:48:41 GMT
EXPOSE 80
# Thu, 27 Oct 2022 22:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 22:48:41 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 22:48:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b4fe8af5e2bd23c9c1a5303b1d320706bc52330058f23c4725df3dadc9cad`  
		Last Modified: Fri, 07 Oct 2022 04:21:55 GMT  
		Size: 673.4 KB (673371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea834e28da0cc4373c270d8a30b17cf4ff012e37b544c8c2a768f43492997ce1`  
		Last Modified: Thu, 27 Oct 2022 22:49:12 GMT  
		Size: 35.2 MB (35159359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5c503d34f7e88b95c5930e79a6bc440d0f9291c825dac16a714a283db65f1`  
		Last Modified: Thu, 27 Oct 2022 22:49:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5f6d8279305cd2439d2ba817891d2f0b6a39a82788cbd8cb70c78cd82e7d71f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31534845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9591f270234191e2457e5ef20e4c9fba74a47169cdb284f6851628341227f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:58:03 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 08 Oct 2022 03:58:07 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 08 Oct 2022 03:58:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 08 Oct 2022 03:58:08 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Oct 2022 03:58:08 GMT
CMD ["traefik"]
# Sat, 08 Oct 2022 03:58:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb1837b21ae6f7a69dfce3afba31ef5efecb4def0a933320f1a3913f37eccf`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 677.7 KB (677723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce6e95c457c38e18b852bac8b792c9541e77b70517d2a1abe199891c65133ad`  
		Last Modified: Sat, 08 Oct 2022 03:59:25 GMT  
		Size: 28.2 MB (28225628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27574205390cbb62143d6e41ff14490c4edde087ebfaca66345274206956b9b`  
		Last Modified: Sat, 08 Oct 2022 03:59:20 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8d7e8847186424c52dca377c7f1d088cf0cba624540ef52ff5618febeae0cd76
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35654345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5a2180dc152f67cb26ec8323b70df284053260a6c2635ca3b02855c8c8308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:47 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:47 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419a1f6cc11ff80386f709f63fad8effa6eddf857f09bbdc097ba541fa4bc4a`  
		Last Modified: Thu, 27 Oct 2022 23:01:21 GMT  
		Size: 673.9 KB (673921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47af98fda9734fb5896c0e9b8fbf61a78b7ffa698a1a48893f6630dc21b8861`  
		Last Modified: Thu, 27 Oct 2022 23:01:24 GMT  
		Size: 32.3 MB (32261617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5637806f38472ff253adaf5a6ae5f23fa72be14a95dc14e5206b20acfb25eb8`  
		Last Modified: Thu, 27 Oct 2022 23:01:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.9` - linux; s390x

```console
$ docker pull traefik@sha256:86ff93cc178de9b8f86436b83bc6e896c65edb55cda098b94882253afdd3eb1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32112411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0174719729d126f9205e2bd2f9d55bdd430ac98c573cb2f2b92d2e5c12bcf9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 07 Oct 2022 09:57:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.1/traefik_v2.9.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 07 Oct 2022 09:57:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 07 Oct 2022 09:57:11 GMT
EXPOSE 80
# Fri, 07 Oct 2022 09:57:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Oct 2022 09:57:12 GMT
CMD ["traefik"]
# Fri, 07 Oct 2022 09:57:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cdf710f5b7ee39c5124c50c753228dc9b8b1c1c0a1a38f1413487548565445c3`  
		Last Modified: Tue, 09 Aug 2022 17:42:56 GMT  
		Size: 2.6 MB (2606087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1ec6f28225d3ff13bc2defe049a19ceecab6d949a0e69884c44e7e28279b`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 677.5 KB (677512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1d229f8b015fe7609ece81d9725b607d8ca5314d0f08667adfd7c13a5d5daf`  
		Last Modified: Fri, 07 Oct 2022 09:57:46 GMT  
		Size: 28.8 MB (28828444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd924ce12d473d0268c58ca23de4965014be194f51da2ab5fa66fbb94384d8e5`  
		Last Modified: Fri, 07 Oct 2022 09:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:49dcb74f197aadf03edc59303f9936b06ce3be7e947c74607eaaeb3b6344fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:v2.9-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:6207a4986cc11e02da65392bfd152733786b87c433a09241a7d5fec2d8988c0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809165937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0500e1f3123ac9672f2d965c2271d84c4d18d4338fb7e9bd81661a0f8588843a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Oct 2022 21:26:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 27 Oct 2022 21:26:17 GMT
EXPOSE 80
# Thu, 27 Oct 2022 21:26:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 21:26:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807f285722ea86cc3d70eac642b38577e2a9058a8e6b90c49dbd064fea4997a`  
		Last Modified: Thu, 27 Oct 2022 21:26:53 GMT  
		Size: 35.7 MB (35661956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332f98b1e5522f72374c2b31a9ebe3adf1feb1b779a72319c0913b32671e42bb`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee544e98bde8d908e40e363c1800ca618bfab13e2ca6ff3a13dcd48d101fa51`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13601bc1cce5482abf666b88a9b7183ff6260c56ebb72603196aab3f51565a0`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9.4`

```console
$ docker pull traefik@sha256:eb15c134829bd8d68eb86fb967acb3a29c594dd7c53a081668a4cc667020ee41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `traefik:v2.9.4` - linux; amd64

```console
$ docker pull traefik@sha256:710a1be6c3f4e92ac1894c482d64eaeda5b13b5e416ea46a050358b6367ba984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38656611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288889429becfa205fc2887f5b51e8b53d3c32021b7614d350ff54ce88bbd4a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:21:14 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 22:48:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 22:48:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 22:48:41 GMT
EXPOSE 80
# Thu, 27 Oct 2022 22:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 22:48:41 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 22:48:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62b4fe8af5e2bd23c9c1a5303b1d320706bc52330058f23c4725df3dadc9cad`  
		Last Modified: Fri, 07 Oct 2022 04:21:55 GMT  
		Size: 673.4 KB (673371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea834e28da0cc4373c270d8a30b17cf4ff012e37b544c8c2a768f43492997ce1`  
		Last Modified: Thu, 27 Oct 2022 22:49:12 GMT  
		Size: 35.2 MB (35159359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5c503d34f7e88b95c5930e79a6bc440d0f9291c825dac16a714a283db65f1`  
		Last Modified: Thu, 27 Oct 2022 22:49:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.9.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8d7e8847186424c52dca377c7f1d088cf0cba624540ef52ff5618febeae0cd76
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35654345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5a2180dc152f67cb26ec8323b70df284053260a6c2635ca3b02855c8c8308`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 23:00:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:00:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:00:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:00:47 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:00:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:00:47 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:00:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419a1f6cc11ff80386f709f63fad8effa6eddf857f09bbdc097ba541fa4bc4a`  
		Last Modified: Thu, 27 Oct 2022 23:01:21 GMT  
		Size: 673.9 KB (673921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47af98fda9734fb5896c0e9b8fbf61a78b7ffa698a1a48893f6630dc21b8861`  
		Last Modified: Thu, 27 Oct 2022 23:01:24 GMT  
		Size: 32.3 MB (32261617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5637806f38472ff253adaf5a6ae5f23fa72be14a95dc14e5206b20acfb25eb8`  
		Last Modified: Thu, 27 Oct 2022 23:01:20 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:49dcb74f197aadf03edc59303f9936b06ce3be7e947c74607eaaeb3b6344fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:v2.9.4-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:6207a4986cc11e02da65392bfd152733786b87c433a09241a7d5fec2d8988c0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809165937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0500e1f3123ac9672f2d965c2271d84c4d18d4338fb7e9bd81661a0f8588843a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Oct 2022 21:26:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 27 Oct 2022 21:26:17 GMT
EXPOSE 80
# Thu, 27 Oct 2022 21:26:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 21:26:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807f285722ea86cc3d70eac642b38577e2a9058a8e6b90c49dbd064fea4997a`  
		Last Modified: Thu, 27 Oct 2022 21:26:53 GMT  
		Size: 35.7 MB (35661956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332f98b1e5522f72374c2b31a9ebe3adf1feb1b779a72319c0913b32671e42bb`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee544e98bde8d908e40e363c1800ca618bfab13e2ca6ff3a13dcd48d101fa51`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13601bc1cce5482abf666b88a9b7183ff6260c56ebb72603196aab3f51565a0`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:49dcb74f197aadf03edc59303f9936b06ce3be7e947c74607eaaeb3b6344fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull traefik@sha256:6207a4986cc11e02da65392bfd152733786b87c433a09241a7d5fec2d8988c0f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809165937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0500e1f3123ac9672f2d965c2271d84c4d18d4338fb7e9bd81661a0f8588843a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Oct 2022 21:26:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 27 Oct 2022 21:26:17 GMT
EXPOSE 80
# Thu, 27 Oct 2022 21:26:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 27 Oct 2022 21:26:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6193ab94a0498ba6454e2a35e189837b37a2eb01403e8b62654bdc28a4569c`  
		Last Modified: Mon, 17 Oct 2022 21:52:22 GMT  
		Size: 849.2 MB (849228999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807f285722ea86cc3d70eac642b38577e2a9058a8e6b90c49dbd064fea4997a`  
		Last Modified: Thu, 27 Oct 2022 21:26:53 GMT  
		Size: 35.7 MB (35661956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332f98b1e5522f72374c2b31a9ebe3adf1feb1b779a72319c0913b32671e42bb`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee544e98bde8d908e40e363c1800ca618bfab13e2ca6ff3a13dcd48d101fa51`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13601bc1cce5482abf666b88a9b7183ff6260c56ebb72603196aab3f51565a0`  
		Last Modified: Thu, 27 Oct 2022 21:26:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
