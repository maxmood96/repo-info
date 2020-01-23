<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7.20`](#traefik1720)
-	[`traefik:1.7.20-alpine`](#traefik1720-alpine)
-	[`traefik:1.7.20-windowsservercore-1809`](#traefik1720-windowsservercore-1809)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:2.1`](#traefik21)
-	[`traefik:2.1.3`](#traefik213)
-	[`traefik:2.1.3-windowsservercore-1809`](#traefik213-windowsservercore-1809)
-	[`traefik:2.1-windowsservercore-1809`](#traefik21-windowsservercore-1809)
-	[`traefik:cantal`](#traefikcantal)
-	[`traefik:cantal-windowsservercore-1809`](#traefikcantal-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7.20`](#traefikv1720)
-	[`traefik:v1.7.20-alpine`](#traefikv1720-alpine)
-	[`traefik:v1.7.20-windowsservercore-1809`](#traefikv1720-windowsservercore-1809)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v2.1`](#traefikv21)
-	[`traefik:v2.1.3`](#traefikv213)
-	[`traefik:v2.1.3-windowsservercore-1809`](#traefikv213-windowsservercore-1809)
-	[`traefik:v2.1-windowsservercore-1809`](#traefikv21-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:5ec34caf19d114f8f0ed76f9bc3dad6ba8cf6d13a1575c4294b59b77709def39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3b1c4d57c57d125a5d949d463d41882fefc957ce117db226aace4e7314e82d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24005352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c63a7d3e502fcbbd8937a2523368c22d0edd1788b8389af095f64038318834`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 01:00:22 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 22:26:52 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:31:38 GMT
COPY file:be1ea92a6d3f63051c9ae787ca41c986b81a56ce7f8b8347b97c3ddc3b4471f5 in / 
# Tue, 10 Dec 2019 22:31:38 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:38 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:31:38 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:31:39 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:42e7d26ec3785f8ce0f20e327cf72404ee054ba022ce9068ad2d28c52e82db2a`  
		Last Modified: Tue, 27 Aug 2019 01:00:52 GMT  
		Size: 132.0 KB (132022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a753f02eeffef33e5e071a6feac9e12fffb36330fc7ef5441f378d0ce67c528`  
		Last Modified: Mon, 21 Oct 2019 22:27:25 GMT  
		Size: 327.3 KB (327346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab927d94d255c72862c3e7ada3f6cdb36f90926b7a8913a080062b17d73f186b`  
		Last Modified: Tue, 10 Dec 2019 22:32:27 GMT  
		Size: 23.5 MB (23545984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3a32e589b7d538f688f0a4d5777ab21dc2e946e22a1b08872aaad72b4192976e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22491539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099411d81ac7bf28b232625f19ecc6590f39c3920418958b3056caa4f85815c4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 26 Aug 2019 23:54:26 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 20:27:55 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 21:57:12 GMT
COPY file:ad6d99c4dea9edfff1bf18494e1c85b8a82b1a74f77a8bf3f437bd05222fbf79 in / 
# Tue, 10 Dec 2019 21:57:14 GMT
EXPOSE 80
# Tue, 10 Dec 2019 21:57:15 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 21:57:16 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 21:57:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:506698346e0f5f486b919abaa7bc72252b3dc553cb28e0d1a5e2b6f3708cf4c0`  
		Last Modified: Mon, 26 Aug 2019 23:55:08 GMT  
		Size: 132.0 KB (132026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037320e6487ea40f4dfb2c29d120090739bc20051bca67eb5e64a072973136`  
		Last Modified: Mon, 21 Oct 2019 20:28:50 GMT  
		Size: 327.4 KB (327388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0d7ab9d9ce392bdaa622a30db2df3963e7ac8b19c846fddc788b2f7fd3f890`  
		Last Modified: Tue, 10 Dec 2019 21:58:07 GMT  
		Size: 22.0 MB (22032125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3a587a9647aca9d58c237389157512cf349f00e99afc0f33959501bc5366b489
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22219190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843151930dcd29bc722fa2e9949bcecfcb0020d961037b85983f47017aa38a58`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 00:16:41 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 23:22:44 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:39:48 GMT
COPY file:2548a09c5388b09356e8109d52a2261b02b840df1156718406457af4ef9eedcd in / 
# Tue, 10 Dec 2019 22:39:50 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:50 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:39:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:39:51 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f07a1cd6fb05ab2fb5b66f5326144f82e52f5580df40a42e400637f8a8f9c6d8`  
		Last Modified: Tue, 27 Aug 2019 00:17:31 GMT  
		Size: 132.0 KB (132021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2afd881e5b94f57a79b2f6bcd9d637c2f7a6aa910f4013045b8653ebe29fdb`  
		Last Modified: Mon, 21 Oct 2019 23:23:36 GMT  
		Size: 327.4 KB (327378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b05c8936168a3f333423ce8dca6ed7e5ad1890ce50b95da487f61aa83440e26`  
		Last Modified: Tue, 10 Dec 2019 22:40:39 GMT  
		Size: 21.8 MB (21759791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.20`

```console
$ docker pull traefik@sha256:5ec34caf19d114f8f0ed76f9bc3dad6ba8cf6d13a1575c4294b59b77709def39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.20` - linux; amd64

```console
$ docker pull traefik@sha256:3b1c4d57c57d125a5d949d463d41882fefc957ce117db226aace4e7314e82d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24005352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c63a7d3e502fcbbd8937a2523368c22d0edd1788b8389af095f64038318834`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 01:00:22 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 22:26:52 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:31:38 GMT
COPY file:be1ea92a6d3f63051c9ae787ca41c986b81a56ce7f8b8347b97c3ddc3b4471f5 in / 
# Tue, 10 Dec 2019 22:31:38 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:38 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:31:38 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:31:39 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:42e7d26ec3785f8ce0f20e327cf72404ee054ba022ce9068ad2d28c52e82db2a`  
		Last Modified: Tue, 27 Aug 2019 01:00:52 GMT  
		Size: 132.0 KB (132022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a753f02eeffef33e5e071a6feac9e12fffb36330fc7ef5441f378d0ce67c528`  
		Last Modified: Mon, 21 Oct 2019 22:27:25 GMT  
		Size: 327.3 KB (327346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab927d94d255c72862c3e7ada3f6cdb36f90926b7a8913a080062b17d73f186b`  
		Last Modified: Tue, 10 Dec 2019 22:32:27 GMT  
		Size: 23.5 MB (23545984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.20` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3a32e589b7d538f688f0a4d5777ab21dc2e946e22a1b08872aaad72b4192976e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22491539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099411d81ac7bf28b232625f19ecc6590f39c3920418958b3056caa4f85815c4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 26 Aug 2019 23:54:26 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 20:27:55 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 21:57:12 GMT
COPY file:ad6d99c4dea9edfff1bf18494e1c85b8a82b1a74f77a8bf3f437bd05222fbf79 in / 
# Tue, 10 Dec 2019 21:57:14 GMT
EXPOSE 80
# Tue, 10 Dec 2019 21:57:15 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 21:57:16 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 21:57:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:506698346e0f5f486b919abaa7bc72252b3dc553cb28e0d1a5e2b6f3708cf4c0`  
		Last Modified: Mon, 26 Aug 2019 23:55:08 GMT  
		Size: 132.0 KB (132026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037320e6487ea40f4dfb2c29d120090739bc20051bca67eb5e64a072973136`  
		Last Modified: Mon, 21 Oct 2019 20:28:50 GMT  
		Size: 327.4 KB (327388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0d7ab9d9ce392bdaa622a30db2df3963e7ac8b19c846fddc788b2f7fd3f890`  
		Last Modified: Tue, 10 Dec 2019 21:58:07 GMT  
		Size: 22.0 MB (22032125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.20` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3a587a9647aca9d58c237389157512cf349f00e99afc0f33959501bc5366b489
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22219190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843151930dcd29bc722fa2e9949bcecfcb0020d961037b85983f47017aa38a58`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 00:16:41 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 23:22:44 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:39:48 GMT
COPY file:2548a09c5388b09356e8109d52a2261b02b840df1156718406457af4ef9eedcd in / 
# Tue, 10 Dec 2019 22:39:50 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:50 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:39:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:39:51 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f07a1cd6fb05ab2fb5b66f5326144f82e52f5580df40a42e400637f8a8f9c6d8`  
		Last Modified: Tue, 27 Aug 2019 00:17:31 GMT  
		Size: 132.0 KB (132021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2afd881e5b94f57a79b2f6bcd9d637c2f7a6aa910f4013045b8653ebe29fdb`  
		Last Modified: Mon, 21 Oct 2019 23:23:36 GMT  
		Size: 327.4 KB (327378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b05c8936168a3f333423ce8dca6ed7e5ad1890ce50b95da487f61aa83440e26`  
		Last Modified: Tue, 10 Dec 2019 22:40:39 GMT  
		Size: 21.8 MB (21759791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.20-alpine`

```console
$ docker pull traefik@sha256:5c83e759dd0242f06079871204c4a70c0a38e9cb926374a7589608376430f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.20-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:f9f7bc3071415790c015ad52995e2997d9d1cfd5cffdde58cb403e15d71fbe4e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27028274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e73a064c8f244ce1fe21cb3abcc9b314309275e3b26fd6ac0276946f669c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:31:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:31:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:31:02 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:31:02 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:31:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d6da64444dd0f60f3c566038d6c9157c290fb6152ec296204e862073f365f`  
		Last Modified: Tue, 10 Dec 2019 22:32:13 GMT  
		Size: 23.5 MB (23546279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7a10facf04db24667668cb9792494b0e49f33e439cccf618f435ef237bfa3`  
		Last Modified: Tue, 10 Dec 2019 22:32:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.20-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:59849962d6b994b67dc7fbc511912c5a1b87944e9b1fda436acb6502c53506a8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25301946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307869ccfa13af9d37cbe35f32b4bfa91f47eb7cb00bad6cfdfbac45293e452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:39 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:42 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d03b0a042ba73cfa9ff088a916bb4dd22cec09c6862278e94c8f4445863f12`  
		Last Modified: Thu, 23 Jan 2020 20:54:01 GMT  
		Size: 22.0 MB (22032328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7026f34a4d522e997bb9203822966f0365b1d11745be187098906406a66e3`  
		Last Modified: Thu, 23 Jan 2020 20:53:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.20-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69880c97f253a7dab9e3fb1e477bc209a297ceb369f259841a14ec194ac5fbe3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25175702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630da378646ff9d16799a8f19fc83d02d28fe478003b44b8f37a8b0a4b715079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:39:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:39:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:39:27 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:39:28 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:39:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ad2d17ee7cb6da8499ef5415cad503d05873da472bcfc6d2ac07e9bdbad2c`  
		Last Modified: Tue, 10 Dec 2019 22:40:19 GMT  
		Size: 21.8 MB (21759668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ac7ce9940a937d298cf00954af64fd399df1a840cad75914caeb0b5cf224`  
		Last Modified: Tue, 10 Dec 2019 22:40:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.20-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5545c7138c85b3bc5ad0b8775ee168ae16c839bddbe83b4af20a1660a4dde29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:1.7.20-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:6cfb866dc049dc285053e1f6a51226552c66627ae5af596fef51d5816d0095a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245517816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8717289fcbe162ad339e623185f4cb3fde105c3346a906b3d9e45e58d582b94c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 22:25:10 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jan 2020 22:25:14 GMT
EXPOSE 80
# Wed, 15 Jan 2020 22:25:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jan 2020 22:25:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa553b540bc891379b327f7ebaf07fc18540471d50ab5ee933ac25c388bbd599`  
		Last Modified: Wed, 15 Jan 2020 22:27:30 GMT  
		Size: 28.1 MB (28101873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a7f9ea7b7d37ae92c7d35e40837cf30a6fb9e06234933ef771963f08e1b5d`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96835f334cd72d34b10c788e7adf2692a9038c2e79e936ff84d1136d3e2ed8e5`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c384663a41950e20d89986102e168d0afd30f4b754869dbcf6a7e1a4d99a9d73`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:5c83e759dd0242f06079871204c4a70c0a38e9cb926374a7589608376430f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:f9f7bc3071415790c015ad52995e2997d9d1cfd5cffdde58cb403e15d71fbe4e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27028274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e73a064c8f244ce1fe21cb3abcc9b314309275e3b26fd6ac0276946f669c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:31:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:31:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:31:02 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:31:02 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:31:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d6da64444dd0f60f3c566038d6c9157c290fb6152ec296204e862073f365f`  
		Last Modified: Tue, 10 Dec 2019 22:32:13 GMT  
		Size: 23.5 MB (23546279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7a10facf04db24667668cb9792494b0e49f33e439cccf618f435ef237bfa3`  
		Last Modified: Tue, 10 Dec 2019 22:32:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:59849962d6b994b67dc7fbc511912c5a1b87944e9b1fda436acb6502c53506a8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25301946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307869ccfa13af9d37cbe35f32b4bfa91f47eb7cb00bad6cfdfbac45293e452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:39 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:42 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d03b0a042ba73cfa9ff088a916bb4dd22cec09c6862278e94c8f4445863f12`  
		Last Modified: Thu, 23 Jan 2020 20:54:01 GMT  
		Size: 22.0 MB (22032328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7026f34a4d522e997bb9203822966f0365b1d11745be187098906406a66e3`  
		Last Modified: Thu, 23 Jan 2020 20:53:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69880c97f253a7dab9e3fb1e477bc209a297ceb369f259841a14ec194ac5fbe3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25175702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630da378646ff9d16799a8f19fc83d02d28fe478003b44b8f37a8b0a4b715079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:39:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:39:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:39:27 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:39:28 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:39:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ad2d17ee7cb6da8499ef5415cad503d05873da472bcfc6d2ac07e9bdbad2c`  
		Last Modified: Tue, 10 Dec 2019 22:40:19 GMT  
		Size: 21.8 MB (21759668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ac7ce9940a937d298cf00954af64fd399df1a840cad75914caeb0b5cf224`  
		Last Modified: Tue, 10 Dec 2019 22:40:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5545c7138c85b3bc5ad0b8775ee168ae16c839bddbe83b4af20a1660a4dde29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:6cfb866dc049dc285053e1f6a51226552c66627ae5af596fef51d5816d0095a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245517816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8717289fcbe162ad339e623185f4cb3fde105c3346a906b3d9e45e58d582b94c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 22:25:10 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jan 2020 22:25:14 GMT
EXPOSE 80
# Wed, 15 Jan 2020 22:25:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jan 2020 22:25:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa553b540bc891379b327f7ebaf07fc18540471d50ab5ee933ac25c388bbd599`  
		Last Modified: Wed, 15 Jan 2020 22:27:30 GMT  
		Size: 28.1 MB (28101873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a7f9ea7b7d37ae92c7d35e40837cf30a6fb9e06234933ef771963f08e1b5d`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96835f334cd72d34b10c788e7adf2692a9038c2e79e936ff84d1136d3e2ed8e5`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c384663a41950e20d89986102e168d0afd30f4b754869dbcf6a7e1a4d99a9d73`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1`

```console
$ docker pull traefik@sha256:e5edf9fea8fcedb039480dcf398aa3279e1506cdff2674c04794cc930f7c4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.1` - linux; amd64

```console
$ docker pull traefik@sha256:16ce63dfe54e6b11c8e1f11e34404607478a1ea0257fbad477832426b191782f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e4cf9e09992de0536741f1ce252f046131a881e69709d9d1d9b653219efdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 05:01:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 05:01:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 05:01:15 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:01:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 05:01:16 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 05:01:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c88a164b3fefd40411797d4c4af9365de098fdd9a632f0a0adc0875f99ab5d`  
		Last Modified: Wed, 22 Jan 2020 05:01:40 GMT  
		Size: 19.5 MB (19538838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65ff63a2d1b8e50ddfb769d6828e1f7f03ae2ec79ad14e8f2da7ffa368511c`  
		Last Modified: Wed, 22 Jan 2020 05:01:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fc0985ab6efd46cffd9157532f2682cf326efdfd0bb454ca7044d73bf96b89f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21573268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893008b3c69b472633c9dc409d78d8c7ebf291799526afdead1369ece43286f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:23 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:24 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efe145ce19ec8ece55144f045adee219ed148ce03443fab05db544a8685e7b`  
		Last Modified: Thu, 23 Jan 2020 20:53:35 GMT  
		Size: 18.3 MB (18303650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f838c6d816804ddca1127e8ec26baeba2222f8de0142edefd6a9a7b3335a7f7`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4559e357810e5e0a4f2524f54c77cc95de87030cb6fd9a7b5949aa527e9db8d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21407174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c147845c6981e275fbbd4e842f8544d4cd36bf6f7f175234b20b4d1bc8b2876`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 04:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 04:20:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 04:20:12 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 04:20:13 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 04:20:14 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e81461f690e8dbc553d4de8266f58bad5baa9ecfa80b7d0817e6294ba72c82`  
		Last Modified: Wed, 22 Jan 2020 04:20:44 GMT  
		Size: 18.0 MB (17991139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cc196abfad67ae916449e24572d62e834760748f3ff5868a59576f3107630`  
		Last Modified: Wed, 22 Jan 2020 04:20:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1.3`

```console
$ docker pull traefik@sha256:e5edf9fea8fcedb039480dcf398aa3279e1506cdff2674c04794cc930f7c4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.1.3` - linux; amd64

```console
$ docker pull traefik@sha256:16ce63dfe54e6b11c8e1f11e34404607478a1ea0257fbad477832426b191782f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e4cf9e09992de0536741f1ce252f046131a881e69709d9d1d9b653219efdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 05:01:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 05:01:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 05:01:15 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:01:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 05:01:16 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 05:01:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c88a164b3fefd40411797d4c4af9365de098fdd9a632f0a0adc0875f99ab5d`  
		Last Modified: Wed, 22 Jan 2020 05:01:40 GMT  
		Size: 19.5 MB (19538838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65ff63a2d1b8e50ddfb769d6828e1f7f03ae2ec79ad14e8f2da7ffa368511c`  
		Last Modified: Wed, 22 Jan 2020 05:01:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fc0985ab6efd46cffd9157532f2682cf326efdfd0bb454ca7044d73bf96b89f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21573268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893008b3c69b472633c9dc409d78d8c7ebf291799526afdead1369ece43286f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:23 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:24 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efe145ce19ec8ece55144f045adee219ed148ce03443fab05db544a8685e7b`  
		Last Modified: Thu, 23 Jan 2020 20:53:35 GMT  
		Size: 18.3 MB (18303650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f838c6d816804ddca1127e8ec26baeba2222f8de0142edefd6a9a7b3335a7f7`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.1.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4559e357810e5e0a4f2524f54c77cc95de87030cb6fd9a7b5949aa527e9db8d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21407174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c147845c6981e275fbbd4e842f8544d4cd36bf6f7f175234b20b4d1bc8b2876`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 04:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 04:20:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 04:20:12 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 04:20:13 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 04:20:14 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e81461f690e8dbc553d4de8266f58bad5baa9ecfa80b7d0817e6294ba72c82`  
		Last Modified: Wed, 22 Jan 2020 04:20:44 GMT  
		Size: 18.0 MB (17991139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cc196abfad67ae916449e24572d62e834760748f3ff5868a59576f3107630`  
		Last Modified: Wed, 22 Jan 2020 04:20:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:48745f9ef6d2873119824b3712650a8ec5ee469c2f120709d321e8aa35344e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:2.1.3-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:e42596a4ab6f5587d0971dc7d8b42791e7cfab035c86f02c9025f45e55eed2a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2241520898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4650d2b8183b0c02b800306ee9fd10777064324a6f2d966d034807652cbdb88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2020 01:21:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Jan 2020 01:21:20 GMT
EXPOSE 80
# Wed, 22 Jan 2020 01:21:22 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Jan 2020 01:21:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac359444ef8b5992a9677d0d9da78088aa1d7bd38988866498033461b5a17f`  
		Last Modified: Wed, 22 Jan 2020 01:22:01 GMT  
		Size: 24.1 MB (24104914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c48b965beae347426e3d11b093239de75b99ff759d731158139bf41d0f3965`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3fa86579b5d352b4071de541439e828bbdf0f9c1d98d562c7d0b0311aac0e`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da57b9c526d121005dfea489e834a4b9f892c96131110374d5687c4e1d423a82`  
		Last Modified: Wed, 22 Jan 2020 01:21:55 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:48745f9ef6d2873119824b3712650a8ec5ee469c2f120709d321e8aa35344e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:2.1-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:e42596a4ab6f5587d0971dc7d8b42791e7cfab035c86f02c9025f45e55eed2a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2241520898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4650d2b8183b0c02b800306ee9fd10777064324a6f2d966d034807652cbdb88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2020 01:21:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Jan 2020 01:21:20 GMT
EXPOSE 80
# Wed, 22 Jan 2020 01:21:22 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Jan 2020 01:21:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac359444ef8b5992a9677d0d9da78088aa1d7bd38988866498033461b5a17f`  
		Last Modified: Wed, 22 Jan 2020 01:22:01 GMT  
		Size: 24.1 MB (24104914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c48b965beae347426e3d11b093239de75b99ff759d731158139bf41d0f3965`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3fa86579b5d352b4071de541439e828bbdf0f9c1d98d562c7d0b0311aac0e`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da57b9c526d121005dfea489e834a4b9f892c96131110374d5687c4e1d423a82`  
		Last Modified: Wed, 22 Jan 2020 01:21:55 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:cantal`

```console
$ docker pull traefik@sha256:e5edf9fea8fcedb039480dcf398aa3279e1506cdff2674c04794cc930f7c4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:cantal` - linux; amd64

```console
$ docker pull traefik@sha256:16ce63dfe54e6b11c8e1f11e34404607478a1ea0257fbad477832426b191782f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e4cf9e09992de0536741f1ce252f046131a881e69709d9d1d9b653219efdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 05:01:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 05:01:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 05:01:15 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:01:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 05:01:16 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 05:01:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c88a164b3fefd40411797d4c4af9365de098fdd9a632f0a0adc0875f99ab5d`  
		Last Modified: Wed, 22 Jan 2020 05:01:40 GMT  
		Size: 19.5 MB (19538838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65ff63a2d1b8e50ddfb769d6828e1f7f03ae2ec79ad14e8f2da7ffa368511c`  
		Last Modified: Wed, 22 Jan 2020 05:01:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:cantal` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fc0985ab6efd46cffd9157532f2682cf326efdfd0bb454ca7044d73bf96b89f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21573268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893008b3c69b472633c9dc409d78d8c7ebf291799526afdead1369ece43286f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:23 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:24 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efe145ce19ec8ece55144f045adee219ed148ce03443fab05db544a8685e7b`  
		Last Modified: Thu, 23 Jan 2020 20:53:35 GMT  
		Size: 18.3 MB (18303650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f838c6d816804ddca1127e8ec26baeba2222f8de0142edefd6a9a7b3335a7f7`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:cantal` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4559e357810e5e0a4f2524f54c77cc95de87030cb6fd9a7b5949aa527e9db8d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21407174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c147845c6981e275fbbd4e842f8544d4cd36bf6f7f175234b20b4d1bc8b2876`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 04:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 04:20:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 04:20:12 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 04:20:13 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 04:20:14 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e81461f690e8dbc553d4de8266f58bad5baa9ecfa80b7d0817e6294ba72c82`  
		Last Modified: Wed, 22 Jan 2020 04:20:44 GMT  
		Size: 18.0 MB (17991139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cc196abfad67ae916449e24572d62e834760748f3ff5868a59576f3107630`  
		Last Modified: Wed, 22 Jan 2020 04:20:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:cantal-windowsservercore-1809`

```console
$ docker pull traefik@sha256:48745f9ef6d2873119824b3712650a8ec5ee469c2f120709d321e8aa35344e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:cantal-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:e42596a4ab6f5587d0971dc7d8b42791e7cfab035c86f02c9025f45e55eed2a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2241520898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4650d2b8183b0c02b800306ee9fd10777064324a6f2d966d034807652cbdb88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2020 01:21:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Jan 2020 01:21:20 GMT
EXPOSE 80
# Wed, 22 Jan 2020 01:21:22 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Jan 2020 01:21:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac359444ef8b5992a9677d0d9da78088aa1d7bd38988866498033461b5a17f`  
		Last Modified: Wed, 22 Jan 2020 01:22:01 GMT  
		Size: 24.1 MB (24104914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c48b965beae347426e3d11b093239de75b99ff759d731158139bf41d0f3965`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3fa86579b5d352b4071de541439e828bbdf0f9c1d98d562c7d0b0311aac0e`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da57b9c526d121005dfea489e834a4b9f892c96131110374d5687c4e1d423a82`  
		Last Modified: Wed, 22 Jan 2020 01:21:55 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:e5edf9fea8fcedb039480dcf398aa3279e1506cdff2674c04794cc930f7c4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:16ce63dfe54e6b11c8e1f11e34404607478a1ea0257fbad477832426b191782f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e4cf9e09992de0536741f1ce252f046131a881e69709d9d1d9b653219efdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 05:01:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 05:01:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 05:01:15 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:01:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 05:01:16 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 05:01:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c88a164b3fefd40411797d4c4af9365de098fdd9a632f0a0adc0875f99ab5d`  
		Last Modified: Wed, 22 Jan 2020 05:01:40 GMT  
		Size: 19.5 MB (19538838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65ff63a2d1b8e50ddfb769d6828e1f7f03ae2ec79ad14e8f2da7ffa368511c`  
		Last Modified: Wed, 22 Jan 2020 05:01:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fc0985ab6efd46cffd9157532f2682cf326efdfd0bb454ca7044d73bf96b89f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21573268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893008b3c69b472633c9dc409d78d8c7ebf291799526afdead1369ece43286f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:23 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:24 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efe145ce19ec8ece55144f045adee219ed148ce03443fab05db544a8685e7b`  
		Last Modified: Thu, 23 Jan 2020 20:53:35 GMT  
		Size: 18.3 MB (18303650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f838c6d816804ddca1127e8ec26baeba2222f8de0142edefd6a9a7b3335a7f7`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4559e357810e5e0a4f2524f54c77cc95de87030cb6fd9a7b5949aa527e9db8d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21407174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c147845c6981e275fbbd4e842f8544d4cd36bf6f7f175234b20b4d1bc8b2876`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 04:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 04:20:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 04:20:12 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 04:20:13 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 04:20:14 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e81461f690e8dbc553d4de8266f58bad5baa9ecfa80b7d0817e6294ba72c82`  
		Last Modified: Wed, 22 Jan 2020 04:20:44 GMT  
		Size: 18.0 MB (17991139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cc196abfad67ae916449e24572d62e834760748f3ff5868a59576f3107630`  
		Last Modified: Wed, 22 Jan 2020 04:20:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:5ec34caf19d114f8f0ed76f9bc3dad6ba8cf6d13a1575c4294b59b77709def39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:3b1c4d57c57d125a5d949d463d41882fefc957ce117db226aace4e7314e82d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24005352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c63a7d3e502fcbbd8937a2523368c22d0edd1788b8389af095f64038318834`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 01:00:22 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 22:26:52 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:31:38 GMT
COPY file:be1ea92a6d3f63051c9ae787ca41c986b81a56ce7f8b8347b97c3ddc3b4471f5 in / 
# Tue, 10 Dec 2019 22:31:38 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:38 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:31:38 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:31:39 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:42e7d26ec3785f8ce0f20e327cf72404ee054ba022ce9068ad2d28c52e82db2a`  
		Last Modified: Tue, 27 Aug 2019 01:00:52 GMT  
		Size: 132.0 KB (132022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a753f02eeffef33e5e071a6feac9e12fffb36330fc7ef5441f378d0ce67c528`  
		Last Modified: Mon, 21 Oct 2019 22:27:25 GMT  
		Size: 327.3 KB (327346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab927d94d255c72862c3e7ada3f6cdb36f90926b7a8913a080062b17d73f186b`  
		Last Modified: Tue, 10 Dec 2019 22:32:27 GMT  
		Size: 23.5 MB (23545984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3a32e589b7d538f688f0a4d5777ab21dc2e946e22a1b08872aaad72b4192976e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22491539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099411d81ac7bf28b232625f19ecc6590f39c3920418958b3056caa4f85815c4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 26 Aug 2019 23:54:26 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 20:27:55 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 21:57:12 GMT
COPY file:ad6d99c4dea9edfff1bf18494e1c85b8a82b1a74f77a8bf3f437bd05222fbf79 in / 
# Tue, 10 Dec 2019 21:57:14 GMT
EXPOSE 80
# Tue, 10 Dec 2019 21:57:15 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 21:57:16 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 21:57:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:506698346e0f5f486b919abaa7bc72252b3dc553cb28e0d1a5e2b6f3708cf4c0`  
		Last Modified: Mon, 26 Aug 2019 23:55:08 GMT  
		Size: 132.0 KB (132026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037320e6487ea40f4dfb2c29d120090739bc20051bca67eb5e64a072973136`  
		Last Modified: Mon, 21 Oct 2019 20:28:50 GMT  
		Size: 327.4 KB (327388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0d7ab9d9ce392bdaa622a30db2df3963e7ac8b19c846fddc788b2f7fd3f890`  
		Last Modified: Tue, 10 Dec 2019 21:58:07 GMT  
		Size: 22.0 MB (22032125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3a587a9647aca9d58c237389157512cf349f00e99afc0f33959501bc5366b489
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22219190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843151930dcd29bc722fa2e9949bcecfcb0020d961037b85983f47017aa38a58`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 00:16:41 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 23:22:44 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:39:48 GMT
COPY file:2548a09c5388b09356e8109d52a2261b02b840df1156718406457af4ef9eedcd in / 
# Tue, 10 Dec 2019 22:39:50 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:50 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:39:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:39:51 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f07a1cd6fb05ab2fb5b66f5326144f82e52f5580df40a42e400637f8a8f9c6d8`  
		Last Modified: Tue, 27 Aug 2019 00:17:31 GMT  
		Size: 132.0 KB (132021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2afd881e5b94f57a79b2f6bcd9d637c2f7a6aa910f4013045b8653ebe29fdb`  
		Last Modified: Mon, 21 Oct 2019 23:23:36 GMT  
		Size: 327.4 KB (327378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b05c8936168a3f333423ce8dca6ed7e5ad1890ce50b95da487f61aa83440e26`  
		Last Modified: Tue, 10 Dec 2019 22:40:39 GMT  
		Size: 21.8 MB (21759791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:5c83e759dd0242f06079871204c4a70c0a38e9cb926374a7589608376430f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:f9f7bc3071415790c015ad52995e2997d9d1cfd5cffdde58cb403e15d71fbe4e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27028274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e73a064c8f244ce1fe21cb3abcc9b314309275e3b26fd6ac0276946f669c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:31:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:31:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:31:02 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:31:02 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:31:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d6da64444dd0f60f3c566038d6c9157c290fb6152ec296204e862073f365f`  
		Last Modified: Tue, 10 Dec 2019 22:32:13 GMT  
		Size: 23.5 MB (23546279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7a10facf04db24667668cb9792494b0e49f33e439cccf618f435ef237bfa3`  
		Last Modified: Tue, 10 Dec 2019 22:32:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:59849962d6b994b67dc7fbc511912c5a1b87944e9b1fda436acb6502c53506a8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25301946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307869ccfa13af9d37cbe35f32b4bfa91f47eb7cb00bad6cfdfbac45293e452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:39 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:42 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d03b0a042ba73cfa9ff088a916bb4dd22cec09c6862278e94c8f4445863f12`  
		Last Modified: Thu, 23 Jan 2020 20:54:01 GMT  
		Size: 22.0 MB (22032328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7026f34a4d522e997bb9203822966f0365b1d11745be187098906406a66e3`  
		Last Modified: Thu, 23 Jan 2020 20:53:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69880c97f253a7dab9e3fb1e477bc209a297ceb369f259841a14ec194ac5fbe3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25175702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630da378646ff9d16799a8f19fc83d02d28fe478003b44b8f37a8b0a4b715079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:39:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:39:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:39:27 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:39:28 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:39:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ad2d17ee7cb6da8499ef5415cad503d05873da472bcfc6d2ac07e9bdbad2c`  
		Last Modified: Tue, 10 Dec 2019 22:40:19 GMT  
		Size: 21.8 MB (21759668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ac7ce9940a937d298cf00954af64fd399df1a840cad75914caeb0b5cf224`  
		Last Modified: Tue, 10 Dec 2019 22:40:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5545c7138c85b3bc5ad0b8775ee168ae16c839bddbe83b4af20a1660a4dde29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:6cfb866dc049dc285053e1f6a51226552c66627ae5af596fef51d5816d0095a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245517816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8717289fcbe162ad339e623185f4cb3fde105c3346a906b3d9e45e58d582b94c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 22:25:10 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jan 2020 22:25:14 GMT
EXPOSE 80
# Wed, 15 Jan 2020 22:25:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jan 2020 22:25:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa553b540bc891379b327f7ebaf07fc18540471d50ab5ee933ac25c388bbd599`  
		Last Modified: Wed, 15 Jan 2020 22:27:30 GMT  
		Size: 28.1 MB (28101873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a7f9ea7b7d37ae92c7d35e40837cf30a6fb9e06234933ef771963f08e1b5d`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96835f334cd72d34b10c788e7adf2692a9038c2e79e936ff84d1136d3e2ed8e5`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c384663a41950e20d89986102e168d0afd30f4b754869dbcf6a7e1a4d99a9d73`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:5ec34caf19d114f8f0ed76f9bc3dad6ba8cf6d13a1575c4294b59b77709def39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:3b1c4d57c57d125a5d949d463d41882fefc957ce117db226aace4e7314e82d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24005352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c63a7d3e502fcbbd8937a2523368c22d0edd1788b8389af095f64038318834`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 01:00:22 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 22:26:52 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:31:38 GMT
COPY file:be1ea92a6d3f63051c9ae787ca41c986b81a56ce7f8b8347b97c3ddc3b4471f5 in / 
# Tue, 10 Dec 2019 22:31:38 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:38 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:31:38 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:31:39 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:42e7d26ec3785f8ce0f20e327cf72404ee054ba022ce9068ad2d28c52e82db2a`  
		Last Modified: Tue, 27 Aug 2019 01:00:52 GMT  
		Size: 132.0 KB (132022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a753f02eeffef33e5e071a6feac9e12fffb36330fc7ef5441f378d0ce67c528`  
		Last Modified: Mon, 21 Oct 2019 22:27:25 GMT  
		Size: 327.3 KB (327346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab927d94d255c72862c3e7ada3f6cdb36f90926b7a8913a080062b17d73f186b`  
		Last Modified: Tue, 10 Dec 2019 22:32:27 GMT  
		Size: 23.5 MB (23545984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3a32e589b7d538f688f0a4d5777ab21dc2e946e22a1b08872aaad72b4192976e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22491539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099411d81ac7bf28b232625f19ecc6590f39c3920418958b3056caa4f85815c4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 26 Aug 2019 23:54:26 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 20:27:55 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 21:57:12 GMT
COPY file:ad6d99c4dea9edfff1bf18494e1c85b8a82b1a74f77a8bf3f437bd05222fbf79 in / 
# Tue, 10 Dec 2019 21:57:14 GMT
EXPOSE 80
# Tue, 10 Dec 2019 21:57:15 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 21:57:16 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 21:57:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:506698346e0f5f486b919abaa7bc72252b3dc553cb28e0d1a5e2b6f3708cf4c0`  
		Last Modified: Mon, 26 Aug 2019 23:55:08 GMT  
		Size: 132.0 KB (132026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037320e6487ea40f4dfb2c29d120090739bc20051bca67eb5e64a072973136`  
		Last Modified: Mon, 21 Oct 2019 20:28:50 GMT  
		Size: 327.4 KB (327388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0d7ab9d9ce392bdaa622a30db2df3963e7ac8b19c846fddc788b2f7fd3f890`  
		Last Modified: Tue, 10 Dec 2019 21:58:07 GMT  
		Size: 22.0 MB (22032125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3a587a9647aca9d58c237389157512cf349f00e99afc0f33959501bc5366b489
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22219190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843151930dcd29bc722fa2e9949bcecfcb0020d961037b85983f47017aa38a58`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 00:16:41 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 23:22:44 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:39:48 GMT
COPY file:2548a09c5388b09356e8109d52a2261b02b840df1156718406457af4ef9eedcd in / 
# Tue, 10 Dec 2019 22:39:50 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:50 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:39:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:39:51 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f07a1cd6fb05ab2fb5b66f5326144f82e52f5580df40a42e400637f8a8f9c6d8`  
		Last Modified: Tue, 27 Aug 2019 00:17:31 GMT  
		Size: 132.0 KB (132021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2afd881e5b94f57a79b2f6bcd9d637c2f7a6aa910f4013045b8653ebe29fdb`  
		Last Modified: Mon, 21 Oct 2019 23:23:36 GMT  
		Size: 327.4 KB (327378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b05c8936168a3f333423ce8dca6ed7e5ad1890ce50b95da487f61aa83440e26`  
		Last Modified: Tue, 10 Dec 2019 22:40:39 GMT  
		Size: 21.8 MB (21759791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.20`

```console
$ docker pull traefik@sha256:5ec34caf19d114f8f0ed76f9bc3dad6ba8cf6d13a1575c4294b59b77709def39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.20` - linux; amd64

```console
$ docker pull traefik@sha256:3b1c4d57c57d125a5d949d463d41882fefc957ce117db226aace4e7314e82d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24005352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c63a7d3e502fcbbd8937a2523368c22d0edd1788b8389af095f64038318834`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 01:00:22 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 22:26:52 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:31:38 GMT
COPY file:be1ea92a6d3f63051c9ae787ca41c986b81a56ce7f8b8347b97c3ddc3b4471f5 in / 
# Tue, 10 Dec 2019 22:31:38 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:38 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:31:38 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:31:39 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:42e7d26ec3785f8ce0f20e327cf72404ee054ba022ce9068ad2d28c52e82db2a`  
		Last Modified: Tue, 27 Aug 2019 01:00:52 GMT  
		Size: 132.0 KB (132022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a753f02eeffef33e5e071a6feac9e12fffb36330fc7ef5441f378d0ce67c528`  
		Last Modified: Mon, 21 Oct 2019 22:27:25 GMT  
		Size: 327.3 KB (327346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab927d94d255c72862c3e7ada3f6cdb36f90926b7a8913a080062b17d73f186b`  
		Last Modified: Tue, 10 Dec 2019 22:32:27 GMT  
		Size: 23.5 MB (23545984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.20` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3a32e589b7d538f688f0a4d5777ab21dc2e946e22a1b08872aaad72b4192976e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22491539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099411d81ac7bf28b232625f19ecc6590f39c3920418958b3056caa4f85815c4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 26 Aug 2019 23:54:26 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 20:27:55 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 21:57:12 GMT
COPY file:ad6d99c4dea9edfff1bf18494e1c85b8a82b1a74f77a8bf3f437bd05222fbf79 in / 
# Tue, 10 Dec 2019 21:57:14 GMT
EXPOSE 80
# Tue, 10 Dec 2019 21:57:15 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 21:57:16 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 21:57:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:506698346e0f5f486b919abaa7bc72252b3dc553cb28e0d1a5e2b6f3708cf4c0`  
		Last Modified: Mon, 26 Aug 2019 23:55:08 GMT  
		Size: 132.0 KB (132026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037320e6487ea40f4dfb2c29d120090739bc20051bca67eb5e64a072973136`  
		Last Modified: Mon, 21 Oct 2019 20:28:50 GMT  
		Size: 327.4 KB (327388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0d7ab9d9ce392bdaa622a30db2df3963e7ac8b19c846fddc788b2f7fd3f890`  
		Last Modified: Tue, 10 Dec 2019 21:58:07 GMT  
		Size: 22.0 MB (22032125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.20` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3a587a9647aca9d58c237389157512cf349f00e99afc0f33959501bc5366b489
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22219190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843151930dcd29bc722fa2e9949bcecfcb0020d961037b85983f47017aa38a58`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 27 Aug 2019 00:16:41 GMT
COPY file:091d2a65366d205fc0db557b2f495da40adb5a33c9d656d02c3ea08bb22f6c4d in /etc/ssl/certs/ 
# Mon, 21 Oct 2019 23:22:44 GMT
COPY dir:e700a731062c6a1130194c74080171046494718874f8e586f78523a64d56715c in /usr/share/ 
# Tue, 10 Dec 2019 22:39:48 GMT
COPY file:2548a09c5388b09356e8109d52a2261b02b840df1156718406457af4ef9eedcd in / 
# Tue, 10 Dec 2019 22:39:50 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:50 GMT
VOLUME [/tmp]
# Tue, 10 Dec 2019 22:39:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Dec 2019 22:39:51 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f07a1cd6fb05ab2fb5b66f5326144f82e52f5580df40a42e400637f8a8f9c6d8`  
		Last Modified: Tue, 27 Aug 2019 00:17:31 GMT  
		Size: 132.0 KB (132021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2afd881e5b94f57a79b2f6bcd9d637c2f7a6aa910f4013045b8653ebe29fdb`  
		Last Modified: Mon, 21 Oct 2019 23:23:36 GMT  
		Size: 327.4 KB (327378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b05c8936168a3f333423ce8dca6ed7e5ad1890ce50b95da487f61aa83440e26`  
		Last Modified: Tue, 10 Dec 2019 22:40:39 GMT  
		Size: 21.8 MB (21759791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.20-alpine`

```console
$ docker pull traefik@sha256:5c83e759dd0242f06079871204c4a70c0a38e9cb926374a7589608376430f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.20-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:f9f7bc3071415790c015ad52995e2997d9d1cfd5cffdde58cb403e15d71fbe4e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27028274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e73a064c8f244ce1fe21cb3abcc9b314309275e3b26fd6ac0276946f669c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:31:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:31:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:31:02 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:31:02 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:31:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d6da64444dd0f60f3c566038d6c9157c290fb6152ec296204e862073f365f`  
		Last Modified: Tue, 10 Dec 2019 22:32:13 GMT  
		Size: 23.5 MB (23546279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7a10facf04db24667668cb9792494b0e49f33e439cccf618f435ef237bfa3`  
		Last Modified: Tue, 10 Dec 2019 22:32:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.20-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:59849962d6b994b67dc7fbc511912c5a1b87944e9b1fda436acb6502c53506a8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25301946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307869ccfa13af9d37cbe35f32b4bfa91f47eb7cb00bad6cfdfbac45293e452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:39 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:42 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d03b0a042ba73cfa9ff088a916bb4dd22cec09c6862278e94c8f4445863f12`  
		Last Modified: Thu, 23 Jan 2020 20:54:01 GMT  
		Size: 22.0 MB (22032328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7026f34a4d522e997bb9203822966f0365b1d11745be187098906406a66e3`  
		Last Modified: Thu, 23 Jan 2020 20:53:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.20-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69880c97f253a7dab9e3fb1e477bc209a297ceb369f259841a14ec194ac5fbe3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25175702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630da378646ff9d16799a8f19fc83d02d28fe478003b44b8f37a8b0a4b715079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:39:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:39:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:39:27 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:39:28 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:39:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ad2d17ee7cb6da8499ef5415cad503d05873da472bcfc6d2ac07e9bdbad2c`  
		Last Modified: Tue, 10 Dec 2019 22:40:19 GMT  
		Size: 21.8 MB (21759668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ac7ce9940a937d298cf00954af64fd399df1a840cad75914caeb0b5cf224`  
		Last Modified: Tue, 10 Dec 2019 22:40:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.20-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5545c7138c85b3bc5ad0b8775ee168ae16c839bddbe83b4af20a1660a4dde29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:v1.7.20-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:6cfb866dc049dc285053e1f6a51226552c66627ae5af596fef51d5816d0095a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245517816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8717289fcbe162ad339e623185f4cb3fde105c3346a906b3d9e45e58d582b94c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 22:25:10 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jan 2020 22:25:14 GMT
EXPOSE 80
# Wed, 15 Jan 2020 22:25:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jan 2020 22:25:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa553b540bc891379b327f7ebaf07fc18540471d50ab5ee933ac25c388bbd599`  
		Last Modified: Wed, 15 Jan 2020 22:27:30 GMT  
		Size: 28.1 MB (28101873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a7f9ea7b7d37ae92c7d35e40837cf30a6fb9e06234933ef771963f08e1b5d`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96835f334cd72d34b10c788e7adf2692a9038c2e79e936ff84d1136d3e2ed8e5`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c384663a41950e20d89986102e168d0afd30f4b754869dbcf6a7e1a4d99a9d73`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:5c83e759dd0242f06079871204c4a70c0a38e9cb926374a7589608376430f8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:f9f7bc3071415790c015ad52995e2997d9d1cfd5cffdde58cb403e15d71fbe4e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27028274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439e73a064c8f244ce1fe21cb3abcc9b314309275e3b26fd6ac0276946f669c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:31:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:31:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:31:02 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:31:02 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:31:03 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198d6da64444dd0f60f3c566038d6c9157c290fb6152ec296204e862073f365f`  
		Last Modified: Tue, 10 Dec 2019 22:32:13 GMT  
		Size: 23.5 MB (23546279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7a10facf04db24667668cb9792494b0e49f33e439cccf618f435ef237bfa3`  
		Last Modified: Tue, 10 Dec 2019 22:32:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:59849962d6b994b67dc7fbc511912c5a1b87944e9b1fda436acb6502c53506a8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25301946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5307869ccfa13af9d37cbe35f32b4bfa91f47eb7cb00bad6cfdfbac45293e452`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:39 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:42 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:43 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d03b0a042ba73cfa9ff088a916bb4dd22cec09c6862278e94c8f4445863f12`  
		Last Modified: Thu, 23 Jan 2020 20:54:01 GMT  
		Size: 22.0 MB (22032328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c7026f34a4d522e997bb9203822966f0365b1d11745be187098906406a66e3`  
		Last Modified: Thu, 23 Jan 2020 20:53:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:69880c97f253a7dab9e3fb1e477bc209a297ceb369f259841a14ec194ac5fbe3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25175702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630da378646ff9d16799a8f19fc83d02d28fe478003b44b8f37a8b0a4b715079`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 10 Dec 2019 22:39:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 10 Dec 2019 22:39:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 10 Dec 2019 22:39:27 GMT
EXPOSE 80
# Tue, 10 Dec 2019 22:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Dec 2019 22:39:28 GMT
CMD ["traefik"]
# Tue, 10 Dec 2019 22:39:29 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ad2d17ee7cb6da8499ef5415cad503d05873da472bcfc6d2ac07e9bdbad2c`  
		Last Modified: Tue, 10 Dec 2019 22:40:19 GMT  
		Size: 21.8 MB (21759668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ac7ce9940a937d298cf00954af64fd399df1a840cad75914caeb0b5cf224`  
		Last Modified: Tue, 10 Dec 2019 22:40:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5545c7138c85b3bc5ad0b8775ee168ae16c839bddbe83b4af20a1660a4dde29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:6cfb866dc049dc285053e1f6a51226552c66627ae5af596fef51d5816d0095a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2245517816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8717289fcbe162ad339e623185f4cb3fde105c3346a906b3d9e45e58d582b94c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 22:25:10 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/containous/traefik/releases/download/v1.7.20/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jan 2020 22:25:14 GMT
EXPOSE 80
# Wed, 15 Jan 2020 22:25:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jan 2020 22:25:17 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa553b540bc891379b327f7ebaf07fc18540471d50ab5ee933ac25c388bbd599`  
		Last Modified: Wed, 15 Jan 2020 22:27:30 GMT  
		Size: 28.1 MB (28101873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a7f9ea7b7d37ae92c7d35e40837cf30a6fb9e06234933ef771963f08e1b5d`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96835f334cd72d34b10c788e7adf2692a9038c2e79e936ff84d1136d3e2ed8e5`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c384663a41950e20d89986102e168d0afd30f4b754869dbcf6a7e1a4d99a9d73`  
		Last Modified: Wed, 15 Jan 2020 22:27:23 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1`

```console
$ docker pull traefik@sha256:e5edf9fea8fcedb039480dcf398aa3279e1506cdff2674c04794cc930f7c4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.1` - linux; amd64

```console
$ docker pull traefik@sha256:16ce63dfe54e6b11c8e1f11e34404607478a1ea0257fbad477832426b191782f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e4cf9e09992de0536741f1ce252f046131a881e69709d9d1d9b653219efdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 05:01:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 05:01:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 05:01:15 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:01:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 05:01:16 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 05:01:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c88a164b3fefd40411797d4c4af9365de098fdd9a632f0a0adc0875f99ab5d`  
		Last Modified: Wed, 22 Jan 2020 05:01:40 GMT  
		Size: 19.5 MB (19538838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65ff63a2d1b8e50ddfb769d6828e1f7f03ae2ec79ad14e8f2da7ffa368511c`  
		Last Modified: Wed, 22 Jan 2020 05:01:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fc0985ab6efd46cffd9157532f2682cf326efdfd0bb454ca7044d73bf96b89f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21573268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893008b3c69b472633c9dc409d78d8c7ebf291799526afdead1369ece43286f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:23 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:24 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efe145ce19ec8ece55144f045adee219ed148ce03443fab05db544a8685e7b`  
		Last Modified: Thu, 23 Jan 2020 20:53:35 GMT  
		Size: 18.3 MB (18303650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f838c6d816804ddca1127e8ec26baeba2222f8de0142edefd6a9a7b3335a7f7`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4559e357810e5e0a4f2524f54c77cc95de87030cb6fd9a7b5949aa527e9db8d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21407174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c147845c6981e275fbbd4e842f8544d4cd36bf6f7f175234b20b4d1bc8b2876`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 04:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 04:20:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 04:20:12 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 04:20:13 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 04:20:14 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e81461f690e8dbc553d4de8266f58bad5baa9ecfa80b7d0817e6294ba72c82`  
		Last Modified: Wed, 22 Jan 2020 04:20:44 GMT  
		Size: 18.0 MB (17991139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cc196abfad67ae916449e24572d62e834760748f3ff5868a59576f3107630`  
		Last Modified: Wed, 22 Jan 2020 04:20:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1.3`

```console
$ docker pull traefik@sha256:e5edf9fea8fcedb039480dcf398aa3279e1506cdff2674c04794cc930f7c4b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.1.3` - linux; amd64

```console
$ docker pull traefik@sha256:16ce63dfe54e6b11c8e1f11e34404607478a1ea0257fbad477832426b191782f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23020833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e4cf9e09992de0536741f1ce252f046131a881e69709d9d1d9b653219efdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 22:26:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 05:01:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 05:01:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 05:01:15 GMT
EXPOSE 80
# Wed, 22 Jan 2020 05:01:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 05:01:16 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 05:01:16 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275722d2e7f6dc3397547bc96af555d5905a44fc2f88a1adb39ddfc6aa2a98b9`  
		Last Modified: Mon, 21 Oct 2019 22:27:05 GMT  
		Size: 694.5 KB (694493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c88a164b3fefd40411797d4c4af9365de098fdd9a632f0a0adc0875f99ab5d`  
		Last Modified: Wed, 22 Jan 2020 05:01:40 GMT  
		Size: 19.5 MB (19538838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65ff63a2d1b8e50ddfb769d6828e1f7f03ae2ec79ad14e8f2da7ffa368511c`  
		Last Modified: Wed, 22 Jan 2020 05:01:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fc0985ab6efd46cffd9157532f2682cf326efdfd0bb454ca7044d73bf96b89f3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21573268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893008b3c69b472633c9dc409d78d8c7ebf291799526afdead1369ece43286f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:52:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 23 Jan 2020 20:52:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 23 Jan 2020 20:52:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 23 Jan 2020 20:52:23 GMT
EXPOSE 80
# Thu, 23 Jan 2020 20:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:52:24 GMT
CMD ["traefik"]
# Thu, 23 Jan 2020 20:52:24 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cce0b3f7bff62be2da6a6ad84b3c9f19602e97675f95f1f29a72440b8e0de2`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 697.8 KB (697843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57efe145ce19ec8ece55144f045adee219ed148ce03443fab05db544a8685e7b`  
		Last Modified: Thu, 23 Jan 2020 20:53:35 GMT  
		Size: 18.3 MB (18303650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f838c6d816804ddca1127e8ec26baeba2222f8de0142edefd6a9a7b3335a7f7`  
		Last Modified: Thu, 23 Jan 2020 20:53:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.1.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4559e357810e5e0a4f2524f54c77cc95de87030cb6fd9a7b5949aa527e9db8d9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21407174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c147845c6981e275fbbd4e842f8544d4cd36bf6f7f175234b20b4d1bc8b2876`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Mon, 21 Oct 2019 23:22:16 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Jan 2020 04:20:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Jan 2020 04:20:11 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Jan 2020 04:20:12 GMT
EXPOSE 80
# Wed, 22 Jan 2020 04:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jan 2020 04:20:13 GMT
CMD ["traefik"]
# Wed, 22 Jan 2020 04:20:14 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21b1a0e782f54ba929f36f1f589cbf9cacb6e15d6644d901741533bec314cec`  
		Last Modified: Mon, 21 Oct 2019 23:23:04 GMT  
		Size: 697.9 KB (697888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e81461f690e8dbc553d4de8266f58bad5baa9ecfa80b7d0817e6294ba72c82`  
		Last Modified: Wed, 22 Jan 2020 04:20:44 GMT  
		Size: 18.0 MB (17991139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81cc196abfad67ae916449e24572d62e834760748f3ff5868a59576f3107630`  
		Last Modified: Wed, 22 Jan 2020 04:20:38 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:48745f9ef6d2873119824b3712650a8ec5ee469c2f120709d321e8aa35344e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:v2.1.3-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:e42596a4ab6f5587d0971dc7d8b42791e7cfab035c86f02c9025f45e55eed2a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2241520898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4650d2b8183b0c02b800306ee9fd10777064324a6f2d966d034807652cbdb88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2020 01:21:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Jan 2020 01:21:20 GMT
EXPOSE 80
# Wed, 22 Jan 2020 01:21:22 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Jan 2020 01:21:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac359444ef8b5992a9677d0d9da78088aa1d7bd38988866498033461b5a17f`  
		Last Modified: Wed, 22 Jan 2020 01:22:01 GMT  
		Size: 24.1 MB (24104914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c48b965beae347426e3d11b093239de75b99ff759d731158139bf41d0f3965`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3fa86579b5d352b4071de541439e828bbdf0f9c1d98d562c7d0b0311aac0e`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da57b9c526d121005dfea489e834a4b9f892c96131110374d5687c4e1d423a82`  
		Last Modified: Wed, 22 Jan 2020 01:21:55 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:48745f9ef6d2873119824b3712650a8ec5ee469c2f120709d321e8aa35344e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:v2.1-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:e42596a4ab6f5587d0971dc7d8b42791e7cfab035c86f02c9025f45e55eed2a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2241520898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4650d2b8183b0c02b800306ee9fd10777064324a6f2d966d034807652cbdb88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2020 01:21:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Jan 2020 01:21:20 GMT
EXPOSE 80
# Wed, 22 Jan 2020 01:21:22 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Jan 2020 01:21:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac359444ef8b5992a9677d0d9da78088aa1d7bd38988866498033461b5a17f`  
		Last Modified: Wed, 22 Jan 2020 01:22:01 GMT  
		Size: 24.1 MB (24104914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c48b965beae347426e3d11b093239de75b99ff759d731158139bf41d0f3965`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3fa86579b5d352b4071de541439e828bbdf0f9c1d98d562c7d0b0311aac0e`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da57b9c526d121005dfea489e834a4b9f892c96131110374d5687c4e1d423a82`  
		Last Modified: Wed, 22 Jan 2020 01:21:55 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:48745f9ef6d2873119824b3712650a8ec5ee469c2f120709d321e8aa35344e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull traefik@sha256:e42596a4ab6f5587d0971dc7d8b42791e7cfab035c86f02c9025f45e55eed2a4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2241520898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4650d2b8183b0c02b800306ee9fd10777064324a6f2d966d034807652cbdb88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2020 01:21:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/containous/traefik/releases/download/v2.1.3/traefik_v2.1.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 22 Jan 2020 01:21:20 GMT
EXPOSE 80
# Wed, 22 Jan 2020 01:21:22 GMT
ENTRYPOINT ["/traefik"]
# Wed, 22 Jan 2020 01:21:23 GMT
LABEL org.opencontainers.image.vendor=Containous org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac359444ef8b5992a9677d0d9da78088aa1d7bd38988866498033461b5a17f`  
		Last Modified: Wed, 22 Jan 2020 01:22:01 GMT  
		Size: 24.1 MB (24104914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c48b965beae347426e3d11b093239de75b99ff759d731158139bf41d0f3965`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a3fa86579b5d352b4071de541439e828bbdf0f9c1d98d562c7d0b0311aac0e`  
		Last Modified: Wed, 22 Jan 2020 01:21:56 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da57b9c526d121005dfea489e834a4b9f892c96131110374d5687c4e1d423a82`  
		Last Modified: Wed, 22 Jan 2020 01:21:55 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
