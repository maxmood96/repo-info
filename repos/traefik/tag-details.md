<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.34`](#traefik1734)
-	[`traefik:1.7.34-alpine`](#traefik1734-alpine)
-	[`traefik:1.7.34-windowsservercore-1809`](#traefik1734-windowsservercore-1809)
-	[`traefik:2.8`](#traefik28)
-	[`traefik:2.8-windowsservercore-1809`](#traefik28-windowsservercore-1809)
-	[`traefik:2.8.1`](#traefik281)
-	[`traefik:2.8.1-windowsservercore-1809`](#traefik281-windowsservercore-1809)
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
-	[`traefik:v2.8`](#traefikv28)
-	[`traefik:v2.8-windowsservercore-1809`](#traefikv28-windowsservercore-1809)
-	[`traefik:v2.8.1`](#traefikv281)
-	[`traefik:v2.8.1-windowsservercore-1809`](#traefikv281-windowsservercore-1809)
-	[`traefik:vacherin`](#traefikvacherin)
-	[`traefik:vacherin-windowsservercore-1809`](#traefikvacherin-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:1d8a41ae1bd54c9e9a5e0cc8da9002638932c53cc3d50c6f0c172238374ebe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:f705216279431ed8ab470318736acd767794a847acda2db325e3e159574bd03c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22607863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43de28b34d397393ca2d0ec8bd6923735fab787f8c3bd3dab0719cd256fcc010`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 18 Mar 2022 06:23:36 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Fri, 18 Mar 2022 06:23:37 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Fri, 18 Mar 2022 06:23:38 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 18 Mar 2022 06:23:39 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:39 GMT
VOLUME [/tmp]
# Fri, 18 Mar 2022 06:23:39 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Mar 2022 06:23:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:903e84870d1b7b581b2c6c362c74751a258cb8e2dbb443bddcd36fe8f29a20ab`  
		Last Modified: Fri, 18 Mar 2022 06:24:59 GMT  
		Size: 117.4 KB (117389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ae7a2b8652023026596365a1dfe88e317d16b1cc8099ee03c20357c95716e`  
		Last Modified: Fri, 18 Mar 2022 06:25:00 GMT  
		Size: 328.5 KB (328522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f483c7bcad16f6ac0813c7a4704d4dc9319bfd6533f10c888b5e2ca21c72dc44`  
		Last Modified: Fri, 18 Mar 2022 06:25:05 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fe6bde6e9349ec036bc3aaec90c095006425bface50ee2f449e0d196cb5850c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21069186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c3451377ef5e2379e4bc19691fb6c14b1a2215326833336e1db9e16cc5ca3`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 22:45:25 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 22:45:27 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 22:45:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Thu, 17 Mar 2022 22:45:33 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:33 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 22:45:34 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 22:45:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:27b61c1d4effca5c7137bfe0c8b6a3a228418ef37998781ad6cc7372c6f7e98f`  
		Last Modified: Thu, 17 Mar 2022 22:48:17 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aae3b48a316f885b1d485fee6b2ffffb3c2c7dea49cea01019d4c103b204da`  
		Last Modified: Thu, 17 Mar 2022 22:48:18 GMT  
		Size: 328.5 KB (328514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82873a2be1cc2b2dfbc565c4bf9960f32b61892f49f0911ec1ac7e310210c3d`  
		Last Modified: Thu, 17 Mar 2022 22:48:34 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c2930d3e36f7feb98470b85e8bc9fce0016fc5eadbc805249e63d6a458eb2323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20577242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7338e148255e82dd93286a1f87db35f499d4e391d7f5f3e1bfb6c71ed4ec2d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 21:07:07 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 21:07:08 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 21:07:09 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 17 Mar 2022 21:07:09 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:07:10 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 21:07:11 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 21:07:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:86cd07830d2730c0aa24f0e47380af5ef760945b5049a2e72a8ebe0675ed6d34`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135b9e65a5ea0b642df02ea2cf73c74a353d1cbfa3b95d048a4adbf0bacf9653`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 328.5 KB (328505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8fa09b05c38fc9116b1446ac3d204200577fd9bfb1801d684657dc722b74b`  
		Last Modified: Thu, 17 Mar 2022 21:08:45 GMT  
		Size: 20.1 MB (20131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:eb08a301bd06b8e71a7dfb44c829e593e6aaa24b0ea6a90cfb09488587911fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:437693178563fbe5e9d51a163f9c5507cfcaf5a52569b7e5814f6ccd71e53ee4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e98bf8d6e3fea93acd477a953dd3276b9ac3a285a9b7cdf1613f806e73a61f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:53:36 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 10:53:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 10:53:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 10:53:56 GMT
EXPOSE 80
# Tue, 05 Apr 2022 10:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:53:56 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 10:53:56 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b5dadc224e5464ecd6b4217323f15e90e06847ef61af9132dc606b1a9863a`  
		Last Modified: Tue, 05 Apr 2022 10:54:28 GMT  
		Size: 666.7 KB (666681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84b4a436968a2d3e0c2d1d3f62ad7c56a1e0a20f0c6e00a8f76f646de636d4`  
		Last Modified: Tue, 05 Apr 2022 10:55:14 GMT  
		Size: 22.2 MB (22162072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb865e347fb64ada1ea356e11aa7f4e81221b6b589b618abf86188a9d3719a`  
		Last Modified: Tue, 05 Apr 2022 10:55:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6907e0a9c3e242920fb2102a261b41864c3d8bf697efa46b6a09596b59c5300e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23922383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db7d675647f8f59a02cd5915f6fd2afab456fbb1716db05032b9111a469f9b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:40:53 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 14:41:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 14:41:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 14:41:49 GMT
EXPOSE 80
# Tue, 05 Apr 2022 14:41:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 14:41:50 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 14:41:50 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a1618fdbb5f9b720d159d71fa3326e20a38c9bba9feb9392f897ab456d07f4`  
		Last Modified: Tue, 05 Apr 2022 14:43:49 GMT  
		Size: 672.5 KB (672528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aba3d211189b35b7f9d6160aa51d316bde615e058a83996627fcb7dfdca0d0`  
		Last Modified: Tue, 05 Apr 2022 14:45:28 GMT  
		Size: 20.6 MB (20623431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ff4f0661732ea1e9661f9d94015bc7b5fcf85d6674fb173e88c50a23840d40`  
		Last Modified: Tue, 05 Apr 2022 14:45:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7bca8f9f0aebebc3c7c5e968e03474b479420b55a77f33683c435fead3366e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23517412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd43ec235cafac033220e63f50aaf33544f0f719f1a51e4d8be83109763738d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:27:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 07:27:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 07:27:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 07:27:39 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:27:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 07:27:41 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 07:27:42 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a873ae44592179453bfc8ffe686a6faef6bae9b61f4465e8844d31d37b4a74`  
		Last Modified: Tue, 05 Apr 2022 07:28:36 GMT  
		Size: 668.3 KB (668291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f2f70dadc3bc4f06bfc6c0eff12d88e357f1a8c8ee2876e16278cb07571b3`  
		Last Modified: Tue, 05 Apr 2022 07:29:28 GMT  
		Size: 20.1 MB (20131364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24699415b41c9daba64f440481479635163834c11c1cb770c1e56ed677d840`  
		Last Modified: Tue, 05 Apr 2022 07:29:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:38d6b6a109eefba8100d1c9f39cbc3f2cbbc65414bd9d4c21a3f3d3803a20e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:fbdf20663eef4b356b91897c11768e710fe5d8c0a20db676b727ace282010c05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2686129323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bff99d35ce807fc8be468d820b698c0aa96bbc198d8fe2d862f033d3a872a7`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 22:58:35 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jun 2022 22:58:36 GMT
EXPOSE 80
# Wed, 15 Jun 2022 22:58:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jun 2022 22:58:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c081bfa67f6b18ab023e3e6f245649e859bd7f6def8eda5884371448bdfa11`  
		Last Modified: Wed, 15 Jun 2022 23:00:34 GMT  
		Size: 22.8 MB (22843843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10edb73d57df6d226de72153277ac47e944dcef4eaadebb4017ed7c9b748699`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0a0dfe9477fcfe1a48749ca97bceaf457e5fb84a996d15fd78917ee6ce177f`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12f9f231fd68bd6cc2c7fab6929a79a59f1df6127ef65cd3a70c3fdd2d84a92`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34`

```console
$ docker pull traefik@sha256:1d8a41ae1bd54c9e9a5e0cc8da9002638932c53cc3d50c6f0c172238374ebe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:f705216279431ed8ab470318736acd767794a847acda2db325e3e159574bd03c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22607863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43de28b34d397393ca2d0ec8bd6923735fab787f8c3bd3dab0719cd256fcc010`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 18 Mar 2022 06:23:36 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Fri, 18 Mar 2022 06:23:37 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Fri, 18 Mar 2022 06:23:38 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 18 Mar 2022 06:23:39 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:39 GMT
VOLUME [/tmp]
# Fri, 18 Mar 2022 06:23:39 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Mar 2022 06:23:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:903e84870d1b7b581b2c6c362c74751a258cb8e2dbb443bddcd36fe8f29a20ab`  
		Last Modified: Fri, 18 Mar 2022 06:24:59 GMT  
		Size: 117.4 KB (117389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ae7a2b8652023026596365a1dfe88e317d16b1cc8099ee03c20357c95716e`  
		Last Modified: Fri, 18 Mar 2022 06:25:00 GMT  
		Size: 328.5 KB (328522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f483c7bcad16f6ac0813c7a4704d4dc9319bfd6533f10c888b5e2ca21c72dc44`  
		Last Modified: Fri, 18 Mar 2022 06:25:05 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fe6bde6e9349ec036bc3aaec90c095006425bface50ee2f449e0d196cb5850c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21069186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c3451377ef5e2379e4bc19691fb6c14b1a2215326833336e1db9e16cc5ca3`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 22:45:25 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 22:45:27 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 22:45:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Thu, 17 Mar 2022 22:45:33 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:33 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 22:45:34 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 22:45:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:27b61c1d4effca5c7137bfe0c8b6a3a228418ef37998781ad6cc7372c6f7e98f`  
		Last Modified: Thu, 17 Mar 2022 22:48:17 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aae3b48a316f885b1d485fee6b2ffffb3c2c7dea49cea01019d4c103b204da`  
		Last Modified: Thu, 17 Mar 2022 22:48:18 GMT  
		Size: 328.5 KB (328514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82873a2be1cc2b2dfbc565c4bf9960f32b61892f49f0911ec1ac7e310210c3d`  
		Last Modified: Thu, 17 Mar 2022 22:48:34 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c2930d3e36f7feb98470b85e8bc9fce0016fc5eadbc805249e63d6a458eb2323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20577242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7338e148255e82dd93286a1f87db35f499d4e391d7f5f3e1bfb6c71ed4ec2d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 21:07:07 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 21:07:08 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 21:07:09 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 17 Mar 2022 21:07:09 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:07:10 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 21:07:11 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 21:07:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:86cd07830d2730c0aa24f0e47380af5ef760945b5049a2e72a8ebe0675ed6d34`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135b9e65a5ea0b642df02ea2cf73c74a353d1cbfa3b95d048a4adbf0bacf9653`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 328.5 KB (328505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8fa09b05c38fc9116b1446ac3d204200577fd9bfb1801d684657dc722b74b`  
		Last Modified: Thu, 17 Mar 2022 21:08:45 GMT  
		Size: 20.1 MB (20131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-alpine`

```console
$ docker pull traefik@sha256:eb08a301bd06b8e71a7dfb44c829e593e6aaa24b0ea6a90cfb09488587911fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:437693178563fbe5e9d51a163f9c5507cfcaf5a52569b7e5814f6ccd71e53ee4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e98bf8d6e3fea93acd477a953dd3276b9ac3a285a9b7cdf1613f806e73a61f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:53:36 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 10:53:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 10:53:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 10:53:56 GMT
EXPOSE 80
# Tue, 05 Apr 2022 10:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:53:56 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 10:53:56 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b5dadc224e5464ecd6b4217323f15e90e06847ef61af9132dc606b1a9863a`  
		Last Modified: Tue, 05 Apr 2022 10:54:28 GMT  
		Size: 666.7 KB (666681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84b4a436968a2d3e0c2d1d3f62ad7c56a1e0a20f0c6e00a8f76f646de636d4`  
		Last Modified: Tue, 05 Apr 2022 10:55:14 GMT  
		Size: 22.2 MB (22162072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb865e347fb64ada1ea356e11aa7f4e81221b6b589b618abf86188a9d3719a`  
		Last Modified: Tue, 05 Apr 2022 10:55:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6907e0a9c3e242920fb2102a261b41864c3d8bf697efa46b6a09596b59c5300e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23922383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db7d675647f8f59a02cd5915f6fd2afab456fbb1716db05032b9111a469f9b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:40:53 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 14:41:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 14:41:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 14:41:49 GMT
EXPOSE 80
# Tue, 05 Apr 2022 14:41:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 14:41:50 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 14:41:50 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a1618fdbb5f9b720d159d71fa3326e20a38c9bba9feb9392f897ab456d07f4`  
		Last Modified: Tue, 05 Apr 2022 14:43:49 GMT  
		Size: 672.5 KB (672528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aba3d211189b35b7f9d6160aa51d316bde615e058a83996627fcb7dfdca0d0`  
		Last Modified: Tue, 05 Apr 2022 14:45:28 GMT  
		Size: 20.6 MB (20623431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ff4f0661732ea1e9661f9d94015bc7b5fcf85d6674fb173e88c50a23840d40`  
		Last Modified: Tue, 05 Apr 2022 14:45:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7bca8f9f0aebebc3c7c5e968e03474b479420b55a77f33683c435fead3366e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23517412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd43ec235cafac033220e63f50aaf33544f0f719f1a51e4d8be83109763738d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:27:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 07:27:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 07:27:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 07:27:39 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:27:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 07:27:41 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 07:27:42 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a873ae44592179453bfc8ffe686a6faef6bae9b61f4465e8844d31d37b4a74`  
		Last Modified: Tue, 05 Apr 2022 07:28:36 GMT  
		Size: 668.3 KB (668291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f2f70dadc3bc4f06bfc6c0eff12d88e357f1a8c8ee2876e16278cb07571b3`  
		Last Modified: Tue, 05 Apr 2022 07:29:28 GMT  
		Size: 20.1 MB (20131364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24699415b41c9daba64f440481479635163834c11c1cb770c1e56ed677d840`  
		Last Modified: Tue, 05 Apr 2022 07:29:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:38d6b6a109eefba8100d1c9f39cbc3f2cbbc65414bd9d4c21a3f3d3803a20e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:1.7.34-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:fbdf20663eef4b356b91897c11768e710fe5d8c0a20db676b727ace282010c05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2686129323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bff99d35ce807fc8be468d820b698c0aa96bbc198d8fe2d862f033d3a872a7`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 22:58:35 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jun 2022 22:58:36 GMT
EXPOSE 80
# Wed, 15 Jun 2022 22:58:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jun 2022 22:58:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c081bfa67f6b18ab023e3e6f245649e859bd7f6def8eda5884371448bdfa11`  
		Last Modified: Wed, 15 Jun 2022 23:00:34 GMT  
		Size: 22.8 MB (22843843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10edb73d57df6d226de72153277ac47e944dcef4eaadebb4017ed7c9b748699`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0a0dfe9477fcfe1a48749ca97bceaf457e5fb84a996d15fd78917ee6ce177f`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12f9f231fd68bd6cc2c7fab6929a79a59f1df6127ef65cd3a70c3fdd2d84a92`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.8`

```console
$ docker pull traefik@sha256:34a823e33751bef0928a1e8a164b9c54ceb118da1949299c98349c7b2a2e71a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.8` - linux; amd64

```console
$ docker pull traefik@sha256:6059596e7c6a8f34bb7bbb5fb81d8b4688be314922f79aa2e30890c7723e0d10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31526511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f5bb1d51fd89f4d1dd27c1c6188d33e3e98d64563df3001a331d00eb759d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:09:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jun 2022 20:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.0/traefik_v2.8.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jun 2022 20:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jun 2022 20:05:00 GMT
EXPOSE 80
# Wed, 29 Jun 2022 20:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 20:05:00 GMT
CMD ["traefik"]
# Wed, 29 Jun 2022 20:05:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cb125bb766321ae78c2a558eb61358ea0c322871a963cc343f07b19a5dfe9f`  
		Last Modified: Tue, 24 May 2022 20:09:52 GMT  
		Size: 667.0 KB (667045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1150aac411ed055934e3803301a3cfe6fdda3dd71c284af62055ecfc5e61fb`  
		Last Modified: Wed, 29 Jun 2022 20:05:46 GMT  
		Size: 28.0 MB (28044539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cb1cb6b60e1b193da5b716e83beb7a372bbe2a248b1959cd904d9a4383a610`  
		Last Modified: Wed, 29 Jun 2022 20:05:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.8` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4379bf5d7475e41ff5ae6566cfcae4e82560dc316e36f6dbf88f3b83e0f84b80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29620809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3589e296dab63c78caaa81a29d56edf0de1057c8ff38a745669a9b0183aa1f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:16:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:49:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:49:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:49:55 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:49:56 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:49:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ca500a6585c4382a3d0562172788318c2044142456377fdbf2c4b279334e26`  
		Last Modified: Tue, 24 May 2022 20:19:13 GMT  
		Size: 672.6 KB (672642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2176c703419c294312ffa0a819f90605449f3c07e4da70837c3e2b7fd0f373`  
		Last Modified: Mon, 11 Jul 2022 22:52:04 GMT  
		Size: 26.3 MB (26325827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e0d99cd37c83378dc8a8a691a194c20f2151bedbee09db4c421c80a06718f`  
		Last Modified: Mon, 11 Jul 2022 22:51:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.8` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e66f395aa15e46c58886eafbe01e33f6f304cb9113562eb8f8d2b38dd92f9d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28980502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8f243fedba81aafc56b6581521f48e637ed4a58fabf28a40b90643197e176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 21:18:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:45:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:45:40 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:45:42 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:45:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdde6df9c5c8f6328c1ce3fe2ca88cea0a7799584b83cafec0322b4d7235d0b7`  
		Last Modified: Tue, 24 May 2022 21:20:14 GMT  
		Size: 668.4 KB (668397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6b23c3eb33697533291d142505fcc948be77e5853ca37636eea6b2c2acb98`  
		Last Modified: Mon, 11 Jul 2022 22:46:34 GMT  
		Size: 25.6 MB (25595260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d284a3c01dd5b382ae96e7f08e5caf0248787d1f68564322ca59bfef2415f`  
		Last Modified: Mon, 11 Jul 2022 22:46:29 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.8` - linux; s390x

```console
$ docker pull traefik@sha256:6ea9b085836d59e8df7f359bb99aca39ec7e0d68a041d38eb17da61841701fc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca4f2abb356bce415864209427e83e9d77c78821c8e98f2063398fbd29b0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:28:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:42:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:42:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:42:21 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:42:23 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:42:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f52582da22b0abbdbb4590735229191759cc22a1119ccdf5af9cd472103ffd`  
		Last Modified: Tue, 24 May 2022 20:29:51 GMT  
		Size: 672.6 KB (672603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b930ac1eec87e82aba9435698128b667daaa01ac4ca287f5a77891ac2f479`  
		Last Modified: Mon, 11 Jul 2022 22:42:59 GMT  
		Size: 27.0 MB (27030666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77035781dfd75f76ffae40fade166e5eee0e70281d4baddae50980704341adb`  
		Last Modified: Mon, 11 Jul 2022 22:42:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.8-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fd8d3a2f66bfb9d9f84a4f8f9e7e08d909f94dfd97275cce3b25bb3f445c60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:2.8-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:a68b5f90b39d164c320f549f54d2aa224a7cc670f522c23eff787cbf25e66a62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691962512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42ca2b9c9ead9aba38766fdbbeb32f75a4133c34a6d0ba028962ffc0c582e7a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 Jul 2022 23:16:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 Jul 2022 23:16:15 GMT
EXPOSE 80
# Mon, 11 Jul 2022 23:16:16 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 Jul 2022 23:16:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6a8e211023b5620c003ee9b3b7ff89aa40bb5086c10ef39fae345de0b5d0b`  
		Last Modified: Mon, 11 Jul 2022 23:17:01 GMT  
		Size: 28.7 MB (28677361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a93abb30aa22760dbb70d24f9e6d2d28906c5d2d7565bbb8295afb417bc0c`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4666697494e0d7a475f956376c112f4901e87153cef8bd7da8b2ba8d0172bf8`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab32db3cc6f4b2a8c3e5d8f202b6838cfca5851bf9858fe6850c7686826e14`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.8.1`

```console
$ docker pull traefik@sha256:f93cf660e227130ec5e5c6977087960b7e26f8c270a59cd287d2147a722d27fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.8.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4379bf5d7475e41ff5ae6566cfcae4e82560dc316e36f6dbf88f3b83e0f84b80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29620809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3589e296dab63c78caaa81a29d56edf0de1057c8ff38a745669a9b0183aa1f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:16:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:49:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:49:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:49:55 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:49:56 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:49:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ca500a6585c4382a3d0562172788318c2044142456377fdbf2c4b279334e26`  
		Last Modified: Tue, 24 May 2022 20:19:13 GMT  
		Size: 672.6 KB (672642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2176c703419c294312ffa0a819f90605449f3c07e4da70837c3e2b7fd0f373`  
		Last Modified: Mon, 11 Jul 2022 22:52:04 GMT  
		Size: 26.3 MB (26325827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e0d99cd37c83378dc8a8a691a194c20f2151bedbee09db4c421c80a06718f`  
		Last Modified: Mon, 11 Jul 2022 22:51:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.8.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e66f395aa15e46c58886eafbe01e33f6f304cb9113562eb8f8d2b38dd92f9d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28980502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8f243fedba81aafc56b6581521f48e637ed4a58fabf28a40b90643197e176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 21:18:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:45:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:45:40 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:45:42 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:45:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdde6df9c5c8f6328c1ce3fe2ca88cea0a7799584b83cafec0322b4d7235d0b7`  
		Last Modified: Tue, 24 May 2022 21:20:14 GMT  
		Size: 668.4 KB (668397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6b23c3eb33697533291d142505fcc948be77e5853ca37636eea6b2c2acb98`  
		Last Modified: Mon, 11 Jul 2022 22:46:34 GMT  
		Size: 25.6 MB (25595260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d284a3c01dd5b382ae96e7f08e5caf0248787d1f68564322ca59bfef2415f`  
		Last Modified: Mon, 11 Jul 2022 22:46:29 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.8.1` - linux; s390x

```console
$ docker pull traefik@sha256:6ea9b085836d59e8df7f359bb99aca39ec7e0d68a041d38eb17da61841701fc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca4f2abb356bce415864209427e83e9d77c78821c8e98f2063398fbd29b0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:28:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:42:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:42:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:42:21 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:42:23 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:42:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f52582da22b0abbdbb4590735229191759cc22a1119ccdf5af9cd472103ffd`  
		Last Modified: Tue, 24 May 2022 20:29:51 GMT  
		Size: 672.6 KB (672603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b930ac1eec87e82aba9435698128b667daaa01ac4ca287f5a77891ac2f479`  
		Last Modified: Mon, 11 Jul 2022 22:42:59 GMT  
		Size: 27.0 MB (27030666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77035781dfd75f76ffae40fade166e5eee0e70281d4baddae50980704341adb`  
		Last Modified: Mon, 11 Jul 2022 22:42:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.8.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fd8d3a2f66bfb9d9f84a4f8f9e7e08d909f94dfd97275cce3b25bb3f445c60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:2.8.1-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:a68b5f90b39d164c320f549f54d2aa224a7cc670f522c23eff787cbf25e66a62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691962512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42ca2b9c9ead9aba38766fdbbeb32f75a4133c34a6d0ba028962ffc0c582e7a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 Jul 2022 23:16:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 Jul 2022 23:16:15 GMT
EXPOSE 80
# Mon, 11 Jul 2022 23:16:16 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 Jul 2022 23:16:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6a8e211023b5620c003ee9b3b7ff89aa40bb5086c10ef39fae345de0b5d0b`  
		Last Modified: Mon, 11 Jul 2022 23:17:01 GMT  
		Size: 28.7 MB (28677361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a93abb30aa22760dbb70d24f9e6d2d28906c5d2d7565bbb8295afb417bc0c`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4666697494e0d7a475f956376c112f4901e87153cef8bd7da8b2ba8d0172bf8`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab32db3cc6f4b2a8c3e5d8f202b6838cfca5851bf9858fe6850c7686826e14`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:34a823e33751bef0928a1e8a164b9c54ceb118da1949299c98349c7b2a2e71a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:6059596e7c6a8f34bb7bbb5fb81d8b4688be314922f79aa2e30890c7723e0d10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31526511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f5bb1d51fd89f4d1dd27c1c6188d33e3e98d64563df3001a331d00eb759d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:09:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jun 2022 20:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.0/traefik_v2.8.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jun 2022 20:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jun 2022 20:05:00 GMT
EXPOSE 80
# Wed, 29 Jun 2022 20:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 20:05:00 GMT
CMD ["traefik"]
# Wed, 29 Jun 2022 20:05:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cb125bb766321ae78c2a558eb61358ea0c322871a963cc343f07b19a5dfe9f`  
		Last Modified: Tue, 24 May 2022 20:09:52 GMT  
		Size: 667.0 KB (667045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1150aac411ed055934e3803301a3cfe6fdda3dd71c284af62055ecfc5e61fb`  
		Last Modified: Wed, 29 Jun 2022 20:05:46 GMT  
		Size: 28.0 MB (28044539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cb1cb6b60e1b193da5b716e83beb7a372bbe2a248b1959cd904d9a4383a610`  
		Last Modified: Wed, 29 Jun 2022 20:05:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4379bf5d7475e41ff5ae6566cfcae4e82560dc316e36f6dbf88f3b83e0f84b80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29620809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3589e296dab63c78caaa81a29d56edf0de1057c8ff38a745669a9b0183aa1f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:16:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:49:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:49:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:49:55 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:49:56 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:49:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ca500a6585c4382a3d0562172788318c2044142456377fdbf2c4b279334e26`  
		Last Modified: Tue, 24 May 2022 20:19:13 GMT  
		Size: 672.6 KB (672642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2176c703419c294312ffa0a819f90605449f3c07e4da70837c3e2b7fd0f373`  
		Last Modified: Mon, 11 Jul 2022 22:52:04 GMT  
		Size: 26.3 MB (26325827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e0d99cd37c83378dc8a8a691a194c20f2151bedbee09db4c421c80a06718f`  
		Last Modified: Mon, 11 Jul 2022 22:51:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e66f395aa15e46c58886eafbe01e33f6f304cb9113562eb8f8d2b38dd92f9d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28980502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8f243fedba81aafc56b6581521f48e637ed4a58fabf28a40b90643197e176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 21:18:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:45:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:45:40 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:45:42 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:45:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdde6df9c5c8f6328c1ce3fe2ca88cea0a7799584b83cafec0322b4d7235d0b7`  
		Last Modified: Tue, 24 May 2022 21:20:14 GMT  
		Size: 668.4 KB (668397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6b23c3eb33697533291d142505fcc948be77e5853ca37636eea6b2c2acb98`  
		Last Modified: Mon, 11 Jul 2022 22:46:34 GMT  
		Size: 25.6 MB (25595260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d284a3c01dd5b382ae96e7f08e5caf0248787d1f68564322ca59bfef2415f`  
		Last Modified: Mon, 11 Jul 2022 22:46:29 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:6ea9b085836d59e8df7f359bb99aca39ec7e0d68a041d38eb17da61841701fc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca4f2abb356bce415864209427e83e9d77c78821c8e98f2063398fbd29b0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:28:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:42:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:42:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:42:21 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:42:23 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:42:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f52582da22b0abbdbb4590735229191759cc22a1119ccdf5af9cd472103ffd`  
		Last Modified: Tue, 24 May 2022 20:29:51 GMT  
		Size: 672.6 KB (672603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b930ac1eec87e82aba9435698128b667daaa01ac4ca287f5a77891ac2f479`  
		Last Modified: Mon, 11 Jul 2022 22:42:59 GMT  
		Size: 27.0 MB (27030666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77035781dfd75f76ffae40fade166e5eee0e70281d4baddae50980704341adb`  
		Last Modified: Mon, 11 Jul 2022 22:42:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:1d8a41ae1bd54c9e9a5e0cc8da9002638932c53cc3d50c6f0c172238374ebe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:f705216279431ed8ab470318736acd767794a847acda2db325e3e159574bd03c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22607863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43de28b34d397393ca2d0ec8bd6923735fab787f8c3bd3dab0719cd256fcc010`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 18 Mar 2022 06:23:36 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Fri, 18 Mar 2022 06:23:37 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Fri, 18 Mar 2022 06:23:38 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 18 Mar 2022 06:23:39 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:39 GMT
VOLUME [/tmp]
# Fri, 18 Mar 2022 06:23:39 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Mar 2022 06:23:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:903e84870d1b7b581b2c6c362c74751a258cb8e2dbb443bddcd36fe8f29a20ab`  
		Last Modified: Fri, 18 Mar 2022 06:24:59 GMT  
		Size: 117.4 KB (117389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ae7a2b8652023026596365a1dfe88e317d16b1cc8099ee03c20357c95716e`  
		Last Modified: Fri, 18 Mar 2022 06:25:00 GMT  
		Size: 328.5 KB (328522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f483c7bcad16f6ac0813c7a4704d4dc9319bfd6533f10c888b5e2ca21c72dc44`  
		Last Modified: Fri, 18 Mar 2022 06:25:05 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fe6bde6e9349ec036bc3aaec90c095006425bface50ee2f449e0d196cb5850c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21069186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c3451377ef5e2379e4bc19691fb6c14b1a2215326833336e1db9e16cc5ca3`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 22:45:25 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 22:45:27 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 22:45:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Thu, 17 Mar 2022 22:45:33 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:33 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 22:45:34 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 22:45:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:27b61c1d4effca5c7137bfe0c8b6a3a228418ef37998781ad6cc7372c6f7e98f`  
		Last Modified: Thu, 17 Mar 2022 22:48:17 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aae3b48a316f885b1d485fee6b2ffffb3c2c7dea49cea01019d4c103b204da`  
		Last Modified: Thu, 17 Mar 2022 22:48:18 GMT  
		Size: 328.5 KB (328514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82873a2be1cc2b2dfbc565c4bf9960f32b61892f49f0911ec1ac7e310210c3d`  
		Last Modified: Thu, 17 Mar 2022 22:48:34 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c2930d3e36f7feb98470b85e8bc9fce0016fc5eadbc805249e63d6a458eb2323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20577242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7338e148255e82dd93286a1f87db35f499d4e391d7f5f3e1bfb6c71ed4ec2d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 21:07:07 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 21:07:08 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 21:07:09 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 17 Mar 2022 21:07:09 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:07:10 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 21:07:11 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 21:07:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:86cd07830d2730c0aa24f0e47380af5ef760945b5049a2e72a8ebe0675ed6d34`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135b9e65a5ea0b642df02ea2cf73c74a353d1cbfa3b95d048a4adbf0bacf9653`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 328.5 KB (328505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8fa09b05c38fc9116b1446ac3d204200577fd9bfb1801d684657dc722b74b`  
		Last Modified: Thu, 17 Mar 2022 21:08:45 GMT  
		Size: 20.1 MB (20131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:eb08a301bd06b8e71a7dfb44c829e593e6aaa24b0ea6a90cfb09488587911fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:437693178563fbe5e9d51a163f9c5507cfcaf5a52569b7e5814f6ccd71e53ee4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e98bf8d6e3fea93acd477a953dd3276b9ac3a285a9b7cdf1613f806e73a61f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:53:36 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 10:53:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 10:53:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 10:53:56 GMT
EXPOSE 80
# Tue, 05 Apr 2022 10:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:53:56 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 10:53:56 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b5dadc224e5464ecd6b4217323f15e90e06847ef61af9132dc606b1a9863a`  
		Last Modified: Tue, 05 Apr 2022 10:54:28 GMT  
		Size: 666.7 KB (666681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84b4a436968a2d3e0c2d1d3f62ad7c56a1e0a20f0c6e00a8f76f646de636d4`  
		Last Modified: Tue, 05 Apr 2022 10:55:14 GMT  
		Size: 22.2 MB (22162072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb865e347fb64ada1ea356e11aa7f4e81221b6b589b618abf86188a9d3719a`  
		Last Modified: Tue, 05 Apr 2022 10:55:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6907e0a9c3e242920fb2102a261b41864c3d8bf697efa46b6a09596b59c5300e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23922383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db7d675647f8f59a02cd5915f6fd2afab456fbb1716db05032b9111a469f9b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:40:53 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 14:41:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 14:41:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 14:41:49 GMT
EXPOSE 80
# Tue, 05 Apr 2022 14:41:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 14:41:50 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 14:41:50 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a1618fdbb5f9b720d159d71fa3326e20a38c9bba9feb9392f897ab456d07f4`  
		Last Modified: Tue, 05 Apr 2022 14:43:49 GMT  
		Size: 672.5 KB (672528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aba3d211189b35b7f9d6160aa51d316bde615e058a83996627fcb7dfdca0d0`  
		Last Modified: Tue, 05 Apr 2022 14:45:28 GMT  
		Size: 20.6 MB (20623431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ff4f0661732ea1e9661f9d94015bc7b5fcf85d6674fb173e88c50a23840d40`  
		Last Modified: Tue, 05 Apr 2022 14:45:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7bca8f9f0aebebc3c7c5e968e03474b479420b55a77f33683c435fead3366e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23517412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd43ec235cafac033220e63f50aaf33544f0f719f1a51e4d8be83109763738d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:27:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 07:27:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 07:27:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 07:27:39 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:27:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 07:27:41 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 07:27:42 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a873ae44592179453bfc8ffe686a6faef6bae9b61f4465e8844d31d37b4a74`  
		Last Modified: Tue, 05 Apr 2022 07:28:36 GMT  
		Size: 668.3 KB (668291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f2f70dadc3bc4f06bfc6c0eff12d88e357f1a8c8ee2876e16278cb07571b3`  
		Last Modified: Tue, 05 Apr 2022 07:29:28 GMT  
		Size: 20.1 MB (20131364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24699415b41c9daba64f440481479635163834c11c1cb770c1e56ed677d840`  
		Last Modified: Tue, 05 Apr 2022 07:29:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:38d6b6a109eefba8100d1c9f39cbc3f2cbbc65414bd9d4c21a3f3d3803a20e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:fbdf20663eef4b356b91897c11768e710fe5d8c0a20db676b727ace282010c05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2686129323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bff99d35ce807fc8be468d820b698c0aa96bbc198d8fe2d862f033d3a872a7`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 22:58:35 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jun 2022 22:58:36 GMT
EXPOSE 80
# Wed, 15 Jun 2022 22:58:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jun 2022 22:58:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c081bfa67f6b18ab023e3e6f245649e859bd7f6def8eda5884371448bdfa11`  
		Last Modified: Wed, 15 Jun 2022 23:00:34 GMT  
		Size: 22.8 MB (22843843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10edb73d57df6d226de72153277ac47e944dcef4eaadebb4017ed7c9b748699`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0a0dfe9477fcfe1a48749ca97bceaf457e5fb84a996d15fd78917ee6ce177f`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12f9f231fd68bd6cc2c7fab6929a79a59f1df6127ef65cd3a70c3fdd2d84a92`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:1d8a41ae1bd54c9e9a5e0cc8da9002638932c53cc3d50c6f0c172238374ebe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:f705216279431ed8ab470318736acd767794a847acda2db325e3e159574bd03c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22607863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43de28b34d397393ca2d0ec8bd6923735fab787f8c3bd3dab0719cd256fcc010`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 18 Mar 2022 06:23:36 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Fri, 18 Mar 2022 06:23:37 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Fri, 18 Mar 2022 06:23:38 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 18 Mar 2022 06:23:39 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:39 GMT
VOLUME [/tmp]
# Fri, 18 Mar 2022 06:23:39 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Mar 2022 06:23:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:903e84870d1b7b581b2c6c362c74751a258cb8e2dbb443bddcd36fe8f29a20ab`  
		Last Modified: Fri, 18 Mar 2022 06:24:59 GMT  
		Size: 117.4 KB (117389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ae7a2b8652023026596365a1dfe88e317d16b1cc8099ee03c20357c95716e`  
		Last Modified: Fri, 18 Mar 2022 06:25:00 GMT  
		Size: 328.5 KB (328522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f483c7bcad16f6ac0813c7a4704d4dc9319bfd6533f10c888b5e2ca21c72dc44`  
		Last Modified: Fri, 18 Mar 2022 06:25:05 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fe6bde6e9349ec036bc3aaec90c095006425bface50ee2f449e0d196cb5850c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21069186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c3451377ef5e2379e4bc19691fb6c14b1a2215326833336e1db9e16cc5ca3`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 22:45:25 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 22:45:27 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 22:45:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Thu, 17 Mar 2022 22:45:33 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:33 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 22:45:34 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 22:45:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:27b61c1d4effca5c7137bfe0c8b6a3a228418ef37998781ad6cc7372c6f7e98f`  
		Last Modified: Thu, 17 Mar 2022 22:48:17 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aae3b48a316f885b1d485fee6b2ffffb3c2c7dea49cea01019d4c103b204da`  
		Last Modified: Thu, 17 Mar 2022 22:48:18 GMT  
		Size: 328.5 KB (328514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82873a2be1cc2b2dfbc565c4bf9960f32b61892f49f0911ec1ac7e310210c3d`  
		Last Modified: Thu, 17 Mar 2022 22:48:34 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c2930d3e36f7feb98470b85e8bc9fce0016fc5eadbc805249e63d6a458eb2323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20577242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7338e148255e82dd93286a1f87db35f499d4e391d7f5f3e1bfb6c71ed4ec2d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 21:07:07 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 21:07:08 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 21:07:09 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 17 Mar 2022 21:07:09 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:07:10 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 21:07:11 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 21:07:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:86cd07830d2730c0aa24f0e47380af5ef760945b5049a2e72a8ebe0675ed6d34`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135b9e65a5ea0b642df02ea2cf73c74a353d1cbfa3b95d048a4adbf0bacf9653`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 328.5 KB (328505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8fa09b05c38fc9116b1446ac3d204200577fd9bfb1801d684657dc722b74b`  
		Last Modified: Thu, 17 Mar 2022 21:08:45 GMT  
		Size: 20.1 MB (20131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:eb08a301bd06b8e71a7dfb44c829e593e6aaa24b0ea6a90cfb09488587911fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:437693178563fbe5e9d51a163f9c5507cfcaf5a52569b7e5814f6ccd71e53ee4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e98bf8d6e3fea93acd477a953dd3276b9ac3a285a9b7cdf1613f806e73a61f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:53:36 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 10:53:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 10:53:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 10:53:56 GMT
EXPOSE 80
# Tue, 05 Apr 2022 10:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:53:56 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 10:53:56 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b5dadc224e5464ecd6b4217323f15e90e06847ef61af9132dc606b1a9863a`  
		Last Modified: Tue, 05 Apr 2022 10:54:28 GMT  
		Size: 666.7 KB (666681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84b4a436968a2d3e0c2d1d3f62ad7c56a1e0a20f0c6e00a8f76f646de636d4`  
		Last Modified: Tue, 05 Apr 2022 10:55:14 GMT  
		Size: 22.2 MB (22162072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb865e347fb64ada1ea356e11aa7f4e81221b6b589b618abf86188a9d3719a`  
		Last Modified: Tue, 05 Apr 2022 10:55:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6907e0a9c3e242920fb2102a261b41864c3d8bf697efa46b6a09596b59c5300e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23922383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db7d675647f8f59a02cd5915f6fd2afab456fbb1716db05032b9111a469f9b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:40:53 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 14:41:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 14:41:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 14:41:49 GMT
EXPOSE 80
# Tue, 05 Apr 2022 14:41:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 14:41:50 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 14:41:50 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a1618fdbb5f9b720d159d71fa3326e20a38c9bba9feb9392f897ab456d07f4`  
		Last Modified: Tue, 05 Apr 2022 14:43:49 GMT  
		Size: 672.5 KB (672528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aba3d211189b35b7f9d6160aa51d316bde615e058a83996627fcb7dfdca0d0`  
		Last Modified: Tue, 05 Apr 2022 14:45:28 GMT  
		Size: 20.6 MB (20623431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ff4f0661732ea1e9661f9d94015bc7b5fcf85d6674fb173e88c50a23840d40`  
		Last Modified: Tue, 05 Apr 2022 14:45:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7bca8f9f0aebebc3c7c5e968e03474b479420b55a77f33683c435fead3366e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23517412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd43ec235cafac033220e63f50aaf33544f0f719f1a51e4d8be83109763738d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:27:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 07:27:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 07:27:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 07:27:39 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:27:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 07:27:41 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 07:27:42 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a873ae44592179453bfc8ffe686a6faef6bae9b61f4465e8844d31d37b4a74`  
		Last Modified: Tue, 05 Apr 2022 07:28:36 GMT  
		Size: 668.3 KB (668291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f2f70dadc3bc4f06bfc6c0eff12d88e357f1a8c8ee2876e16278cb07571b3`  
		Last Modified: Tue, 05 Apr 2022 07:29:28 GMT  
		Size: 20.1 MB (20131364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24699415b41c9daba64f440481479635163834c11c1cb770c1e56ed677d840`  
		Last Modified: Tue, 05 Apr 2022 07:29:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:38d6b6a109eefba8100d1c9f39cbc3f2cbbc65414bd9d4c21a3f3d3803a20e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:fbdf20663eef4b356b91897c11768e710fe5d8c0a20db676b727ace282010c05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2686129323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bff99d35ce807fc8be468d820b698c0aa96bbc198d8fe2d862f033d3a872a7`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 22:58:35 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jun 2022 22:58:36 GMT
EXPOSE 80
# Wed, 15 Jun 2022 22:58:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jun 2022 22:58:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c081bfa67f6b18ab023e3e6f245649e859bd7f6def8eda5884371448bdfa11`  
		Last Modified: Wed, 15 Jun 2022 23:00:34 GMT  
		Size: 22.8 MB (22843843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10edb73d57df6d226de72153277ac47e944dcef4eaadebb4017ed7c9b748699`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0a0dfe9477fcfe1a48749ca97bceaf457e5fb84a996d15fd78917ee6ce177f`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12f9f231fd68bd6cc2c7fab6929a79a59f1df6127ef65cd3a70c3fdd2d84a92`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34`

```console
$ docker pull traefik@sha256:1d8a41ae1bd54c9e9a5e0cc8da9002638932c53cc3d50c6f0c172238374ebe8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:f705216279431ed8ab470318736acd767794a847acda2db325e3e159574bd03c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22607863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43de28b34d397393ca2d0ec8bd6923735fab787f8c3bd3dab0719cd256fcc010`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 18 Mar 2022 06:23:36 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Fri, 18 Mar 2022 06:23:37 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Fri, 18 Mar 2022 06:23:38 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 18 Mar 2022 06:23:39 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:39 GMT
VOLUME [/tmp]
# Fri, 18 Mar 2022 06:23:39 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Mar 2022 06:23:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:903e84870d1b7b581b2c6c362c74751a258cb8e2dbb443bddcd36fe8f29a20ab`  
		Last Modified: Fri, 18 Mar 2022 06:24:59 GMT  
		Size: 117.4 KB (117389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ae7a2b8652023026596365a1dfe88e317d16b1cc8099ee03c20357c95716e`  
		Last Modified: Fri, 18 Mar 2022 06:25:00 GMT  
		Size: 328.5 KB (328522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f483c7bcad16f6ac0813c7a4704d4dc9319bfd6533f10c888b5e2ca21c72dc44`  
		Last Modified: Fri, 18 Mar 2022 06:25:05 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fe6bde6e9349ec036bc3aaec90c095006425bface50ee2f449e0d196cb5850c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21069186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5c3451377ef5e2379e4bc19691fb6c14b1a2215326833336e1db9e16cc5ca3`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 22:45:25 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 22:45:27 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 22:45:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Thu, 17 Mar 2022 22:45:33 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:33 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 22:45:34 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 22:45:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:27b61c1d4effca5c7137bfe0c8b6a3a228418ef37998781ad6cc7372c6f7e98f`  
		Last Modified: Thu, 17 Mar 2022 22:48:17 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aae3b48a316f885b1d485fee6b2ffffb3c2c7dea49cea01019d4c103b204da`  
		Last Modified: Thu, 17 Mar 2022 22:48:18 GMT  
		Size: 328.5 KB (328514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82873a2be1cc2b2dfbc565c4bf9960f32b61892f49f0911ec1ac7e310210c3d`  
		Last Modified: Thu, 17 Mar 2022 22:48:34 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:c2930d3e36f7feb98470b85e8bc9fce0016fc5eadbc805249e63d6a458eb2323
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20577242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7338e148255e82dd93286a1f87db35f499d4e391d7f5f3e1bfb6c71ed4ec2d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Mar 2022 21:07:07 GMT
COPY file:8536203e9de8580f4424aff73a3be4185daba1818e4bfa286f2b290d1459aeb9 in /etc/ssl/certs/ 
# Thu, 17 Mar 2022 21:07:08 GMT
COPY dir:a84372748b89eb90478bb1b120b7c8fff3112421d7f93e50fbeae3f53adc6788 in /usr/share/ 
# Thu, 17 Mar 2022 21:07:09 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 17 Mar 2022 21:07:09 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:07:10 GMT
VOLUME [/tmp]
# Thu, 17 Mar 2022 21:07:11 GMT
ENTRYPOINT ["/traefik"]
# Thu, 17 Mar 2022 21:07:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:86cd07830d2730c0aa24f0e47380af5ef760945b5049a2e72a8ebe0675ed6d34`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 117.4 KB (117390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135b9e65a5ea0b642df02ea2cf73c74a353d1cbfa3b95d048a4adbf0bacf9653`  
		Last Modified: Thu, 17 Mar 2022 21:08:41 GMT  
		Size: 328.5 KB (328505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee8fa09b05c38fc9116b1446ac3d204200577fd9bfb1801d684657dc722b74b`  
		Last Modified: Thu, 17 Mar 2022 21:08:45 GMT  
		Size: 20.1 MB (20131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-alpine`

```console
$ docker pull traefik@sha256:eb08a301bd06b8e71a7dfb44c829e593e6aaa24b0ea6a90cfb09488587911fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:437693178563fbe5e9d51a163f9c5507cfcaf5a52569b7e5814f6ccd71e53ee4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e98bf8d6e3fea93acd477a953dd3276b9ac3a285a9b7cdf1613f806e73a61f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:53:36 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 10:53:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 10:53:56 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 10:53:56 GMT
EXPOSE 80
# Tue, 05 Apr 2022 10:53:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 10:53:56 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 10:53:56 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b5dadc224e5464ecd6b4217323f15e90e06847ef61af9132dc606b1a9863a`  
		Last Modified: Tue, 05 Apr 2022 10:54:28 GMT  
		Size: 666.7 KB (666681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae84b4a436968a2d3e0c2d1d3f62ad7c56a1e0a20f0c6e00a8f76f646de636d4`  
		Last Modified: Tue, 05 Apr 2022 10:55:14 GMT  
		Size: 22.2 MB (22162072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beb865e347fb64ada1ea356e11aa7f4e81221b6b589b618abf86188a9d3719a`  
		Last Modified: Tue, 05 Apr 2022 10:55:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6907e0a9c3e242920fb2102a261b41864c3d8bf697efa46b6a09596b59c5300e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23922383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db7d675647f8f59a02cd5915f6fd2afab456fbb1716db05032b9111a469f9b4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:40:53 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 14:41:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 14:41:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 14:41:49 GMT
EXPOSE 80
# Tue, 05 Apr 2022 14:41:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 14:41:50 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 14:41:50 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a1618fdbb5f9b720d159d71fa3326e20a38c9bba9feb9392f897ab456d07f4`  
		Last Modified: Tue, 05 Apr 2022 14:43:49 GMT  
		Size: 672.5 KB (672528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2aba3d211189b35b7f9d6160aa51d316bde615e058a83996627fcb7dfdca0d0`  
		Last Modified: Tue, 05 Apr 2022 14:45:28 GMT  
		Size: 20.6 MB (20623431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ff4f0661732ea1e9661f9d94015bc7b5fcf85d6674fb173e88c50a23840d40`  
		Last Modified: Tue, 05 Apr 2022 14:45:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:7bca8f9f0aebebc3c7c5e968e03474b479420b55a77f33683c435fead3366e18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23517412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd43ec235cafac033220e63f50aaf33544f0f719f1a51e4d8be83109763738d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:27:04 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 05 Apr 2022 07:27:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Tue, 05 Apr 2022 07:27:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 05 Apr 2022 07:27:39 GMT
EXPOSE 80
# Tue, 05 Apr 2022 07:27:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Apr 2022 07:27:41 GMT
CMD ["traefik"]
# Tue, 05 Apr 2022 07:27:42 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a873ae44592179453bfc8ffe686a6faef6bae9b61f4465e8844d31d37b4a74`  
		Last Modified: Tue, 05 Apr 2022 07:28:36 GMT  
		Size: 668.3 KB (668291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1f2f70dadc3bc4f06bfc6c0eff12d88e357f1a8c8ee2876e16278cb07571b3`  
		Last Modified: Tue, 05 Apr 2022 07:29:28 GMT  
		Size: 20.1 MB (20131364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c24699415b41c9daba64f440481479635163834c11c1cb770c1e56ed677d840`  
		Last Modified: Tue, 05 Apr 2022 07:29:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:38d6b6a109eefba8100d1c9f39cbc3f2cbbc65414bd9d4c21a3f3d3803a20e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:v1.7.34-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:fbdf20663eef4b356b91897c11768e710fe5d8c0a20db676b727ace282010c05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2686129323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bff99d35ce807fc8be468d820b698c0aa96bbc198d8fe2d862f033d3a872a7`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jun 2022 22:58:35 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 15 Jun 2022 22:58:36 GMT
EXPOSE 80
# Wed, 15 Jun 2022 22:58:37 GMT
ENTRYPOINT ["/traefik"]
# Wed, 15 Jun 2022 22:58:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c081bfa67f6b18ab023e3e6f245649e859bd7f6def8eda5884371448bdfa11`  
		Last Modified: Wed, 15 Jun 2022 23:00:34 GMT  
		Size: 22.8 MB (22843843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10edb73d57df6d226de72153277ac47e944dcef4eaadebb4017ed7c9b748699`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0a0dfe9477fcfe1a48749ca97bceaf457e5fb84a996d15fd78917ee6ce177f`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12f9f231fd68bd6cc2c7fab6929a79a59f1df6127ef65cd3a70c3fdd2d84a92`  
		Last Modified: Wed, 15 Jun 2022 23:00:27 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.8`

```console
$ docker pull traefik@sha256:34a823e33751bef0928a1e8a164b9c54ceb118da1949299c98349c7b2a2e71a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.8` - linux; amd64

```console
$ docker pull traefik@sha256:6059596e7c6a8f34bb7bbb5fb81d8b4688be314922f79aa2e30890c7723e0d10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31526511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f5bb1d51fd89f4d1dd27c1c6188d33e3e98d64563df3001a331d00eb759d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:09:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jun 2022 20:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.0/traefik_v2.8.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jun 2022 20:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jun 2022 20:05:00 GMT
EXPOSE 80
# Wed, 29 Jun 2022 20:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 20:05:00 GMT
CMD ["traefik"]
# Wed, 29 Jun 2022 20:05:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cb125bb766321ae78c2a558eb61358ea0c322871a963cc343f07b19a5dfe9f`  
		Last Modified: Tue, 24 May 2022 20:09:52 GMT  
		Size: 667.0 KB (667045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1150aac411ed055934e3803301a3cfe6fdda3dd71c284af62055ecfc5e61fb`  
		Last Modified: Wed, 29 Jun 2022 20:05:46 GMT  
		Size: 28.0 MB (28044539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cb1cb6b60e1b193da5b716e83beb7a372bbe2a248b1959cd904d9a4383a610`  
		Last Modified: Wed, 29 Jun 2022 20:05:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.8` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4379bf5d7475e41ff5ae6566cfcae4e82560dc316e36f6dbf88f3b83e0f84b80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29620809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3589e296dab63c78caaa81a29d56edf0de1057c8ff38a745669a9b0183aa1f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:16:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:49:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:49:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:49:55 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:49:56 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:49:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ca500a6585c4382a3d0562172788318c2044142456377fdbf2c4b279334e26`  
		Last Modified: Tue, 24 May 2022 20:19:13 GMT  
		Size: 672.6 KB (672642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2176c703419c294312ffa0a819f90605449f3c07e4da70837c3e2b7fd0f373`  
		Last Modified: Mon, 11 Jul 2022 22:52:04 GMT  
		Size: 26.3 MB (26325827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e0d99cd37c83378dc8a8a691a194c20f2151bedbee09db4c421c80a06718f`  
		Last Modified: Mon, 11 Jul 2022 22:51:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.8` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e66f395aa15e46c58886eafbe01e33f6f304cb9113562eb8f8d2b38dd92f9d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28980502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8f243fedba81aafc56b6581521f48e637ed4a58fabf28a40b90643197e176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 21:18:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:45:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:45:40 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:45:42 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:45:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdde6df9c5c8f6328c1ce3fe2ca88cea0a7799584b83cafec0322b4d7235d0b7`  
		Last Modified: Tue, 24 May 2022 21:20:14 GMT  
		Size: 668.4 KB (668397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6b23c3eb33697533291d142505fcc948be77e5853ca37636eea6b2c2acb98`  
		Last Modified: Mon, 11 Jul 2022 22:46:34 GMT  
		Size: 25.6 MB (25595260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d284a3c01dd5b382ae96e7f08e5caf0248787d1f68564322ca59bfef2415f`  
		Last Modified: Mon, 11 Jul 2022 22:46:29 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.8` - linux; s390x

```console
$ docker pull traefik@sha256:6ea9b085836d59e8df7f359bb99aca39ec7e0d68a041d38eb17da61841701fc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca4f2abb356bce415864209427e83e9d77c78821c8e98f2063398fbd29b0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:28:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:42:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:42:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:42:21 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:42:23 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:42:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f52582da22b0abbdbb4590735229191759cc22a1119ccdf5af9cd472103ffd`  
		Last Modified: Tue, 24 May 2022 20:29:51 GMT  
		Size: 672.6 KB (672603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b930ac1eec87e82aba9435698128b667daaa01ac4ca287f5a77891ac2f479`  
		Last Modified: Mon, 11 Jul 2022 22:42:59 GMT  
		Size: 27.0 MB (27030666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77035781dfd75f76ffae40fade166e5eee0e70281d4baddae50980704341adb`  
		Last Modified: Mon, 11 Jul 2022 22:42:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.8-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fd8d3a2f66bfb9d9f84a4f8f9e7e08d909f94dfd97275cce3b25bb3f445c60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:v2.8-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:a68b5f90b39d164c320f549f54d2aa224a7cc670f522c23eff787cbf25e66a62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691962512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42ca2b9c9ead9aba38766fdbbeb32f75a4133c34a6d0ba028962ffc0c582e7a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 Jul 2022 23:16:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 Jul 2022 23:16:15 GMT
EXPOSE 80
# Mon, 11 Jul 2022 23:16:16 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 Jul 2022 23:16:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6a8e211023b5620c003ee9b3b7ff89aa40bb5086c10ef39fae345de0b5d0b`  
		Last Modified: Mon, 11 Jul 2022 23:17:01 GMT  
		Size: 28.7 MB (28677361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a93abb30aa22760dbb70d24f9e6d2d28906c5d2d7565bbb8295afb417bc0c`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4666697494e0d7a475f956376c112f4901e87153cef8bd7da8b2ba8d0172bf8`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab32db3cc6f4b2a8c3e5d8f202b6838cfca5851bf9858fe6850c7686826e14`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.8.1`

```console
$ docker pull traefik@sha256:f93cf660e227130ec5e5c6977087960b7e26f8c270a59cd287d2147a722d27fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.8.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4379bf5d7475e41ff5ae6566cfcae4e82560dc316e36f6dbf88f3b83e0f84b80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29620809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3589e296dab63c78caaa81a29d56edf0de1057c8ff38a745669a9b0183aa1f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:16:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:49:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:49:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:49:55 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:49:56 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:49:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ca500a6585c4382a3d0562172788318c2044142456377fdbf2c4b279334e26`  
		Last Modified: Tue, 24 May 2022 20:19:13 GMT  
		Size: 672.6 KB (672642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2176c703419c294312ffa0a819f90605449f3c07e4da70837c3e2b7fd0f373`  
		Last Modified: Mon, 11 Jul 2022 22:52:04 GMT  
		Size: 26.3 MB (26325827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e0d99cd37c83378dc8a8a691a194c20f2151bedbee09db4c421c80a06718f`  
		Last Modified: Mon, 11 Jul 2022 22:51:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.8.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e66f395aa15e46c58886eafbe01e33f6f304cb9113562eb8f8d2b38dd92f9d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28980502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8f243fedba81aafc56b6581521f48e637ed4a58fabf28a40b90643197e176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 21:18:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:45:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:45:40 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:45:42 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:45:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdde6df9c5c8f6328c1ce3fe2ca88cea0a7799584b83cafec0322b4d7235d0b7`  
		Last Modified: Tue, 24 May 2022 21:20:14 GMT  
		Size: 668.4 KB (668397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6b23c3eb33697533291d142505fcc948be77e5853ca37636eea6b2c2acb98`  
		Last Modified: Mon, 11 Jul 2022 22:46:34 GMT  
		Size: 25.6 MB (25595260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d284a3c01dd5b382ae96e7f08e5caf0248787d1f68564322ca59bfef2415f`  
		Last Modified: Mon, 11 Jul 2022 22:46:29 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.8.1` - linux; s390x

```console
$ docker pull traefik@sha256:6ea9b085836d59e8df7f359bb99aca39ec7e0d68a041d38eb17da61841701fc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca4f2abb356bce415864209427e83e9d77c78821c8e98f2063398fbd29b0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:28:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:42:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:42:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:42:21 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:42:23 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:42:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f52582da22b0abbdbb4590735229191759cc22a1119ccdf5af9cd472103ffd`  
		Last Modified: Tue, 24 May 2022 20:29:51 GMT  
		Size: 672.6 KB (672603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b930ac1eec87e82aba9435698128b667daaa01ac4ca287f5a77891ac2f479`  
		Last Modified: Mon, 11 Jul 2022 22:42:59 GMT  
		Size: 27.0 MB (27030666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77035781dfd75f76ffae40fade166e5eee0e70281d4baddae50980704341adb`  
		Last Modified: Mon, 11 Jul 2022 22:42:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.8.1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fd8d3a2f66bfb9d9f84a4f8f9e7e08d909f94dfd97275cce3b25bb3f445c60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:v2.8.1-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:a68b5f90b39d164c320f549f54d2aa224a7cc670f522c23eff787cbf25e66a62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691962512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42ca2b9c9ead9aba38766fdbbeb32f75a4133c34a6d0ba028962ffc0c582e7a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 Jul 2022 23:16:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 Jul 2022 23:16:15 GMT
EXPOSE 80
# Mon, 11 Jul 2022 23:16:16 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 Jul 2022 23:16:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6a8e211023b5620c003ee9b3b7ff89aa40bb5086c10ef39fae345de0b5d0b`  
		Last Modified: Mon, 11 Jul 2022 23:17:01 GMT  
		Size: 28.7 MB (28677361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a93abb30aa22760dbb70d24f9e6d2d28906c5d2d7565bbb8295afb417bc0c`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4666697494e0d7a475f956376c112f4901e87153cef8bd7da8b2ba8d0172bf8`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab32db3cc6f4b2a8c3e5d8f202b6838cfca5851bf9858fe6850c7686826e14`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:vacherin`

```console
$ docker pull traefik@sha256:34a823e33751bef0928a1e8a164b9c54ceb118da1949299c98349c7b2a2e71a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:vacherin` - linux; amd64

```console
$ docker pull traefik@sha256:6059596e7c6a8f34bb7bbb5fb81d8b4688be314922f79aa2e30890c7723e0d10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31526511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f5bb1d51fd89f4d1dd27c1c6188d33e3e98d64563df3001a331d00eb759d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:09:12 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Jun 2022 20:04:59 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.0/traefik_v2.8.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Jun 2022 20:05:00 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Jun 2022 20:05:00 GMT
EXPOSE 80
# Wed, 29 Jun 2022 20:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 20:05:00 GMT
CMD ["traefik"]
# Wed, 29 Jun 2022 20:05:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cb125bb766321ae78c2a558eb61358ea0c322871a963cc343f07b19a5dfe9f`  
		Last Modified: Tue, 24 May 2022 20:09:52 GMT  
		Size: 667.0 KB (667045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1150aac411ed055934e3803301a3cfe6fdda3dd71c284af62055ecfc5e61fb`  
		Last Modified: Wed, 29 Jun 2022 20:05:46 GMT  
		Size: 28.0 MB (28044539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41cb1cb6b60e1b193da5b716e83beb7a372bbe2a248b1959cd904d9a4383a610`  
		Last Modified: Wed, 29 Jun 2022 20:05:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:vacherin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4379bf5d7475e41ff5ae6566cfcae4e82560dc316e36f6dbf88f3b83e0f84b80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29620809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3589e296dab63c78caaa81a29d56edf0de1057c8ff38a745669a9b0183aa1f93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:16:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:49:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:49:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:49:55 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:49:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:49:56 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:49:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ca500a6585c4382a3d0562172788318c2044142456377fdbf2c4b279334e26`  
		Last Modified: Tue, 24 May 2022 20:19:13 GMT  
		Size: 672.6 KB (672642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2176c703419c294312ffa0a819f90605449f3c07e4da70837c3e2b7fd0f373`  
		Last Modified: Mon, 11 Jul 2022 22:52:04 GMT  
		Size: 26.3 MB (26325827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e0d99cd37c83378dc8a8a691a194c20f2151bedbee09db4c421c80a06718f`  
		Last Modified: Mon, 11 Jul 2022 22:51:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:vacherin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e66f395aa15e46c58886eafbe01e33f6f304cb9113562eb8f8d2b38dd92f9d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28980502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f8f243fedba81aafc56b6581521f48e637ed4a58fabf28a40b90643197e176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 21:18:51 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:45:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:45:40 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:45:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:45:42 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:45:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdde6df9c5c8f6328c1ce3fe2ca88cea0a7799584b83cafec0322b4d7235d0b7`  
		Last Modified: Tue, 24 May 2022 21:20:14 GMT  
		Size: 668.4 KB (668397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e6b23c3eb33697533291d142505fcc948be77e5853ca37636eea6b2c2acb98`  
		Last Modified: Mon, 11 Jul 2022 22:46:34 GMT  
		Size: 25.6 MB (25595260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1d284a3c01dd5b382ae96e7f08e5caf0248787d1f68564322ca59bfef2415f`  
		Last Modified: Mon, 11 Jul 2022 22:46:29 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:vacherin` - linux; s390x

```console
$ docker pull traefik@sha256:6ea9b085836d59e8df7f359bb99aca39ec7e0d68a041d38eb17da61841701fc5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca4f2abb356bce415864209427e83e9d77c78821c8e98f2063398fbd29b0c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 24 May 2022 20:28:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jul 2022 22:42:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jul 2022 22:42:21 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jul 2022 22:42:21 GMT
EXPOSE 80
# Mon, 11 Jul 2022 22:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jul 2022 22:42:23 GMT
CMD ["traefik"]
# Mon, 11 Jul 2022 22:42:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f52582da22b0abbdbb4590735229191759cc22a1119ccdf5af9cd472103ffd`  
		Last Modified: Tue, 24 May 2022 20:29:51 GMT  
		Size: 672.6 KB (672603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0b930ac1eec87e82aba9435698128b667daaa01ac4ca287f5a77891ac2f479`  
		Last Modified: Mon, 11 Jul 2022 22:42:59 GMT  
		Size: 27.0 MB (27030666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77035781dfd75f76ffae40fade166e5eee0e70281d4baddae50980704341adb`  
		Last Modified: Mon, 11 Jul 2022 22:42:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:vacherin-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fd8d3a2f66bfb9d9f84a4f8f9e7e08d909f94dfd97275cce3b25bb3f445c60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:vacherin-windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:a68b5f90b39d164c320f549f54d2aa224a7cc670f522c23eff787cbf25e66a62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691962512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42ca2b9c9ead9aba38766fdbbeb32f75a4133c34a6d0ba028962ffc0c582e7a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 Jul 2022 23:16:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 Jul 2022 23:16:15 GMT
EXPOSE 80
# Mon, 11 Jul 2022 23:16:16 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 Jul 2022 23:16:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6a8e211023b5620c003ee9b3b7ff89aa40bb5086c10ef39fae345de0b5d0b`  
		Last Modified: Mon, 11 Jul 2022 23:17:01 GMT  
		Size: 28.7 MB (28677361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a93abb30aa22760dbb70d24f9e6d2d28906c5d2d7565bbb8295afb417bc0c`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4666697494e0d7a475f956376c112f4901e87153cef8bd7da8b2ba8d0172bf8`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab32db3cc6f4b2a8c3e5d8f202b6838cfca5851bf9858fe6850c7686826e14`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:fd8d3a2f66bfb9d9f84a4f8f9e7e08d909f94dfd97275cce3b25bb3f445c60ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull traefik@sha256:a68b5f90b39d164c320f549f54d2aa224a7cc670f522c23eff787cbf25e66a62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2691962512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42ca2b9c9ead9aba38766fdbbeb32f75a4133c34a6d0ba028962ffc0c582e7a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 12:18:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 Jul 2022 23:16:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.8.1/traefik_v2.8.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 Jul 2022 23:16:15 GMT
EXPOSE 80
# Mon, 11 Jul 2022 23:16:16 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 Jul 2022 23:16:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4ed911f97ae3a2a6279c70738e5692b14369ac11871a2bbd2f6ad301419527ad`  
		Last Modified: Wed, 15 Jun 2022 12:50:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c6a8e211023b5620c003ee9b3b7ff89aa40bb5086c10ef39fae345de0b5d0b`  
		Last Modified: Mon, 11 Jul 2022 23:17:01 GMT  
		Size: 28.7 MB (28677361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a93abb30aa22760dbb70d24f9e6d2d28906c5d2d7565bbb8295afb417bc0c`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4666697494e0d7a475f956376c112f4901e87153cef8bd7da8b2ba8d0172bf8`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab32db3cc6f4b2a8c3e5d8f202b6838cfca5851bf9858fe6850c7686826e14`  
		Last Modified: Mon, 11 Jul 2022 23:16:54 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
