<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.30`](#traefik1730)
-	[`traefik:1.7.30-alpine`](#traefik1730-alpine)
-	[`traefik:1.7.30-windowsservercore-1809`](#traefik1730-windowsservercore-1809)
-	[`traefik:2.4`](#traefik24)
-	[`traefik:2.4-windowsservercore-1809`](#traefik24-windowsservercore-1809)
-	[`traefik:2.4.13`](#traefik2413)
-	[`traefik:2.4.13-windowsservercore-1809`](#traefik2413-windowsservercore-1809)
-	[`traefik:2.5`](#traefik25)
-	[`traefik:2.5-windowsservercore-1809`](#traefik25-windowsservercore-1809)
-	[`traefik:2.5.0-rc6`](#traefik250-rc6)
-	[`traefik:2.5.0-rc6-windowsservercore-1809`](#traefik250-rc6-windowsservercore-1809)
-	[`traefik:brie`](#traefikbrie)
-	[`traefik:brie-windowsservercore-1809`](#traefikbrie-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:livarot`](#traefiklivarot)
-	[`traefik:livarot-windowsservercore-1809`](#traefiklivarot-windowsservercore-1809)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v1.7.30`](#traefikv1730)
-	[`traefik:v1.7.30-alpine`](#traefikv1730-alpine)
-	[`traefik:v1.7.30-windowsservercore-1809`](#traefikv1730-windowsservercore-1809)
-	[`traefik:v2.4`](#traefikv24)
-	[`traefik:v2.4-windowsservercore-1809`](#traefikv24-windowsservercore-1809)
-	[`traefik:v2.4.13`](#traefikv2413)
-	[`traefik:v2.4.13-windowsservercore-1809`](#traefikv2413-windowsservercore-1809)
-	[`traefik:v2.5`](#traefikv25)
-	[`traefik:v2.5-windowsservercore-1809`](#traefikv25-windowsservercore-1809)
-	[`traefik:v2.5.0-rc6`](#traefikv250-rc6)
-	[`traefik:v2.5.0-rc6-windowsservercore-1809`](#traefikv250-rc6-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:ca3883356d24f9fd6d36f0450d7f6f17a233317943517f6036c20ebf7c137781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:13bd9d65c0558740d1b8b6f8de06f314003be9b54eec4b8b67dad2cf58d037c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cea7c66ee3601de1cf66168feceac0bc9ac1147103e54d63f742e570bb0ca`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 22 Jun 2021 21:21:29 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 22 Jun 2021 21:21:31 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 22 Jun 2021 21:21:34 GMT
COPY file:440b6b1ebd389a2397ffb187ded4c85dcf37b7284d94c693b0b603d51247c683 in / 
# Tue, 22 Jun 2021 21:21:35 GMT
EXPOSE 80
# Tue, 22 Jun 2021 21:21:35 GMT
VOLUME [/tmp]
# Tue, 22 Jun 2021 21:21:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 22 Jun 2021 21:21:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:00918d1fc688f95413059b21ca56a6453b74d2808448ca35ed04b737d4a22c74`  
		Last Modified: Tue, 22 Jun 2021 21:24:22 GMT  
		Size: 130.9 KB (130871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e7abe8d1c9d1c5c74050eb312423f911185ce6cc705d32631fad6a1b3a4450`  
		Last Modified: Tue, 22 Jun 2021 21:24:23 GMT  
		Size: 308.9 KB (308853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee57e616d21eeb2181fd86ab18cbdb3be5af9c65ddb68c3657ebba7e266a191`  
		Last Modified: Tue, 22 Jun 2021 21:24:33 GMT  
		Size: 16.5 MB (16516801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f7fe0c0982ce55e8882f88193462be30b654f27dd1c5014243efd6fd85d563ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16533633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c3dd29cfce4ed4d7084315b52be936e63726239cbae0f98cf0c36cfdd8707a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 16 Jun 2021 11:17:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY file:6fdd60dc35db1c19a5de5ed8b57f159a6e121ba0f1ddb3e48a6e185da99f8cca in / 
# Wed, 16 Jun 2021 11:17:49 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:49 GMT
VOLUME [/tmp]
# Wed, 16 Jun 2021 11:17:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 16 Jun 2021 11:17:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ba07573b64554f7a74d3d3b27c42e28f5209c9d82f79b2596a6b190ee5475c72`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a5756798f3769843250c96f2b11eca4d4c83a91616dd5d97d17399022fc6e`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 308.9 KB (308857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af1647ff43bc2a163e816afb6eb2c410d240b736297469f44ec6db498f13fc`  
		Last Modified: Wed, 16 Jun 2021 11:19:28 GMT  
		Size: 16.1 MB (16093904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:1fa5d3b0e00c6b2b10eab9ea0e149f0930f36fb46dee9f56ec2a2c04570685f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:5e1e280e8e56520c8ebc11425f2c9fe66c9fae4714d65833d7f15c40fde8fb80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55847f6ab3e15d3f6304ec3271273146b44942dff17926a61366afbdf6736671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 15 Apr 2021 03:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 15 Apr 2021 03:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 15 Apr 2021 03:05:00 GMT
EXPOSE 80
# Thu, 15 Apr 2021 03:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 03:05:01 GMT
CMD ["traefik"]
# Thu, 15 Apr 2021 03:05:01 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40cdaabf18912622322046bb5eeda16c1ac513a094389e9b12b33ff02abb2c`  
		Last Modified: Thu, 15 Apr 2021 03:06:32 GMT  
		Size: 17.7 MB (17684875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ec9b7bad03eb2d44d70526dbd5478e8ee4043e8445168201605f71fafbb22e`  
		Last Modified: Thu, 15 Apr 2021 03:06:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6d12e7dd314491c93f36925c26748d18e9e7728c9f9d903bbe4120a9931ba35c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ddc131d7b096108dc285679a6bd9b6687758a14c5b8001347fbea7fe0bbc64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:27:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:27:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:29 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:31 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:32 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01457397f14eabab444a0392f736186f6c1469179bc6fafc66054e13a1ccd8`  
		Last Modified: Fri, 30 Jul 2021 22:31:21 GMT  
		Size: 16.5 MB (16516925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bba084b6a881bc33691e5efbdbbcb852b478fe5225e01b3132cc511ff78b89e`  
		Last Modified: Fri, 30 Jul 2021 22:31:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2d441643d23da8a818a8e403f0a3ca49e14979fb6aa79f86a8404669f7cc9b72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19496836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184b20b066615f1d8a085e3d6675d33e45801aca796ccc8defaae328b0b2b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 16 Jun 2021 11:17:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 16 Jun 2021 11:17:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 16 Jun 2021 11:17:38 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Jun 2021 11:17:38 GMT
CMD ["traefik"]
# Wed, 16 Jun 2021 11:17:38 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc700f9acd83a1c32048c47de8af63581c2a73eca263f30db7c161ca1855f2`  
		Last Modified: Wed, 16 Jun 2021 11:19:04 GMT  
		Size: 16.1 MB (16093993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e249b2d31cb237f67cb1f9438d0ec9e3357c69a8762ebbefa98b9815013727`  
		Last Modified: Wed, 16 Jun 2021 11:19:01 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7d1d137d268e564085e5c05f918bf4346a8290ab611c57d1ccf1e08e79b0006e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:ec1da595d84f5b3257698735564626a30c0560d9e68aa759d32cf96ed1625015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2704291103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e6922cc13d4e220d195b7a6d7aac00de05dfb4bb78eb345efe16dd2a6ebd88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:23:45 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 11 Aug 2021 22:23:48 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:23:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:23:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e191a5bf292d7a12c5f917dde336d2439d4d22f34b3ccc93ba2ec56eb429a5e`  
		Last Modified: Wed, 11 Aug 2021 22:25:11 GMT  
		Size: 18.3 MB (18287524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e368da9720874eda4c481f2fbfbc13d345ce8b07efd443a946a7f0a002163a9e`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a826777ecee2f4cb9fcf66ed49eff2226c0e7d5efcd438e572f89c791bfaaa`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac5b0da240f2ab9425ecd3484d6a900c5563251d11a6c4f9872fdc3f02f1635`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.30`

```console
$ docker pull traefik@sha256:ca3883356d24f9fd6d36f0450d7f6f17a233317943517f6036c20ebf7c137781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.30` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.30` - linux; arm variant v6

```console
$ docker pull traefik@sha256:13bd9d65c0558740d1b8b6f8de06f314003be9b54eec4b8b67dad2cf58d037c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cea7c66ee3601de1cf66168feceac0bc9ac1147103e54d63f742e570bb0ca`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 22 Jun 2021 21:21:29 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 22 Jun 2021 21:21:31 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 22 Jun 2021 21:21:34 GMT
COPY file:440b6b1ebd389a2397ffb187ded4c85dcf37b7284d94c693b0b603d51247c683 in / 
# Tue, 22 Jun 2021 21:21:35 GMT
EXPOSE 80
# Tue, 22 Jun 2021 21:21:35 GMT
VOLUME [/tmp]
# Tue, 22 Jun 2021 21:21:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 22 Jun 2021 21:21:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:00918d1fc688f95413059b21ca56a6453b74d2808448ca35ed04b737d4a22c74`  
		Last Modified: Tue, 22 Jun 2021 21:24:22 GMT  
		Size: 130.9 KB (130871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e7abe8d1c9d1c5c74050eb312423f911185ce6cc705d32631fad6a1b3a4450`  
		Last Modified: Tue, 22 Jun 2021 21:24:23 GMT  
		Size: 308.9 KB (308853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee57e616d21eeb2181fd86ab18cbdb3be5af9c65ddb68c3657ebba7e266a191`  
		Last Modified: Tue, 22 Jun 2021 21:24:33 GMT  
		Size: 16.5 MB (16516801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.30` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f7fe0c0982ce55e8882f88193462be30b654f27dd1c5014243efd6fd85d563ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16533633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c3dd29cfce4ed4d7084315b52be936e63726239cbae0f98cf0c36cfdd8707a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 16 Jun 2021 11:17:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY file:6fdd60dc35db1c19a5de5ed8b57f159a6e121ba0f1ddb3e48a6e185da99f8cca in / 
# Wed, 16 Jun 2021 11:17:49 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:49 GMT
VOLUME [/tmp]
# Wed, 16 Jun 2021 11:17:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 16 Jun 2021 11:17:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ba07573b64554f7a74d3d3b27c42e28f5209c9d82f79b2596a6b190ee5475c72`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a5756798f3769843250c96f2b11eca4d4c83a91616dd5d97d17399022fc6e`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 308.9 KB (308857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af1647ff43bc2a163e816afb6eb2c410d240b736297469f44ec6db498f13fc`  
		Last Modified: Wed, 16 Jun 2021 11:19:28 GMT  
		Size: 16.1 MB (16093904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.30-alpine`

```console
$ docker pull traefik@sha256:1fa5d3b0e00c6b2b10eab9ea0e149f0930f36fb46dee9f56ec2a2c04570685f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.30-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:5e1e280e8e56520c8ebc11425f2c9fe66c9fae4714d65833d7f15c40fde8fb80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55847f6ab3e15d3f6304ec3271273146b44942dff17926a61366afbdf6736671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 15 Apr 2021 03:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 15 Apr 2021 03:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 15 Apr 2021 03:05:00 GMT
EXPOSE 80
# Thu, 15 Apr 2021 03:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 03:05:01 GMT
CMD ["traefik"]
# Thu, 15 Apr 2021 03:05:01 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40cdaabf18912622322046bb5eeda16c1ac513a094389e9b12b33ff02abb2c`  
		Last Modified: Thu, 15 Apr 2021 03:06:32 GMT  
		Size: 17.7 MB (17684875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ec9b7bad03eb2d44d70526dbd5478e8ee4043e8445168201605f71fafbb22e`  
		Last Modified: Thu, 15 Apr 2021 03:06:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.30-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6d12e7dd314491c93f36925c26748d18e9e7728c9f9d903bbe4120a9931ba35c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ddc131d7b096108dc285679a6bd9b6687758a14c5b8001347fbea7fe0bbc64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:27:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:27:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:29 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:31 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:32 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01457397f14eabab444a0392f736186f6c1469179bc6fafc66054e13a1ccd8`  
		Last Modified: Fri, 30 Jul 2021 22:31:21 GMT  
		Size: 16.5 MB (16516925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bba084b6a881bc33691e5efbdbbcb852b478fe5225e01b3132cc511ff78b89e`  
		Last Modified: Fri, 30 Jul 2021 22:31:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.30-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2d441643d23da8a818a8e403f0a3ca49e14979fb6aa79f86a8404669f7cc9b72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19496836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184b20b066615f1d8a085e3d6675d33e45801aca796ccc8defaae328b0b2b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 16 Jun 2021 11:17:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 16 Jun 2021 11:17:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 16 Jun 2021 11:17:38 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Jun 2021 11:17:38 GMT
CMD ["traefik"]
# Wed, 16 Jun 2021 11:17:38 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc700f9acd83a1c32048c47de8af63581c2a73eca263f30db7c161ca1855f2`  
		Last Modified: Wed, 16 Jun 2021 11:19:04 GMT  
		Size: 16.1 MB (16093993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e249b2d31cb237f67cb1f9438d0ec9e3357c69a8762ebbefa98b9815013727`  
		Last Modified: Wed, 16 Jun 2021 11:19:01 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.30-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7d1d137d268e564085e5c05f918bf4346a8290ab611c57d1ccf1e08e79b0006e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:1.7.30-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:ec1da595d84f5b3257698735564626a30c0560d9e68aa759d32cf96ed1625015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2704291103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e6922cc13d4e220d195b7a6d7aac00de05dfb4bb78eb345efe16dd2a6ebd88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:23:45 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 11 Aug 2021 22:23:48 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:23:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:23:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e191a5bf292d7a12c5f917dde336d2439d4d22f34b3ccc93ba2ec56eb429a5e`  
		Last Modified: Wed, 11 Aug 2021 22:25:11 GMT  
		Size: 18.3 MB (18287524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e368da9720874eda4c481f2fbfbc13d345ce8b07efd443a946a7f0a002163a9e`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a826777ecee2f4cb9fcf66ed49eff2226c0e7d5efcd438e572f89c791bfaaa`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac5b0da240f2ab9425ecd3484d6a900c5563251d11a6c4f9872fdc3f02f1635`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4`

```console
$ docker pull traefik@sha256:3123d05e444f6297592c8443bcffe4bd291ab5b62e11a3d4eeb7ba3fd809540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.4` - linux; amd64

```console
$ docker pull traefik@sha256:577994c7e49027d4184ee5740f54c467970ac6a308bdc50d55dfc805884531da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28046777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d3b9e70c4801587dd39574069fb09dc0d7ca2853092ac7ef53d0b75484a389`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 19:38:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 19:38:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 19:38:17 GMT
EXPOSE 80
# Fri, 30 Jul 2021 19:38:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 19:38:17 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 19:38:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd0fbf25cb90ae5844a1d4d0e85f517bc8cf0460d690c234c64e25de3f96f4b`  
		Last Modified: Fri, 30 Jul 2021 19:39:00 GMT  
		Size: 24.6 MB (24555954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ff7bc59db0b71017ce81a509bb65fea811e77277c32790eaacd4bbc8da423`  
		Last Modified: Fri, 30 Jul 2021 19:38:54 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5590ac7c1fb6040858fab793166b5e38f736652eb35c6c24ea56405d6017e8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26227229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d8f9270701f73afed1ff644a8b1d1124581418fa76527b45ea36641bb46db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:26:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:26:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:00 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:01 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b4e80431610821828160c0db44a02f117fccba4819a25adcc3bd9de58c22b4`  
		Last Modified: Fri, 30 Jul 2021 22:30:42 GMT  
		Size: 22.9 MB (22927935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae175f92c8d1f8b56063ad6238b79ce13588462980d692812b911c38065b76`  
		Last Modified: Fri, 30 Jul 2021 22:30:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5f3e802ce52bdd128498b75e1674c1286618e179d92ec547fb147054fa0a6dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25677450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be24b747da93d6c52d40f45404f8719c173a42b464b5789cc5474025c9089d34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 31 Jul 2021 02:36:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 31 Jul 2021 02:36:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 31 Jul 2021 02:36:20 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 31 Jul 2021 02:36:20 GMT
CMD ["traefik"]
# Sat, 31 Jul 2021 02:36:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ae7432b0647d420cf1b58fb8cf6cc41e8f62576eb2a2181636f0b1947e5e5`  
		Last Modified: Sat, 31 Jul 2021 02:37:33 GMT  
		Size: 22.3 MB (22274609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fea4bbca0e60d625a8cf83e9cad012b191eeaf6ce210d0e8ad56eb6d671f55`  
		Last Modified: Sat, 31 Jul 2021 02:37:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a41615d98172a2fa72371c2026ca919d961a0141966882c9914e5bff68f47bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:2.4-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:17fb216505087b084207b38a95d318992a40ae9ba46dc5e317274fc03831cc55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711238978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04699076d1a9eab653f094db7c2158a9869145ca0834f07f333749478cef23e9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:22:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Aug 2021 22:22:28 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:22:31 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:22:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90912d474c5962712685bc6a855937158d3241e468bfc55e023043dc0506479`  
		Last Modified: Wed, 11 Aug 2021 22:24:46 GMT  
		Size: 25.2 MB (25235339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919f221aa6cefffe52ce573cb4ddb0bf9c9138050cf2a5234228e15cf1328e42`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ce0016f6836c00ec8a261a8201f3bb23f298c6dd72d97ec880c262da230c84`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d73b6175e27dc1afd99d86249be714563d37eea5bfc9bb3cc75352377979f2`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4.13`

```console
$ docker pull traefik@sha256:3123d05e444f6297592c8443bcffe4bd291ab5b62e11a3d4eeb7ba3fd809540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.4.13` - linux; amd64

```console
$ docker pull traefik@sha256:577994c7e49027d4184ee5740f54c467970ac6a308bdc50d55dfc805884531da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28046777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d3b9e70c4801587dd39574069fb09dc0d7ca2853092ac7ef53d0b75484a389`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 19:38:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 19:38:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 19:38:17 GMT
EXPOSE 80
# Fri, 30 Jul 2021 19:38:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 19:38:17 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 19:38:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd0fbf25cb90ae5844a1d4d0e85f517bc8cf0460d690c234c64e25de3f96f4b`  
		Last Modified: Fri, 30 Jul 2021 19:39:00 GMT  
		Size: 24.6 MB (24555954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ff7bc59db0b71017ce81a509bb65fea811e77277c32790eaacd4bbc8da423`  
		Last Modified: Fri, 30 Jul 2021 19:38:54 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4.13` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5590ac7c1fb6040858fab793166b5e38f736652eb35c6c24ea56405d6017e8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26227229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d8f9270701f73afed1ff644a8b1d1124581418fa76527b45ea36641bb46db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:26:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:26:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:00 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:01 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b4e80431610821828160c0db44a02f117fccba4819a25adcc3bd9de58c22b4`  
		Last Modified: Fri, 30 Jul 2021 22:30:42 GMT  
		Size: 22.9 MB (22927935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae175f92c8d1f8b56063ad6238b79ce13588462980d692812b911c38065b76`  
		Last Modified: Fri, 30 Jul 2021 22:30:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4.13` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5f3e802ce52bdd128498b75e1674c1286618e179d92ec547fb147054fa0a6dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25677450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be24b747da93d6c52d40f45404f8719c173a42b464b5789cc5474025c9089d34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 31 Jul 2021 02:36:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 31 Jul 2021 02:36:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 31 Jul 2021 02:36:20 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 31 Jul 2021 02:36:20 GMT
CMD ["traefik"]
# Sat, 31 Jul 2021 02:36:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ae7432b0647d420cf1b58fb8cf6cc41e8f62576eb2a2181636f0b1947e5e5`  
		Last Modified: Sat, 31 Jul 2021 02:37:33 GMT  
		Size: 22.3 MB (22274609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fea4bbca0e60d625a8cf83e9cad012b191eeaf6ce210d0e8ad56eb6d671f55`  
		Last Modified: Sat, 31 Jul 2021 02:37:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4.13-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a41615d98172a2fa72371c2026ca919d961a0141966882c9914e5bff68f47bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:2.4.13-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:17fb216505087b084207b38a95d318992a40ae9ba46dc5e317274fc03831cc55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711238978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04699076d1a9eab653f094db7c2158a9869145ca0834f07f333749478cef23e9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:22:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Aug 2021 22:22:28 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:22:31 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:22:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90912d474c5962712685bc6a855937158d3241e468bfc55e023043dc0506479`  
		Last Modified: Wed, 11 Aug 2021 22:24:46 GMT  
		Size: 25.2 MB (25235339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919f221aa6cefffe52ce573cb4ddb0bf9c9138050cf2a5234228e15cf1328e42`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ce0016f6836c00ec8a261a8201f3bb23f298c6dd72d97ec880c262da230c84`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d73b6175e27dc1afd99d86249be714563d37eea5bfc9bb3cc75352377979f2`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5`

```console
$ docker pull traefik@sha256:9a22b1f60185764cadad4b2e5e895692a30fa01d65fbdc6592086cb31927c009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.5` - linux; amd64

```console
$ docker pull traefik@sha256:5cf0f6f96eb3c1d842bde27570878080393490a1c56c4117371d0c711bdd6122
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29030210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e265e1a81deb1daf89e5c6aa5fc92530f4d161ee693b89f0d5139ff91b7006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:37:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:37:37 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:37:38 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:37:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de16b6b635cbe20431112779adbbec2c4cc4062b2cbd8e5f39f081cdc74b41`  
		Last Modified: Fri, 13 Aug 2021 17:38:15 GMT  
		Size: 25.5 MB (25539385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f3d12cbb37e9c333debd6789c07b57b1e3317c7320a46339d48d746364ea3`  
		Last Modified: Fri, 13 Aug 2021 17:38:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d310b0051b6bdc3f56de74e0bca05b77bc9a497eb645428f8a609d62d665cbed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27264742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456b74e6f707f664ae849cc6edbdf3e69e0e6b63d37b89245312325ae27c51b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 18:03:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 18:03:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 18:03:22 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:03:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 18:03:23 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 18:03:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d736c480b7334d24e37d91c1ac3970aeb2f712bcec45494889bfc9ad7d9542f1`  
		Last Modified: Fri, 13 Aug 2021 18:06:03 GMT  
		Size: 24.0 MB (23965449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bf2333fbdb4ab0cce4f6f7f335421a90eb5c22abd271e24fdd90fda939507c`  
		Last Modified: Fri, 13 Aug 2021 18:05:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4553d27d5498959cea468421b7ed21e1a0ff822ac33a000ed53f2d19344bfb4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26700383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369563dbadf2d8a1e9860dac2b0469d7a507abf6c93ceffe00eed3dedd8d8c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:59:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:59:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:59:03 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:59:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:59:03 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:59:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19ee3061b5137cccaa71936b92503bc7ad40448089ba3d9befefe2cc4704ea`  
		Last Modified: Fri, 13 Aug 2021 18:00:18 GMT  
		Size: 23.3 MB (23297541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4143541af4e761731d18e8cb2557254937a27d42f8f27006a71a28a591eee3ca`  
		Last Modified: Fri, 13 Aug 2021 18:00:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b820c4be9523bec256c1091016e7f970b71ab31b101737eaee5e51c2bae7ba8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:2.5-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:cd296b2bd2892e99fdd72a49ada4fac54bf817a915d237f38042b21b6085f90c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712167705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a703a092323bb002d8b92665beb21ffc083c638935c7ebb3837ce15e15e1a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 18:28:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 13 Aug 2021 18:28:55 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:28:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 13 Aug 2021 18:29:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c454cb2f602228450ec4fe34ac1f2b3920fb09214bba9a201488118b7c4ca29`  
		Last Modified: Fri, 13 Aug 2021 18:29:43 GMT  
		Size: 26.2 MB (26164069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643f63b774a4b29d2347de436de9797ca0cebb3926a482b617a60237f21defa`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ad92d1b8849434207a60b6a10e6471e712f1de8a3be734920f6b7fa5ae710d`  
		Last Modified: Fri, 13 Aug 2021 18:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148535e4415b8b37ed988af60b37db3a5f5919d26c0d0a1b34d837ce40f5b5d3`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5.0-rc6`

```console
$ docker pull traefik@sha256:9a22b1f60185764cadad4b2e5e895692a30fa01d65fbdc6592086cb31927c009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.5.0-rc6` - linux; amd64

```console
$ docker pull traefik@sha256:5cf0f6f96eb3c1d842bde27570878080393490a1c56c4117371d0c711bdd6122
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29030210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e265e1a81deb1daf89e5c6aa5fc92530f4d161ee693b89f0d5139ff91b7006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:37:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:37:37 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:37:38 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:37:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de16b6b635cbe20431112779adbbec2c4cc4062b2cbd8e5f39f081cdc74b41`  
		Last Modified: Fri, 13 Aug 2021 17:38:15 GMT  
		Size: 25.5 MB (25539385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f3d12cbb37e9c333debd6789c07b57b1e3317c7320a46339d48d746364ea3`  
		Last Modified: Fri, 13 Aug 2021 17:38:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5.0-rc6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d310b0051b6bdc3f56de74e0bca05b77bc9a497eb645428f8a609d62d665cbed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27264742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456b74e6f707f664ae849cc6edbdf3e69e0e6b63d37b89245312325ae27c51b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 18:03:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 18:03:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 18:03:22 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:03:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 18:03:23 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 18:03:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d736c480b7334d24e37d91c1ac3970aeb2f712bcec45494889bfc9ad7d9542f1`  
		Last Modified: Fri, 13 Aug 2021 18:06:03 GMT  
		Size: 24.0 MB (23965449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bf2333fbdb4ab0cce4f6f7f335421a90eb5c22abd271e24fdd90fda939507c`  
		Last Modified: Fri, 13 Aug 2021 18:05:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5.0-rc6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4553d27d5498959cea468421b7ed21e1a0ff822ac33a000ed53f2d19344bfb4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26700383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369563dbadf2d8a1e9860dac2b0469d7a507abf6c93ceffe00eed3dedd8d8c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:59:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:59:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:59:03 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:59:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:59:03 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:59:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19ee3061b5137cccaa71936b92503bc7ad40448089ba3d9befefe2cc4704ea`  
		Last Modified: Fri, 13 Aug 2021 18:00:18 GMT  
		Size: 23.3 MB (23297541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4143541af4e761731d18e8cb2557254937a27d42f8f27006a71a28a591eee3ca`  
		Last Modified: Fri, 13 Aug 2021 18:00:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5.0-rc6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b820c4be9523bec256c1091016e7f970b71ab31b101737eaee5e51c2bae7ba8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:2.5.0-rc6-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:cd296b2bd2892e99fdd72a49ada4fac54bf817a915d237f38042b21b6085f90c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712167705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a703a092323bb002d8b92665beb21ffc083c638935c7ebb3837ce15e15e1a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 18:28:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 13 Aug 2021 18:28:55 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:28:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 13 Aug 2021 18:29:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c454cb2f602228450ec4fe34ac1f2b3920fb09214bba9a201488118b7c4ca29`  
		Last Modified: Fri, 13 Aug 2021 18:29:43 GMT  
		Size: 26.2 MB (26164069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643f63b774a4b29d2347de436de9797ca0cebb3926a482b617a60237f21defa`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ad92d1b8849434207a60b6a10e6471e712f1de8a3be734920f6b7fa5ae710d`  
		Last Modified: Fri, 13 Aug 2021 18:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148535e4415b8b37ed988af60b37db3a5f5919d26c0d0a1b34d837ce40f5b5d3`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:brie`

```console
$ docker pull traefik@sha256:9a22b1f60185764cadad4b2e5e895692a30fa01d65fbdc6592086cb31927c009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:brie` - linux; amd64

```console
$ docker pull traefik@sha256:5cf0f6f96eb3c1d842bde27570878080393490a1c56c4117371d0c711bdd6122
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29030210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e265e1a81deb1daf89e5c6aa5fc92530f4d161ee693b89f0d5139ff91b7006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:37:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:37:37 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:37:38 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:37:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de16b6b635cbe20431112779adbbec2c4cc4062b2cbd8e5f39f081cdc74b41`  
		Last Modified: Fri, 13 Aug 2021 17:38:15 GMT  
		Size: 25.5 MB (25539385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f3d12cbb37e9c333debd6789c07b57b1e3317c7320a46339d48d746364ea3`  
		Last Modified: Fri, 13 Aug 2021 17:38:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d310b0051b6bdc3f56de74e0bca05b77bc9a497eb645428f8a609d62d665cbed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27264742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456b74e6f707f664ae849cc6edbdf3e69e0e6b63d37b89245312325ae27c51b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 18:03:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 18:03:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 18:03:22 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:03:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 18:03:23 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 18:03:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d736c480b7334d24e37d91c1ac3970aeb2f712bcec45494889bfc9ad7d9542f1`  
		Last Modified: Fri, 13 Aug 2021 18:06:03 GMT  
		Size: 24.0 MB (23965449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bf2333fbdb4ab0cce4f6f7f335421a90eb5c22abd271e24fdd90fda939507c`  
		Last Modified: Fri, 13 Aug 2021 18:05:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4553d27d5498959cea468421b7ed21e1a0ff822ac33a000ed53f2d19344bfb4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26700383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369563dbadf2d8a1e9860dac2b0469d7a507abf6c93ceffe00eed3dedd8d8c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:59:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:59:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:59:03 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:59:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:59:03 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:59:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19ee3061b5137cccaa71936b92503bc7ad40448089ba3d9befefe2cc4704ea`  
		Last Modified: Fri, 13 Aug 2021 18:00:18 GMT  
		Size: 23.3 MB (23297541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4143541af4e761731d18e8cb2557254937a27d42f8f27006a71a28a591eee3ca`  
		Last Modified: Fri, 13 Aug 2021 18:00:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:brie-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b820c4be9523bec256c1091016e7f970b71ab31b101737eaee5e51c2bae7ba8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:brie-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:cd296b2bd2892e99fdd72a49ada4fac54bf817a915d237f38042b21b6085f90c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712167705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a703a092323bb002d8b92665beb21ffc083c638935c7ebb3837ce15e15e1a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 18:28:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 13 Aug 2021 18:28:55 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:28:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 13 Aug 2021 18:29:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c454cb2f602228450ec4fe34ac1f2b3920fb09214bba9a201488118b7c4ca29`  
		Last Modified: Fri, 13 Aug 2021 18:29:43 GMT  
		Size: 26.2 MB (26164069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643f63b774a4b29d2347de436de9797ca0cebb3926a482b617a60237f21defa`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ad92d1b8849434207a60b6a10e6471e712f1de8a3be734920f6b7fa5ae710d`  
		Last Modified: Fri, 13 Aug 2021 18:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148535e4415b8b37ed988af60b37db3a5f5919d26c0d0a1b34d837ce40f5b5d3`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:3123d05e444f6297592c8443bcffe4bd291ab5b62e11a3d4eeb7ba3fd809540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:577994c7e49027d4184ee5740f54c467970ac6a308bdc50d55dfc805884531da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28046777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d3b9e70c4801587dd39574069fb09dc0d7ca2853092ac7ef53d0b75484a389`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 19:38:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 19:38:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 19:38:17 GMT
EXPOSE 80
# Fri, 30 Jul 2021 19:38:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 19:38:17 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 19:38:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd0fbf25cb90ae5844a1d4d0e85f517bc8cf0460d690c234c64e25de3f96f4b`  
		Last Modified: Fri, 30 Jul 2021 19:39:00 GMT  
		Size: 24.6 MB (24555954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ff7bc59db0b71017ce81a509bb65fea811e77277c32790eaacd4bbc8da423`  
		Last Modified: Fri, 30 Jul 2021 19:38:54 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5590ac7c1fb6040858fab793166b5e38f736652eb35c6c24ea56405d6017e8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26227229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d8f9270701f73afed1ff644a8b1d1124581418fa76527b45ea36641bb46db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:26:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:26:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:00 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:01 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b4e80431610821828160c0db44a02f117fccba4819a25adcc3bd9de58c22b4`  
		Last Modified: Fri, 30 Jul 2021 22:30:42 GMT  
		Size: 22.9 MB (22927935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae175f92c8d1f8b56063ad6238b79ce13588462980d692812b911c38065b76`  
		Last Modified: Fri, 30 Jul 2021 22:30:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5f3e802ce52bdd128498b75e1674c1286618e179d92ec547fb147054fa0a6dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25677450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be24b747da93d6c52d40f45404f8719c173a42b464b5789cc5474025c9089d34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 31 Jul 2021 02:36:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 31 Jul 2021 02:36:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 31 Jul 2021 02:36:20 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 31 Jul 2021 02:36:20 GMT
CMD ["traefik"]
# Sat, 31 Jul 2021 02:36:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ae7432b0647d420cf1b58fb8cf6cc41e8f62576eb2a2181636f0b1947e5e5`  
		Last Modified: Sat, 31 Jul 2021 02:37:33 GMT  
		Size: 22.3 MB (22274609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fea4bbca0e60d625a8cf83e9cad012b191eeaf6ce210d0e8ad56eb6d671f55`  
		Last Modified: Sat, 31 Jul 2021 02:37:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:livarot`

```console
$ docker pull traefik@sha256:3123d05e444f6297592c8443bcffe4bd291ab5b62e11a3d4eeb7ba3fd809540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:livarot` - linux; amd64

```console
$ docker pull traefik@sha256:577994c7e49027d4184ee5740f54c467970ac6a308bdc50d55dfc805884531da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28046777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d3b9e70c4801587dd39574069fb09dc0d7ca2853092ac7ef53d0b75484a389`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 19:38:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 19:38:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 19:38:17 GMT
EXPOSE 80
# Fri, 30 Jul 2021 19:38:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 19:38:17 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 19:38:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd0fbf25cb90ae5844a1d4d0e85f517bc8cf0460d690c234c64e25de3f96f4b`  
		Last Modified: Fri, 30 Jul 2021 19:39:00 GMT  
		Size: 24.6 MB (24555954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ff7bc59db0b71017ce81a509bb65fea811e77277c32790eaacd4bbc8da423`  
		Last Modified: Fri, 30 Jul 2021 19:38:54 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5590ac7c1fb6040858fab793166b5e38f736652eb35c6c24ea56405d6017e8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26227229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d8f9270701f73afed1ff644a8b1d1124581418fa76527b45ea36641bb46db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:26:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:26:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:00 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:01 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b4e80431610821828160c0db44a02f117fccba4819a25adcc3bd9de58c22b4`  
		Last Modified: Fri, 30 Jul 2021 22:30:42 GMT  
		Size: 22.9 MB (22927935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae175f92c8d1f8b56063ad6238b79ce13588462980d692812b911c38065b76`  
		Last Modified: Fri, 30 Jul 2021 22:30:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5f3e802ce52bdd128498b75e1674c1286618e179d92ec547fb147054fa0a6dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25677450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be24b747da93d6c52d40f45404f8719c173a42b464b5789cc5474025c9089d34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 31 Jul 2021 02:36:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 31 Jul 2021 02:36:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 31 Jul 2021 02:36:20 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 31 Jul 2021 02:36:20 GMT
CMD ["traefik"]
# Sat, 31 Jul 2021 02:36:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ae7432b0647d420cf1b58fb8cf6cc41e8f62576eb2a2181636f0b1947e5e5`  
		Last Modified: Sat, 31 Jul 2021 02:37:33 GMT  
		Size: 22.3 MB (22274609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fea4bbca0e60d625a8cf83e9cad012b191eeaf6ce210d0e8ad56eb6d671f55`  
		Last Modified: Sat, 31 Jul 2021 02:37:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:livarot-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a41615d98172a2fa72371c2026ca919d961a0141966882c9914e5bff68f47bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:livarot-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:17fb216505087b084207b38a95d318992a40ae9ba46dc5e317274fc03831cc55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711238978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04699076d1a9eab653f094db7c2158a9869145ca0834f07f333749478cef23e9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:22:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Aug 2021 22:22:28 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:22:31 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:22:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90912d474c5962712685bc6a855937158d3241e468bfc55e023043dc0506479`  
		Last Modified: Wed, 11 Aug 2021 22:24:46 GMT  
		Size: 25.2 MB (25235339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919f221aa6cefffe52ce573cb4ddb0bf9c9138050cf2a5234228e15cf1328e42`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ce0016f6836c00ec8a261a8201f3bb23f298c6dd72d97ec880c262da230c84`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d73b6175e27dc1afd99d86249be714563d37eea5bfc9bb3cc75352377979f2`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:ca3883356d24f9fd6d36f0450d7f6f17a233317943517f6036c20ebf7c137781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:13bd9d65c0558740d1b8b6f8de06f314003be9b54eec4b8b67dad2cf58d037c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cea7c66ee3601de1cf66168feceac0bc9ac1147103e54d63f742e570bb0ca`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 22 Jun 2021 21:21:29 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 22 Jun 2021 21:21:31 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 22 Jun 2021 21:21:34 GMT
COPY file:440b6b1ebd389a2397ffb187ded4c85dcf37b7284d94c693b0b603d51247c683 in / 
# Tue, 22 Jun 2021 21:21:35 GMT
EXPOSE 80
# Tue, 22 Jun 2021 21:21:35 GMT
VOLUME [/tmp]
# Tue, 22 Jun 2021 21:21:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 22 Jun 2021 21:21:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:00918d1fc688f95413059b21ca56a6453b74d2808448ca35ed04b737d4a22c74`  
		Last Modified: Tue, 22 Jun 2021 21:24:22 GMT  
		Size: 130.9 KB (130871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e7abe8d1c9d1c5c74050eb312423f911185ce6cc705d32631fad6a1b3a4450`  
		Last Modified: Tue, 22 Jun 2021 21:24:23 GMT  
		Size: 308.9 KB (308853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee57e616d21eeb2181fd86ab18cbdb3be5af9c65ddb68c3657ebba7e266a191`  
		Last Modified: Tue, 22 Jun 2021 21:24:33 GMT  
		Size: 16.5 MB (16516801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f7fe0c0982ce55e8882f88193462be30b654f27dd1c5014243efd6fd85d563ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16533633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c3dd29cfce4ed4d7084315b52be936e63726239cbae0f98cf0c36cfdd8707a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 16 Jun 2021 11:17:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY file:6fdd60dc35db1c19a5de5ed8b57f159a6e121ba0f1ddb3e48a6e185da99f8cca in / 
# Wed, 16 Jun 2021 11:17:49 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:49 GMT
VOLUME [/tmp]
# Wed, 16 Jun 2021 11:17:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 16 Jun 2021 11:17:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ba07573b64554f7a74d3d3b27c42e28f5209c9d82f79b2596a6b190ee5475c72`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a5756798f3769843250c96f2b11eca4d4c83a91616dd5d97d17399022fc6e`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 308.9 KB (308857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af1647ff43bc2a163e816afb6eb2c410d240b736297469f44ec6db498f13fc`  
		Last Modified: Wed, 16 Jun 2021 11:19:28 GMT  
		Size: 16.1 MB (16093904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:1fa5d3b0e00c6b2b10eab9ea0e149f0930f36fb46dee9f56ec2a2c04570685f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:5e1e280e8e56520c8ebc11425f2c9fe66c9fae4714d65833d7f15c40fde8fb80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55847f6ab3e15d3f6304ec3271273146b44942dff17926a61366afbdf6736671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 15 Apr 2021 03:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 15 Apr 2021 03:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 15 Apr 2021 03:05:00 GMT
EXPOSE 80
# Thu, 15 Apr 2021 03:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 03:05:01 GMT
CMD ["traefik"]
# Thu, 15 Apr 2021 03:05:01 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40cdaabf18912622322046bb5eeda16c1ac513a094389e9b12b33ff02abb2c`  
		Last Modified: Thu, 15 Apr 2021 03:06:32 GMT  
		Size: 17.7 MB (17684875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ec9b7bad03eb2d44d70526dbd5478e8ee4043e8445168201605f71fafbb22e`  
		Last Modified: Thu, 15 Apr 2021 03:06:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6d12e7dd314491c93f36925c26748d18e9e7728c9f9d903bbe4120a9931ba35c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ddc131d7b096108dc285679a6bd9b6687758a14c5b8001347fbea7fe0bbc64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:27:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:27:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:29 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:31 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:32 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01457397f14eabab444a0392f736186f6c1469179bc6fafc66054e13a1ccd8`  
		Last Modified: Fri, 30 Jul 2021 22:31:21 GMT  
		Size: 16.5 MB (16516925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bba084b6a881bc33691e5efbdbbcb852b478fe5225e01b3132cc511ff78b89e`  
		Last Modified: Fri, 30 Jul 2021 22:31:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2d441643d23da8a818a8e403f0a3ca49e14979fb6aa79f86a8404669f7cc9b72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19496836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184b20b066615f1d8a085e3d6675d33e45801aca796ccc8defaae328b0b2b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 16 Jun 2021 11:17:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 16 Jun 2021 11:17:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 16 Jun 2021 11:17:38 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Jun 2021 11:17:38 GMT
CMD ["traefik"]
# Wed, 16 Jun 2021 11:17:38 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc700f9acd83a1c32048c47de8af63581c2a73eca263f30db7c161ca1855f2`  
		Last Modified: Wed, 16 Jun 2021 11:19:04 GMT  
		Size: 16.1 MB (16093993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e249b2d31cb237f67cb1f9438d0ec9e3357c69a8762ebbefa98b9815013727`  
		Last Modified: Wed, 16 Jun 2021 11:19:01 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7d1d137d268e564085e5c05f918bf4346a8290ab611c57d1ccf1e08e79b0006e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:ec1da595d84f5b3257698735564626a30c0560d9e68aa759d32cf96ed1625015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2704291103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e6922cc13d4e220d195b7a6d7aac00de05dfb4bb78eb345efe16dd2a6ebd88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:23:45 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 11 Aug 2021 22:23:48 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:23:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:23:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e191a5bf292d7a12c5f917dde336d2439d4d22f34b3ccc93ba2ec56eb429a5e`  
		Last Modified: Wed, 11 Aug 2021 22:25:11 GMT  
		Size: 18.3 MB (18287524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e368da9720874eda4c481f2fbfbc13d345ce8b07efd443a946a7f0a002163a9e`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a826777ecee2f4cb9fcf66ed49eff2226c0e7d5efcd438e572f89c791bfaaa`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac5b0da240f2ab9425ecd3484d6a900c5563251d11a6c4f9872fdc3f02f1635`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:ca3883356d24f9fd6d36f0450d7f6f17a233317943517f6036c20ebf7c137781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:13bd9d65c0558740d1b8b6f8de06f314003be9b54eec4b8b67dad2cf58d037c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cea7c66ee3601de1cf66168feceac0bc9ac1147103e54d63f742e570bb0ca`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 22 Jun 2021 21:21:29 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 22 Jun 2021 21:21:31 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 22 Jun 2021 21:21:34 GMT
COPY file:440b6b1ebd389a2397ffb187ded4c85dcf37b7284d94c693b0b603d51247c683 in / 
# Tue, 22 Jun 2021 21:21:35 GMT
EXPOSE 80
# Tue, 22 Jun 2021 21:21:35 GMT
VOLUME [/tmp]
# Tue, 22 Jun 2021 21:21:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 22 Jun 2021 21:21:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:00918d1fc688f95413059b21ca56a6453b74d2808448ca35ed04b737d4a22c74`  
		Last Modified: Tue, 22 Jun 2021 21:24:22 GMT  
		Size: 130.9 KB (130871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e7abe8d1c9d1c5c74050eb312423f911185ce6cc705d32631fad6a1b3a4450`  
		Last Modified: Tue, 22 Jun 2021 21:24:23 GMT  
		Size: 308.9 KB (308853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee57e616d21eeb2181fd86ab18cbdb3be5af9c65ddb68c3657ebba7e266a191`  
		Last Modified: Tue, 22 Jun 2021 21:24:33 GMT  
		Size: 16.5 MB (16516801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f7fe0c0982ce55e8882f88193462be30b654f27dd1c5014243efd6fd85d563ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16533633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c3dd29cfce4ed4d7084315b52be936e63726239cbae0f98cf0c36cfdd8707a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 16 Jun 2021 11:17:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY file:6fdd60dc35db1c19a5de5ed8b57f159a6e121ba0f1ddb3e48a6e185da99f8cca in / 
# Wed, 16 Jun 2021 11:17:49 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:49 GMT
VOLUME [/tmp]
# Wed, 16 Jun 2021 11:17:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 16 Jun 2021 11:17:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ba07573b64554f7a74d3d3b27c42e28f5209c9d82f79b2596a6b190ee5475c72`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a5756798f3769843250c96f2b11eca4d4c83a91616dd5d97d17399022fc6e`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 308.9 KB (308857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af1647ff43bc2a163e816afb6eb2c410d240b736297469f44ec6db498f13fc`  
		Last Modified: Wed, 16 Jun 2021 11:19:28 GMT  
		Size: 16.1 MB (16093904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:1fa5d3b0e00c6b2b10eab9ea0e149f0930f36fb46dee9f56ec2a2c04570685f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:5e1e280e8e56520c8ebc11425f2c9fe66c9fae4714d65833d7f15c40fde8fb80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55847f6ab3e15d3f6304ec3271273146b44942dff17926a61366afbdf6736671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 15 Apr 2021 03:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 15 Apr 2021 03:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 15 Apr 2021 03:05:00 GMT
EXPOSE 80
# Thu, 15 Apr 2021 03:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 03:05:01 GMT
CMD ["traefik"]
# Thu, 15 Apr 2021 03:05:01 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40cdaabf18912622322046bb5eeda16c1ac513a094389e9b12b33ff02abb2c`  
		Last Modified: Thu, 15 Apr 2021 03:06:32 GMT  
		Size: 17.7 MB (17684875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ec9b7bad03eb2d44d70526dbd5478e8ee4043e8445168201605f71fafbb22e`  
		Last Modified: Thu, 15 Apr 2021 03:06:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6d12e7dd314491c93f36925c26748d18e9e7728c9f9d903bbe4120a9931ba35c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ddc131d7b096108dc285679a6bd9b6687758a14c5b8001347fbea7fe0bbc64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:27:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:27:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:29 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:31 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:32 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01457397f14eabab444a0392f736186f6c1469179bc6fafc66054e13a1ccd8`  
		Last Modified: Fri, 30 Jul 2021 22:31:21 GMT  
		Size: 16.5 MB (16516925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bba084b6a881bc33691e5efbdbbcb852b478fe5225e01b3132cc511ff78b89e`  
		Last Modified: Fri, 30 Jul 2021 22:31:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2d441643d23da8a818a8e403f0a3ca49e14979fb6aa79f86a8404669f7cc9b72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19496836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184b20b066615f1d8a085e3d6675d33e45801aca796ccc8defaae328b0b2b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 16 Jun 2021 11:17:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 16 Jun 2021 11:17:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 16 Jun 2021 11:17:38 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Jun 2021 11:17:38 GMT
CMD ["traefik"]
# Wed, 16 Jun 2021 11:17:38 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc700f9acd83a1c32048c47de8af63581c2a73eca263f30db7c161ca1855f2`  
		Last Modified: Wed, 16 Jun 2021 11:19:04 GMT  
		Size: 16.1 MB (16093993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e249b2d31cb237f67cb1f9438d0ec9e3357c69a8762ebbefa98b9815013727`  
		Last Modified: Wed, 16 Jun 2021 11:19:01 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7d1d137d268e564085e5c05f918bf4346a8290ab611c57d1ccf1e08e79b0006e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:ec1da595d84f5b3257698735564626a30c0560d9e68aa759d32cf96ed1625015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2704291103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e6922cc13d4e220d195b7a6d7aac00de05dfb4bb78eb345efe16dd2a6ebd88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:23:45 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 11 Aug 2021 22:23:48 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:23:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:23:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e191a5bf292d7a12c5f917dde336d2439d4d22f34b3ccc93ba2ec56eb429a5e`  
		Last Modified: Wed, 11 Aug 2021 22:25:11 GMT  
		Size: 18.3 MB (18287524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e368da9720874eda4c481f2fbfbc13d345ce8b07efd443a946a7f0a002163a9e`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a826777ecee2f4cb9fcf66ed49eff2226c0e7d5efcd438e572f89c791bfaaa`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac5b0da240f2ab9425ecd3484d6a900c5563251d11a6c4f9872fdc3f02f1635`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.30`

```console
$ docker pull traefik@sha256:ca3883356d24f9fd6d36f0450d7f6f17a233317943517f6036c20ebf7c137781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.30` - linux; amd64

```console
$ docker pull traefik@sha256:353827cc14120a14b1eccbb2714039763d9cefc284213b53d82d14e110fadc39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18124621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2126389e0b0dbd13da033d79636b0f0626d73f1a6da0935ce6ce9eccae112a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 09 Mar 2021 01:32:48 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 09 Mar 2021 01:32:49 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Thu, 08 Apr 2021 20:07:38 GMT
COPY file:bc0b1c0235bda22a75d2ef00a982989cdf1da3240f077584bca5c6b560a4c13a in / 
# Thu, 08 Apr 2021 20:07:38 GMT
EXPOSE 80
# Thu, 08 Apr 2021 20:07:39 GMT
VOLUME [/tmp]
# Thu, 08 Apr 2021 20:07:39 GMT
ENTRYPOINT ["/traefik"]
# Thu, 08 Apr 2021 20:07:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:53f50c15495c67f391a5750288681a589b19a39c4b78e7ebc0934606cc3d0bc3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 130.9 KB (130870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c044b3636c16c5ab8fc96a04f320c9f97ea23aaffec9adb2d8f20ebaef93f3`  
		Last Modified: Tue, 09 Mar 2021 01:33:59 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb3d26b40720e4da5cbeb15193c698565e23551a24cc4abc4acd1b7de414279`  
		Last Modified: Thu, 08 Apr 2021 20:08:34 GMT  
		Size: 17.7 MB (17684928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.30` - linux; arm variant v6

```console
$ docker pull traefik@sha256:13bd9d65c0558740d1b8b6f8de06f314003be9b54eec4b8b67dad2cf58d037c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16956525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cea7c66ee3601de1cf66168feceac0bc9ac1147103e54d63f742e570bb0ca`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 22 Jun 2021 21:21:29 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Tue, 22 Jun 2021 21:21:31 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Tue, 22 Jun 2021 21:21:34 GMT
COPY file:440b6b1ebd389a2397ffb187ded4c85dcf37b7284d94c693b0b603d51247c683 in / 
# Tue, 22 Jun 2021 21:21:35 GMT
EXPOSE 80
# Tue, 22 Jun 2021 21:21:35 GMT
VOLUME [/tmp]
# Tue, 22 Jun 2021 21:21:35 GMT
ENTRYPOINT ["/traefik"]
# Tue, 22 Jun 2021 21:21:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:00918d1fc688f95413059b21ca56a6453b74d2808448ca35ed04b737d4a22c74`  
		Last Modified: Tue, 22 Jun 2021 21:24:22 GMT  
		Size: 130.9 KB (130871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e7abe8d1c9d1c5c74050eb312423f911185ce6cc705d32631fad6a1b3a4450`  
		Last Modified: Tue, 22 Jun 2021 21:24:23 GMT  
		Size: 308.9 KB (308853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee57e616d21eeb2181fd86ab18cbdb3be5af9c65ddb68c3657ebba7e266a191`  
		Last Modified: Tue, 22 Jun 2021 21:24:33 GMT  
		Size: 16.5 MB (16516801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.30` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f7fe0c0982ce55e8882f88193462be30b654f27dd1c5014243efd6fd85d563ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16533633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c3dd29cfce4ed4d7084315b52be936e63726239cbae0f98cf0c36cfdd8707a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 16 Jun 2021 11:17:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY dir:379603788862c2a6c57432d70b0a67f561fe00310e1b958c9ecf85381b1c9cd9 in /usr/share/ 
# Wed, 16 Jun 2021 11:17:48 GMT
COPY file:6fdd60dc35db1c19a5de5ed8b57f159a6e121ba0f1ddb3e48a6e185da99f8cca in / 
# Wed, 16 Jun 2021 11:17:49 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:49 GMT
VOLUME [/tmp]
# Wed, 16 Jun 2021 11:17:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 16 Jun 2021 11:17:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ba07573b64554f7a74d3d3b27c42e28f5209c9d82f79b2596a6b190ee5475c72`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a5756798f3769843250c96f2b11eca4d4c83a91616dd5d97d17399022fc6e`  
		Last Modified: Wed, 16 Jun 2021 11:19:25 GMT  
		Size: 308.9 KB (308857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6af1647ff43bc2a163e816afb6eb2c410d240b736297469f44ec6db498f13fc`  
		Last Modified: Wed, 16 Jun 2021 11:19:28 GMT  
		Size: 16.1 MB (16093904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.30-alpine`

```console
$ docker pull traefik@sha256:1fa5d3b0e00c6b2b10eab9ea0e149f0930f36fb46dee9f56ec2a2c04570685f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.30-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:5e1e280e8e56520c8ebc11425f2c9fe66c9fae4714d65833d7f15c40fde8fb80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21175700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55847f6ab3e15d3f6304ec3271273146b44942dff17926a61366afbdf6736671`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 15 Apr 2021 03:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 15 Apr 2021 03:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 15 Apr 2021 03:05:00 GMT
EXPOSE 80
# Thu, 15 Apr 2021 03:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Apr 2021 03:05:01 GMT
CMD ["traefik"]
# Thu, 15 Apr 2021 03:05:01 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40cdaabf18912622322046bb5eeda16c1ac513a094389e9b12b33ff02abb2c`  
		Last Modified: Thu, 15 Apr 2021 03:06:32 GMT  
		Size: 17.7 MB (17684875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ec9b7bad03eb2d44d70526dbd5478e8ee4043e8445168201605f71fafbb22e`  
		Last Modified: Thu, 15 Apr 2021 03:06:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.30-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6d12e7dd314491c93f36925c26748d18e9e7728c9f9d903bbe4120a9931ba35c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19816219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ddc131d7b096108dc285679a6bd9b6687758a14c5b8001347fbea7fe0bbc64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:27:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:27:28 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:29 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:31 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:32 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b01457397f14eabab444a0392f736186f6c1469179bc6fafc66054e13a1ccd8`  
		Last Modified: Fri, 30 Jul 2021 22:31:21 GMT  
		Size: 16.5 MB (16516925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bba084b6a881bc33691e5efbdbbcb852b478fe5225e01b3132cc511ff78b89e`  
		Last Modified: Fri, 30 Jul 2021 22:31:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.30-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:2d441643d23da8a818a8e403f0a3ca49e14979fb6aa79f86a8404669f7cc9b72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19496836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184b20b066615f1d8a085e3d6675d33e45801aca796ccc8defaae328b0b2b1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 16 Jun 2021 11:17:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 16 Jun 2021 11:17:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 16 Jun 2021 11:17:38 GMT
EXPOSE 80
# Wed, 16 Jun 2021 11:17:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Jun 2021 11:17:38 GMT
CMD ["traefik"]
# Wed, 16 Jun 2021 11:17:38 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cc700f9acd83a1c32048c47de8af63581c2a73eca263f30db7c161ca1855f2`  
		Last Modified: Wed, 16 Jun 2021 11:19:04 GMT  
		Size: 16.1 MB (16093993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e249b2d31cb237f67cb1f9438d0ec9e3357c69a8762ebbefa98b9815013727`  
		Last Modified: Wed, 16 Jun 2021 11:19:01 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.30-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7d1d137d268e564085e5c05f918bf4346a8290ab611c57d1ccf1e08e79b0006e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:v1.7.30-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:ec1da595d84f5b3257698735564626a30c0560d9e68aa759d32cf96ed1625015
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2704291103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e6922cc13d4e220d195b7a6d7aac00de05dfb4bb78eb345efe16dd2a6ebd88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:23:45 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.30/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 11 Aug 2021 22:23:48 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:23:50 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:23:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e191a5bf292d7a12c5f917dde336d2439d4d22f34b3ccc93ba2ec56eb429a5e`  
		Last Modified: Wed, 11 Aug 2021 22:25:11 GMT  
		Size: 18.3 MB (18287524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e368da9720874eda4c481f2fbfbc13d345ce8b07efd443a946a7f0a002163a9e`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a826777ecee2f4cb9fcf66ed49eff2226c0e7d5efcd438e572f89c791bfaaa`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac5b0da240f2ab9425ecd3484d6a900c5563251d11a6c4f9872fdc3f02f1635`  
		Last Modified: Wed, 11 Aug 2021 22:25:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4`

```console
$ docker pull traefik@sha256:3123d05e444f6297592c8443bcffe4bd291ab5b62e11a3d4eeb7ba3fd809540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.4` - linux; amd64

```console
$ docker pull traefik@sha256:577994c7e49027d4184ee5740f54c467970ac6a308bdc50d55dfc805884531da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28046777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d3b9e70c4801587dd39574069fb09dc0d7ca2853092ac7ef53d0b75484a389`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 19:38:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 19:38:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 19:38:17 GMT
EXPOSE 80
# Fri, 30 Jul 2021 19:38:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 19:38:17 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 19:38:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd0fbf25cb90ae5844a1d4d0e85f517bc8cf0460d690c234c64e25de3f96f4b`  
		Last Modified: Fri, 30 Jul 2021 19:39:00 GMT  
		Size: 24.6 MB (24555954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ff7bc59db0b71017ce81a509bb65fea811e77277c32790eaacd4bbc8da423`  
		Last Modified: Fri, 30 Jul 2021 19:38:54 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5590ac7c1fb6040858fab793166b5e38f736652eb35c6c24ea56405d6017e8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26227229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d8f9270701f73afed1ff644a8b1d1124581418fa76527b45ea36641bb46db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:26:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:26:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:00 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:01 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b4e80431610821828160c0db44a02f117fccba4819a25adcc3bd9de58c22b4`  
		Last Modified: Fri, 30 Jul 2021 22:30:42 GMT  
		Size: 22.9 MB (22927935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae175f92c8d1f8b56063ad6238b79ce13588462980d692812b911c38065b76`  
		Last Modified: Fri, 30 Jul 2021 22:30:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5f3e802ce52bdd128498b75e1674c1286618e179d92ec547fb147054fa0a6dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25677450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be24b747da93d6c52d40f45404f8719c173a42b464b5789cc5474025c9089d34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 31 Jul 2021 02:36:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 31 Jul 2021 02:36:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 31 Jul 2021 02:36:20 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 31 Jul 2021 02:36:20 GMT
CMD ["traefik"]
# Sat, 31 Jul 2021 02:36:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ae7432b0647d420cf1b58fb8cf6cc41e8f62576eb2a2181636f0b1947e5e5`  
		Last Modified: Sat, 31 Jul 2021 02:37:33 GMT  
		Size: 22.3 MB (22274609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fea4bbca0e60d625a8cf83e9cad012b191eeaf6ce210d0e8ad56eb6d671f55`  
		Last Modified: Sat, 31 Jul 2021 02:37:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a41615d98172a2fa72371c2026ca919d961a0141966882c9914e5bff68f47bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:v2.4-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:17fb216505087b084207b38a95d318992a40ae9ba46dc5e317274fc03831cc55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711238978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04699076d1a9eab653f094db7c2158a9869145ca0834f07f333749478cef23e9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:22:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Aug 2021 22:22:28 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:22:31 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:22:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90912d474c5962712685bc6a855937158d3241e468bfc55e023043dc0506479`  
		Last Modified: Wed, 11 Aug 2021 22:24:46 GMT  
		Size: 25.2 MB (25235339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919f221aa6cefffe52ce573cb4ddb0bf9c9138050cf2a5234228e15cf1328e42`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ce0016f6836c00ec8a261a8201f3bb23f298c6dd72d97ec880c262da230c84`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d73b6175e27dc1afd99d86249be714563d37eea5bfc9bb3cc75352377979f2`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4.13`

```console
$ docker pull traefik@sha256:3123d05e444f6297592c8443bcffe4bd291ab5b62e11a3d4eeb7ba3fd809540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.4.13` - linux; amd64

```console
$ docker pull traefik@sha256:577994c7e49027d4184ee5740f54c467970ac6a308bdc50d55dfc805884531da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28046777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d3b9e70c4801587dd39574069fb09dc0d7ca2853092ac7ef53d0b75484a389`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 19:38:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 19:38:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 19:38:17 GMT
EXPOSE 80
# Fri, 30 Jul 2021 19:38:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 19:38:17 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 19:38:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd0fbf25cb90ae5844a1d4d0e85f517bc8cf0460d690c234c64e25de3f96f4b`  
		Last Modified: Fri, 30 Jul 2021 19:39:00 GMT  
		Size: 24.6 MB (24555954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ff7bc59db0b71017ce81a509bb65fea811e77277c32790eaacd4bbc8da423`  
		Last Modified: Fri, 30 Jul 2021 19:38:54 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4.13` - linux; arm variant v6

```console
$ docker pull traefik@sha256:5590ac7c1fb6040858fab793166b5e38f736652eb35c6c24ea56405d6017e8f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26227229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9d8f9270701f73afed1ff644a8b1d1124581418fa76527b45ea36641bb46db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 30 Jul 2021 22:26:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 30 Jul 2021 22:26:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 30 Jul 2021 22:27:00 GMT
EXPOSE 80
# Fri, 30 Jul 2021 22:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 22:27:01 GMT
CMD ["traefik"]
# Fri, 30 Jul 2021 22:27:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b4e80431610821828160c0db44a02f117fccba4819a25adcc3bd9de58c22b4`  
		Last Modified: Fri, 30 Jul 2021 22:30:42 GMT  
		Size: 22.9 MB (22927935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ae175f92c8d1f8b56063ad6238b79ce13588462980d692812b911c38065b76`  
		Last Modified: Fri, 30 Jul 2021 22:30:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4.13` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5f3e802ce52bdd128498b75e1674c1286618e179d92ec547fb147054fa0a6dfd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25677450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be24b747da93d6c52d40f45404f8719c173a42b464b5789cc5474025c9089d34`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 31 Jul 2021 02:36:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 31 Jul 2021 02:36:20 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 31 Jul 2021 02:36:20 GMT
EXPOSE 80
# Sat, 31 Jul 2021 02:36:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 31 Jul 2021 02:36:20 GMT
CMD ["traefik"]
# Sat, 31 Jul 2021 02:36:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ae7432b0647d420cf1b58fb8cf6cc41e8f62576eb2a2181636f0b1947e5e5`  
		Last Modified: Sat, 31 Jul 2021 02:37:33 GMT  
		Size: 22.3 MB (22274609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fea4bbca0e60d625a8cf83e9cad012b191eeaf6ce210d0e8ad56eb6d671f55`  
		Last Modified: Sat, 31 Jul 2021 02:37:29 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4.13-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a41615d98172a2fa72371c2026ca919d961a0141966882c9914e5bff68f47bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:v2.4.13-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:17fb216505087b084207b38a95d318992a40ae9ba46dc5e317274fc03831cc55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711238978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04699076d1a9eab653f094db7c2158a9869145ca0834f07f333749478cef23e9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:22:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Aug 2021 22:22:28 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:22:31 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:22:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90912d474c5962712685bc6a855937158d3241e468bfc55e023043dc0506479`  
		Last Modified: Wed, 11 Aug 2021 22:24:46 GMT  
		Size: 25.2 MB (25235339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919f221aa6cefffe52ce573cb4ddb0bf9c9138050cf2a5234228e15cf1328e42`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ce0016f6836c00ec8a261a8201f3bb23f298c6dd72d97ec880c262da230c84`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d73b6175e27dc1afd99d86249be714563d37eea5bfc9bb3cc75352377979f2`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5`

```console
$ docker pull traefik@sha256:9a22b1f60185764cadad4b2e5e895692a30fa01d65fbdc6592086cb31927c009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.5` - linux; amd64

```console
$ docker pull traefik@sha256:5cf0f6f96eb3c1d842bde27570878080393490a1c56c4117371d0c711bdd6122
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29030210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e265e1a81deb1daf89e5c6aa5fc92530f4d161ee693b89f0d5139ff91b7006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:37:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:37:37 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:37:38 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:37:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de16b6b635cbe20431112779adbbec2c4cc4062b2cbd8e5f39f081cdc74b41`  
		Last Modified: Fri, 13 Aug 2021 17:38:15 GMT  
		Size: 25.5 MB (25539385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f3d12cbb37e9c333debd6789c07b57b1e3317c7320a46339d48d746364ea3`  
		Last Modified: Fri, 13 Aug 2021 17:38:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d310b0051b6bdc3f56de74e0bca05b77bc9a497eb645428f8a609d62d665cbed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27264742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456b74e6f707f664ae849cc6edbdf3e69e0e6b63d37b89245312325ae27c51b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 18:03:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 18:03:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 18:03:22 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:03:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 18:03:23 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 18:03:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d736c480b7334d24e37d91c1ac3970aeb2f712bcec45494889bfc9ad7d9542f1`  
		Last Modified: Fri, 13 Aug 2021 18:06:03 GMT  
		Size: 24.0 MB (23965449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bf2333fbdb4ab0cce4f6f7f335421a90eb5c22abd271e24fdd90fda939507c`  
		Last Modified: Fri, 13 Aug 2021 18:05:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4553d27d5498959cea468421b7ed21e1a0ff822ac33a000ed53f2d19344bfb4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26700383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369563dbadf2d8a1e9860dac2b0469d7a507abf6c93ceffe00eed3dedd8d8c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:59:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:59:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:59:03 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:59:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:59:03 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:59:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19ee3061b5137cccaa71936b92503bc7ad40448089ba3d9befefe2cc4704ea`  
		Last Modified: Fri, 13 Aug 2021 18:00:18 GMT  
		Size: 23.3 MB (23297541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4143541af4e761731d18e8cb2557254937a27d42f8f27006a71a28a591eee3ca`  
		Last Modified: Fri, 13 Aug 2021 18:00:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b820c4be9523bec256c1091016e7f970b71ab31b101737eaee5e51c2bae7ba8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:v2.5-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:cd296b2bd2892e99fdd72a49ada4fac54bf817a915d237f38042b21b6085f90c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712167705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a703a092323bb002d8b92665beb21ffc083c638935c7ebb3837ce15e15e1a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 18:28:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 13 Aug 2021 18:28:55 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:28:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 13 Aug 2021 18:29:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c454cb2f602228450ec4fe34ac1f2b3920fb09214bba9a201488118b7c4ca29`  
		Last Modified: Fri, 13 Aug 2021 18:29:43 GMT  
		Size: 26.2 MB (26164069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643f63b774a4b29d2347de436de9797ca0cebb3926a482b617a60237f21defa`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ad92d1b8849434207a60b6a10e6471e712f1de8a3be734920f6b7fa5ae710d`  
		Last Modified: Fri, 13 Aug 2021 18:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148535e4415b8b37ed988af60b37db3a5f5919d26c0d0a1b34d837ce40f5b5d3`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5.0-rc6`

```console
$ docker pull traefik@sha256:9a22b1f60185764cadad4b2e5e895692a30fa01d65fbdc6592086cb31927c009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.5.0-rc6` - linux; amd64

```console
$ docker pull traefik@sha256:5cf0f6f96eb3c1d842bde27570878080393490a1c56c4117371d0c711bdd6122
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (29030210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e265e1a81deb1daf89e5c6aa5fc92530f4d161ee693b89f0d5139ff91b7006`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:37:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:37:37 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:37:38 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:37:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0de16b6b635cbe20431112779adbbec2c4cc4062b2cbd8e5f39f081cdc74b41`  
		Last Modified: Fri, 13 Aug 2021 17:38:15 GMT  
		Size: 25.5 MB (25539385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f3d12cbb37e9c333debd6789c07b57b1e3317c7320a46339d48d746364ea3`  
		Last Modified: Fri, 13 Aug 2021 17:38:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5.0-rc6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d310b0051b6bdc3f56de74e0bca05b77bc9a497eb645428f8a609d62d665cbed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27264742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456b74e6f707f664ae849cc6edbdf3e69e0e6b63d37b89245312325ae27c51b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Fri, 30 Jul 2021 22:26:29 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 18:03:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 18:03:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 18:03:22 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:03:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 18:03:23 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 18:03:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed02d963bbf86d6e5434c3d67ade07a501b2cbc61b6ae18dfc155ede8f3b1591`  
		Last Modified: Fri, 30 Jul 2021 22:29:56 GMT  
		Size: 677.0 KB (677014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d736c480b7334d24e37d91c1ac3970aeb2f712bcec45494889bfc9ad7d9542f1`  
		Last Modified: Fri, 13 Aug 2021 18:06:03 GMT  
		Size: 24.0 MB (23965449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bf2333fbdb4ab0cce4f6f7f335421a90eb5c22abd271e24fdd90fda939507c`  
		Last Modified: Fri, 13 Aug 2021 18:05:47 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5.0-rc6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4553d27d5498959cea468421b7ed21e1a0ff822ac33a000ed53f2d19344bfb4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26700383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5369563dbadf2d8a1e9860dac2b0469d7a507abf6c93ceffe00eed3dedd8d8c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 13 Aug 2021 17:59:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 13 Aug 2021 17:59:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 13 Aug 2021 17:59:03 GMT
EXPOSE 80
# Fri, 13 Aug 2021 17:59:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Aug 2021 17:59:03 GMT
CMD ["traefik"]
# Fri, 13 Aug 2021 17:59:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c19ee3061b5137cccaa71936b92503bc7ad40448089ba3d9befefe2cc4704ea`  
		Last Modified: Fri, 13 Aug 2021 18:00:18 GMT  
		Size: 23.3 MB (23297541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4143541af4e761731d18e8cb2557254937a27d42f8f27006a71a28a591eee3ca`  
		Last Modified: Fri, 13 Aug 2021 18:00:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5.0-rc6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b820c4be9523bec256c1091016e7f970b71ab31b101737eaee5e51c2bae7ba8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:v2.5.0-rc6-windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:cd296b2bd2892e99fdd72a49ada4fac54bf817a915d237f38042b21b6085f90c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2712167705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1a703a092323bb002d8b92665beb21ffc083c638935c7ebb3837ce15e15e1a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Aug 2021 18:28:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.0-rc6/traefik_v2.5.0-rc6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 13 Aug 2021 18:28:55 GMT
EXPOSE 80
# Fri, 13 Aug 2021 18:28:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 13 Aug 2021 18:29:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c454cb2f602228450ec4fe34ac1f2b3920fb09214bba9a201488118b7c4ca29`  
		Last Modified: Fri, 13 Aug 2021 18:29:43 GMT  
		Size: 26.2 MB (26164069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7643f63b774a4b29d2347de436de9797ca0cebb3926a482b617a60237f21defa`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ad92d1b8849434207a60b6a10e6471e712f1de8a3be734920f6b7fa5ae710d`  
		Last Modified: Fri, 13 Aug 2021 18:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148535e4415b8b37ed988af60b37db3a5f5919d26c0d0a1b34d837ce40f5b5d3`  
		Last Modified: Fri, 13 Aug 2021 18:29:36 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:a41615d98172a2fa72371c2026ca919d961a0141966882c9914e5bff68f47bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull traefik@sha256:17fb216505087b084207b38a95d318992a40ae9ba46dc5e317274fc03831cc55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2711238978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04699076d1a9eab653f094db7c2158a9869145ca0834f07f333749478cef23e9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 22:22:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.13/traefik_v2.4.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Aug 2021 22:22:28 GMT
EXPOSE 80
# Wed, 11 Aug 2021 22:22:31 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Aug 2021 22:22:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90912d474c5962712685bc6a855937158d3241e468bfc55e023043dc0506479`  
		Last Modified: Wed, 11 Aug 2021 22:24:46 GMT  
		Size: 25.2 MB (25235339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919f221aa6cefffe52ce573cb4ddb0bf9c9138050cf2a5234228e15cf1328e42`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ce0016f6836c00ec8a261a8201f3bb23f298c6dd72d97ec880c262da230c84`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d73b6175e27dc1afd99d86249be714563d37eea5bfc9bb3cc75352377979f2`  
		Last Modified: Wed, 11 Aug 2021 22:24:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
