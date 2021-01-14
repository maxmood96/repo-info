<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7.28`](#traefik1728)
-	[`traefik:1.7.28-alpine`](#traefik1728-alpine)
-	[`traefik:1.7.28-windowsservercore-1809`](#traefik1728-windowsservercore-1809)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:2.3`](#traefik23)
-	[`traefik:2.3.7`](#traefik237)
-	[`traefik:2.3.7-windowsservercore-1809`](#traefik237-windowsservercore-1809)
-	[`traefik:2.3-windowsservercore-1809`](#traefik23-windowsservercore-1809)
-	[`traefik:2.4`](#traefik24)
-	[`traefik:2.4.0-rc2`](#traefik240-rc2)
-	[`traefik:2.4.0-rc2-windowsservercore-1809`](#traefik240-rc2-windowsservercore-1809)
-	[`traefik:2.4-windowsservercore-1809`](#traefik24-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:livarot`](#traefiklivarot)
-	[`traefik:livarot-windowsservercore-1809`](#traefiklivarot-windowsservercore-1809)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:picodon`](#traefikpicodon)
-	[`traefik:picodon-windowsservercore-1809`](#traefikpicodon-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7.28`](#traefikv1728)
-	[`traefik:v1.7.28-alpine`](#traefikv1728-alpine)
-	[`traefik:v1.7.28-windowsservercore-1809`](#traefikv1728-windowsservercore-1809)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v2.3`](#traefikv23)
-	[`traefik:v2.3.7`](#traefikv237)
-	[`traefik:v2.3.7-windowsservercore-1809`](#traefikv237-windowsservercore-1809)
-	[`traefik:v2.3-windowsservercore-1809`](#traefikv23-windowsservercore-1809)
-	[`traefik:v2.4`](#traefikv24)
-	[`traefik:v2.4.0-rc2`](#traefikv240-rc2)
-	[`traefik:v2.4.0-rc2-windowsservercore-1809`](#traefikv240-rc2-windowsservercore-1809)
-	[`traefik:v2.4-windowsservercore-1809`](#traefikv24-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:998fc0cce3df0fe066005d6e94a7fa8b20749155fb54b4ebd1603e039b842feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:154e065982592220c9355925d9e60348eec6850418754ee76840f83501341b00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21553283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d67ddf1c8b647742ebb1ea0d3edb163dff028640b772832fa325b6b7df830f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:48:11 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:48:11 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 22:29:46 GMT
COPY file:94b9997cc55c7732c9fc173c119f980e4a38eba20b96a90170a3d7fade75f0eb in / 
# Wed, 13 Jan 2021 22:29:47 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:47 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 22:29:47 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 22:29:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:79de75e85675fa9abbac17b57205d3e0dfcf2bd2fc4cbc194f2aaf917435425e`  
		Last Modified: Thu, 17 Dec 2020 00:49:17 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e925284bb6370a549da51637ed98a8e574317473e082cc4be745d87327c7f`  
		Last Modified: Thu, 17 Dec 2020 00:49:18 GMT  
		Size: 306.4 KB (306411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81848bd29c493bb51f93a0bf98cf3958436af2128b6890d7a28a35b7dfc352c0`  
		Last Modified: Wed, 13 Jan 2021 22:30:48 GMT  
		Size: 21.1 MB (21116000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2f69dff9f3e67a011f08fc6a59fc3f72aa26533b5b9c8cd127e1f90948cbaf09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20205544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da195dbaa64e13483787db1f21a4e602751bd363ac5c6e594e5e17c1f2420aec`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:26:48 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:57:06 GMT
COPY file:3d9c1552db5b4c73ac7fe21268eeb20506f000d2e59d7be76697f45a50d32c64 in / 
# Wed, 13 Jan 2021 21:57:07 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:57:08 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:57:09 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:57:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc6fb65827756c9d95005162623d443b2bd3e445269bcb1a7006e080726d3c`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 306.5 KB (306458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0280c8ba5c59856146b5130ce0c0eb8b83b9dcc2dea1d69991723680815054f`  
		Last Modified: Wed, 13 Jan 2021 21:58:11 GMT  
		Size: 19.8 MB (19768213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:468570d210f86c4366e666dac62c34b3054c230ee0b4d61c36e37ed276550b39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fff7cc610524cb77e4767eb66f534053cc0f45853e096fb250937594f9913d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:27:58 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:46:55 GMT
COPY file:6bab4a8fc3d272fc29bc5ff42634cb12785fea9e23b0cf50f077702217bb6c03 in / 
# Wed, 13 Jan 2021 21:46:56 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:56 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:46:57 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:46:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c32c03119dbb32c844511340cb40a21ba5a56b90862cf603dec2e49cf5ab20d`  
		Last Modified: Thu, 17 Dec 2020 00:29:57 GMT  
		Size: 306.5 KB (306466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7f3a967c907bfe4aeb896ba6da80cfaf9bce19fcb39b51a6378b00596760d`  
		Last Modified: Wed, 13 Jan 2021 21:47:50 GMT  
		Size: 19.5 MB (19486049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.28`

```console
$ docker pull traefik@sha256:998fc0cce3df0fe066005d6e94a7fa8b20749155fb54b4ebd1603e039b842feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.28` - linux; amd64

```console
$ docker pull traefik@sha256:154e065982592220c9355925d9e60348eec6850418754ee76840f83501341b00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21553283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d67ddf1c8b647742ebb1ea0d3edb163dff028640b772832fa325b6b7df830f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:48:11 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:48:11 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 22:29:46 GMT
COPY file:94b9997cc55c7732c9fc173c119f980e4a38eba20b96a90170a3d7fade75f0eb in / 
# Wed, 13 Jan 2021 22:29:47 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:47 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 22:29:47 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 22:29:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:79de75e85675fa9abbac17b57205d3e0dfcf2bd2fc4cbc194f2aaf917435425e`  
		Last Modified: Thu, 17 Dec 2020 00:49:17 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e925284bb6370a549da51637ed98a8e574317473e082cc4be745d87327c7f`  
		Last Modified: Thu, 17 Dec 2020 00:49:18 GMT  
		Size: 306.4 KB (306411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81848bd29c493bb51f93a0bf98cf3958436af2128b6890d7a28a35b7dfc352c0`  
		Last Modified: Wed, 13 Jan 2021 22:30:48 GMT  
		Size: 21.1 MB (21116000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.28` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2f69dff9f3e67a011f08fc6a59fc3f72aa26533b5b9c8cd127e1f90948cbaf09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20205544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da195dbaa64e13483787db1f21a4e602751bd363ac5c6e594e5e17c1f2420aec`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:26:48 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:57:06 GMT
COPY file:3d9c1552db5b4c73ac7fe21268eeb20506f000d2e59d7be76697f45a50d32c64 in / 
# Wed, 13 Jan 2021 21:57:07 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:57:08 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:57:09 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:57:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc6fb65827756c9d95005162623d443b2bd3e445269bcb1a7006e080726d3c`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 306.5 KB (306458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0280c8ba5c59856146b5130ce0c0eb8b83b9dcc2dea1d69991723680815054f`  
		Last Modified: Wed, 13 Jan 2021 21:58:11 GMT  
		Size: 19.8 MB (19768213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.28` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:468570d210f86c4366e666dac62c34b3054c230ee0b4d61c36e37ed276550b39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fff7cc610524cb77e4767eb66f534053cc0f45853e096fb250937594f9913d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:27:58 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:46:55 GMT
COPY file:6bab4a8fc3d272fc29bc5ff42634cb12785fea9e23b0cf50f077702217bb6c03 in / 
# Wed, 13 Jan 2021 21:46:56 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:56 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:46:57 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:46:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c32c03119dbb32c844511340cb40a21ba5a56b90862cf603dec2e49cf5ab20d`  
		Last Modified: Thu, 17 Dec 2020 00:29:57 GMT  
		Size: 306.5 KB (306466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7f3a967c907bfe4aeb896ba6da80cfaf9bce19fcb39b51a6378b00596760d`  
		Last Modified: Wed, 13 Jan 2021 21:47:50 GMT  
		Size: 19.5 MB (19486049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.28-alpine`

```console
$ docker pull traefik@sha256:d232a757f6c487484b3640973fbb0287e747e6b357bc1dc75faa07b26da14a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.28-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:cb19d2e6f6575fb121eb2181cbd50f783c1995bf515cba8c7bbab7d9b6859949
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24603200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ecef4edf395a65a22e7b3c46ec4b16c869c1a5386a1ea0305132dc68266f04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 22:29:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 22:29:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 22:29:27 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 22:29:28 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 22:29:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8923725f26216ece246718b634aabb038e3ba78292d388ebb7350cc0d89ba1`  
		Last Modified: Wed, 13 Jan 2021 22:30:25 GMT  
		Size: 21.1 MB (21116271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8abe3b22d27fbf46de589e10d21107bd248a725e59317b3fc6a78a83e9c940`  
		Last Modified: Wed, 13 Jan 2021 22:30:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.28-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:198e33555ab98a4ea7b448b1f818b9663ab2f8fe98f0966543390a711e55692d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23064299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92898625b48315d465f9a4d3ad8e32c8b224bb4617bff335d0840bbd9ce1aced`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:56:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:56:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:56:48 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:56:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:56:49 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:56:49 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102471939d830c2c1e2668e0dd48049fc6ce2f332ead14922e8a55086f8816ef`  
		Last Modified: Wed, 13 Jan 2021 21:57:48 GMT  
		Size: 19.8 MB (19768260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a399e8ce2234a61da5e35bf382eefe32e24435b8c5805b773299d16a01b022`  
		Last Modified: Wed, 13 Jan 2021 21:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.28-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a144e4ba9554f68e6903986ca95090991e87d3c7a3e45809bfd602a5bda85a3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22884874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c65bf1525b68d03c1cc5d512338cf2608b5742b1e06e6ea57c492e61afee7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:46:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:46:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:46:39 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:46:41 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:46:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50dc3ca8b514cac3bfbf2a6303d6be654d1a94f584f6f24d4e62522b80bd36b`  
		Last Modified: Wed, 13 Jan 2021 21:47:33 GMT  
		Size: 19.5 MB (19486044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4205a3b9bbaa8f65f3bd5780aeb6e4cc761d5f7d6de7cb70588b41ed018c72`  
		Last Modified: Wed, 13 Jan 2021 21:47:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.28-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8f2b9d477c5d31806d427f5dad762d9f448c131bb284641f3977b914e655afd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:1.7.28-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:91b9a8ca83df9afc2b41003518d4b4f9d8e8a21f77880fd74d543670c7ab4da9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2466262882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962de1a7e3fc419a74eb2ea94e4c40359d9f53a93caec6bd1e61f1944ccf282`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Jan 2021 01:16:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 14 Jan 2021 01:16:24 GMT
EXPOSE 80
# Thu, 14 Jan 2021 01:16:25 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Jan 2021 01:16:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84697de3c7d0310176f36e2fe57e5688d23e486eb5b5febf6dbf860e763d1750`  
		Last Modified: Thu, 14 Jan 2021 01:17:09 GMT  
		Size: 30.5 MB (30486249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069ca4204690196a12b1d26a1b7d9b54c2d8fc7db082a3a4a9e21bfdf55d63d1`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaebdd4a9fa6db73d7167e0d944af020e0ddfe54da3ed92807a14054a53d669`  
		Last Modified: Thu, 14 Jan 2021 01:17:01 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454fe39b046d9fedbd9e0b3f698556592463406933b790b272dd909d5bd90d53`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:d232a757f6c487484b3640973fbb0287e747e6b357bc1dc75faa07b26da14a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:cb19d2e6f6575fb121eb2181cbd50f783c1995bf515cba8c7bbab7d9b6859949
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24603200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ecef4edf395a65a22e7b3c46ec4b16c869c1a5386a1ea0305132dc68266f04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 22:29:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 22:29:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 22:29:27 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 22:29:28 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 22:29:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8923725f26216ece246718b634aabb038e3ba78292d388ebb7350cc0d89ba1`  
		Last Modified: Wed, 13 Jan 2021 22:30:25 GMT  
		Size: 21.1 MB (21116271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8abe3b22d27fbf46de589e10d21107bd248a725e59317b3fc6a78a83e9c940`  
		Last Modified: Wed, 13 Jan 2021 22:30:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:198e33555ab98a4ea7b448b1f818b9663ab2f8fe98f0966543390a711e55692d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23064299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92898625b48315d465f9a4d3ad8e32c8b224bb4617bff335d0840bbd9ce1aced`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:56:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:56:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:56:48 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:56:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:56:49 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:56:49 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102471939d830c2c1e2668e0dd48049fc6ce2f332ead14922e8a55086f8816ef`  
		Last Modified: Wed, 13 Jan 2021 21:57:48 GMT  
		Size: 19.8 MB (19768260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a399e8ce2234a61da5e35bf382eefe32e24435b8c5805b773299d16a01b022`  
		Last Modified: Wed, 13 Jan 2021 21:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a144e4ba9554f68e6903986ca95090991e87d3c7a3e45809bfd602a5bda85a3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22884874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c65bf1525b68d03c1cc5d512338cf2608b5742b1e06e6ea57c492e61afee7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:46:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:46:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:46:39 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:46:41 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:46:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50dc3ca8b514cac3bfbf2a6303d6be654d1a94f584f6f24d4e62522b80bd36b`  
		Last Modified: Wed, 13 Jan 2021 21:47:33 GMT  
		Size: 19.5 MB (19486044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4205a3b9bbaa8f65f3bd5780aeb6e4cc761d5f7d6de7cb70588b41ed018c72`  
		Last Modified: Wed, 13 Jan 2021 21:47:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8f2b9d477c5d31806d427f5dad762d9f448c131bb284641f3977b914e655afd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:91b9a8ca83df9afc2b41003518d4b4f9d8e8a21f77880fd74d543670c7ab4da9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2466262882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962de1a7e3fc419a74eb2ea94e4c40359d9f53a93caec6bd1e61f1944ccf282`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Jan 2021 01:16:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 14 Jan 2021 01:16:24 GMT
EXPOSE 80
# Thu, 14 Jan 2021 01:16:25 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Jan 2021 01:16:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84697de3c7d0310176f36e2fe57e5688d23e486eb5b5febf6dbf860e763d1750`  
		Last Modified: Thu, 14 Jan 2021 01:17:09 GMT  
		Size: 30.5 MB (30486249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069ca4204690196a12b1d26a1b7d9b54c2d8fc7db082a3a4a9e21bfdf55d63d1`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaebdd4a9fa6db73d7167e0d944af020e0ddfe54da3ed92807a14054a53d669`  
		Last Modified: Thu, 14 Jan 2021 01:17:01 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454fe39b046d9fedbd9e0b3f698556592463406933b790b272dd909d5bd90d53`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3`

```console
$ docker pull traefik@sha256:0181e35c5af98f7f30fb391f91a6dbd281a90d7cf971e9909e26afd4ea923251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.3` - linux; amd64

```console
$ docker pull traefik@sha256:0aca29bb8e51aa69569b15b8b7f08328e6957cbec201dd532304b3329e5a82a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28387061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb0268e5b5fb0a4a9cb3f9e1d559dcc034cd9290b4faea2b03cd50f05042bd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Jan 2021 01:29:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Jan 2021 01:29:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Jan 2021 01:29:57 GMT
EXPOSE 80
# Tue, 12 Jan 2021 01:29:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 01:29:58 GMT
CMD ["traefik"]
# Tue, 12 Jan 2021 01:29:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00390834f324ba7030874c57968d6d7ee2f354e377a5bf938933ee1d39ce6abb`  
		Last Modified: Tue, 12 Jan 2021 01:30:53 GMT  
		Size: 24.9 MB (24900132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f159f39400907c1a2cf02624898430f0de90f3a8c7852b361029222623263`  
		Last Modified: Tue, 12 Jan 2021 01:30:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:866e86d9fed207750fcd6190a8378efdc4cf7378d7473adc7cefd1c47191659b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26482921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d24aa2dc32fc8e97983f070a55ec25388b336c2abd8dc31a1989b6e40c48dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:52 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:54 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404789ba4d57d5ebd3b9e346ab72911d9cda4e7f9395248ea5bf3bdd24e42949`  
		Last Modified: Mon, 11 Jan 2021 23:57:59 GMT  
		Size: 23.2 MB (23186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa14f62f5fc51679fe0d4c53102854dcfec037295c4ede9af9dbb4ecfe545a0`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a514d1067beb769fd25480cba0ffc0bd2aa5f44a004f9d33dc0465c3db9f5c3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26111594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24230cfd873ab4443c7220976542b2f075654cae3e8fccbaac8566b2cb4859`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:50 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:52 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb41b44f2a7a3f798996c121379f863b52ffee788ba79ada6d2cbe591a1153`  
		Last Modified: Mon, 11 Jan 2021 23:57:48 GMT  
		Size: 22.7 MB (22712763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fcc3d290ad4bbced9b6b0286aa15edb6d4b398deda5bb13fa7ce6f4b9013a`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3.7`

```console
$ docker pull traefik@sha256:0181e35c5af98f7f30fb391f91a6dbd281a90d7cf971e9909e26afd4ea923251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.3.7` - linux; amd64

```console
$ docker pull traefik@sha256:0aca29bb8e51aa69569b15b8b7f08328e6957cbec201dd532304b3329e5a82a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28387061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb0268e5b5fb0a4a9cb3f9e1d559dcc034cd9290b4faea2b03cd50f05042bd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Jan 2021 01:29:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Jan 2021 01:29:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Jan 2021 01:29:57 GMT
EXPOSE 80
# Tue, 12 Jan 2021 01:29:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 01:29:58 GMT
CMD ["traefik"]
# Tue, 12 Jan 2021 01:29:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00390834f324ba7030874c57968d6d7ee2f354e377a5bf938933ee1d39ce6abb`  
		Last Modified: Tue, 12 Jan 2021 01:30:53 GMT  
		Size: 24.9 MB (24900132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f159f39400907c1a2cf02624898430f0de90f3a8c7852b361029222623263`  
		Last Modified: Tue, 12 Jan 2021 01:30:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:866e86d9fed207750fcd6190a8378efdc4cf7378d7473adc7cefd1c47191659b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26482921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d24aa2dc32fc8e97983f070a55ec25388b336c2abd8dc31a1989b6e40c48dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:52 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:54 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404789ba4d57d5ebd3b9e346ab72911d9cda4e7f9395248ea5bf3bdd24e42949`  
		Last Modified: Mon, 11 Jan 2021 23:57:59 GMT  
		Size: 23.2 MB (23186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa14f62f5fc51679fe0d4c53102854dcfec037295c4ede9af9dbb4ecfe545a0`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.3.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a514d1067beb769fd25480cba0ffc0bd2aa5f44a004f9d33dc0465c3db9f5c3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26111594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24230cfd873ab4443c7220976542b2f075654cae3e8fccbaac8566b2cb4859`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:50 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:52 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb41b44f2a7a3f798996c121379f863b52ffee788ba79ada6d2cbe591a1153`  
		Last Modified: Mon, 11 Jan 2021 23:57:48 GMT  
		Size: 22.7 MB (22712763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fcc3d290ad4bbced9b6b0286aa15edb6d4b398deda5bb13fa7ce6f4b9013a`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d5aace4a65d4ac287ee01df27a8a08a303dc1c1ab3b8c4dd5ee845cf5ab47f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:2.3.7-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:40f8fe38de1fc5b8677764a6d5835c2f91a089348a958efe44032c49310e0ea5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470404577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0011bc7c1cd89741d499d69fe62ed8c50b251d90bb3dd01350d6f945dace6e89`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:15:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:15:37 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:15:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:15:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6c5b0a97b9671b4e08aa00ddb88caedc356102697742d6f378e5af7994ed05`  
		Last Modified: Wed, 13 Jan 2021 13:19:00 GMT  
		Size: 34.6 MB (34627945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275937a63dff0407d503768537bd0fefd61c0e7484713f860a115caf944feaa7`  
		Last Modified: Wed, 13 Jan 2021 13:18:19 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea03fb9da7a541e90efca3d37faffbacf68c1b876bc44ebbd5c67c5f275d35`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee034dc2f4eaff9d6bf00b65b0f122e98cb38e86c8b2afa3256d0c8207de0e5`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d5aace4a65d4ac287ee01df27a8a08a303dc1c1ab3b8c4dd5ee845cf5ab47f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:2.3-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:40f8fe38de1fc5b8677764a6d5835c2f91a089348a958efe44032c49310e0ea5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470404577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0011bc7c1cd89741d499d69fe62ed8c50b251d90bb3dd01350d6f945dace6e89`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:15:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:15:37 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:15:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:15:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6c5b0a97b9671b4e08aa00ddb88caedc356102697742d6f378e5af7994ed05`  
		Last Modified: Wed, 13 Jan 2021 13:19:00 GMT  
		Size: 34.6 MB (34627945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275937a63dff0407d503768537bd0fefd61c0e7484713f860a115caf944feaa7`  
		Last Modified: Wed, 13 Jan 2021 13:18:19 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea03fb9da7a541e90efca3d37faffbacf68c1b876bc44ebbd5c67c5f275d35`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee034dc2f4eaff9d6bf00b65b0f122e98cb38e86c8b2afa3256d0c8207de0e5`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4`

```console
$ docker pull traefik@sha256:13d613be07961b1bf97a5e4826a20c01c312367495f85385c4750a9085e7bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.4` - linux; amd64

```console
$ docker pull traefik@sha256:42401810722b981bee516647dab6028688dd2b3246f4e56a7d5309e6806b21b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29074781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c19b1291a4277be960aaca74928af3dfb9313bb8b463e9d1ec842be6a9f228e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 09:49:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 09:49:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 09:49:30 GMT
EXPOSE 80
# Wed, 13 Jan 2021 09:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 09:49:30 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 09:49:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16bf8c9b9a1f7cc43c306353cd2ddfa5de3c14db5b512efa1bfa1bb01998fb8`  
		Last Modified: Wed, 13 Jan 2021 09:50:11 GMT  
		Size: 25.6 MB (25587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640e96d3797b9f24dd02e7fddfc5726478b3854e303ad398da8289e196e2b392`  
		Last Modified: Wed, 13 Jan 2021 09:50:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2943b6dbc5cce7b549c88f208e3eec0736d4f305e6f2eb45973e4d31412253de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27111407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5575a2605168aea584cde15a4395f18c45b2685e5692cdd6b2f538b52bfb3cfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 01:02:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 01:02:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 01:02:15 GMT
EXPOSE 80
# Wed, 13 Jan 2021 01:02:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 01:02:18 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 01:02:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787df9c7681db127330ef3ffc8d6f21800c11f0ada5cb694d614cbfefbdd096a`  
		Last Modified: Wed, 13 Jan 2021 01:03:15 GMT  
		Size: 23.8 MB (23815368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e09316753dc27b18cafd3e135ab0a5ed07abcad6a26f04ad1800e4a693d87a5`  
		Last Modified: Wed, 13 Jan 2021 01:03:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:148ff9dd39b58ca532d96369af3b2cda1b9a1865dabd6ceeb5253e329cf40c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26736606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0524ae4495e503c237291bd7e5cf898f40e2a0cb36c626b43151f885f308731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 06:09:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 06:09:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 06:09:23 GMT
EXPOSE 80
# Wed, 13 Jan 2021 06:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 06:09:24 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 06:09:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5274a1d1e4be5ba614ecb3a12c06bffef192457ed200d9e7f05e7b0f7860a8`  
		Last Modified: Wed, 13 Jan 2021 06:10:16 GMT  
		Size: 23.3 MB (23337776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240f3cfce0cfe96476300fc4562f75c89fe8ad624aa64a8db56edfa7c241bfcb`  
		Last Modified: Wed, 13 Jan 2021 06:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4.0-rc2`

```console
$ docker pull traefik@sha256:13d613be07961b1bf97a5e4826a20c01c312367495f85385c4750a9085e7bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.4.0-rc2` - linux; amd64

```console
$ docker pull traefik@sha256:42401810722b981bee516647dab6028688dd2b3246f4e56a7d5309e6806b21b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29074781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c19b1291a4277be960aaca74928af3dfb9313bb8b463e9d1ec842be6a9f228e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 09:49:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 09:49:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 09:49:30 GMT
EXPOSE 80
# Wed, 13 Jan 2021 09:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 09:49:30 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 09:49:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16bf8c9b9a1f7cc43c306353cd2ddfa5de3c14db5b512efa1bfa1bb01998fb8`  
		Last Modified: Wed, 13 Jan 2021 09:50:11 GMT  
		Size: 25.6 MB (25587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640e96d3797b9f24dd02e7fddfc5726478b3854e303ad398da8289e196e2b392`  
		Last Modified: Wed, 13 Jan 2021 09:50:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4.0-rc2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2943b6dbc5cce7b549c88f208e3eec0736d4f305e6f2eb45973e4d31412253de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27111407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5575a2605168aea584cde15a4395f18c45b2685e5692cdd6b2f538b52bfb3cfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 01:02:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 01:02:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 01:02:15 GMT
EXPOSE 80
# Wed, 13 Jan 2021 01:02:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 01:02:18 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 01:02:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787df9c7681db127330ef3ffc8d6f21800c11f0ada5cb694d614cbfefbdd096a`  
		Last Modified: Wed, 13 Jan 2021 01:03:15 GMT  
		Size: 23.8 MB (23815368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e09316753dc27b18cafd3e135ab0a5ed07abcad6a26f04ad1800e4a693d87a5`  
		Last Modified: Wed, 13 Jan 2021 01:03:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.4.0-rc2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:148ff9dd39b58ca532d96369af3b2cda1b9a1865dabd6ceeb5253e329cf40c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26736606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0524ae4495e503c237291bd7e5cf898f40e2a0cb36c626b43151f885f308731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 06:09:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 06:09:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 06:09:23 GMT
EXPOSE 80
# Wed, 13 Jan 2021 06:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 06:09:24 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 06:09:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5274a1d1e4be5ba614ecb3a12c06bffef192457ed200d9e7f05e7b0f7860a8`  
		Last Modified: Wed, 13 Jan 2021 06:10:16 GMT  
		Size: 23.3 MB (23337776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240f3cfce0cfe96476300fc4562f75c89fe8ad624aa64a8db56edfa7c241bfcb`  
		Last Modified: Wed, 13 Jan 2021 06:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4.0-rc2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b3997e6fd462c42a96d11e7c1d78eb9d873d15f52fc726d20608a92bd06f853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:2.4.0-rc2-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:efcce1a8b23e8de5d1aeb5e445ea5f114140e9401967d4a36d10022399c89708
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471100192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46e43162aa7035ce3b0a895000a66777d2f050a80c29f9d706c97a52fb4759d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:14:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:14:31 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:14:32 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116638bca58c127c2ec8da559c11513038fa82eea012d15b0fc6041ca676750`  
		Last Modified: Wed, 13 Jan 2021 13:17:58 GMT  
		Size: 35.3 MB (35323488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8638b72f94f87f9242a92efb9242270c5cd406775e12ddedc1dd4da5fa1fea5`  
		Last Modified: Wed, 13 Jan 2021 13:17:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88821eec1273c142fbde11d869ceb0e5bd9ce94842c40f27b93f5dd0823d78ab`  
		Last Modified: Wed, 13 Jan 2021 13:17:24 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e03b07855cc717b7969b2868a7c0e581f38d8efc5c19a0bdc177824decae27`  
		Last Modified: Wed, 13 Jan 2021 13:17:20 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b3997e6fd462c42a96d11e7c1d78eb9d873d15f52fc726d20608a92bd06f853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:2.4-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:efcce1a8b23e8de5d1aeb5e445ea5f114140e9401967d4a36d10022399c89708
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471100192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46e43162aa7035ce3b0a895000a66777d2f050a80c29f9d706c97a52fb4759d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:14:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:14:31 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:14:32 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116638bca58c127c2ec8da559c11513038fa82eea012d15b0fc6041ca676750`  
		Last Modified: Wed, 13 Jan 2021 13:17:58 GMT  
		Size: 35.3 MB (35323488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8638b72f94f87f9242a92efb9242270c5cd406775e12ddedc1dd4da5fa1fea5`  
		Last Modified: Wed, 13 Jan 2021 13:17:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88821eec1273c142fbde11d869ceb0e5bd9ce94842c40f27b93f5dd0823d78ab`  
		Last Modified: Wed, 13 Jan 2021 13:17:24 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e03b07855cc717b7969b2868a7c0e581f38d8efc5c19a0bdc177824decae27`  
		Last Modified: Wed, 13 Jan 2021 13:17:20 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:0181e35c5af98f7f30fb391f91a6dbd281a90d7cf971e9909e26afd4ea923251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:0aca29bb8e51aa69569b15b8b7f08328e6957cbec201dd532304b3329e5a82a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28387061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb0268e5b5fb0a4a9cb3f9e1d559dcc034cd9290b4faea2b03cd50f05042bd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Jan 2021 01:29:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Jan 2021 01:29:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Jan 2021 01:29:57 GMT
EXPOSE 80
# Tue, 12 Jan 2021 01:29:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 01:29:58 GMT
CMD ["traefik"]
# Tue, 12 Jan 2021 01:29:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00390834f324ba7030874c57968d6d7ee2f354e377a5bf938933ee1d39ce6abb`  
		Last Modified: Tue, 12 Jan 2021 01:30:53 GMT  
		Size: 24.9 MB (24900132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f159f39400907c1a2cf02624898430f0de90f3a8c7852b361029222623263`  
		Last Modified: Tue, 12 Jan 2021 01:30:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:866e86d9fed207750fcd6190a8378efdc4cf7378d7473adc7cefd1c47191659b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26482921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d24aa2dc32fc8e97983f070a55ec25388b336c2abd8dc31a1989b6e40c48dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:52 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:54 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404789ba4d57d5ebd3b9e346ab72911d9cda4e7f9395248ea5bf3bdd24e42949`  
		Last Modified: Mon, 11 Jan 2021 23:57:59 GMT  
		Size: 23.2 MB (23186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa14f62f5fc51679fe0d4c53102854dcfec037295c4ede9af9dbb4ecfe545a0`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a514d1067beb769fd25480cba0ffc0bd2aa5f44a004f9d33dc0465c3db9f5c3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26111594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24230cfd873ab4443c7220976542b2f075654cae3e8fccbaac8566b2cb4859`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:50 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:52 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb41b44f2a7a3f798996c121379f863b52ffee788ba79ada6d2cbe591a1153`  
		Last Modified: Mon, 11 Jan 2021 23:57:48 GMT  
		Size: 22.7 MB (22712763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fcc3d290ad4bbced9b6b0286aa15edb6d4b398deda5bb13fa7ce6f4b9013a`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:livarot`

```console
$ docker pull traefik@sha256:13d613be07961b1bf97a5e4826a20c01c312367495f85385c4750a9085e7bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:livarot` - linux; amd64

```console
$ docker pull traefik@sha256:42401810722b981bee516647dab6028688dd2b3246f4e56a7d5309e6806b21b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29074781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c19b1291a4277be960aaca74928af3dfb9313bb8b463e9d1ec842be6a9f228e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 09:49:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 09:49:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 09:49:30 GMT
EXPOSE 80
# Wed, 13 Jan 2021 09:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 09:49:30 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 09:49:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16bf8c9b9a1f7cc43c306353cd2ddfa5de3c14db5b512efa1bfa1bb01998fb8`  
		Last Modified: Wed, 13 Jan 2021 09:50:11 GMT  
		Size: 25.6 MB (25587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640e96d3797b9f24dd02e7fddfc5726478b3854e303ad398da8289e196e2b392`  
		Last Modified: Wed, 13 Jan 2021 09:50:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2943b6dbc5cce7b549c88f208e3eec0736d4f305e6f2eb45973e4d31412253de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27111407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5575a2605168aea584cde15a4395f18c45b2685e5692cdd6b2f538b52bfb3cfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 01:02:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 01:02:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 01:02:15 GMT
EXPOSE 80
# Wed, 13 Jan 2021 01:02:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 01:02:18 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 01:02:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787df9c7681db127330ef3ffc8d6f21800c11f0ada5cb694d614cbfefbdd096a`  
		Last Modified: Wed, 13 Jan 2021 01:03:15 GMT  
		Size: 23.8 MB (23815368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e09316753dc27b18cafd3e135ab0a5ed07abcad6a26f04ad1800e4a693d87a5`  
		Last Modified: Wed, 13 Jan 2021 01:03:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:livarot` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:148ff9dd39b58ca532d96369af3b2cda1b9a1865dabd6ceeb5253e329cf40c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26736606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0524ae4495e503c237291bd7e5cf898f40e2a0cb36c626b43151f885f308731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 06:09:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 06:09:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 06:09:23 GMT
EXPOSE 80
# Wed, 13 Jan 2021 06:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 06:09:24 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 06:09:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5274a1d1e4be5ba614ecb3a12c06bffef192457ed200d9e7f05e7b0f7860a8`  
		Last Modified: Wed, 13 Jan 2021 06:10:16 GMT  
		Size: 23.3 MB (23337776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240f3cfce0cfe96476300fc4562f75c89fe8ad624aa64a8db56edfa7c241bfcb`  
		Last Modified: Wed, 13 Jan 2021 06:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:livarot-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b3997e6fd462c42a96d11e7c1d78eb9d873d15f52fc726d20608a92bd06f853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:livarot-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:efcce1a8b23e8de5d1aeb5e445ea5f114140e9401967d4a36d10022399c89708
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471100192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46e43162aa7035ce3b0a895000a66777d2f050a80c29f9d706c97a52fb4759d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:14:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:14:31 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:14:32 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116638bca58c127c2ec8da559c11513038fa82eea012d15b0fc6041ca676750`  
		Last Modified: Wed, 13 Jan 2021 13:17:58 GMT  
		Size: 35.3 MB (35323488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8638b72f94f87f9242a92efb9242270c5cd406775e12ddedc1dd4da5fa1fea5`  
		Last Modified: Wed, 13 Jan 2021 13:17:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88821eec1273c142fbde11d869ceb0e5bd9ce94842c40f27b93f5dd0823d78ab`  
		Last Modified: Wed, 13 Jan 2021 13:17:24 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e03b07855cc717b7969b2868a7c0e581f38d8efc5c19a0bdc177824decae27`  
		Last Modified: Wed, 13 Jan 2021 13:17:20 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:998fc0cce3df0fe066005d6e94a7fa8b20749155fb54b4ebd1603e039b842feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:154e065982592220c9355925d9e60348eec6850418754ee76840f83501341b00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21553283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d67ddf1c8b647742ebb1ea0d3edb163dff028640b772832fa325b6b7df830f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:48:11 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:48:11 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 22:29:46 GMT
COPY file:94b9997cc55c7732c9fc173c119f980e4a38eba20b96a90170a3d7fade75f0eb in / 
# Wed, 13 Jan 2021 22:29:47 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:47 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 22:29:47 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 22:29:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:79de75e85675fa9abbac17b57205d3e0dfcf2bd2fc4cbc194f2aaf917435425e`  
		Last Modified: Thu, 17 Dec 2020 00:49:17 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e925284bb6370a549da51637ed98a8e574317473e082cc4be745d87327c7f`  
		Last Modified: Thu, 17 Dec 2020 00:49:18 GMT  
		Size: 306.4 KB (306411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81848bd29c493bb51f93a0bf98cf3958436af2128b6890d7a28a35b7dfc352c0`  
		Last Modified: Wed, 13 Jan 2021 22:30:48 GMT  
		Size: 21.1 MB (21116000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2f69dff9f3e67a011f08fc6a59fc3f72aa26533b5b9c8cd127e1f90948cbaf09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20205544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da195dbaa64e13483787db1f21a4e602751bd363ac5c6e594e5e17c1f2420aec`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:26:48 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:57:06 GMT
COPY file:3d9c1552db5b4c73ac7fe21268eeb20506f000d2e59d7be76697f45a50d32c64 in / 
# Wed, 13 Jan 2021 21:57:07 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:57:08 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:57:09 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:57:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc6fb65827756c9d95005162623d443b2bd3e445269bcb1a7006e080726d3c`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 306.5 KB (306458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0280c8ba5c59856146b5130ce0c0eb8b83b9dcc2dea1d69991723680815054f`  
		Last Modified: Wed, 13 Jan 2021 21:58:11 GMT  
		Size: 19.8 MB (19768213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:468570d210f86c4366e666dac62c34b3054c230ee0b4d61c36e37ed276550b39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fff7cc610524cb77e4767eb66f534053cc0f45853e096fb250937594f9913d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:27:58 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:46:55 GMT
COPY file:6bab4a8fc3d272fc29bc5ff42634cb12785fea9e23b0cf50f077702217bb6c03 in / 
# Wed, 13 Jan 2021 21:46:56 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:56 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:46:57 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:46:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c32c03119dbb32c844511340cb40a21ba5a56b90862cf603dec2e49cf5ab20d`  
		Last Modified: Thu, 17 Dec 2020 00:29:57 GMT  
		Size: 306.5 KB (306466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7f3a967c907bfe4aeb896ba6da80cfaf9bce19fcb39b51a6378b00596760d`  
		Last Modified: Wed, 13 Jan 2021 21:47:50 GMT  
		Size: 19.5 MB (19486049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:d232a757f6c487484b3640973fbb0287e747e6b357bc1dc75faa07b26da14a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:cb19d2e6f6575fb121eb2181cbd50f783c1995bf515cba8c7bbab7d9b6859949
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24603200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ecef4edf395a65a22e7b3c46ec4b16c869c1a5386a1ea0305132dc68266f04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 22:29:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 22:29:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 22:29:27 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 22:29:28 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 22:29:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8923725f26216ece246718b634aabb038e3ba78292d388ebb7350cc0d89ba1`  
		Last Modified: Wed, 13 Jan 2021 22:30:25 GMT  
		Size: 21.1 MB (21116271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8abe3b22d27fbf46de589e10d21107bd248a725e59317b3fc6a78a83e9c940`  
		Last Modified: Wed, 13 Jan 2021 22:30:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:198e33555ab98a4ea7b448b1f818b9663ab2f8fe98f0966543390a711e55692d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23064299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92898625b48315d465f9a4d3ad8e32c8b224bb4617bff335d0840bbd9ce1aced`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:56:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:56:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:56:48 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:56:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:56:49 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:56:49 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102471939d830c2c1e2668e0dd48049fc6ce2f332ead14922e8a55086f8816ef`  
		Last Modified: Wed, 13 Jan 2021 21:57:48 GMT  
		Size: 19.8 MB (19768260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a399e8ce2234a61da5e35bf382eefe32e24435b8c5805b773299d16a01b022`  
		Last Modified: Wed, 13 Jan 2021 21:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a144e4ba9554f68e6903986ca95090991e87d3c7a3e45809bfd602a5bda85a3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22884874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c65bf1525b68d03c1cc5d512338cf2608b5742b1e06e6ea57c492e61afee7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:46:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:46:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:46:39 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:46:41 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:46:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50dc3ca8b514cac3bfbf2a6303d6be654d1a94f584f6f24d4e62522b80bd36b`  
		Last Modified: Wed, 13 Jan 2021 21:47:33 GMT  
		Size: 19.5 MB (19486044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4205a3b9bbaa8f65f3bd5780aeb6e4cc761d5f7d6de7cb70588b41ed018c72`  
		Last Modified: Wed, 13 Jan 2021 21:47:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8f2b9d477c5d31806d427f5dad762d9f448c131bb284641f3977b914e655afd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:91b9a8ca83df9afc2b41003518d4b4f9d8e8a21f77880fd74d543670c7ab4da9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2466262882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962de1a7e3fc419a74eb2ea94e4c40359d9f53a93caec6bd1e61f1944ccf282`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Jan 2021 01:16:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 14 Jan 2021 01:16:24 GMT
EXPOSE 80
# Thu, 14 Jan 2021 01:16:25 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Jan 2021 01:16:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84697de3c7d0310176f36e2fe57e5688d23e486eb5b5febf6dbf860e763d1750`  
		Last Modified: Thu, 14 Jan 2021 01:17:09 GMT  
		Size: 30.5 MB (30486249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069ca4204690196a12b1d26a1b7d9b54c2d8fc7db082a3a4a9e21bfdf55d63d1`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaebdd4a9fa6db73d7167e0d944af020e0ddfe54da3ed92807a14054a53d669`  
		Last Modified: Thu, 14 Jan 2021 01:17:01 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454fe39b046d9fedbd9e0b3f698556592463406933b790b272dd909d5bd90d53`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:picodon`

```console
$ docker pull traefik@sha256:0181e35c5af98f7f30fb391f91a6dbd281a90d7cf971e9909e26afd4ea923251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:picodon` - linux; amd64

```console
$ docker pull traefik@sha256:0aca29bb8e51aa69569b15b8b7f08328e6957cbec201dd532304b3329e5a82a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28387061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb0268e5b5fb0a4a9cb3f9e1d559dcc034cd9290b4faea2b03cd50f05042bd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Jan 2021 01:29:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Jan 2021 01:29:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Jan 2021 01:29:57 GMT
EXPOSE 80
# Tue, 12 Jan 2021 01:29:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 01:29:58 GMT
CMD ["traefik"]
# Tue, 12 Jan 2021 01:29:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00390834f324ba7030874c57968d6d7ee2f354e377a5bf938933ee1d39ce6abb`  
		Last Modified: Tue, 12 Jan 2021 01:30:53 GMT  
		Size: 24.9 MB (24900132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f159f39400907c1a2cf02624898430f0de90f3a8c7852b361029222623263`  
		Last Modified: Tue, 12 Jan 2021 01:30:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:picodon` - linux; arm variant v6

```console
$ docker pull traefik@sha256:866e86d9fed207750fcd6190a8378efdc4cf7378d7473adc7cefd1c47191659b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26482921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d24aa2dc32fc8e97983f070a55ec25388b336c2abd8dc31a1989b6e40c48dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:52 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:54 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404789ba4d57d5ebd3b9e346ab72911d9cda4e7f9395248ea5bf3bdd24e42949`  
		Last Modified: Mon, 11 Jan 2021 23:57:59 GMT  
		Size: 23.2 MB (23186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa14f62f5fc51679fe0d4c53102854dcfec037295c4ede9af9dbb4ecfe545a0`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:picodon` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a514d1067beb769fd25480cba0ffc0bd2aa5f44a004f9d33dc0465c3db9f5c3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26111594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24230cfd873ab4443c7220976542b2f075654cae3e8fccbaac8566b2cb4859`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:50 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:52 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb41b44f2a7a3f798996c121379f863b52ffee788ba79ada6d2cbe591a1153`  
		Last Modified: Mon, 11 Jan 2021 23:57:48 GMT  
		Size: 22.7 MB (22712763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fcc3d290ad4bbced9b6b0286aa15edb6d4b398deda5bb13fa7ce6f4b9013a`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:picodon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d5aace4a65d4ac287ee01df27a8a08a303dc1c1ab3b8c4dd5ee845cf5ab47f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:picodon-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:40f8fe38de1fc5b8677764a6d5835c2f91a089348a958efe44032c49310e0ea5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470404577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0011bc7c1cd89741d499d69fe62ed8c50b251d90bb3dd01350d6f945dace6e89`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:15:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:15:37 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:15:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:15:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6c5b0a97b9671b4e08aa00ddb88caedc356102697742d6f378e5af7994ed05`  
		Last Modified: Wed, 13 Jan 2021 13:19:00 GMT  
		Size: 34.6 MB (34627945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275937a63dff0407d503768537bd0fefd61c0e7484713f860a115caf944feaa7`  
		Last Modified: Wed, 13 Jan 2021 13:18:19 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea03fb9da7a541e90efca3d37faffbacf68c1b876bc44ebbd5c67c5f275d35`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee034dc2f4eaff9d6bf00b65b0f122e98cb38e86c8b2afa3256d0c8207de0e5`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:998fc0cce3df0fe066005d6e94a7fa8b20749155fb54b4ebd1603e039b842feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:154e065982592220c9355925d9e60348eec6850418754ee76840f83501341b00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21553283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d67ddf1c8b647742ebb1ea0d3edb163dff028640b772832fa325b6b7df830f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:48:11 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:48:11 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 22:29:46 GMT
COPY file:94b9997cc55c7732c9fc173c119f980e4a38eba20b96a90170a3d7fade75f0eb in / 
# Wed, 13 Jan 2021 22:29:47 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:47 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 22:29:47 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 22:29:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:79de75e85675fa9abbac17b57205d3e0dfcf2bd2fc4cbc194f2aaf917435425e`  
		Last Modified: Thu, 17 Dec 2020 00:49:17 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e925284bb6370a549da51637ed98a8e574317473e082cc4be745d87327c7f`  
		Last Modified: Thu, 17 Dec 2020 00:49:18 GMT  
		Size: 306.4 KB (306411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81848bd29c493bb51f93a0bf98cf3958436af2128b6890d7a28a35b7dfc352c0`  
		Last Modified: Wed, 13 Jan 2021 22:30:48 GMT  
		Size: 21.1 MB (21116000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2f69dff9f3e67a011f08fc6a59fc3f72aa26533b5b9c8cd127e1f90948cbaf09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20205544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da195dbaa64e13483787db1f21a4e602751bd363ac5c6e594e5e17c1f2420aec`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:26:48 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:57:06 GMT
COPY file:3d9c1552db5b4c73ac7fe21268eeb20506f000d2e59d7be76697f45a50d32c64 in / 
# Wed, 13 Jan 2021 21:57:07 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:57:08 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:57:09 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:57:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc6fb65827756c9d95005162623d443b2bd3e445269bcb1a7006e080726d3c`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 306.5 KB (306458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0280c8ba5c59856146b5130ce0c0eb8b83b9dcc2dea1d69991723680815054f`  
		Last Modified: Wed, 13 Jan 2021 21:58:11 GMT  
		Size: 19.8 MB (19768213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:468570d210f86c4366e666dac62c34b3054c230ee0b4d61c36e37ed276550b39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fff7cc610524cb77e4767eb66f534053cc0f45853e096fb250937594f9913d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:27:58 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:46:55 GMT
COPY file:6bab4a8fc3d272fc29bc5ff42634cb12785fea9e23b0cf50f077702217bb6c03 in / 
# Wed, 13 Jan 2021 21:46:56 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:56 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:46:57 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:46:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c32c03119dbb32c844511340cb40a21ba5a56b90862cf603dec2e49cf5ab20d`  
		Last Modified: Thu, 17 Dec 2020 00:29:57 GMT  
		Size: 306.5 KB (306466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7f3a967c907bfe4aeb896ba6da80cfaf9bce19fcb39b51a6378b00596760d`  
		Last Modified: Wed, 13 Jan 2021 21:47:50 GMT  
		Size: 19.5 MB (19486049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.28`

```console
$ docker pull traefik@sha256:998fc0cce3df0fe066005d6e94a7fa8b20749155fb54b4ebd1603e039b842feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.28` - linux; amd64

```console
$ docker pull traefik@sha256:154e065982592220c9355925d9e60348eec6850418754ee76840f83501341b00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21553283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d67ddf1c8b647742ebb1ea0d3edb163dff028640b772832fa325b6b7df830f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:48:11 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:48:11 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 22:29:46 GMT
COPY file:94b9997cc55c7732c9fc173c119f980e4a38eba20b96a90170a3d7fade75f0eb in / 
# Wed, 13 Jan 2021 22:29:47 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:47 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 22:29:47 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 22:29:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:79de75e85675fa9abbac17b57205d3e0dfcf2bd2fc4cbc194f2aaf917435425e`  
		Last Modified: Thu, 17 Dec 2020 00:49:17 GMT  
		Size: 130.9 KB (130872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0e925284bb6370a549da51637ed98a8e574317473e082cc4be745d87327c7f`  
		Last Modified: Thu, 17 Dec 2020 00:49:18 GMT  
		Size: 306.4 KB (306411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81848bd29c493bb51f93a0bf98cf3958436af2128b6890d7a28a35b7dfc352c0`  
		Last Modified: Wed, 13 Jan 2021 22:30:48 GMT  
		Size: 21.1 MB (21116000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.28` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2f69dff9f3e67a011f08fc6a59fc3f72aa26533b5b9c8cd127e1f90948cbaf09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20205544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da195dbaa64e13483787db1f21a4e602751bd363ac5c6e594e5e17c1f2420aec`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:26:47 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:26:48 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:57:06 GMT
COPY file:3d9c1552db5b4c73ac7fe21268eeb20506f000d2e59d7be76697f45a50d32c64 in / 
# Wed, 13 Jan 2021 21:57:07 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:57:08 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:57:09 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:57:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:26c529e82b09c489524aa4f787754320793a95eb7aa7eaf306c517b76818ec25`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc6fb65827756c9d95005162623d443b2bd3e445269bcb1a7006e080726d3c`  
		Last Modified: Thu, 17 Dec 2020 00:28:41 GMT  
		Size: 306.5 KB (306458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0280c8ba5c59856146b5130ce0c0eb8b83b9dcc2dea1d69991723680815054f`  
		Last Modified: Wed, 13 Jan 2021 21:58:11 GMT  
		Size: 19.8 MB (19768213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.28` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:468570d210f86c4366e666dac62c34b3054c230ee0b4d61c36e37ed276550b39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fff7cc610524cb77e4767eb66f534053cc0f45853e096fb250937594f9913d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:27:56 GMT
COPY file:cd6264d9a7514a8fbc3eb7b400566d36178794d2b757959812cc3abc6f13a97b in /etc/ssl/certs/ 
# Thu, 17 Dec 2020 00:27:58 GMT
COPY dir:83da415af0ff24b3b9d10f857aa8c724a3bc93523f3e047b827e7554fe1f9e08 in /usr/share/ 
# Wed, 13 Jan 2021 21:46:55 GMT
COPY file:6bab4a8fc3d272fc29bc5ff42634cb12785fea9e23b0cf50f077702217bb6c03 in / 
# Wed, 13 Jan 2021 21:46:56 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:56 GMT
VOLUME [/tmp]
# Wed, 13 Jan 2021 21:46:57 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 21:46:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7dccf22d113d483cac839141f2028cbf6ac2e0c6aa4a1716c5e7b575b162028c`  
		Last Modified: Thu, 17 Dec 2020 00:29:55 GMT  
		Size: 130.9 KB (130873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c32c03119dbb32c844511340cb40a21ba5a56b90862cf603dec2e49cf5ab20d`  
		Last Modified: Thu, 17 Dec 2020 00:29:57 GMT  
		Size: 306.5 KB (306466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f7f3a967c907bfe4aeb896ba6da80cfaf9bce19fcb39b51a6378b00596760d`  
		Last Modified: Wed, 13 Jan 2021 21:47:50 GMT  
		Size: 19.5 MB (19486049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.28-alpine`

```console
$ docker pull traefik@sha256:d232a757f6c487484b3640973fbb0287e747e6b357bc1dc75faa07b26da14a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.28-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:cb19d2e6f6575fb121eb2181cbd50f783c1995bf515cba8c7bbab7d9b6859949
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24603200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ecef4edf395a65a22e7b3c46ec4b16c869c1a5386a1ea0305132dc68266f04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 22:29:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 22:29:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 22:29:27 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 22:29:28 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 22:29:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8923725f26216ece246718b634aabb038e3ba78292d388ebb7350cc0d89ba1`  
		Last Modified: Wed, 13 Jan 2021 22:30:25 GMT  
		Size: 21.1 MB (21116271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8abe3b22d27fbf46de589e10d21107bd248a725e59317b3fc6a78a83e9c940`  
		Last Modified: Wed, 13 Jan 2021 22:30:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.28-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:198e33555ab98a4ea7b448b1f818b9663ab2f8fe98f0966543390a711e55692d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23064299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92898625b48315d465f9a4d3ad8e32c8b224bb4617bff335d0840bbd9ce1aced`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:56:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:56:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:56:48 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:56:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:56:49 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:56:49 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102471939d830c2c1e2668e0dd48049fc6ce2f332ead14922e8a55086f8816ef`  
		Last Modified: Wed, 13 Jan 2021 21:57:48 GMT  
		Size: 19.8 MB (19768260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a399e8ce2234a61da5e35bf382eefe32e24435b8c5805b773299d16a01b022`  
		Last Modified: Wed, 13 Jan 2021 21:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.28-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a144e4ba9554f68e6903986ca95090991e87d3c7a3e45809bfd602a5bda85a3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22884874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c65bf1525b68d03c1cc5d512338cf2608b5742b1e06e6ea57c492e61afee7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:46:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:46:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:46:39 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:46:41 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:46:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50dc3ca8b514cac3bfbf2a6303d6be654d1a94f584f6f24d4e62522b80bd36b`  
		Last Modified: Wed, 13 Jan 2021 21:47:33 GMT  
		Size: 19.5 MB (19486044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4205a3b9bbaa8f65f3bd5780aeb6e4cc761d5f7d6de7cb70588b41ed018c72`  
		Last Modified: Wed, 13 Jan 2021 21:47:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.28-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8f2b9d477c5d31806d427f5dad762d9f448c131bb284641f3977b914e655afd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:v1.7.28-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:91b9a8ca83df9afc2b41003518d4b4f9d8e8a21f77880fd74d543670c7ab4da9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2466262882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962de1a7e3fc419a74eb2ea94e4c40359d9f53a93caec6bd1e61f1944ccf282`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Jan 2021 01:16:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 14 Jan 2021 01:16:24 GMT
EXPOSE 80
# Thu, 14 Jan 2021 01:16:25 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Jan 2021 01:16:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84697de3c7d0310176f36e2fe57e5688d23e486eb5b5febf6dbf860e763d1750`  
		Last Modified: Thu, 14 Jan 2021 01:17:09 GMT  
		Size: 30.5 MB (30486249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069ca4204690196a12b1d26a1b7d9b54c2d8fc7db082a3a4a9e21bfdf55d63d1`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaebdd4a9fa6db73d7167e0d944af020e0ddfe54da3ed92807a14054a53d669`  
		Last Modified: Thu, 14 Jan 2021 01:17:01 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454fe39b046d9fedbd9e0b3f698556592463406933b790b272dd909d5bd90d53`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:d232a757f6c487484b3640973fbb0287e747e6b357bc1dc75faa07b26da14a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:cb19d2e6f6575fb121eb2181cbd50f783c1995bf515cba8c7bbab7d9b6859949
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24603200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ecef4edf395a65a22e7b3c46ec4b16c869c1a5386a1ea0305132dc68266f04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 22:29:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 22:29:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 22:29:27 GMT
EXPOSE 80
# Wed, 13 Jan 2021 22:29:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 22:29:28 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 22:29:28 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8923725f26216ece246718b634aabb038e3ba78292d388ebb7350cc0d89ba1`  
		Last Modified: Wed, 13 Jan 2021 22:30:25 GMT  
		Size: 21.1 MB (21116271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8abe3b22d27fbf46de589e10d21107bd248a725e59317b3fc6a78a83e9c940`  
		Last Modified: Wed, 13 Jan 2021 22:30:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:198e33555ab98a4ea7b448b1f818b9663ab2f8fe98f0966543390a711e55692d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23064299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92898625b48315d465f9a4d3ad8e32c8b224bb4617bff335d0840bbd9ce1aced`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:56:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:56:47 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:56:48 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:56:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:56:49 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:56:49 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102471939d830c2c1e2668e0dd48049fc6ce2f332ead14922e8a55086f8816ef`  
		Last Modified: Wed, 13 Jan 2021 21:57:48 GMT  
		Size: 19.8 MB (19768260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a399e8ce2234a61da5e35bf382eefe32e24435b8c5805b773299d16a01b022`  
		Last Modified: Wed, 13 Jan 2021 21:57:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a144e4ba9554f68e6903986ca95090991e87d3c7a3e45809bfd602a5bda85a3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22884874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c65bf1525b68d03c1cc5d512338cf2608b5742b1e06e6ea57c492e61afee7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 21:46:38 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 21:46:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 21:46:39 GMT
EXPOSE 80
# Wed, 13 Jan 2021 21:46:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 21:46:41 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 21:46:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50dc3ca8b514cac3bfbf2a6303d6be654d1a94f584f6f24d4e62522b80bd36b`  
		Last Modified: Wed, 13 Jan 2021 21:47:33 GMT  
		Size: 19.5 MB (19486044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4205a3b9bbaa8f65f3bd5780aeb6e4cc761d5f7d6de7cb70588b41ed018c72`  
		Last Modified: Wed, 13 Jan 2021 21:47:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8f2b9d477c5d31806d427f5dad762d9f448c131bb284641f3977b914e655afd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:91b9a8ca83df9afc2b41003518d4b4f9d8e8a21f77880fd74d543670c7ab4da9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2466262882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6962de1a7e3fc419a74eb2ea94e4c40359d9f53a93caec6bd1e61f1944ccf282`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Jan 2021 01:16:20 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.28/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 14 Jan 2021 01:16:24 GMT
EXPOSE 80
# Thu, 14 Jan 2021 01:16:25 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Jan 2021 01:16:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84697de3c7d0310176f36e2fe57e5688d23e486eb5b5febf6dbf860e763d1750`  
		Last Modified: Thu, 14 Jan 2021 01:17:09 GMT  
		Size: 30.5 MB (30486249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069ca4204690196a12b1d26a1b7d9b54c2d8fc7db082a3a4a9e21bfdf55d63d1`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adaebdd4a9fa6db73d7167e0d944af020e0ddfe54da3ed92807a14054a53d669`  
		Last Modified: Thu, 14 Jan 2021 01:17:01 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454fe39b046d9fedbd9e0b3f698556592463406933b790b272dd909d5bd90d53`  
		Last Modified: Thu, 14 Jan 2021 01:17:02 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3`

```console
$ docker pull traefik@sha256:0181e35c5af98f7f30fb391f91a6dbd281a90d7cf971e9909e26afd4ea923251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.3` - linux; amd64

```console
$ docker pull traefik@sha256:0aca29bb8e51aa69569b15b8b7f08328e6957cbec201dd532304b3329e5a82a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28387061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb0268e5b5fb0a4a9cb3f9e1d559dcc034cd9290b4faea2b03cd50f05042bd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Jan 2021 01:29:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Jan 2021 01:29:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Jan 2021 01:29:57 GMT
EXPOSE 80
# Tue, 12 Jan 2021 01:29:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 01:29:58 GMT
CMD ["traefik"]
# Tue, 12 Jan 2021 01:29:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00390834f324ba7030874c57968d6d7ee2f354e377a5bf938933ee1d39ce6abb`  
		Last Modified: Tue, 12 Jan 2021 01:30:53 GMT  
		Size: 24.9 MB (24900132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f159f39400907c1a2cf02624898430f0de90f3a8c7852b361029222623263`  
		Last Modified: Tue, 12 Jan 2021 01:30:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:866e86d9fed207750fcd6190a8378efdc4cf7378d7473adc7cefd1c47191659b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26482921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d24aa2dc32fc8e97983f070a55ec25388b336c2abd8dc31a1989b6e40c48dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:52 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:54 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404789ba4d57d5ebd3b9e346ab72911d9cda4e7f9395248ea5bf3bdd24e42949`  
		Last Modified: Mon, 11 Jan 2021 23:57:59 GMT  
		Size: 23.2 MB (23186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa14f62f5fc51679fe0d4c53102854dcfec037295c4ede9af9dbb4ecfe545a0`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a514d1067beb769fd25480cba0ffc0bd2aa5f44a004f9d33dc0465c3db9f5c3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26111594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24230cfd873ab4443c7220976542b2f075654cae3e8fccbaac8566b2cb4859`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:50 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:52 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb41b44f2a7a3f798996c121379f863b52ffee788ba79ada6d2cbe591a1153`  
		Last Modified: Mon, 11 Jan 2021 23:57:48 GMT  
		Size: 22.7 MB (22712763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fcc3d290ad4bbced9b6b0286aa15edb6d4b398deda5bb13fa7ce6f4b9013a`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3.7`

```console
$ docker pull traefik@sha256:0181e35c5af98f7f30fb391f91a6dbd281a90d7cf971e9909e26afd4ea923251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.3.7` - linux; amd64

```console
$ docker pull traefik@sha256:0aca29bb8e51aa69569b15b8b7f08328e6957cbec201dd532304b3329e5a82a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28387061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb0268e5b5fb0a4a9cb3f9e1d559dcc034cd9290b4faea2b03cd50f05042bd6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 12 Jan 2021 01:29:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 12 Jan 2021 01:29:57 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 12 Jan 2021 01:29:57 GMT
EXPOSE 80
# Tue, 12 Jan 2021 01:29:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Jan 2021 01:29:58 GMT
CMD ["traefik"]
# Tue, 12 Jan 2021 01:29:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00390834f324ba7030874c57968d6d7ee2f354e377a5bf938933ee1d39ce6abb`  
		Last Modified: Tue, 12 Jan 2021 01:30:53 GMT  
		Size: 24.9 MB (24900132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059f159f39400907c1a2cf02624898430f0de90f3a8c7852b361029222623263`  
		Last Modified: Tue, 12 Jan 2021 01:30:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:866e86d9fed207750fcd6190a8378efdc4cf7378d7473adc7cefd1c47191659b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26482921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d24aa2dc32fc8e97983f070a55ec25388b336c2abd8dc31a1989b6e40c48dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:52 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:54 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404789ba4d57d5ebd3b9e346ab72911d9cda4e7f9395248ea5bf3bdd24e42949`  
		Last Modified: Mon, 11 Jan 2021 23:57:59 GMT  
		Size: 23.2 MB (23186881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa14f62f5fc51679fe0d4c53102854dcfec037295c4ede9af9dbb4ecfe545a0`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.3.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a514d1067beb769fd25480cba0ffc0bd2aa5f44a004f9d33dc0465c3db9f5c3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26111594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d24230cfd873ab4443c7220976542b2f075654cae3e8fccbaac8566b2cb4859`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 11 Jan 2021 23:56:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 11 Jan 2021 23:56:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 11 Jan 2021 23:56:50 GMT
EXPOSE 80
# Mon, 11 Jan 2021 23:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 Jan 2021 23:56:52 GMT
CMD ["traefik"]
# Mon, 11 Jan 2021 23:56:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb41b44f2a7a3f798996c121379f863b52ffee788ba79ada6d2cbe591a1153`  
		Last Modified: Mon, 11 Jan 2021 23:57:48 GMT  
		Size: 22.7 MB (22712763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892fcc3d290ad4bbced9b6b0286aa15edb6d4b398deda5bb13fa7ce6f4b9013a`  
		Last Modified: Mon, 11 Jan 2021 23:57:41 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d5aace4a65d4ac287ee01df27a8a08a303dc1c1ab3b8c4dd5ee845cf5ab47f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:v2.3.7-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:40f8fe38de1fc5b8677764a6d5835c2f91a089348a958efe44032c49310e0ea5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470404577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0011bc7c1cd89741d499d69fe62ed8c50b251d90bb3dd01350d6f945dace6e89`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:15:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:15:37 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:15:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:15:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6c5b0a97b9671b4e08aa00ddb88caedc356102697742d6f378e5af7994ed05`  
		Last Modified: Wed, 13 Jan 2021 13:19:00 GMT  
		Size: 34.6 MB (34627945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275937a63dff0407d503768537bd0fefd61c0e7484713f860a115caf944feaa7`  
		Last Modified: Wed, 13 Jan 2021 13:18:19 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea03fb9da7a541e90efca3d37faffbacf68c1b876bc44ebbd5c67c5f275d35`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee034dc2f4eaff9d6bf00b65b0f122e98cb38e86c8b2afa3256d0c8207de0e5`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:d5aace4a65d4ac287ee01df27a8a08a303dc1c1ab3b8c4dd5ee845cf5ab47f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:v2.3-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:40f8fe38de1fc5b8677764a6d5835c2f91a089348a958efe44032c49310e0ea5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470404577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0011bc7c1cd89741d499d69fe62ed8c50b251d90bb3dd01350d6f945dace6e89`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:15:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:15:37 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:15:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:15:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6c5b0a97b9671b4e08aa00ddb88caedc356102697742d6f378e5af7994ed05`  
		Last Modified: Wed, 13 Jan 2021 13:19:00 GMT  
		Size: 34.6 MB (34627945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275937a63dff0407d503768537bd0fefd61c0e7484713f860a115caf944feaa7`  
		Last Modified: Wed, 13 Jan 2021 13:18:19 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea03fb9da7a541e90efca3d37faffbacf68c1b876bc44ebbd5c67c5f275d35`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee034dc2f4eaff9d6bf00b65b0f122e98cb38e86c8b2afa3256d0c8207de0e5`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4`

```console
$ docker pull traefik@sha256:13d613be07961b1bf97a5e4826a20c01c312367495f85385c4750a9085e7bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.4` - linux; amd64

```console
$ docker pull traefik@sha256:42401810722b981bee516647dab6028688dd2b3246f4e56a7d5309e6806b21b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29074781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c19b1291a4277be960aaca74928af3dfb9313bb8b463e9d1ec842be6a9f228e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 09:49:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 09:49:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 09:49:30 GMT
EXPOSE 80
# Wed, 13 Jan 2021 09:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 09:49:30 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 09:49:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16bf8c9b9a1f7cc43c306353cd2ddfa5de3c14db5b512efa1bfa1bb01998fb8`  
		Last Modified: Wed, 13 Jan 2021 09:50:11 GMT  
		Size: 25.6 MB (25587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640e96d3797b9f24dd02e7fddfc5726478b3854e303ad398da8289e196e2b392`  
		Last Modified: Wed, 13 Jan 2021 09:50:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2943b6dbc5cce7b549c88f208e3eec0736d4f305e6f2eb45973e4d31412253de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27111407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5575a2605168aea584cde15a4395f18c45b2685e5692cdd6b2f538b52bfb3cfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 01:02:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 01:02:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 01:02:15 GMT
EXPOSE 80
# Wed, 13 Jan 2021 01:02:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 01:02:18 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 01:02:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787df9c7681db127330ef3ffc8d6f21800c11f0ada5cb694d614cbfefbdd096a`  
		Last Modified: Wed, 13 Jan 2021 01:03:15 GMT  
		Size: 23.8 MB (23815368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e09316753dc27b18cafd3e135ab0a5ed07abcad6a26f04ad1800e4a693d87a5`  
		Last Modified: Wed, 13 Jan 2021 01:03:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:148ff9dd39b58ca532d96369af3b2cda1b9a1865dabd6ceeb5253e329cf40c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26736606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0524ae4495e503c237291bd7e5cf898f40e2a0cb36c626b43151f885f308731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 06:09:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 06:09:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 06:09:23 GMT
EXPOSE 80
# Wed, 13 Jan 2021 06:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 06:09:24 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 06:09:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5274a1d1e4be5ba614ecb3a12c06bffef192457ed200d9e7f05e7b0f7860a8`  
		Last Modified: Wed, 13 Jan 2021 06:10:16 GMT  
		Size: 23.3 MB (23337776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240f3cfce0cfe96476300fc4562f75c89fe8ad624aa64a8db56edfa7c241bfcb`  
		Last Modified: Wed, 13 Jan 2021 06:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4.0-rc2`

```console
$ docker pull traefik@sha256:13d613be07961b1bf97a5e4826a20c01c312367495f85385c4750a9085e7bf05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.4.0-rc2` - linux; amd64

```console
$ docker pull traefik@sha256:42401810722b981bee516647dab6028688dd2b3246f4e56a7d5309e6806b21b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29074781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c19b1291a4277be960aaca74928af3dfb9313bb8b463e9d1ec842be6a9f228e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:47:33 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 09:49:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 09:49:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 09:49:30 GMT
EXPOSE 80
# Wed, 13 Jan 2021 09:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 09:49:30 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 09:49:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d0c2f48fede0de57585b470af3e8e9aa5534db90642859512370fa53ffac21`  
		Last Modified: Thu, 17 Dec 2020 00:48:37 GMT  
		Size: 671.7 KB (671697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16bf8c9b9a1f7cc43c306353cd2ddfa5de3c14db5b512efa1bfa1bb01998fb8`  
		Last Modified: Wed, 13 Jan 2021 09:50:11 GMT  
		Size: 25.6 MB (25587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640e96d3797b9f24dd02e7fddfc5726478b3854e303ad398da8289e196e2b392`  
		Last Modified: Wed, 13 Jan 2021 09:50:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4.0-rc2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2943b6dbc5cce7b549c88f208e3eec0736d4f305e6f2eb45973e4d31412253de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27111407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5575a2605168aea584cde15a4395f18c45b2685e5692cdd6b2f538b52bfb3cfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:25:55 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 01:02:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 01:02:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 01:02:15 GMT
EXPOSE 80
# Wed, 13 Jan 2021 01:02:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 01:02:18 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 01:02:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab096bb24791df9de14fbfc840265a32c0d9f7be463db3a782da6095c0e6ad5b`  
		Last Modified: Thu, 17 Dec 2020 00:27:24 GMT  
		Size: 674.9 KB (674902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787df9c7681db127330ef3ffc8d6f21800c11f0ada5cb694d614cbfefbdd096a`  
		Last Modified: Wed, 13 Jan 2021 01:03:15 GMT  
		Size: 23.8 MB (23815368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e09316753dc27b18cafd3e135ab0a5ed07abcad6a26f04ad1800e4a693d87a5`  
		Last Modified: Wed, 13 Jan 2021 01:03:07 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.4.0-rc2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:148ff9dd39b58ca532d96369af3b2cda1b9a1865dabd6ceeb5253e329cf40c86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26736606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0524ae4495e503c237291bd7e5cf898f40e2a0cb36c626b43151f885f308731`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:27:02 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Jan 2021 06:09:21 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Jan 2021 06:09:22 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Jan 2021 06:09:23 GMT
EXPOSE 80
# Wed, 13 Jan 2021 06:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Jan 2021 06:09:24 GMT
CMD ["traefik"]
# Wed, 13 Jan 2021 06:09:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278abd308a18c136f69dcabbba1dc64486ebdad665d4a2f4ab14d2826ec08b06`  
		Last Modified: Thu, 17 Dec 2020 00:28:38 GMT  
		Size: 673.2 KB (673246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5274a1d1e4be5ba614ecb3a12c06bffef192457ed200d9e7f05e7b0f7860a8`  
		Last Modified: Wed, 13 Jan 2021 06:10:16 GMT  
		Size: 23.3 MB (23337776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240f3cfce0cfe96476300fc4562f75c89fe8ad624aa64a8db56edfa7c241bfcb`  
		Last Modified: Wed, 13 Jan 2021 06:10:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4.0-rc2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b3997e6fd462c42a96d11e7c1d78eb9d873d15f52fc726d20608a92bd06f853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:v2.4.0-rc2-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:efcce1a8b23e8de5d1aeb5e445ea5f114140e9401967d4a36d10022399c89708
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471100192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46e43162aa7035ce3b0a895000a66777d2f050a80c29f9d706c97a52fb4759d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:14:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:14:31 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:14:32 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116638bca58c127c2ec8da559c11513038fa82eea012d15b0fc6041ca676750`  
		Last Modified: Wed, 13 Jan 2021 13:17:58 GMT  
		Size: 35.3 MB (35323488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8638b72f94f87f9242a92efb9242270c5cd406775e12ddedc1dd4da5fa1fea5`  
		Last Modified: Wed, 13 Jan 2021 13:17:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88821eec1273c142fbde11d869ceb0e5bd9ce94842c40f27b93f5dd0823d78ab`  
		Last Modified: Wed, 13 Jan 2021 13:17:24 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e03b07855cc717b7969b2868a7c0e581f38d8efc5c19a0bdc177824decae27`  
		Last Modified: Wed, 13 Jan 2021 13:17:20 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.4-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b3997e6fd462c42a96d11e7c1d78eb9d873d15f52fc726d20608a92bd06f853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:v2.4-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:efcce1a8b23e8de5d1aeb5e445ea5f114140e9401967d4a36d10022399c89708
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471100192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46e43162aa7035ce3b0a895000a66777d2f050a80c29f9d706c97a52fb4759d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:14:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.4.0-rc2/traefik_v2.4.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:14:31 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:14:32 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:14:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116638bca58c127c2ec8da559c11513038fa82eea012d15b0fc6041ca676750`  
		Last Modified: Wed, 13 Jan 2021 13:17:58 GMT  
		Size: 35.3 MB (35323488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8638b72f94f87f9242a92efb9242270c5cd406775e12ddedc1dd4da5fa1fea5`  
		Last Modified: Wed, 13 Jan 2021 13:17:22 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88821eec1273c142fbde11d869ceb0e5bd9ce94842c40f27b93f5dd0823d78ab`  
		Last Modified: Wed, 13 Jan 2021 13:17:24 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e03b07855cc717b7969b2868a7c0e581f38d8efc5c19a0bdc177824decae27`  
		Last Modified: Wed, 13 Jan 2021 13:17:20 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:d5aace4a65d4ac287ee01df27a8a08a303dc1c1ab3b8c4dd5ee845cf5ab47f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull traefik@sha256:40f8fe38de1fc5b8677764a6d5835c2f91a089348a958efe44032c49310e0ea5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470404577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0011bc7c1cd89741d499d69fe62ed8c50b251d90bb3dd01350d6f945dace6e89`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 13:15:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.7/traefik_v2.3.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Jan 2021 13:15:37 GMT
EXPOSE 80
# Wed, 13 Jan 2021 13:15:39 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Jan 2021 13:15:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6c5b0a97b9671b4e08aa00ddb88caedc356102697742d6f378e5af7994ed05`  
		Last Modified: Wed, 13 Jan 2021 13:19:00 GMT  
		Size: 34.6 MB (34627945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275937a63dff0407d503768537bd0fefd61c0e7484713f860a115caf944feaa7`  
		Last Modified: Wed, 13 Jan 2021 13:18:19 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ea03fb9da7a541e90efca3d37faffbacf68c1b876bc44ebbd5c67c5f275d35`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee034dc2f4eaff9d6bf00b65b0f122e98cb38e86c8b2afa3256d0c8207de0e5`  
		Last Modified: Wed, 13 Jan 2021 13:18:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
