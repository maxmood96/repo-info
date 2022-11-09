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
$ docker pull traefik@sha256:89181f04a4f280eb644a6eab5829fc3e8059839bf8a75e4b912f0645b0f575c4
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
$ docker pull traefik@sha256:e690232cc6f5790b767b24035b2250779c1cf0f3989f81beb1aeaaa384b0178e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47989dd8837c7900cf2b444d04b069650e580eb5b5c96590f8997f17e236c0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 28 Oct 2022 00:15:28 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 28 Oct 2022 00:15:30 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 28 Oct 2022 00:15:30 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:30 GMT
VOLUME [/tmp]
# Fri, 28 Oct 2022 00:15:30 GMT
ENTRYPOINT ["/traefik"]
# Fri, 28 Oct 2022 00:15:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b507ebee3426425e2764f8ebd6549db6dfb80fd6ff52ecbeefdb14979e404f6d`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 320.1 KB (320052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ea5e4e50172dc8b7f47a76ddca55c03808d852bac2bf211279355576c6705`  
		Last Modified: Fri, 28 Oct 2022 00:17:24 GMT  
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
$ docker pull traefik@sha256:f99466db5cbcf2019afd580ff253bd6d7682fc9e1e4eb9cc786d3e85e4b91a7a
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
$ docker pull traefik@sha256:50f35b26a1a5b1bc0a3ce748b8595758c7fd1664b5f7e0b5757d0375aa9b5c45
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd97463ba8af2a4bf9fda6f6afdb43a6a3ddd80940275b48a397b147640e685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:15:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:18 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:19 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:19 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fbe39709604ff95e4df1403b6c2df9d199c5379e0d2ab1a87612bb7cff2a6`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
		Size: 677.4 KB (677360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21608e548924b2bae6736b125a617af8d7ef05cb619494808647c25bfa8a7485`  
		Last Modified: Fri, 28 Oct 2022 00:16:58 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8183137e9089f319a7d5aec2aca3e1c5d1a87ecbadfe2f9ae7eea9ce940d2f`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
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
$ docker pull traefik@sha256:ba22fa49d06eb335a538647f8ac6b53100619cef2d6dac06269da6c557709513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:8c0df9f3b6b67923ad88bb8c325e64f06bfec58ede2be72f6161a12fb58b0514
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2801442412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbcd25321baf9b5e717f95aad8a5c850725ea21067094e561b04f95f5e73c5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:39:46 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Nov 2022 19:39:47 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:39:48 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:39:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114e02070c38ac40033338b737577f7ed16181f6ce5ef3a282eb2a91b99c1967`  
		Last Modified: Wed, 09 Nov 2022 19:40:52 GMT  
		Size: 22.9 MB (22850203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ef1b6118e3b8dff31c6ada18f95988302cf4293219d1043eb9b810b79f9ec`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8499782a4e49b27eacd6a70cb60fb670341838fe2a3a9103ec45ff34bbe922c9`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadd67eff429b70dc14789c1a0f220cf3c25607c2b6a8145d3756731eb5b771a`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34`

```console
$ docker pull traefik@sha256:89181f04a4f280eb644a6eab5829fc3e8059839bf8a75e4b912f0645b0f575c4
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
$ docker pull traefik@sha256:e690232cc6f5790b767b24035b2250779c1cf0f3989f81beb1aeaaa384b0178e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47989dd8837c7900cf2b444d04b069650e580eb5b5c96590f8997f17e236c0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 28 Oct 2022 00:15:28 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 28 Oct 2022 00:15:30 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 28 Oct 2022 00:15:30 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:30 GMT
VOLUME [/tmp]
# Fri, 28 Oct 2022 00:15:30 GMT
ENTRYPOINT ["/traefik"]
# Fri, 28 Oct 2022 00:15:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b507ebee3426425e2764f8ebd6549db6dfb80fd6ff52ecbeefdb14979e404f6d`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 320.1 KB (320052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ea5e4e50172dc8b7f47a76ddca55c03808d852bac2bf211279355576c6705`  
		Last Modified: Fri, 28 Oct 2022 00:17:24 GMT  
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
$ docker pull traefik@sha256:f99466db5cbcf2019afd580ff253bd6d7682fc9e1e4eb9cc786d3e85e4b91a7a
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
$ docker pull traefik@sha256:50f35b26a1a5b1bc0a3ce748b8595758c7fd1664b5f7e0b5757d0375aa9b5c45
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd97463ba8af2a4bf9fda6f6afdb43a6a3ddd80940275b48a397b147640e685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:15:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:18 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:19 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:19 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fbe39709604ff95e4df1403b6c2df9d199c5379e0d2ab1a87612bb7cff2a6`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
		Size: 677.4 KB (677360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21608e548924b2bae6736b125a617af8d7ef05cb619494808647c25bfa8a7485`  
		Last Modified: Fri, 28 Oct 2022 00:16:58 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8183137e9089f319a7d5aec2aca3e1c5d1a87ecbadfe2f9ae7eea9ce940d2f`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
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
$ docker pull traefik@sha256:ba22fa49d06eb335a538647f8ac6b53100619cef2d6dac06269da6c557709513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:1.7.34-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:8c0df9f3b6b67923ad88bb8c325e64f06bfec58ede2be72f6161a12fb58b0514
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2801442412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbcd25321baf9b5e717f95aad8a5c850725ea21067094e561b04f95f5e73c5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:39:46 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Nov 2022 19:39:47 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:39:48 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:39:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114e02070c38ac40033338b737577f7ed16181f6ce5ef3a282eb2a91b99c1967`  
		Last Modified: Wed, 09 Nov 2022 19:40:52 GMT  
		Size: 22.9 MB (22850203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ef1b6118e3b8dff31c6ada18f95988302cf4293219d1043eb9b810b79f9ec`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8499782a4e49b27eacd6a70cb60fb670341838fe2a3a9103ec45ff34bbe922c9`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadd67eff429b70dc14789c1a0f220cf3c25607c2b6a8145d3756731eb5b771a`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9`

```console
$ docker pull traefik@sha256:4c388f477f5b7aa48420694d90db0ecb96b4ecede60b9b7589c87858abf87b60
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
$ docker pull traefik@sha256:1e65ca10d89714f3d091d1c41b4888ce591f327f96f4864bcc75dcda41c3496d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36505931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82f2ca04665d13ffc32727e9f1b3d2bae3bceff0262f39110a26f8009a936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:01 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:01 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf7d4e7a7df61784fa16d23d7d91644c5bf4a9b7d093a504e22e48cdd0275c`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 677.5 KB (677550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc2d590e7b7a26355c16a3711e1228c5f2b2a02a9a165f6d287c15c3099d8`  
		Last Modified: Fri, 28 Oct 2022 00:16:28 GMT  
		Size: 33.2 MB (33196886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291d5df795b7f5a27e7bc8921d3e046c6a88799e8ea77cd415dedbda756335ea`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 368.0 B  
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
$ docker pull traefik@sha256:235dcc83f19f2eb7c31e4ffffc5f17789413876587f233fc0c3c809fbe52d279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37323303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9c260a887d167ff907016e9743339d14768d337892d50d2145f08b99d7c47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:28:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:28:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:28:14 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:28:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:28:15 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:28:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a60e2bd2cd920edb930e19aca96b210f8a3fda41521f6ee1195d50b3ab1f9de1`  
		Last Modified: Thu, 27 Oct 2022 23:28:45 GMT  
		Size: 34.0 MB (34039336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb828af0cb57af780cf952557ab1e15e873d5ceb57356da63b4b01e6f9d079`  
		Last Modified: Thu, 27 Oct 2022 23:28:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fc7f1107103b2ae2fa0994d00adf6449cb325d68bb714cd8676b4828bad51a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:2.9-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:9e831c3e34a7ba03b26c220e70f18be9185063c19dc327dc042114488488e1d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2814256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a46a6698c0d6de9e6c83ceeb3eda68120d771f525827ffae038f5b01f80fcb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:38:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Nov 2022 19:38:08 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:38:10 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:38:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457b5602c76a5bee2862f07b1b43f115cf4d8eb57db1efd704949cd44e0ddf1`  
		Last Modified: Wed, 09 Nov 2022 19:40:25 GMT  
		Size: 35.7 MB (35664347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f18a5dff4fd50f36989efdcaea2ce96bb76f0e27155ebe945b78ed9c54493`  
		Last Modified: Wed, 09 Nov 2022 19:40:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0efee0efe52876c56d9d88d913c87aa07c31780df61b3e5d39767967c8f92c`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1f7d7d03b62b82ed6e5a9a0bcd5f8eac821ee45411f9b690c71ff5cd7b5832`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9.4`

```console
$ docker pull traefik@sha256:4c388f477f5b7aa48420694d90db0ecb96b4ecede60b9b7589c87858abf87b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

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

### `traefik:2.9.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1e65ca10d89714f3d091d1c41b4888ce591f327f96f4864bcc75dcda41c3496d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36505931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82f2ca04665d13ffc32727e9f1b3d2bae3bceff0262f39110a26f8009a936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:01 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:01 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf7d4e7a7df61784fa16d23d7d91644c5bf4a9b7d093a504e22e48cdd0275c`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 677.5 KB (677550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc2d590e7b7a26355c16a3711e1228c5f2b2a02a9a165f6d287c15c3099d8`  
		Last Modified: Fri, 28 Oct 2022 00:16:28 GMT  
		Size: 33.2 MB (33196886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291d5df795b7f5a27e7bc8921d3e046c6a88799e8ea77cd415dedbda756335ea`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 368.0 B  
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

### `traefik:2.9.4` - linux; s390x

```console
$ docker pull traefik@sha256:235dcc83f19f2eb7c31e4ffffc5f17789413876587f233fc0c3c809fbe52d279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37323303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9c260a887d167ff907016e9743339d14768d337892d50d2145f08b99d7c47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:28:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:28:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:28:14 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:28:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:28:15 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:28:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a60e2bd2cd920edb930e19aca96b210f8a3fda41521f6ee1195d50b3ab1f9de1`  
		Last Modified: Thu, 27 Oct 2022 23:28:45 GMT  
		Size: 34.0 MB (34039336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb828af0cb57af780cf952557ab1e15e873d5ceb57356da63b4b01e6f9d079`  
		Last Modified: Thu, 27 Oct 2022 23:28:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fc7f1107103b2ae2fa0994d00adf6449cb325d68bb714cd8676b4828bad51a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:2.9.4-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:9e831c3e34a7ba03b26c220e70f18be9185063c19dc327dc042114488488e1d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2814256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a46a6698c0d6de9e6c83ceeb3eda68120d771f525827ffae038f5b01f80fcb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:38:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Nov 2022 19:38:08 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:38:10 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:38:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457b5602c76a5bee2862f07b1b43f115cf4d8eb57db1efd704949cd44e0ddf1`  
		Last Modified: Wed, 09 Nov 2022 19:40:25 GMT  
		Size: 35.7 MB (35664347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f18a5dff4fd50f36989efdcaea2ce96bb76f0e27155ebe945b78ed9c54493`  
		Last Modified: Wed, 09 Nov 2022 19:40:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0efee0efe52876c56d9d88d913c87aa07c31780df61b3e5d39767967c8f92c`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1f7d7d03b62b82ed6e5a9a0bcd5f8eac821ee45411f9b690c71ff5cd7b5832`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:banon`

```console
$ docker pull traefik@sha256:4c388f477f5b7aa48420694d90db0ecb96b4ecede60b9b7589c87858abf87b60
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
$ docker pull traefik@sha256:1e65ca10d89714f3d091d1c41b4888ce591f327f96f4864bcc75dcda41c3496d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36505931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82f2ca04665d13ffc32727e9f1b3d2bae3bceff0262f39110a26f8009a936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:01 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:01 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf7d4e7a7df61784fa16d23d7d91644c5bf4a9b7d093a504e22e48cdd0275c`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 677.5 KB (677550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc2d590e7b7a26355c16a3711e1228c5f2b2a02a9a165f6d287c15c3099d8`  
		Last Modified: Fri, 28 Oct 2022 00:16:28 GMT  
		Size: 33.2 MB (33196886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291d5df795b7f5a27e7bc8921d3e046c6a88799e8ea77cd415dedbda756335ea`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 368.0 B  
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
$ docker pull traefik@sha256:235dcc83f19f2eb7c31e4ffffc5f17789413876587f233fc0c3c809fbe52d279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37323303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9c260a887d167ff907016e9743339d14768d337892d50d2145f08b99d7c47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:28:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:28:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:28:14 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:28:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:28:15 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:28:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a60e2bd2cd920edb930e19aca96b210f8a3fda41521f6ee1195d50b3ab1f9de1`  
		Last Modified: Thu, 27 Oct 2022 23:28:45 GMT  
		Size: 34.0 MB (34039336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb828af0cb57af780cf952557ab1e15e873d5ceb57356da63b4b01e6f9d079`  
		Last Modified: Thu, 27 Oct 2022 23:28:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:banon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fc7f1107103b2ae2fa0994d00adf6449cb325d68bb714cd8676b4828bad51a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:banon-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:9e831c3e34a7ba03b26c220e70f18be9185063c19dc327dc042114488488e1d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2814256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a46a6698c0d6de9e6c83ceeb3eda68120d771f525827ffae038f5b01f80fcb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:38:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Nov 2022 19:38:08 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:38:10 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:38:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457b5602c76a5bee2862f07b1b43f115cf4d8eb57db1efd704949cd44e0ddf1`  
		Last Modified: Wed, 09 Nov 2022 19:40:25 GMT  
		Size: 35.7 MB (35664347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f18a5dff4fd50f36989efdcaea2ce96bb76f0e27155ebe945b78ed9c54493`  
		Last Modified: Wed, 09 Nov 2022 19:40:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0efee0efe52876c56d9d88d913c87aa07c31780df61b3e5d39767967c8f92c`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1f7d7d03b62b82ed6e5a9a0bcd5f8eac821ee45411f9b690c71ff5cd7b5832`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:4c388f477f5b7aa48420694d90db0ecb96b4ecede60b9b7589c87858abf87b60
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
$ docker pull traefik@sha256:1e65ca10d89714f3d091d1c41b4888ce591f327f96f4864bcc75dcda41c3496d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36505931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82f2ca04665d13ffc32727e9f1b3d2bae3bceff0262f39110a26f8009a936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:01 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:01 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf7d4e7a7df61784fa16d23d7d91644c5bf4a9b7d093a504e22e48cdd0275c`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 677.5 KB (677550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc2d590e7b7a26355c16a3711e1228c5f2b2a02a9a165f6d287c15c3099d8`  
		Last Modified: Fri, 28 Oct 2022 00:16:28 GMT  
		Size: 33.2 MB (33196886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291d5df795b7f5a27e7bc8921d3e046c6a88799e8ea77cd415dedbda756335ea`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 368.0 B  
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
$ docker pull traefik@sha256:235dcc83f19f2eb7c31e4ffffc5f17789413876587f233fc0c3c809fbe52d279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37323303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9c260a887d167ff907016e9743339d14768d337892d50d2145f08b99d7c47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:28:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:28:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:28:14 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:28:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:28:15 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:28:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a60e2bd2cd920edb930e19aca96b210f8a3fda41521f6ee1195d50b3ab1f9de1`  
		Last Modified: Thu, 27 Oct 2022 23:28:45 GMT  
		Size: 34.0 MB (34039336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb828af0cb57af780cf952557ab1e15e873d5ceb57356da63b4b01e6f9d079`  
		Last Modified: Thu, 27 Oct 2022 23:28:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:89181f04a4f280eb644a6eab5829fc3e8059839bf8a75e4b912f0645b0f575c4
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
$ docker pull traefik@sha256:e690232cc6f5790b767b24035b2250779c1cf0f3989f81beb1aeaaa384b0178e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47989dd8837c7900cf2b444d04b069650e580eb5b5c96590f8997f17e236c0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 28 Oct 2022 00:15:28 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 28 Oct 2022 00:15:30 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 28 Oct 2022 00:15:30 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:30 GMT
VOLUME [/tmp]
# Fri, 28 Oct 2022 00:15:30 GMT
ENTRYPOINT ["/traefik"]
# Fri, 28 Oct 2022 00:15:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b507ebee3426425e2764f8ebd6549db6dfb80fd6ff52ecbeefdb14979e404f6d`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 320.1 KB (320052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ea5e4e50172dc8b7f47a76ddca55c03808d852bac2bf211279355576c6705`  
		Last Modified: Fri, 28 Oct 2022 00:17:24 GMT  
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
$ docker pull traefik@sha256:f99466db5cbcf2019afd580ff253bd6d7682fc9e1e4eb9cc786d3e85e4b91a7a
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
$ docker pull traefik@sha256:50f35b26a1a5b1bc0a3ce748b8595758c7fd1664b5f7e0b5757d0375aa9b5c45
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd97463ba8af2a4bf9fda6f6afdb43a6a3ddd80940275b48a397b147640e685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:15:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:18 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:19 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:19 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fbe39709604ff95e4df1403b6c2df9d199c5379e0d2ab1a87612bb7cff2a6`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
		Size: 677.4 KB (677360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21608e548924b2bae6736b125a617af8d7ef05cb619494808647c25bfa8a7485`  
		Last Modified: Fri, 28 Oct 2022 00:16:58 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8183137e9089f319a7d5aec2aca3e1c5d1a87ecbadfe2f9ae7eea9ce940d2f`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
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
$ docker pull traefik@sha256:ba22fa49d06eb335a538647f8ac6b53100619cef2d6dac06269da6c557709513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:8c0df9f3b6b67923ad88bb8c325e64f06bfec58ede2be72f6161a12fb58b0514
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2801442412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbcd25321baf9b5e717f95aad8a5c850725ea21067094e561b04f95f5e73c5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:39:46 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Nov 2022 19:39:47 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:39:48 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:39:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114e02070c38ac40033338b737577f7ed16181f6ce5ef3a282eb2a91b99c1967`  
		Last Modified: Wed, 09 Nov 2022 19:40:52 GMT  
		Size: 22.9 MB (22850203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ef1b6118e3b8dff31c6ada18f95988302cf4293219d1043eb9b810b79f9ec`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8499782a4e49b27eacd6a70cb60fb670341838fe2a3a9103ec45ff34bbe922c9`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadd67eff429b70dc14789c1a0f220cf3c25607c2b6a8145d3756731eb5b771a`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:89181f04a4f280eb644a6eab5829fc3e8059839bf8a75e4b912f0645b0f575c4
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
$ docker pull traefik@sha256:e690232cc6f5790b767b24035b2250779c1cf0f3989f81beb1aeaaa384b0178e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47989dd8837c7900cf2b444d04b069650e580eb5b5c96590f8997f17e236c0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 28 Oct 2022 00:15:28 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 28 Oct 2022 00:15:30 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 28 Oct 2022 00:15:30 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:30 GMT
VOLUME [/tmp]
# Fri, 28 Oct 2022 00:15:30 GMT
ENTRYPOINT ["/traefik"]
# Fri, 28 Oct 2022 00:15:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b507ebee3426425e2764f8ebd6549db6dfb80fd6ff52ecbeefdb14979e404f6d`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 320.1 KB (320052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ea5e4e50172dc8b7f47a76ddca55c03808d852bac2bf211279355576c6705`  
		Last Modified: Fri, 28 Oct 2022 00:17:24 GMT  
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
$ docker pull traefik@sha256:f99466db5cbcf2019afd580ff253bd6d7682fc9e1e4eb9cc786d3e85e4b91a7a
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
$ docker pull traefik@sha256:50f35b26a1a5b1bc0a3ce748b8595758c7fd1664b5f7e0b5757d0375aa9b5c45
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd97463ba8af2a4bf9fda6f6afdb43a6a3ddd80940275b48a397b147640e685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:15:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:18 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:19 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:19 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fbe39709604ff95e4df1403b6c2df9d199c5379e0d2ab1a87612bb7cff2a6`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
		Size: 677.4 KB (677360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21608e548924b2bae6736b125a617af8d7ef05cb619494808647c25bfa8a7485`  
		Last Modified: Fri, 28 Oct 2022 00:16:58 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8183137e9089f319a7d5aec2aca3e1c5d1a87ecbadfe2f9ae7eea9ce940d2f`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
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
$ docker pull traefik@sha256:ba22fa49d06eb335a538647f8ac6b53100619cef2d6dac06269da6c557709513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:8c0df9f3b6b67923ad88bb8c325e64f06bfec58ede2be72f6161a12fb58b0514
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2801442412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbcd25321baf9b5e717f95aad8a5c850725ea21067094e561b04f95f5e73c5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:39:46 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Nov 2022 19:39:47 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:39:48 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:39:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114e02070c38ac40033338b737577f7ed16181f6ce5ef3a282eb2a91b99c1967`  
		Last Modified: Wed, 09 Nov 2022 19:40:52 GMT  
		Size: 22.9 MB (22850203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ef1b6118e3b8dff31c6ada18f95988302cf4293219d1043eb9b810b79f9ec`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8499782a4e49b27eacd6a70cb60fb670341838fe2a3a9103ec45ff34bbe922c9`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadd67eff429b70dc14789c1a0f220cf3c25607c2b6a8145d3756731eb5b771a`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34`

```console
$ docker pull traefik@sha256:89181f04a4f280eb644a6eab5829fc3e8059839bf8a75e4b912f0645b0f575c4
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
$ docker pull traefik@sha256:e690232cc6f5790b767b24035b2250779c1cf0f3989f81beb1aeaaa384b0178e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47989dd8837c7900cf2b444d04b069650e580eb5b5c96590f8997f17e236c0`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 28 Oct 2022 00:15:28 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 28 Oct 2022 00:15:30 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 28 Oct 2022 00:15:30 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:30 GMT
VOLUME [/tmp]
# Fri, 28 Oct 2022 00:15:30 GMT
ENTRYPOINT ["/traefik"]
# Fri, 28 Oct 2022 00:15:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b507ebee3426425e2764f8ebd6549db6dfb80fd6ff52ecbeefdb14979e404f6d`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 320.1 KB (320052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ea5e4e50172dc8b7f47a76ddca55c03808d852bac2bf211279355576c6705`  
		Last Modified: Fri, 28 Oct 2022 00:17:24 GMT  
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
$ docker pull traefik@sha256:f99466db5cbcf2019afd580ff253bd6d7682fc9e1e4eb9cc786d3e85e4b91a7a
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
$ docker pull traefik@sha256:50f35b26a1a5b1bc0a3ce748b8595758c7fd1664b5f7e0b5757d0375aa9b5c45
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd97463ba8af2a4bf9fda6f6afdb43a6a3ddd80940275b48a397b147640e685c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:15:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:18 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:18 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:19 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:19 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996fbe39709604ff95e4df1403b6c2df9d199c5379e0d2ab1a87612bb7cff2a6`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
		Size: 677.4 KB (677360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21608e548924b2bae6736b125a617af8d7ef05cb619494808647c25bfa8a7485`  
		Last Modified: Fri, 28 Oct 2022 00:16:58 GMT  
		Size: 20.6 MB (20623430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8183137e9089f319a7d5aec2aca3e1c5d1a87ecbadfe2f9ae7eea9ce940d2f`  
		Last Modified: Fri, 28 Oct 2022 00:16:54 GMT  
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
$ docker pull traefik@sha256:ba22fa49d06eb335a538647f8ac6b53100619cef2d6dac06269da6c557709513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:v1.7.34-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:8c0df9f3b6b67923ad88bb8c325e64f06bfec58ede2be72f6161a12fb58b0514
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2801442412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffbcd25321baf9b5e717f95aad8a5c850725ea21067094e561b04f95f5e73c5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:39:46 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Nov 2022 19:39:47 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:39:48 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:39:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114e02070c38ac40033338b737577f7ed16181f6ce5ef3a282eb2a91b99c1967`  
		Last Modified: Wed, 09 Nov 2022 19:40:52 GMT  
		Size: 22.9 MB (22850203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ef1b6118e3b8dff31c6ada18f95988302cf4293219d1043eb9b810b79f9ec`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8499782a4e49b27eacd6a70cb60fb670341838fe2a3a9103ec45ff34bbe922c9`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadd67eff429b70dc14789c1a0f220cf3c25607c2b6a8145d3756731eb5b771a`  
		Last Modified: Wed, 09 Nov 2022 19:40:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9`

```console
$ docker pull traefik@sha256:4c388f477f5b7aa48420694d90db0ecb96b4ecede60b9b7589c87858abf87b60
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
$ docker pull traefik@sha256:1e65ca10d89714f3d091d1c41b4888ce591f327f96f4864bcc75dcda41c3496d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36505931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82f2ca04665d13ffc32727e9f1b3d2bae3bceff0262f39110a26f8009a936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:01 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:01 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf7d4e7a7df61784fa16d23d7d91644c5bf4a9b7d093a504e22e48cdd0275c`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 677.5 KB (677550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc2d590e7b7a26355c16a3711e1228c5f2b2a02a9a165f6d287c15c3099d8`  
		Last Modified: Fri, 28 Oct 2022 00:16:28 GMT  
		Size: 33.2 MB (33196886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291d5df795b7f5a27e7bc8921d3e046c6a88799e8ea77cd415dedbda756335ea`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 368.0 B  
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
$ docker pull traefik@sha256:235dcc83f19f2eb7c31e4ffffc5f17789413876587f233fc0c3c809fbe52d279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37323303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9c260a887d167ff907016e9743339d14768d337892d50d2145f08b99d7c47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:28:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:28:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:28:14 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:28:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:28:15 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:28:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a60e2bd2cd920edb930e19aca96b210f8a3fda41521f6ee1195d50b3ab1f9de1`  
		Last Modified: Thu, 27 Oct 2022 23:28:45 GMT  
		Size: 34.0 MB (34039336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb828af0cb57af780cf952557ab1e15e873d5ceb57356da63b4b01e6f9d079`  
		Last Modified: Thu, 27 Oct 2022 23:28:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fc7f1107103b2ae2fa0994d00adf6449cb325d68bb714cd8676b4828bad51a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:v2.9-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:9e831c3e34a7ba03b26c220e70f18be9185063c19dc327dc042114488488e1d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2814256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a46a6698c0d6de9e6c83ceeb3eda68120d771f525827ffae038f5b01f80fcb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:38:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Nov 2022 19:38:08 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:38:10 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:38:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457b5602c76a5bee2862f07b1b43f115cf4d8eb57db1efd704949cd44e0ddf1`  
		Last Modified: Wed, 09 Nov 2022 19:40:25 GMT  
		Size: 35.7 MB (35664347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f18a5dff4fd50f36989efdcaea2ce96bb76f0e27155ebe945b78ed9c54493`  
		Last Modified: Wed, 09 Nov 2022 19:40:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0efee0efe52876c56d9d88d913c87aa07c31780df61b3e5d39767967c8f92c`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1f7d7d03b62b82ed6e5a9a0bcd5f8eac821ee45411f9b690c71ff5cd7b5832`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9.4`

```console
$ docker pull traefik@sha256:4c388f477f5b7aa48420694d90db0ecb96b4ecede60b9b7589c87858abf87b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

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

### `traefik:v2.9.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:1e65ca10d89714f3d091d1c41b4888ce591f327f96f4864bcc75dcda41c3496d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36505931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e82f2ca04665d13ffc32727e9f1b3d2bae3bceff0262f39110a26f8009a936d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 28 Oct 2022 00:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 28 Oct 2022 00:15:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 28 Oct 2022 00:15:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 28 Oct 2022 00:15:01 GMT
EXPOSE 80
# Fri, 28 Oct 2022 00:15:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 00:15:01 GMT
CMD ["traefik"]
# Fri, 28 Oct 2022 00:15:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eaf7d4e7a7df61784fa16d23d7d91644c5bf4a9b7d093a504e22e48cdd0275c`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 677.5 KB (677550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460bc2d590e7b7a26355c16a3711e1228c5f2b2a02a9a165f6d287c15c3099d8`  
		Last Modified: Fri, 28 Oct 2022 00:16:28 GMT  
		Size: 33.2 MB (33196886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291d5df795b7f5a27e7bc8921d3e046c6a88799e8ea77cd415dedbda756335ea`  
		Last Modified: Fri, 28 Oct 2022 00:16:22 GMT  
		Size: 368.0 B  
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

### `traefik:v2.9.4` - linux; s390x

```console
$ docker pull traefik@sha256:235dcc83f19f2eb7c31e4ffffc5f17789413876587f233fc0c3c809fbe52d279
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37323303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e9c260a887d167ff907016e9743339d14768d337892d50d2145f08b99d7c47`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:54 GMT
ADD file:7489fa84133e97e4f40b13dd5159989b3594c9627d9147bfc4e33134944cc368 in / 
# Tue, 09 Aug 2022 17:41:54 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:56:58 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 27 Oct 2022 23:28:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 27 Oct 2022 23:28:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 27 Oct 2022 23:28:14 GMT
EXPOSE 80
# Thu, 27 Oct 2022 23:28:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 23:28:15 GMT
CMD ["traefik"]
# Thu, 27 Oct 2022 23:28:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a60e2bd2cd920edb930e19aca96b210f8a3fda41521f6ee1195d50b3ab1f9de1`  
		Last Modified: Thu, 27 Oct 2022 23:28:45 GMT  
		Size: 34.0 MB (34039336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63eb828af0cb57af780cf952557ab1e15e873d5ceb57356da63b4b01e6f9d079`  
		Last Modified: Thu, 27 Oct 2022 23:28:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fc7f1107103b2ae2fa0994d00adf6449cb325d68bb714cd8676b4828bad51a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:v2.9.4-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:9e831c3e34a7ba03b26c220e70f18be9185063c19dc327dc042114488488e1d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2814256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a46a6698c0d6de9e6c83ceeb3eda68120d771f525827ffae038f5b01f80fcb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:38:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Nov 2022 19:38:08 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:38:10 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:38:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457b5602c76a5bee2862f07b1b43f115cf4d8eb57db1efd704949cd44e0ddf1`  
		Last Modified: Wed, 09 Nov 2022 19:40:25 GMT  
		Size: 35.7 MB (35664347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f18a5dff4fd50f36989efdcaea2ce96bb76f0e27155ebe945b78ed9c54493`  
		Last Modified: Wed, 09 Nov 2022 19:40:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0efee0efe52876c56d9d88d913c87aa07c31780df61b3e5d39767967c8f92c`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1f7d7d03b62b82ed6e5a9a0bcd5f8eac821ee45411f9b690c71ff5cd7b5832`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:fc7f1107103b2ae2fa0994d00adf6449cb325d68bb714cd8676b4828bad51a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:9e831c3e34a7ba03b26c220e70f18be9185063c19dc327dc042114488488e1d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2814256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a46a6698c0d6de9e6c83ceeb3eda68120d771f525827ffae038f5b01f80fcb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:38:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Nov 2022 19:38:08 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:38:10 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:38:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457b5602c76a5bee2862f07b1b43f115cf4d8eb57db1efd704949cd44e0ddf1`  
		Last Modified: Wed, 09 Nov 2022 19:40:25 GMT  
		Size: 35.7 MB (35664347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f18a5dff4fd50f36989efdcaea2ce96bb76f0e27155ebe945b78ed9c54493`  
		Last Modified: Wed, 09 Nov 2022 19:40:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0efee0efe52876c56d9d88d913c87aa07c31780df61b3e5d39767967c8f92c`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1f7d7d03b62b82ed6e5a9a0bcd5f8eac821ee45411f9b690c71ff5cd7b5832`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
