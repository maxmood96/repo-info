<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.34`](#traefik1734)
-	[`traefik:1.7.34-alpine`](#traefik1734-alpine)
-	[`traefik:1.7.34-windowsservercore-1809`](#traefik1734-windowsservercore-1809)
-	[`traefik:2.5`](#traefik25)
-	[`traefik:2.5-windowsservercore-1809`](#traefik25-windowsservercore-1809)
-	[`traefik:2.5.6`](#traefik256)
-	[`traefik:2.5.6-windowsservercore-1809`](#traefik256-windowsservercore-1809)
-	[`traefik:2.6`](#traefik26)
-	[`traefik:2.6-windowsservercore-1809`](#traefik26-windowsservercore-1809)
-	[`traefik:2.6.0-rc1`](#traefik260-rc1)
-	[`traefik:2.6.0-rc1-windowsservercore-1809`](#traefik260-rc1-windowsservercore-1809)
-	[`traefik:brie`](#traefikbrie)
-	[`traefik:brie-windowsservercore-1809`](#traefikbrie-windowsservercore-1809)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:maroilles`](#traefikmaroilles)
-	[`traefik:maroilles-alpine`](#traefikmaroilles-alpine)
-	[`traefik:maroilles-windowsservercore-1809`](#traefikmaroilles-windowsservercore-1809)
-	[`traefik:rocamadour`](#traefikrocamadour)
-	[`traefik:rocamadour-windowsservercore-1809`](#traefikrocamadour-windowsservercore-1809)
-	[`traefik:v1.7`](#traefikv17)
-	[`traefik:v1.7-alpine`](#traefikv17-alpine)
-	[`traefik:v1.7-windowsservercore-1809`](#traefikv17-windowsservercore-1809)
-	[`traefik:v1.7.34`](#traefikv1734)
-	[`traefik:v1.7.34-alpine`](#traefikv1734-alpine)
-	[`traefik:v1.7.34-windowsservercore-1809`](#traefikv1734-windowsservercore-1809)
-	[`traefik:v2.5`](#traefikv25)
-	[`traefik:v2.5-windowsservercore-1809`](#traefikv25-windowsservercore-1809)
-	[`traefik:v2.5.6`](#traefikv256)
-	[`traefik:v2.5.6-windowsservercore-1809`](#traefikv256-windowsservercore-1809)
-	[`traefik:v2.6`](#traefikv26)
-	[`traefik:v2.6-windowsservercore-1809`](#traefikv26-windowsservercore-1809)
-	[`traefik:v2.6.0-rc1`](#traefikv260-rc1)
-	[`traefik:v2.6.0-rc1-windowsservercore-1809`](#traefikv260-rc1-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1a913ea8b21e3257a626ca50cf17972f60587a0e11206ffd0b77962179c5aadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f0cc2e765448d62b87e2093e7cddf4e6b64c02bca6c6930b7ebe7307f936691
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734441373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31705b6293bb21e22bea0ff456562b95b079f7741cd17b448a1f4113c7e7b633`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:33:48 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 11 Jan 2022 18:33:51 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:33:52 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:33:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f01ad1772364c9b4326d7171fc538f5fdd04b7d2037e7350fe5910b217bfdf9`  
		Last Modified: Tue, 11 Jan 2022 18:35:22 GMT  
		Size: 22.9 MB (22851160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec4aeedc20d74a474e364188e91d16eb0c7ce65e090f34a2f3aa3915b5c86e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80c5729d5b119720fa3073cd758b994417cb3b1f2c8842ccfb43a39b3671200`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458290c1b8da92b5b64631c6f63a0053d3b5c04d0172b022f5c24d6a443e687e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1a913ea8b21e3257a626ca50cf17972f60587a0e11206ffd0b77962179c5aadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:1.7.34-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f0cc2e765448d62b87e2093e7cddf4e6b64c02bca6c6930b7ebe7307f936691
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734441373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31705b6293bb21e22bea0ff456562b95b079f7741cd17b448a1f4113c7e7b633`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:33:48 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 11 Jan 2022 18:33:51 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:33:52 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:33:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f01ad1772364c9b4326d7171fc538f5fdd04b7d2037e7350fe5910b217bfdf9`  
		Last Modified: Tue, 11 Jan 2022 18:35:22 GMT  
		Size: 22.9 MB (22851160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec4aeedc20d74a474e364188e91d16eb0c7ce65e090f34a2f3aa3915b5c86e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80c5729d5b119720fa3073cd758b994417cb3b1f2c8842ccfb43a39b3671200`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458290c1b8da92b5b64631c6f63a0053d3b5c04d0172b022f5c24d6a443e687e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5`

```console
$ docker pull traefik@sha256:2f603f8d3abe1dd3a4eb28960c55506be48293b41ea2c6ed4a4297c851a57a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.5` - linux; amd64

```console
$ docker pull traefik@sha256:cb6c620b70f3981b2323cf759d452164e84ed6ce82c2a2a84e0df825a8428309
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29972198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd4bc25ad14d7c652b17d49804dfb99a9ed702faa006ac2f9bdf72c8716a15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 22:16:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 22:16:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 22:16:58 GMT
EXPOSE 80
# Wed, 22 Dec 2021 22:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 22:16:59 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 22:16:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f585f616a119577ed9e482bc2cffb1e83b76b09f5dbe8bd8245a6b9f8c29ed1`  
		Last Modified: Wed, 22 Dec 2021 22:17:37 GMT  
		Size: 26.5 MB (26471025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f598fe2b15ae64b945b5336fe57e028160d13c4e52ec2c8d538c951c20f69e`  
		Last Modified: Wed, 22 Dec 2021 22:17:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f1c9f63db180cf2dfdca8229e56f85389a73367a3995fccb1c3add288f21e12c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28172686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234a638e7f0d02ef0a807f5740cdd175613d99442d80f6caba8804466b6f1469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 19:09:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 19:09:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 19:09:27 GMT
EXPOSE 80
# Wed, 22 Dec 2021 19:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 19:09:28 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 19:09:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e98886206e7f64a9779b3489c82d9839a44bccf18be9747ffc8cf8359e214b`  
		Last Modified: Wed, 22 Dec 2021 19:11:58 GMT  
		Size: 24.9 MB (24853954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4b667e2a330d44a4e5f8bf80ae096df60ece9abe4a7d926062bbcd2126495`  
		Last Modified: Wed, 22 Dec 2021 19:11:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:43d5ae2e4cf69416d7364123e26c9e535079ba82e28cf18292f3e9c240ea014c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27556586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34574e935bdaf7af66692ba2b2085bf15015615a9eeed74b2568febd5959b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 20:10:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 20:10:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 20:10:01 GMT
EXPOSE 80
# Wed, 22 Dec 2021 20:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 20:10:03 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 20:10:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78551cc4d851ad8a96da3591e6e80f48913b89a1043a82e0e898b4fca661b305`  
		Last Modified: Wed, 22 Dec 2021 20:12:04 GMT  
		Size: 24.2 MB (24158511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7356b461e22137b8d7713e06bf23fa5930c13ff60ff89a76b7196c188a8a08`  
		Last Modified: Wed, 22 Dec 2021 20:12:00 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:acae7ced1a3294fe967f2e1e8d396840e91fbdfd749d6ced85884e308471a3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:2.5-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f6cd3447fbb1dfcaa3582fb0a304f6a34f4fb770ac28f8210bd053888b6bf50
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738638539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588533eb932d8c260b9d6882222b501a3e930d8a2578b19fdf79a2f554346bcf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:32:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:32:16 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:32:19 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:32:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1277073e66653b947a55a8cfd8ffbe88f9519a0f06c88c11c9196354d2fb543`  
		Last Modified: Tue, 11 Jan 2022 18:34:57 GMT  
		Size: 27.0 MB (27048392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe8208ec331b73e29d6dbce63a950a0526bd90094e4302b1bbaceb8c980908`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9ed58f572b8f88d14c2540527b95641d559fb1c1fba2ecc25c72e5bfe415`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a1a799b0d8d278a16dda6bc4be628233f46b5ff8d89b097fd76a34d2b1aa15`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5.6`

```console
$ docker pull traefik@sha256:2f603f8d3abe1dd3a4eb28960c55506be48293b41ea2c6ed4a4297c851a57a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.5.6` - linux; amd64

```console
$ docker pull traefik@sha256:cb6c620b70f3981b2323cf759d452164e84ed6ce82c2a2a84e0df825a8428309
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29972198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd4bc25ad14d7c652b17d49804dfb99a9ed702faa006ac2f9bdf72c8716a15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 22:16:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 22:16:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 22:16:58 GMT
EXPOSE 80
# Wed, 22 Dec 2021 22:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 22:16:59 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 22:16:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f585f616a119577ed9e482bc2cffb1e83b76b09f5dbe8bd8245a6b9f8c29ed1`  
		Last Modified: Wed, 22 Dec 2021 22:17:37 GMT  
		Size: 26.5 MB (26471025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f598fe2b15ae64b945b5336fe57e028160d13c4e52ec2c8d538c951c20f69e`  
		Last Modified: Wed, 22 Dec 2021 22:17:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f1c9f63db180cf2dfdca8229e56f85389a73367a3995fccb1c3add288f21e12c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28172686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234a638e7f0d02ef0a807f5740cdd175613d99442d80f6caba8804466b6f1469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 19:09:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 19:09:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 19:09:27 GMT
EXPOSE 80
# Wed, 22 Dec 2021 19:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 19:09:28 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 19:09:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e98886206e7f64a9779b3489c82d9839a44bccf18be9747ffc8cf8359e214b`  
		Last Modified: Wed, 22 Dec 2021 19:11:58 GMT  
		Size: 24.9 MB (24853954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4b667e2a330d44a4e5f8bf80ae096df60ece9abe4a7d926062bbcd2126495`  
		Last Modified: Wed, 22 Dec 2021 19:11:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.5.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:43d5ae2e4cf69416d7364123e26c9e535079ba82e28cf18292f3e9c240ea014c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27556586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34574e935bdaf7af66692ba2b2085bf15015615a9eeed74b2568febd5959b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 20:10:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 20:10:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 20:10:01 GMT
EXPOSE 80
# Wed, 22 Dec 2021 20:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 20:10:03 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 20:10:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78551cc4d851ad8a96da3591e6e80f48913b89a1043a82e0e898b4fca661b305`  
		Last Modified: Wed, 22 Dec 2021 20:12:04 GMT  
		Size: 24.2 MB (24158511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7356b461e22137b8d7713e06bf23fa5930c13ff60ff89a76b7196c188a8a08`  
		Last Modified: Wed, 22 Dec 2021 20:12:00 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.5.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:acae7ced1a3294fe967f2e1e8d396840e91fbdfd749d6ced85884e308471a3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:2.5.6-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f6cd3447fbb1dfcaa3582fb0a304f6a34f4fb770ac28f8210bd053888b6bf50
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738638539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588533eb932d8c260b9d6882222b501a3e930d8a2578b19fdf79a2f554346bcf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:32:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:32:16 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:32:19 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:32:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1277073e66653b947a55a8cfd8ffbe88f9519a0f06c88c11c9196354d2fb543`  
		Last Modified: Tue, 11 Jan 2022 18:34:57 GMT  
		Size: 27.0 MB (27048392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe8208ec331b73e29d6dbce63a950a0526bd90094e4302b1bbaceb8c980908`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9ed58f572b8f88d14c2540527b95641d559fb1c1fba2ecc25c72e5bfe415`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a1a799b0d8d278a16dda6bc4be628233f46b5ff8d89b097fd76a34d2b1aa15`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6`

```console
$ docker pull traefik@sha256:44cbafeaa8d0387751ccb557a7738bb1d2a908cdd358e8acefcfcb8e8b9faf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.6` - linux; amd64

```console
$ docker pull traefik@sha256:d65d0be92a53c004a163cb35e4c0c31a58edebcef1de496a319b028fa2bd09a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30168792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c77ac9166db72d9e4f271680b434cb985f4659125da1c2222034612341133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 19:20:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 19:20:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 19:20:01 GMT
EXPOSE 80
# Mon, 20 Dec 2021 19:20:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 19:20:01 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 19:20:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95732e323f1180b16089b3709e32acdd925d45c058c88e3fd9a278f8ebf095a`  
		Last Modified: Mon, 20 Dec 2021 19:20:37 GMT  
		Size: 26.7 MB (26667619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37884b0fee928687a29eb238763446dec983cdb4b55cca61344a6b6b3d5a8739`  
		Last Modified: Mon, 20 Dec 2021 19:20:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9412c15369af505532c1ad0c0378858e69c5560577d3c4dd422a7eae780bebf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28356316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae4a6ab517da91a17d91e9cca6df953b502f957c4af15614219234360d27ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:54:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:54:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:54:34 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:54:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:54:35 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:54:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9a02ab1647767183c89cef77baf75a346b7c836766c7ba9d151931029fee8`  
		Last Modified: Mon, 20 Dec 2021 20:57:10 GMT  
		Size: 25.0 MB (25037585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d05989a6849f306b9d9e656d3adbcbc0ed81703b8eb04f5b1866dc81461c51`  
		Last Modified: Mon, 20 Dec 2021 20:56:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fef2273c4d6362f6f6a8731289199649a1371c47fb86832312a741b60f34ab51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27731175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff94a5e8b4283cbe7686990ac4b5491d757c3b95426c68306cbf29abdf5167c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:38:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:38:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:38:19 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:38:21 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:38:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13202376be157cfd94c1b46e9036d7c86c3d6141f948f8d24e9e5d13aabec7fc`  
		Last Modified: Mon, 20 Dec 2021 20:39:29 GMT  
		Size: 24.3 MB (24333099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a13b6a2df421f21f76b73016fac8a53c1f3beb98ab0dba482b91f3d9f305235`  
		Last Modified: Mon, 20 Dec 2021 20:39:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b847b8cd2aa9e9c483b6d54e77a6276536cbe15f85ca4f77fcb42d5ca26a9a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:2.6-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:2c2e9b3dac623411b3750becff04a1a55de68ce405b73a3f7e5e8a7e345941fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738841422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a3cc03e9f6c0ec5bb50241833d17ad495a6bffb77f8a35e81d3da283bba5b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:30:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:30:43 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:30:44 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2030cd81ffa233f949c1e5a83056069701ebb118f21dcfcbe387c0f462f3702`  
		Last Modified: Tue, 11 Jan 2022 18:34:34 GMT  
		Size: 27.3 MB (27251289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323285e35591d8353fda5a8100943aefaa5db24514f9c76f4a5ad73118c791b8`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b99bcd7b1ec339f6ad70787bfaf6c7f12e0f5d055abebe251993c55db49f56`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cab45e7657cd77f6eb771b157511d491e8982974da7717c50a59ac28491619`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6.0-rc1`

```console
$ docker pull traefik@sha256:44cbafeaa8d0387751ccb557a7738bb1d2a908cdd358e8acefcfcb8e8b9faf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:2.6.0-rc1` - linux; amd64

```console
$ docker pull traefik@sha256:d65d0be92a53c004a163cb35e4c0c31a58edebcef1de496a319b028fa2bd09a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30168792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c77ac9166db72d9e4f271680b434cb985f4659125da1c2222034612341133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 19:20:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 19:20:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 19:20:01 GMT
EXPOSE 80
# Mon, 20 Dec 2021 19:20:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 19:20:01 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 19:20:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95732e323f1180b16089b3709e32acdd925d45c058c88e3fd9a278f8ebf095a`  
		Last Modified: Mon, 20 Dec 2021 19:20:37 GMT  
		Size: 26.7 MB (26667619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37884b0fee928687a29eb238763446dec983cdb4b55cca61344a6b6b3d5a8739`  
		Last Modified: Mon, 20 Dec 2021 19:20:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6.0-rc1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9412c15369af505532c1ad0c0378858e69c5560577d3c4dd422a7eae780bebf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28356316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae4a6ab517da91a17d91e9cca6df953b502f957c4af15614219234360d27ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:54:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:54:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:54:34 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:54:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:54:35 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:54:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9a02ab1647767183c89cef77baf75a346b7c836766c7ba9d151931029fee8`  
		Last Modified: Mon, 20 Dec 2021 20:57:10 GMT  
		Size: 25.0 MB (25037585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d05989a6849f306b9d9e656d3adbcbc0ed81703b8eb04f5b1866dc81461c51`  
		Last Modified: Mon, 20 Dec 2021 20:56:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6.0-rc1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fef2273c4d6362f6f6a8731289199649a1371c47fb86832312a741b60f34ab51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27731175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff94a5e8b4283cbe7686990ac4b5491d757c3b95426c68306cbf29abdf5167c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:38:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:38:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:38:19 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:38:21 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:38:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13202376be157cfd94c1b46e9036d7c86c3d6141f948f8d24e9e5d13aabec7fc`  
		Last Modified: Mon, 20 Dec 2021 20:39:29 GMT  
		Size: 24.3 MB (24333099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a13b6a2df421f21f76b73016fac8a53c1f3beb98ab0dba482b91f3d9f305235`  
		Last Modified: Mon, 20 Dec 2021 20:39:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6.0-rc1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b847b8cd2aa9e9c483b6d54e77a6276536cbe15f85ca4f77fcb42d5ca26a9a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:2.6.0-rc1-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:2c2e9b3dac623411b3750becff04a1a55de68ce405b73a3f7e5e8a7e345941fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738841422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a3cc03e9f6c0ec5bb50241833d17ad495a6bffb77f8a35e81d3da283bba5b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:30:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:30:43 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:30:44 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2030cd81ffa233f949c1e5a83056069701ebb118f21dcfcbe387c0f462f3702`  
		Last Modified: Tue, 11 Jan 2022 18:34:34 GMT  
		Size: 27.3 MB (27251289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323285e35591d8353fda5a8100943aefaa5db24514f9c76f4a5ad73118c791b8`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b99bcd7b1ec339f6ad70787bfaf6c7f12e0f5d055abebe251993c55db49f56`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cab45e7657cd77f6eb771b157511d491e8982974da7717c50a59ac28491619`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:brie`

```console
$ docker pull traefik@sha256:2f603f8d3abe1dd3a4eb28960c55506be48293b41ea2c6ed4a4297c851a57a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:brie` - linux; amd64

```console
$ docker pull traefik@sha256:cb6c620b70f3981b2323cf759d452164e84ed6ce82c2a2a84e0df825a8428309
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29972198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd4bc25ad14d7c652b17d49804dfb99a9ed702faa006ac2f9bdf72c8716a15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 22:16:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 22:16:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 22:16:58 GMT
EXPOSE 80
# Wed, 22 Dec 2021 22:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 22:16:59 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 22:16:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f585f616a119577ed9e482bc2cffb1e83b76b09f5dbe8bd8245a6b9f8c29ed1`  
		Last Modified: Wed, 22 Dec 2021 22:17:37 GMT  
		Size: 26.5 MB (26471025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f598fe2b15ae64b945b5336fe57e028160d13c4e52ec2c8d538c951c20f69e`  
		Last Modified: Wed, 22 Dec 2021 22:17:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f1c9f63db180cf2dfdca8229e56f85389a73367a3995fccb1c3add288f21e12c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28172686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234a638e7f0d02ef0a807f5740cdd175613d99442d80f6caba8804466b6f1469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 19:09:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 19:09:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 19:09:27 GMT
EXPOSE 80
# Wed, 22 Dec 2021 19:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 19:09:28 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 19:09:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e98886206e7f64a9779b3489c82d9839a44bccf18be9747ffc8cf8359e214b`  
		Last Modified: Wed, 22 Dec 2021 19:11:58 GMT  
		Size: 24.9 MB (24853954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4b667e2a330d44a4e5f8bf80ae096df60ece9abe4a7d926062bbcd2126495`  
		Last Modified: Wed, 22 Dec 2021 19:11:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:43d5ae2e4cf69416d7364123e26c9e535079ba82e28cf18292f3e9c240ea014c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27556586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34574e935bdaf7af66692ba2b2085bf15015615a9eeed74b2568febd5959b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 20:10:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 20:10:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 20:10:01 GMT
EXPOSE 80
# Wed, 22 Dec 2021 20:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 20:10:03 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 20:10:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78551cc4d851ad8a96da3591e6e80f48913b89a1043a82e0e898b4fca661b305`  
		Last Modified: Wed, 22 Dec 2021 20:12:04 GMT  
		Size: 24.2 MB (24158511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7356b461e22137b8d7713e06bf23fa5930c13ff60ff89a76b7196c188a8a08`  
		Last Modified: Wed, 22 Dec 2021 20:12:00 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:brie-windowsservercore-1809`

```console
$ docker pull traefik@sha256:acae7ced1a3294fe967f2e1e8d396840e91fbdfd749d6ced85884e308471a3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:brie-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f6cd3447fbb1dfcaa3582fb0a304f6a34f4fb770ac28f8210bd053888b6bf50
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738638539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588533eb932d8c260b9d6882222b501a3e930d8a2578b19fdf79a2f554346bcf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:32:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:32:16 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:32:19 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:32:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1277073e66653b947a55a8cfd8ffbe88f9519a0f06c88c11c9196354d2fb543`  
		Last Modified: Tue, 11 Jan 2022 18:34:57 GMT  
		Size: 27.0 MB (27048392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe8208ec331b73e29d6dbce63a950a0526bd90094e4302b1bbaceb8c980908`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9ed58f572b8f88d14c2540527b95641d559fb1c1fba2ecc25c72e5bfe415`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a1a799b0d8d278a16dda6bc4be628233f46b5ff8d89b097fd76a34d2b1aa15`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:2f603f8d3abe1dd3a4eb28960c55506be48293b41ea2c6ed4a4297c851a57a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:cb6c620b70f3981b2323cf759d452164e84ed6ce82c2a2a84e0df825a8428309
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29972198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd4bc25ad14d7c652b17d49804dfb99a9ed702faa006ac2f9bdf72c8716a15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 22:16:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 22:16:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 22:16:58 GMT
EXPOSE 80
# Wed, 22 Dec 2021 22:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 22:16:59 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 22:16:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f585f616a119577ed9e482bc2cffb1e83b76b09f5dbe8bd8245a6b9f8c29ed1`  
		Last Modified: Wed, 22 Dec 2021 22:17:37 GMT  
		Size: 26.5 MB (26471025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f598fe2b15ae64b945b5336fe57e028160d13c4e52ec2c8d538c951c20f69e`  
		Last Modified: Wed, 22 Dec 2021 22:17:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f1c9f63db180cf2dfdca8229e56f85389a73367a3995fccb1c3add288f21e12c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28172686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234a638e7f0d02ef0a807f5740cdd175613d99442d80f6caba8804466b6f1469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 19:09:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 19:09:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 19:09:27 GMT
EXPOSE 80
# Wed, 22 Dec 2021 19:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 19:09:28 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 19:09:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e98886206e7f64a9779b3489c82d9839a44bccf18be9747ffc8cf8359e214b`  
		Last Modified: Wed, 22 Dec 2021 19:11:58 GMT  
		Size: 24.9 MB (24853954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4b667e2a330d44a4e5f8bf80ae096df60ece9abe4a7d926062bbcd2126495`  
		Last Modified: Wed, 22 Dec 2021 19:11:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:43d5ae2e4cf69416d7364123e26c9e535079ba82e28cf18292f3e9c240ea014c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27556586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34574e935bdaf7af66692ba2b2085bf15015615a9eeed74b2568febd5959b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 20:10:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 20:10:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 20:10:01 GMT
EXPOSE 80
# Wed, 22 Dec 2021 20:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 20:10:03 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 20:10:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78551cc4d851ad8a96da3591e6e80f48913b89a1043a82e0e898b4fca661b305`  
		Last Modified: Wed, 22 Dec 2021 20:12:04 GMT  
		Size: 24.2 MB (24158511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7356b461e22137b8d7713e06bf23fa5930c13ff60ff89a76b7196c188a8a08`  
		Last Modified: Wed, 22 Dec 2021 20:12:00 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1a913ea8b21e3257a626ca50cf17972f60587a0e11206ffd0b77962179c5aadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f0cc2e765448d62b87e2093e7cddf4e6b64c02bca6c6930b7ebe7307f936691
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734441373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31705b6293bb21e22bea0ff456562b95b079f7741cd17b448a1f4113c7e7b633`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:33:48 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 11 Jan 2022 18:33:51 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:33:52 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:33:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f01ad1772364c9b4326d7171fc538f5fdd04b7d2037e7350fe5910b217bfdf9`  
		Last Modified: Tue, 11 Jan 2022 18:35:22 GMT  
		Size: 22.9 MB (22851160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec4aeedc20d74a474e364188e91d16eb0c7ce65e090f34a2f3aa3915b5c86e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80c5729d5b119720fa3073cd758b994417cb3b1f2c8842ccfb43a39b3671200`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458290c1b8da92b5b64631c6f63a0053d3b5c04d0172b022f5c24d6a443e687e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:rocamadour`

```console
$ docker pull traefik@sha256:44cbafeaa8d0387751ccb557a7738bb1d2a908cdd358e8acefcfcb8e8b9faf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:rocamadour` - linux; amd64

```console
$ docker pull traefik@sha256:d65d0be92a53c004a163cb35e4c0c31a58edebcef1de496a319b028fa2bd09a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30168792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c77ac9166db72d9e4f271680b434cb985f4659125da1c2222034612341133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 19:20:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 19:20:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 19:20:01 GMT
EXPOSE 80
# Mon, 20 Dec 2021 19:20:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 19:20:01 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 19:20:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95732e323f1180b16089b3709e32acdd925d45c058c88e3fd9a278f8ebf095a`  
		Last Modified: Mon, 20 Dec 2021 19:20:37 GMT  
		Size: 26.7 MB (26667619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37884b0fee928687a29eb238763446dec983cdb4b55cca61344a6b6b3d5a8739`  
		Last Modified: Mon, 20 Dec 2021 19:20:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9412c15369af505532c1ad0c0378858e69c5560577d3c4dd422a7eae780bebf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28356316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae4a6ab517da91a17d91e9cca6df953b502f957c4af15614219234360d27ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:54:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:54:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:54:34 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:54:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:54:35 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:54:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9a02ab1647767183c89cef77baf75a346b7c836766c7ba9d151931029fee8`  
		Last Modified: Mon, 20 Dec 2021 20:57:10 GMT  
		Size: 25.0 MB (25037585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d05989a6849f306b9d9e656d3adbcbc0ed81703b8eb04f5b1866dc81461c51`  
		Last Modified: Mon, 20 Dec 2021 20:56:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fef2273c4d6362f6f6a8731289199649a1371c47fb86832312a741b60f34ab51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27731175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff94a5e8b4283cbe7686990ac4b5491d757c3b95426c68306cbf29abdf5167c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:38:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:38:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:38:19 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:38:21 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:38:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13202376be157cfd94c1b46e9036d7c86c3d6141f948f8d24e9e5d13aabec7fc`  
		Last Modified: Mon, 20 Dec 2021 20:39:29 GMT  
		Size: 24.3 MB (24333099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a13b6a2df421f21f76b73016fac8a53c1f3beb98ab0dba482b91f3d9f305235`  
		Last Modified: Mon, 20 Dec 2021 20:39:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:rocamadour-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b847b8cd2aa9e9c483b6d54e77a6276536cbe15f85ca4f77fcb42d5ca26a9a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:rocamadour-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:2c2e9b3dac623411b3750becff04a1a55de68ce405b73a3f7e5e8a7e345941fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738841422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a3cc03e9f6c0ec5bb50241833d17ad495a6bffb77f8a35e81d3da283bba5b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:30:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:30:43 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:30:44 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2030cd81ffa233f949c1e5a83056069701ebb118f21dcfcbe387c0f462f3702`  
		Last Modified: Tue, 11 Jan 2022 18:34:34 GMT  
		Size: 27.3 MB (27251289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323285e35591d8353fda5a8100943aefaa5db24514f9c76f4a5ad73118c791b8`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b99bcd7b1ec339f6ad70787bfaf6c7f12e0f5d055abebe251993c55db49f56`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cab45e7657cd77f6eb771b157511d491e8982974da7717c50a59ac28491619`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1a913ea8b21e3257a626ca50cf17972f60587a0e11206ffd0b77962179c5aadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f0cc2e765448d62b87e2093e7cddf4e6b64c02bca6c6930b7ebe7307f936691
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734441373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31705b6293bb21e22bea0ff456562b95b079f7741cd17b448a1f4113c7e7b633`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:33:48 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 11 Jan 2022 18:33:51 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:33:52 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:33:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f01ad1772364c9b4326d7171fc538f5fdd04b7d2037e7350fe5910b217bfdf9`  
		Last Modified: Tue, 11 Jan 2022 18:35:22 GMT  
		Size: 22.9 MB (22851160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec4aeedc20d74a474e364188e91d16eb0c7ce65e090f34a2f3aa3915b5c86e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80c5729d5b119720fa3073cd758b994417cb3b1f2c8842ccfb43a39b3671200`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458290c1b8da92b5b64631c6f63a0053d3b5c04d0172b022f5c24d6a443e687e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34`

```console
$ docker pull traefik@sha256:16ab8f1f8facbfa34f11411735be42ca09cc207f4f607f874c0951659aeac258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:316eeccf5b0e15c7557194096f1b75b8f3ce3de0052c6ebe7c45b005bd53b366
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22612937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7608bd808d08bc0d844935c654371ee6693c80e036ed2c11c4a5ad3178d8e553`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 17:58:25 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 07:23:46 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:32:47 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 10 Dec 2021 21:32:48 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:48 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:32:48 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:32:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13e52be55f8d958b3ebb4e73685de5dd10ff4b4af613c4d23424519693aa01e0`  
		Last Modified: Tue, 05 Oct 2021 17:59:12 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a918f6229a44912f657372ae3d390880a3bf6c27e51417a093520abf943f47`  
		Last Modified: Sat, 13 Nov 2021 07:25:13 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51ca2df8b1b62bfda71acdff9512e649432f7669c2b4f58f50db456c5fa7b5b`  
		Last Modified: Fri, 10 Dec 2021 21:34:00 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4ae8110451cd8b856050c0519b9106085bf2fb213c1810b559effa377cc9176b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5d0502d4402e86fa35987d85b84ae56e01f0b4054937aea39094c4be01ea6a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 05 Oct 2021 00:02:38 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Sat, 13 Nov 2021 06:52:39 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 21:50:42 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 10 Dec 2021 21:50:43 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:43 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 21:50:44 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 21:50:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:611185932e68f8b41b94235c966a6c2d26bb4a0f053993c6e49edc01123213f9`  
		Last Modified: Tue, 05 Oct 2021 00:04:56 GMT  
		Size: 122.4 KB (122407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81282f8b9fcf1f821d7dab2ed1f6addbda565118cc5ee95d9de4ae8ff91333f`  
		Last Modified: Sat, 13 Nov 2021 06:55:43 GMT  
		Size: 328.6 KB (328578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3730ee17455103047e8a361f9e99218a36fcfc41b26fb92516fd9be41ba39c`  
		Last Modified: Fri, 10 Dec 2021 21:53:45 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:adc574c52a5b551c4d5ad2be0d2840be3053c2ea51530325497ea3b12cb9f585
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20582290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2a34f8b1feaaf314ac5500fe3f4d71ab33659cc44ca8e5389b8eb36d344b19`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Mon, 08 Nov 2021 20:23:04 GMT
COPY file:c8f727cb8b17c5a8735e609a9b9f333f20765e36c457d0557ed48693a6694880 in /etc/ssl/certs/ 
# Mon, 08 Nov 2021 20:23:05 GMT
COPY dir:c22cc1c2c366de443c999e78a53f0bde0b523a72b38a70fa92f5c6322439c95e in /usr/share/ 
# Fri, 10 Dec 2021 22:10:54 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 10 Dec 2021 22:10:54 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:55 GMT
VOLUME [/tmp]
# Fri, 10 Dec 2021 22:10:56 GMT
ENTRYPOINT ["/traefik"]
# Fri, 10 Dec 2021 22:10:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:078e101c84a7a75069b9c18efdfc2b24c9840aa136b34eb6e3a0ebe1b74d0a94`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 122.4 KB (122399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7a624fda7cabc945cc9d9f610f256d933b121fdafa2052d617cf3144bbe2aa`  
		Last Modified: Mon, 08 Nov 2021 20:24:37 GMT  
		Size: 328.5 KB (328545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3ecfc2ff53e207251e72b68f2570d2a5dae382ad897f8ad4c2811e482770d6`  
		Last Modified: Fri, 10 Dec 2021 22:12:29 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:1a913ea8b21e3257a626ca50cf17972f60587a0e11206ffd0b77962179c5aadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:v1.7.34-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f0cc2e765448d62b87e2093e7cddf4e6b64c02bca6c6930b7ebe7307f936691
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734441373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31705b6293bb21e22bea0ff456562b95b079f7741cd17b448a1f4113c7e7b633`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:33:48 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 11 Jan 2022 18:33:51 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:33:52 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:33:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f01ad1772364c9b4326d7171fc538f5fdd04b7d2037e7350fe5910b217bfdf9`  
		Last Modified: Tue, 11 Jan 2022 18:35:22 GMT  
		Size: 22.9 MB (22851160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec4aeedc20d74a474e364188e91d16eb0c7ce65e090f34a2f3aa3915b5c86e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80c5729d5b119720fa3073cd758b994417cb3b1f2c8842ccfb43a39b3671200`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.5 KB (1455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458290c1b8da92b5b64631c6f63a0053d3b5c04d0172b022f5c24d6a443e687e`  
		Last Modified: Tue, 11 Jan 2022 18:35:15 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5`

```console
$ docker pull traefik@sha256:2f603f8d3abe1dd3a4eb28960c55506be48293b41ea2c6ed4a4297c851a57a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.5` - linux; amd64

```console
$ docker pull traefik@sha256:cb6c620b70f3981b2323cf759d452164e84ed6ce82c2a2a84e0df825a8428309
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29972198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd4bc25ad14d7c652b17d49804dfb99a9ed702faa006ac2f9bdf72c8716a15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 22:16:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 22:16:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 22:16:58 GMT
EXPOSE 80
# Wed, 22 Dec 2021 22:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 22:16:59 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 22:16:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f585f616a119577ed9e482bc2cffb1e83b76b09f5dbe8bd8245a6b9f8c29ed1`  
		Last Modified: Wed, 22 Dec 2021 22:17:37 GMT  
		Size: 26.5 MB (26471025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f598fe2b15ae64b945b5336fe57e028160d13c4e52ec2c8d538c951c20f69e`  
		Last Modified: Wed, 22 Dec 2021 22:17:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f1c9f63db180cf2dfdca8229e56f85389a73367a3995fccb1c3add288f21e12c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28172686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234a638e7f0d02ef0a807f5740cdd175613d99442d80f6caba8804466b6f1469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 19:09:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 19:09:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 19:09:27 GMT
EXPOSE 80
# Wed, 22 Dec 2021 19:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 19:09:28 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 19:09:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e98886206e7f64a9779b3489c82d9839a44bccf18be9747ffc8cf8359e214b`  
		Last Modified: Wed, 22 Dec 2021 19:11:58 GMT  
		Size: 24.9 MB (24853954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4b667e2a330d44a4e5f8bf80ae096df60ece9abe4a7d926062bbcd2126495`  
		Last Modified: Wed, 22 Dec 2021 19:11:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:43d5ae2e4cf69416d7364123e26c9e535079ba82e28cf18292f3e9c240ea014c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27556586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34574e935bdaf7af66692ba2b2085bf15015615a9eeed74b2568febd5959b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 20:10:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 20:10:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 20:10:01 GMT
EXPOSE 80
# Wed, 22 Dec 2021 20:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 20:10:03 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 20:10:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78551cc4d851ad8a96da3591e6e80f48913b89a1043a82e0e898b4fca661b305`  
		Last Modified: Wed, 22 Dec 2021 20:12:04 GMT  
		Size: 24.2 MB (24158511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7356b461e22137b8d7713e06bf23fa5930c13ff60ff89a76b7196c188a8a08`  
		Last Modified: Wed, 22 Dec 2021 20:12:00 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:acae7ced1a3294fe967f2e1e8d396840e91fbdfd749d6ced85884e308471a3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:v2.5-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f6cd3447fbb1dfcaa3582fb0a304f6a34f4fb770ac28f8210bd053888b6bf50
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738638539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588533eb932d8c260b9d6882222b501a3e930d8a2578b19fdf79a2f554346bcf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:32:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:32:16 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:32:19 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:32:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1277073e66653b947a55a8cfd8ffbe88f9519a0f06c88c11c9196354d2fb543`  
		Last Modified: Tue, 11 Jan 2022 18:34:57 GMT  
		Size: 27.0 MB (27048392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe8208ec331b73e29d6dbce63a950a0526bd90094e4302b1bbaceb8c980908`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9ed58f572b8f88d14c2540527b95641d559fb1c1fba2ecc25c72e5bfe415`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a1a799b0d8d278a16dda6bc4be628233f46b5ff8d89b097fd76a34d2b1aa15`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5.6`

```console
$ docker pull traefik@sha256:2f603f8d3abe1dd3a4eb28960c55506be48293b41ea2c6ed4a4297c851a57a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.5.6` - linux; amd64

```console
$ docker pull traefik@sha256:cb6c620b70f3981b2323cf759d452164e84ed6ce82c2a2a84e0df825a8428309
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29972198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd4bc25ad14d7c652b17d49804dfb99a9ed702faa006ac2f9bdf72c8716a15d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 22:16:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 22:16:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 22:16:58 GMT
EXPOSE 80
# Wed, 22 Dec 2021 22:16:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 22:16:59 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 22:16:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f585f616a119577ed9e482bc2cffb1e83b76b09f5dbe8bd8245a6b9f8c29ed1`  
		Last Modified: Wed, 22 Dec 2021 22:17:37 GMT  
		Size: 26.5 MB (26471025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f598fe2b15ae64b945b5336fe57e028160d13c4e52ec2c8d538c951c20f69e`  
		Last Modified: Wed, 22 Dec 2021 22:17:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f1c9f63db180cf2dfdca8229e56f85389a73367a3995fccb1c3add288f21e12c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28172686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234a638e7f0d02ef0a807f5740cdd175613d99442d80f6caba8804466b6f1469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 19:09:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 19:09:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 19:09:27 GMT
EXPOSE 80
# Wed, 22 Dec 2021 19:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 19:09:28 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 19:09:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e98886206e7f64a9779b3489c82d9839a44bccf18be9747ffc8cf8359e214b`  
		Last Modified: Wed, 22 Dec 2021 19:11:58 GMT  
		Size: 24.9 MB (24853954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4b667e2a330d44a4e5f8bf80ae096df60ece9abe4a7d926062bbcd2126495`  
		Last Modified: Wed, 22 Dec 2021 19:11:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.5.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:43d5ae2e4cf69416d7364123e26c9e535079ba82e28cf18292f3e9c240ea014c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27556586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34574e935bdaf7af66692ba2b2085bf15015615a9eeed74b2568febd5959b37`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 22 Dec 2021 20:10:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 22 Dec 2021 20:10:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 22 Dec 2021 20:10:01 GMT
EXPOSE 80
# Wed, 22 Dec 2021 20:10:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Dec 2021 20:10:03 GMT
CMD ["traefik"]
# Wed, 22 Dec 2021 20:10:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78551cc4d851ad8a96da3591e6e80f48913b89a1043a82e0e898b4fca661b305`  
		Last Modified: Wed, 22 Dec 2021 20:12:04 GMT  
		Size: 24.2 MB (24158511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7356b461e22137b8d7713e06bf23fa5930c13ff60ff89a76b7196c188a8a08`  
		Last Modified: Wed, 22 Dec 2021 20:12:00 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.5.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:acae7ced1a3294fe967f2e1e8d396840e91fbdfd749d6ced85884e308471a3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:v2.5.6-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f6cd3447fbb1dfcaa3582fb0a304f6a34f4fb770ac28f8210bd053888b6bf50
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738638539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588533eb932d8c260b9d6882222b501a3e930d8a2578b19fdf79a2f554346bcf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:32:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:32:16 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:32:19 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:32:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1277073e66653b947a55a8cfd8ffbe88f9519a0f06c88c11c9196354d2fb543`  
		Last Modified: Tue, 11 Jan 2022 18:34:57 GMT  
		Size: 27.0 MB (27048392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe8208ec331b73e29d6dbce63a950a0526bd90094e4302b1bbaceb8c980908`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9ed58f572b8f88d14c2540527b95641d559fb1c1fba2ecc25c72e5bfe415`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a1a799b0d8d278a16dda6bc4be628233f46b5ff8d89b097fd76a34d2b1aa15`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6`

```console
$ docker pull traefik@sha256:44cbafeaa8d0387751ccb557a7738bb1d2a908cdd358e8acefcfcb8e8b9faf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.6` - linux; amd64

```console
$ docker pull traefik@sha256:d65d0be92a53c004a163cb35e4c0c31a58edebcef1de496a319b028fa2bd09a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30168792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c77ac9166db72d9e4f271680b434cb985f4659125da1c2222034612341133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 19:20:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 19:20:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 19:20:01 GMT
EXPOSE 80
# Mon, 20 Dec 2021 19:20:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 19:20:01 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 19:20:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95732e323f1180b16089b3709e32acdd925d45c058c88e3fd9a278f8ebf095a`  
		Last Modified: Mon, 20 Dec 2021 19:20:37 GMT  
		Size: 26.7 MB (26667619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37884b0fee928687a29eb238763446dec983cdb4b55cca61344a6b6b3d5a8739`  
		Last Modified: Mon, 20 Dec 2021 19:20:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9412c15369af505532c1ad0c0378858e69c5560577d3c4dd422a7eae780bebf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28356316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae4a6ab517da91a17d91e9cca6df953b502f957c4af15614219234360d27ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:54:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:54:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:54:34 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:54:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:54:35 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:54:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9a02ab1647767183c89cef77baf75a346b7c836766c7ba9d151931029fee8`  
		Last Modified: Mon, 20 Dec 2021 20:57:10 GMT  
		Size: 25.0 MB (25037585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d05989a6849f306b9d9e656d3adbcbc0ed81703b8eb04f5b1866dc81461c51`  
		Last Modified: Mon, 20 Dec 2021 20:56:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fef2273c4d6362f6f6a8731289199649a1371c47fb86832312a741b60f34ab51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27731175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff94a5e8b4283cbe7686990ac4b5491d757c3b95426c68306cbf29abdf5167c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:38:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:38:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:38:19 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:38:21 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:38:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13202376be157cfd94c1b46e9036d7c86c3d6141f948f8d24e9e5d13aabec7fc`  
		Last Modified: Mon, 20 Dec 2021 20:39:29 GMT  
		Size: 24.3 MB (24333099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a13b6a2df421f21f76b73016fac8a53c1f3beb98ab0dba482b91f3d9f305235`  
		Last Modified: Mon, 20 Dec 2021 20:39:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b847b8cd2aa9e9c483b6d54e77a6276536cbe15f85ca4f77fcb42d5ca26a9a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:v2.6-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:2c2e9b3dac623411b3750becff04a1a55de68ce405b73a3f7e5e8a7e345941fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738841422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a3cc03e9f6c0ec5bb50241833d17ad495a6bffb77f8a35e81d3da283bba5b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:30:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:30:43 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:30:44 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2030cd81ffa233f949c1e5a83056069701ebb118f21dcfcbe387c0f462f3702`  
		Last Modified: Tue, 11 Jan 2022 18:34:34 GMT  
		Size: 27.3 MB (27251289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323285e35591d8353fda5a8100943aefaa5db24514f9c76f4a5ad73118c791b8`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b99bcd7b1ec339f6ad70787bfaf6c7f12e0f5d055abebe251993c55db49f56`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cab45e7657cd77f6eb771b157511d491e8982974da7717c50a59ac28491619`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6.0-rc1`

```console
$ docker pull traefik@sha256:44cbafeaa8d0387751ccb557a7738bb1d2a908cdd358e8acefcfcb8e8b9faf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v2.6.0-rc1` - linux; amd64

```console
$ docker pull traefik@sha256:d65d0be92a53c004a163cb35e4c0c31a58edebcef1de496a319b028fa2bd09a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30168792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c77ac9166db72d9e4f271680b434cb985f4659125da1c2222034612341133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 19:20:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 19:20:01 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 19:20:01 GMT
EXPOSE 80
# Mon, 20 Dec 2021 19:20:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 19:20:01 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 19:20:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95732e323f1180b16089b3709e32acdd925d45c058c88e3fd9a278f8ebf095a`  
		Last Modified: Mon, 20 Dec 2021 19:20:37 GMT  
		Size: 26.7 MB (26667619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37884b0fee928687a29eb238763446dec983cdb4b55cca61344a6b6b3d5a8739`  
		Last Modified: Mon, 20 Dec 2021 19:20:33 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6.0-rc1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:9412c15369af505532c1ad0c0378858e69c5560577d3c4dd422a7eae780bebf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28356316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae4a6ab517da91a17d91e9cca6df953b502f957c4af15614219234360d27ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:54:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:54:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:54:34 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:54:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:54:35 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:54:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a9a02ab1647767183c89cef77baf75a346b7c836766c7ba9d151931029fee8`  
		Last Modified: Mon, 20 Dec 2021 20:57:10 GMT  
		Size: 25.0 MB (25037585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d05989a6849f306b9d9e656d3adbcbc0ed81703b8eb04f5b1866dc81461c51`  
		Last Modified: Mon, 20 Dec 2021 20:56:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6.0-rc1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fef2273c4d6362f6f6a8731289199649a1371c47fb86832312a741b60f34ab51
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27731175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff94a5e8b4283cbe7686990ac4b5491d757c3b95426c68306cbf29abdf5167c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 20 Dec 2021 20:38:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 20 Dec 2021 20:38:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 20 Dec 2021 20:38:19 GMT
EXPOSE 80
# Mon, 20 Dec 2021 20:38:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Dec 2021 20:38:21 GMT
CMD ["traefik"]
# Mon, 20 Dec 2021 20:38:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13202376be157cfd94c1b46e9036d7c86c3d6141f948f8d24e9e5d13aabec7fc`  
		Last Modified: Mon, 20 Dec 2021 20:39:29 GMT  
		Size: 24.3 MB (24333099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a13b6a2df421f21f76b73016fac8a53c1f3beb98ab0dba482b91f3d9f305235`  
		Last Modified: Mon, 20 Dec 2021 20:39:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6.0-rc1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b847b8cd2aa9e9c483b6d54e77a6276536cbe15f85ca4f77fcb42d5ca26a9a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:v2.6.0-rc1-windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:2c2e9b3dac623411b3750becff04a1a55de68ce405b73a3f7e5e8a7e345941fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738841422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a3cc03e9f6c0ec5bb50241833d17ad495a6bffb77f8a35e81d3da283bba5b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:30:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.0-rc1/traefik_v2.6.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:30:43 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:30:44 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:30:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2030cd81ffa233f949c1e5a83056069701ebb118f21dcfcbe387c0f462f3702`  
		Last Modified: Tue, 11 Jan 2022 18:34:34 GMT  
		Size: 27.3 MB (27251289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323285e35591d8353fda5a8100943aefaa5db24514f9c76f4a5ad73118c791b8`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b99bcd7b1ec339f6ad70787bfaf6c7f12e0f5d055abebe251993c55db49f56`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cab45e7657cd77f6eb771b157511d491e8982974da7717c50a59ac28491619`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:acae7ced1a3294fe967f2e1e8d396840e91fbdfd749d6ced85884e308471a3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull traefik@sha256:0f6cd3447fbb1dfcaa3582fb0a304f6a34f4fb770ac28f8210bd053888b6bf50
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738638539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588533eb932d8c260b9d6882222b501a3e930d8a2578b19fdf79a2f554346bcf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 05:42:07 GMT
RUN Install update 1809-amd64
# Tue, 11 Jan 2022 18:28:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 18:32:15 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.5.6/traefik_v2.5.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Jan 2022 18:32:16 GMT
EXPOSE 80
# Tue, 11 Jan 2022 18:32:19 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Jan 2022 18:32:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ca87ac6c02d88482e9b4bf7c5b3be47ddaa1940332b4730a0b1384b4efb987cf`  
		Size: 993.3 MB (993251600 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d817badb08ee5a6edbd47efdaa8f9393db0c59d351be8a78deda5364ab70de7f`  
		Last Modified: Tue, 11 Jan 2022 18:34:27 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1277073e66653b947a55a8cfd8ffbe88f9519a0f06c88c11c9196354d2fb543`  
		Last Modified: Tue, 11 Jan 2022 18:34:57 GMT  
		Size: 27.0 MB (27048392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fe8208ec331b73e29d6dbce63a950a0526bd90094e4302b1bbaceb8c980908`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129e9ed58f572b8f88d14c2540527b95641d559fb1c1fba2ecc25c72e5bfe415`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a1a799b0d8d278a16dda6bc4be628233f46b5ff8d89b097fd76a34d2b1aa15`  
		Last Modified: Tue, 11 Jan 2022 18:34:51 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
