<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:1.7`](#traefik17)
-	[`traefik:1.7-alpine`](#traefik17-alpine)
-	[`traefik:1.7-windowsservercore-1809`](#traefik17-windowsservercore-1809)
-	[`traefik:1.7.34`](#traefik1734)
-	[`traefik:1.7.34-alpine`](#traefik1734-alpine)
-	[`traefik:1.7.34-windowsservercore-1809`](#traefik1734-windowsservercore-1809)
-	[`traefik:2.6`](#traefik26)
-	[`traefik:2.6-windowsservercore-1809`](#traefik26-windowsservercore-1809)
-	[`traefik:2.6.2`](#traefik262)
-	[`traefik:2.6.2-windowsservercore-1809`](#traefik262-windowsservercore-1809)
-	[`traefik:2.7`](#traefik27)
-	[`traefik:2.7-windowsservercore-1809`](#traefik27-windowsservercore-1809)
-	[`traefik:2.7.0-rc1`](#traefik270-rc1)
-	[`traefik:2.7.0-rc1-windowsservercore-1809`](#traefik270-rc1-windowsservercore-1809)
-	[`traefik:epoisses`](#traefikepoisses)
-	[`traefik:epoisses-windowsservercore-1809`](#traefikepoisses-windowsservercore-1809)
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
-	[`traefik:v2.6`](#traefikv26)
-	[`traefik:v2.6-windowsservercore-1809`](#traefikv26-windowsservercore-1809)
-	[`traefik:v2.6.2`](#traefikv262)
-	[`traefik:v2.6.2-windowsservercore-1809`](#traefikv262-windowsservercore-1809)
-	[`traefik:v2.7`](#traefikv27)
-	[`traefik:v2.7-windowsservercore-1809`](#traefikv27-windowsservercore-1809)
-	[`traefik:v2.7.0-rc1`](#traefikv270-rc1)
-	[`traefik:v2.7.0-rc1-windowsservercore-1809`](#traefikv270-rc1-windowsservercore-1809)
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
$ docker pull traefik@sha256:8ac75422d559a55193d20df11116ea951ad962f7dcdf3bd76a51f81f460de821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:04c41c7c3ff03d006e93029fb6bce95a448a32900c47487cf2f54f4df2d42f56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25645268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb8c5f993e88b67da6b9d2b5ee0a09e7f6a576c70e19f8bd1031adae54418ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 18 Mar 2022 06:23:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 18 Mar 2022 06:23:24 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 18 Mar 2022 06:23:24 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Mar 2022 06:23:24 GMT
CMD ["traefik"]
# Fri, 18 Mar 2022 06:23:25 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9a06ba42895ffa47fb412ee9c0fe6cc5c33d4bf08ca4a76e74f7040bc82206`  
		Last Modified: Fri, 18 Mar 2022 06:24:42 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b266beb8763fa8eeb482f01673624fb468758ac98bb28cc16881d8f94e1f54c`  
		Last Modified: Fri, 18 Mar 2022 06:24:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:08be027ed453b435111cb912908324ee1f5f0d77db60b6d6f9f10003d2c62674
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23925625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fbe3dd0a206256fa43655ee4af71da94003b6377978bc54ccdb219452f1bcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 22:45:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 22:45:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 22:45:04 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:45:05 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 22:45:06 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244182210987061535c909a9a2aace43df0eb4ee95953b8813c3792dd4ba5b37`  
		Last Modified: Thu, 17 Mar 2022 22:47:55 GMT  
		Size: 20.6 MB (20623423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb981a93f73996a8309c5494870b9e83074dae0470e145590d2148af320281cf`  
		Last Modified: Thu, 17 Mar 2022 22:47:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1e7c544b79ed103ad6d22cd9941ca3416e02897a9cb7f75120f6fd5f1949d90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23515893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a718e3a556a699675cb6d5655875c7240cd58d718536719147125b9d171870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 21:06:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 21:06:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 21:06:55 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 21:06:57 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 21:06:58 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe57c71a6e6bc8b2eda9db22fd05c14079977728ba28062721c5d71106b23ab9`  
		Last Modified: Thu, 17 Mar 2022 21:08:21 GMT  
		Size: 20.1 MB (20131382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535366a8854793a298d798c23544e4ad0849c13ce51c5687ad00f9864bebe75a`  
		Last Modified: Thu, 17 Mar 2022 21:08:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:85ffe3d43fd4929a0e48d226e018af240fbbd8ea9a03685f74f1c78c432f85b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:67d210fa3d7dcb1ebc3b3b5f3bfdaac7d18195e1bb2b83fa2c1b1f48d09b08dd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738303983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ebd04310fbdd68b4e7225310f8a6f2dec3a0330af0d02b74a9a0e35b79945b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:53:09 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Mar 2022 18:53:10 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:53:11 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Mar 2022 18:53:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd63edc5d2bde654b771ee58c8e9bb78539127758e862053223f402d3eaea68`  
		Last Modified: Wed, 09 Mar 2022 18:54:50 GMT  
		Size: 22.8 MB (22845783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cefe3e1f9703a33ffdf92a9c03b8a4738222fe08ea99aded6416f848aa300e9`  
		Last Modified: Wed, 09 Mar 2022 18:54:27 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f3b18eb0ddb1cb4c6b01a2abc4127403c6a67c630a8c05c6be5f43ab74acc`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bcba10ab84d161e2dc32a48f6bc15da23d8aabdb22bbf4a89499ce18583d46`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1389 bytes)  
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
$ docker pull traefik@sha256:8ac75422d559a55193d20df11116ea951ad962f7dcdf3bd76a51f81f460de821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:04c41c7c3ff03d006e93029fb6bce95a448a32900c47487cf2f54f4df2d42f56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25645268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb8c5f993e88b67da6b9d2b5ee0a09e7f6a576c70e19f8bd1031adae54418ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 18 Mar 2022 06:23:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 18 Mar 2022 06:23:24 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 18 Mar 2022 06:23:24 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Mar 2022 06:23:24 GMT
CMD ["traefik"]
# Fri, 18 Mar 2022 06:23:25 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9a06ba42895ffa47fb412ee9c0fe6cc5c33d4bf08ca4a76e74f7040bc82206`  
		Last Modified: Fri, 18 Mar 2022 06:24:42 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b266beb8763fa8eeb482f01673624fb468758ac98bb28cc16881d8f94e1f54c`  
		Last Modified: Fri, 18 Mar 2022 06:24:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:08be027ed453b435111cb912908324ee1f5f0d77db60b6d6f9f10003d2c62674
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23925625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fbe3dd0a206256fa43655ee4af71da94003b6377978bc54ccdb219452f1bcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 22:45:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 22:45:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 22:45:04 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:45:05 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 22:45:06 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244182210987061535c909a9a2aace43df0eb4ee95953b8813c3792dd4ba5b37`  
		Last Modified: Thu, 17 Mar 2022 22:47:55 GMT  
		Size: 20.6 MB (20623423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb981a93f73996a8309c5494870b9e83074dae0470e145590d2148af320281cf`  
		Last Modified: Thu, 17 Mar 2022 22:47:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1e7c544b79ed103ad6d22cd9941ca3416e02897a9cb7f75120f6fd5f1949d90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23515893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a718e3a556a699675cb6d5655875c7240cd58d718536719147125b9d171870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 21:06:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 21:06:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 21:06:55 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 21:06:57 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 21:06:58 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe57c71a6e6bc8b2eda9db22fd05c14079977728ba28062721c5d71106b23ab9`  
		Last Modified: Thu, 17 Mar 2022 21:08:21 GMT  
		Size: 20.1 MB (20131382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535366a8854793a298d798c23544e4ad0849c13ce51c5687ad00f9864bebe75a`  
		Last Modified: Thu, 17 Mar 2022 21:08:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:85ffe3d43fd4929a0e48d226e018af240fbbd8ea9a03685f74f1c78c432f85b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:1.7.34-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:67d210fa3d7dcb1ebc3b3b5f3bfdaac7d18195e1bb2b83fa2c1b1f48d09b08dd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738303983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ebd04310fbdd68b4e7225310f8a6f2dec3a0330af0d02b74a9a0e35b79945b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:53:09 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Mar 2022 18:53:10 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:53:11 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Mar 2022 18:53:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd63edc5d2bde654b771ee58c8e9bb78539127758e862053223f402d3eaea68`  
		Last Modified: Wed, 09 Mar 2022 18:54:50 GMT  
		Size: 22.8 MB (22845783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cefe3e1f9703a33ffdf92a9c03b8a4738222fe08ea99aded6416f848aa300e9`  
		Last Modified: Wed, 09 Mar 2022 18:54:27 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f3b18eb0ddb1cb4c6b01a2abc4127403c6a67c630a8c05c6be5f43ab74acc`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bcba10ab84d161e2dc32a48f6bc15da23d8aabdb22bbf4a89499ce18583d46`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6`

```console
$ docker pull traefik@sha256:860fc052d2b48c0b05b76c47baeb6fdeea316b8950afc1e230e51f11e2b71157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.6` - linux; amd64

```console
$ docker pull traefik@sha256:b8ca739c8361611a964dfa5f023750de17f34e342997c50dbdfb5a38e3450edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30339417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0dc6675f5f00f8e256dd10f2ae3a6e9c72e101fefe340a7578c5cebef1e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:08 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:08 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4fa573d59a67acc4371181255191bdb4b7076976c4b419df716d42b807114`  
		Last Modified: Fri, 25 Mar 2022 01:37:01 GMT  
		Size: 26.9 MB (26856210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff15934093e3aba34a0e8ff6dc63870642eb043f5fa6a0601211910e54994d76`  
		Last Modified: Fri, 25 Mar 2022 01:36:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:473045fcf57e944e78c7985cd420f2aa74600a5c32625153a19763461403d67a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f6c8b8c1db1b0d145e6a3e42d9cf31d572968bafe60205235c70e31905e20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:49 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:50 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d15861ba3656bac0bf7350e50bc7965ab614fa0d0d2b2d2363d7c537272498`  
		Last Modified: Thu, 24 Mar 2022 23:05:53 GMT  
		Size: 25.2 MB (25213677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe35863b15e69b331cb86aec04d56420be2c4a8d2d7907fa5c6a5c924d682b`  
		Last Modified: Thu, 24 Mar 2022 23:05:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a4f13c83df426b98306e592a0c084a38eb6205329cd3a6c5d6961f855a4bf375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27885391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef507d0470ecf849d69dba8f5f48bbeb0aaef90c5fe1f2785b6ae52565f264e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:52 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:54 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bcc34080ce16bec6deac23ee8508c2109ec4b6ed36cc90d1ed88b86217f99`  
		Last Modified: Fri, 25 Mar 2022 02:27:21 GMT  
		Size: 24.5 MB (24500880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2737b6b44221cb2c0f986312da01294c49ccddef5a6cbcb23f7e4da0adc987`  
		Last Modified: Fri, 25 Mar 2022 02:27:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6` - linux; s390x

```console
$ docker pull traefik@sha256:0ad3044a0cad96d56ddbc33d49951d1fba2dcd526648e4d8603a4ae5b982306b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29138079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c233c314a609dec253c443a92364cf96858016644c8212037d325faa58d0f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:58 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:58 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a795666c55ec202853627c2c7d338884cece42772fb6c12f0ac380ff558944`  
		Last Modified: Fri, 25 Mar 2022 00:32:00 GMT  
		Size: 25.9 MB (25860036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbf4dda32a155a274fd925f019944c1617ce43b9cc288bb3931e793acf041b`  
		Last Modified: Fri, 25 Mar 2022 00:31:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:65434d6814d7057964abe547d596828914443859613e8babbebc8256218a8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:2.6-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:8f74813cea5a837efd6b0233cc8f8e1ba58dbc017e9063dd6e0f41f0e337d3f2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742900692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de1050781331302a08d35b247b99ed30e38f7478ed59f9aaa3d5591766a7a5c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:17:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:17:35 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:17:36 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:17:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce6f4fdd887fab65f610dfbbd9047a42d1f5010d54dd773da1960e0be81d18c`  
		Last Modified: Thu, 24 Mar 2022 23:19:06 GMT  
		Size: 27.4 MB (27442514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194905ba9de641fb766068bd0d2adc5e44d3ad51a6895ac0769593315f272eda`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef3d84d9f2492e9648efc00341ac09f2f323c9cd87485bf58b0e2f520380b1`  
		Last Modified: Thu, 24 Mar 2022 23:19:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107216789aeb5347d5ac3e42177fae7ebfd271935c9b48bed8f8d78dddee204`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6.2`

```console
$ docker pull traefik@sha256:860fc052d2b48c0b05b76c47baeb6fdeea316b8950afc1e230e51f11e2b71157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.6.2` - linux; amd64

```console
$ docker pull traefik@sha256:b8ca739c8361611a964dfa5f023750de17f34e342997c50dbdfb5a38e3450edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30339417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0dc6675f5f00f8e256dd10f2ae3a6e9c72e101fefe340a7578c5cebef1e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:08 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:08 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4fa573d59a67acc4371181255191bdb4b7076976c4b419df716d42b807114`  
		Last Modified: Fri, 25 Mar 2022 01:37:01 GMT  
		Size: 26.9 MB (26856210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff15934093e3aba34a0e8ff6dc63870642eb043f5fa6a0601211910e54994d76`  
		Last Modified: Fri, 25 Mar 2022 01:36:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:473045fcf57e944e78c7985cd420f2aa74600a5c32625153a19763461403d67a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f6c8b8c1db1b0d145e6a3e42d9cf31d572968bafe60205235c70e31905e20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:49 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:50 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d15861ba3656bac0bf7350e50bc7965ab614fa0d0d2b2d2363d7c537272498`  
		Last Modified: Thu, 24 Mar 2022 23:05:53 GMT  
		Size: 25.2 MB (25213677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe35863b15e69b331cb86aec04d56420be2c4a8d2d7907fa5c6a5c924d682b`  
		Last Modified: Thu, 24 Mar 2022 23:05:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a4f13c83df426b98306e592a0c084a38eb6205329cd3a6c5d6961f855a4bf375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27885391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef507d0470ecf849d69dba8f5f48bbeb0aaef90c5fe1f2785b6ae52565f264e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:52 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:54 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bcc34080ce16bec6deac23ee8508c2109ec4b6ed36cc90d1ed88b86217f99`  
		Last Modified: Fri, 25 Mar 2022 02:27:21 GMT  
		Size: 24.5 MB (24500880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2737b6b44221cb2c0f986312da01294c49ccddef5a6cbcb23f7e4da0adc987`  
		Last Modified: Fri, 25 Mar 2022 02:27:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.6.2` - linux; s390x

```console
$ docker pull traefik@sha256:0ad3044a0cad96d56ddbc33d49951d1fba2dcd526648e4d8603a4ae5b982306b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29138079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c233c314a609dec253c443a92364cf96858016644c8212037d325faa58d0f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:58 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:58 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a795666c55ec202853627c2c7d338884cece42772fb6c12f0ac380ff558944`  
		Last Modified: Fri, 25 Mar 2022 00:32:00 GMT  
		Size: 25.9 MB (25860036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbf4dda32a155a274fd925f019944c1617ce43b9cc288bb3931e793acf041b`  
		Last Modified: Fri, 25 Mar 2022 00:31:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.6.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:65434d6814d7057964abe547d596828914443859613e8babbebc8256218a8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:2.6.2-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:8f74813cea5a837efd6b0233cc8f8e1ba58dbc017e9063dd6e0f41f0e337d3f2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742900692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de1050781331302a08d35b247b99ed30e38f7478ed59f9aaa3d5591766a7a5c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:17:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:17:35 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:17:36 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:17:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce6f4fdd887fab65f610dfbbd9047a42d1f5010d54dd773da1960e0be81d18c`  
		Last Modified: Thu, 24 Mar 2022 23:19:06 GMT  
		Size: 27.4 MB (27442514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194905ba9de641fb766068bd0d2adc5e44d3ad51a6895ac0769593315f272eda`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef3d84d9f2492e9648efc00341ac09f2f323c9cd87485bf58b0e2f520380b1`  
		Last Modified: Thu, 24 Mar 2022 23:19:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107216789aeb5347d5ac3e42177fae7ebfd271935c9b48bed8f8d78dddee204`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.7`

```console
$ docker pull traefik@sha256:0c4ffaae9a318156d54fe26708819b61eaca3e024b52e899f0eaec25fc8c7e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.7` - linux; amd64

```console
$ docker pull traefik@sha256:20bfd389c3edae915394054bfe49f1d3aee4a806cbb6092f1c99b3add07bf1b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39992d581315a0b4b88f1e398c91dc4fc82ac4d5e4585f6b595c1ca74cd095c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:02 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:02 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdc75d2cb9ce1d3a6d44a3113d73337e408229f53699ccb417ca658b67a31bc`  
		Last Modified: Fri, 25 Mar 2022 01:36:41 GMT  
		Size: 27.4 MB (27394827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb17bd7149a04c28c3479b82ba24f491312b5e98d4f7fd7dd95d50685430be2`  
		Last Modified: Fri, 25 Mar 2022 01:36:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6559ba9320b3bc7bdbfacc86318d152c40350fb98bcccf8d9672844e15110426
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28985121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de721efb2e4bdc486928aaff68345cc5f0781bf7e3712aaf7a661c5bf0d550e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:24 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:26 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab9a8bb707f561dcd006c6c7e3d8b74f4010b711dbfc2b2cfe9922c7ce8975`  
		Last Modified: Thu, 24 Mar 2022 23:05:13 GMT  
		Size: 25.7 MB (25682919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef4ee5181ca8f86dc5e5543aa574a902b87e1fba760958cd65b77d177c2466`  
		Last Modified: Thu, 24 Mar 2022 23:04:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d857e522cbb1d2704be8e7455dae9d53943f304786171f2c1fa030d73121432e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28364399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985d429d196f31f082d4ce2802c33fed48027bf9ab84e6516926e53091e163`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:38 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:40 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d19cd8203c75d96b65bcb8e88efa57a03f46ae016db6f2bd9ae0834cc459bf`  
		Last Modified: Fri, 25 Mar 2022 02:26:56 GMT  
		Size: 25.0 MB (24979888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd8f6940877a3a5261afd917b904f04430958a88a70505509cde1772d4c50db`  
		Last Modified: Fri, 25 Mar 2022 02:26:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.7` - linux; s390x

```console
$ docker pull traefik@sha256:09f52f8e5cf8dc3b0b0d25c12a99525769fc1214b978c8c4c6f1046ce13378da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29651905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7669e71c0dd08df6a88e4fe7f4192dcd4316a3880160c55bff11932ba06b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:46 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:46 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d2f51aa128fa862dd0743f43958f7cd6f649bf5722880ca504c9dc31052475`  
		Last Modified: Fri, 25 Mar 2022 00:31:41 GMT  
		Size: 26.4 MB (26373860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625ffde3f2367f11b2beb2d81d847d0703e3960e1acda315768539670cb3d8b4`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:02cb9628336c1bf73cfac41139e2293027287239ae93ac5030aa9132aeda0d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:2.7-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:47de1bfb0bae1a4ee272e93d523b8ba99781128c9c316dd2802432fe8b1aa300
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2743445028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d74c6ff9fd0ef0716d30ef3f47b96a6d81de3ee295920b148e8264be305842b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:16:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:16:23 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:16:24 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:16:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402d6b88042d7c0947353009ce4d477073e2736a9f31534244d33cf3420d459`  
		Last Modified: Thu, 24 Mar 2022 23:18:44 GMT  
		Size: 28.0 MB (27986759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76163e7d770a4111be892c0857a408bad2a2a6ab1acd826d443abe36b71d53cb`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfd6950346955cbf1855212200aaee09ed23996558944c2547f1c1f656d8c96`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15197f7b1ac7bc1c0ec20983eac3e25094ba3d991969d2785f3ae76e95f1345d`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.7.0-rc1`

```console
$ docker pull traefik@sha256:0c4ffaae9a318156d54fe26708819b61eaca3e024b52e899f0eaec25fc8c7e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.7.0-rc1` - linux; amd64

```console
$ docker pull traefik@sha256:20bfd389c3edae915394054bfe49f1d3aee4a806cbb6092f1c99b3add07bf1b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39992d581315a0b4b88f1e398c91dc4fc82ac4d5e4585f6b595c1ca74cd095c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:02 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:02 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdc75d2cb9ce1d3a6d44a3113d73337e408229f53699ccb417ca658b67a31bc`  
		Last Modified: Fri, 25 Mar 2022 01:36:41 GMT  
		Size: 27.4 MB (27394827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb17bd7149a04c28c3479b82ba24f491312b5e98d4f7fd7dd95d50685430be2`  
		Last Modified: Fri, 25 Mar 2022 01:36:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.7.0-rc1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6559ba9320b3bc7bdbfacc86318d152c40350fb98bcccf8d9672844e15110426
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28985121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de721efb2e4bdc486928aaff68345cc5f0781bf7e3712aaf7a661c5bf0d550e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:24 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:26 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab9a8bb707f561dcd006c6c7e3d8b74f4010b711dbfc2b2cfe9922c7ce8975`  
		Last Modified: Thu, 24 Mar 2022 23:05:13 GMT  
		Size: 25.7 MB (25682919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef4ee5181ca8f86dc5e5543aa574a902b87e1fba760958cd65b77d177c2466`  
		Last Modified: Thu, 24 Mar 2022 23:04:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.7.0-rc1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d857e522cbb1d2704be8e7455dae9d53943f304786171f2c1fa030d73121432e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28364399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985d429d196f31f082d4ce2802c33fed48027bf9ab84e6516926e53091e163`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:38 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:40 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d19cd8203c75d96b65bcb8e88efa57a03f46ae016db6f2bd9ae0834cc459bf`  
		Last Modified: Fri, 25 Mar 2022 02:26:56 GMT  
		Size: 25.0 MB (24979888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd8f6940877a3a5261afd917b904f04430958a88a70505509cde1772d4c50db`  
		Last Modified: Fri, 25 Mar 2022 02:26:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.7.0-rc1` - linux; s390x

```console
$ docker pull traefik@sha256:09f52f8e5cf8dc3b0b0d25c12a99525769fc1214b978c8c4c6f1046ce13378da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29651905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7669e71c0dd08df6a88e4fe7f4192dcd4316a3880160c55bff11932ba06b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:46 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:46 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d2f51aa128fa862dd0743f43958f7cd6f649bf5722880ca504c9dc31052475`  
		Last Modified: Fri, 25 Mar 2022 00:31:41 GMT  
		Size: 26.4 MB (26373860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625ffde3f2367f11b2beb2d81d847d0703e3960e1acda315768539670cb3d8b4`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.7.0-rc1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:02cb9628336c1bf73cfac41139e2293027287239ae93ac5030aa9132aeda0d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:2.7.0-rc1-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:47de1bfb0bae1a4ee272e93d523b8ba99781128c9c316dd2802432fe8b1aa300
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2743445028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d74c6ff9fd0ef0716d30ef3f47b96a6d81de3ee295920b148e8264be305842b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:16:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:16:23 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:16:24 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:16:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402d6b88042d7c0947353009ce4d477073e2736a9f31534244d33cf3420d459`  
		Last Modified: Thu, 24 Mar 2022 23:18:44 GMT  
		Size: 28.0 MB (27986759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76163e7d770a4111be892c0857a408bad2a2a6ab1acd826d443abe36b71d53cb`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfd6950346955cbf1855212200aaee09ed23996558944c2547f1c1f656d8c96`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15197f7b1ac7bc1c0ec20983eac3e25094ba3d991969d2785f3ae76e95f1345d`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:epoisses`

```console
$ docker pull traefik@sha256:0c4ffaae9a318156d54fe26708819b61eaca3e024b52e899f0eaec25fc8c7e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:epoisses` - linux; amd64

```console
$ docker pull traefik@sha256:20bfd389c3edae915394054bfe49f1d3aee4a806cbb6092f1c99b3add07bf1b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39992d581315a0b4b88f1e398c91dc4fc82ac4d5e4585f6b595c1ca74cd095c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:02 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:02 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdc75d2cb9ce1d3a6d44a3113d73337e408229f53699ccb417ca658b67a31bc`  
		Last Modified: Fri, 25 Mar 2022 01:36:41 GMT  
		Size: 27.4 MB (27394827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb17bd7149a04c28c3479b82ba24f491312b5e98d4f7fd7dd95d50685430be2`  
		Last Modified: Fri, 25 Mar 2022 01:36:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:epoisses` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6559ba9320b3bc7bdbfacc86318d152c40350fb98bcccf8d9672844e15110426
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28985121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de721efb2e4bdc486928aaff68345cc5f0781bf7e3712aaf7a661c5bf0d550e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:24 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:26 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab9a8bb707f561dcd006c6c7e3d8b74f4010b711dbfc2b2cfe9922c7ce8975`  
		Last Modified: Thu, 24 Mar 2022 23:05:13 GMT  
		Size: 25.7 MB (25682919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef4ee5181ca8f86dc5e5543aa574a902b87e1fba760958cd65b77d177c2466`  
		Last Modified: Thu, 24 Mar 2022 23:04:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:epoisses` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d857e522cbb1d2704be8e7455dae9d53943f304786171f2c1fa030d73121432e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28364399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985d429d196f31f082d4ce2802c33fed48027bf9ab84e6516926e53091e163`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:38 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:40 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d19cd8203c75d96b65bcb8e88efa57a03f46ae016db6f2bd9ae0834cc459bf`  
		Last Modified: Fri, 25 Mar 2022 02:26:56 GMT  
		Size: 25.0 MB (24979888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd8f6940877a3a5261afd917b904f04430958a88a70505509cde1772d4c50db`  
		Last Modified: Fri, 25 Mar 2022 02:26:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:epoisses` - linux; s390x

```console
$ docker pull traefik@sha256:09f52f8e5cf8dc3b0b0d25c12a99525769fc1214b978c8c4c6f1046ce13378da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29651905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7669e71c0dd08df6a88e4fe7f4192dcd4316a3880160c55bff11932ba06b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:46 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:46 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d2f51aa128fa862dd0743f43958f7cd6f649bf5722880ca504c9dc31052475`  
		Last Modified: Fri, 25 Mar 2022 00:31:41 GMT  
		Size: 26.4 MB (26373860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625ffde3f2367f11b2beb2d81d847d0703e3960e1acda315768539670cb3d8b4`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:epoisses-windowsservercore-1809`

```console
$ docker pull traefik@sha256:02cb9628336c1bf73cfac41139e2293027287239ae93ac5030aa9132aeda0d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:epoisses-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:47de1bfb0bae1a4ee272e93d523b8ba99781128c9c316dd2802432fe8b1aa300
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2743445028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d74c6ff9fd0ef0716d30ef3f47b96a6d81de3ee295920b148e8264be305842b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:16:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:16:23 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:16:24 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:16:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402d6b88042d7c0947353009ce4d477073e2736a9f31534244d33cf3420d459`  
		Last Modified: Thu, 24 Mar 2022 23:18:44 GMT  
		Size: 28.0 MB (27986759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76163e7d770a4111be892c0857a408bad2a2a6ab1acd826d443abe36b71d53cb`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfd6950346955cbf1855212200aaee09ed23996558944c2547f1c1f656d8c96`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15197f7b1ac7bc1c0ec20983eac3e25094ba3d991969d2785f3ae76e95f1345d`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:860fc052d2b48c0b05b76c47baeb6fdeea316b8950afc1e230e51f11e2b71157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:b8ca739c8361611a964dfa5f023750de17f34e342997c50dbdfb5a38e3450edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30339417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0dc6675f5f00f8e256dd10f2ae3a6e9c72e101fefe340a7578c5cebef1e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:08 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:08 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4fa573d59a67acc4371181255191bdb4b7076976c4b419df716d42b807114`  
		Last Modified: Fri, 25 Mar 2022 01:37:01 GMT  
		Size: 26.9 MB (26856210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff15934093e3aba34a0e8ff6dc63870642eb043f5fa6a0601211910e54994d76`  
		Last Modified: Fri, 25 Mar 2022 01:36:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:473045fcf57e944e78c7985cd420f2aa74600a5c32625153a19763461403d67a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f6c8b8c1db1b0d145e6a3e42d9cf31d572968bafe60205235c70e31905e20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:49 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:50 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d15861ba3656bac0bf7350e50bc7965ab614fa0d0d2b2d2363d7c537272498`  
		Last Modified: Thu, 24 Mar 2022 23:05:53 GMT  
		Size: 25.2 MB (25213677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe35863b15e69b331cb86aec04d56420be2c4a8d2d7907fa5c6a5c924d682b`  
		Last Modified: Thu, 24 Mar 2022 23:05:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a4f13c83df426b98306e592a0c084a38eb6205329cd3a6c5d6961f855a4bf375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27885391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef507d0470ecf849d69dba8f5f48bbeb0aaef90c5fe1f2785b6ae52565f264e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:52 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:54 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bcc34080ce16bec6deac23ee8508c2109ec4b6ed36cc90d1ed88b86217f99`  
		Last Modified: Fri, 25 Mar 2022 02:27:21 GMT  
		Size: 24.5 MB (24500880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2737b6b44221cb2c0f986312da01294c49ccddef5a6cbcb23f7e4da0adc987`  
		Last Modified: Fri, 25 Mar 2022 02:27:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:0ad3044a0cad96d56ddbc33d49951d1fba2dcd526648e4d8603a4ae5b982306b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29138079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c233c314a609dec253c443a92364cf96858016644c8212037d325faa58d0f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:58 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:58 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a795666c55ec202853627c2c7d338884cece42772fb6c12f0ac380ff558944`  
		Last Modified: Fri, 25 Mar 2022 00:32:00 GMT  
		Size: 25.9 MB (25860036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbf4dda32a155a274fd925f019944c1617ce43b9cc288bb3931e793acf041b`  
		Last Modified: Fri, 25 Mar 2022 00:31:56 GMT  
		Size: 367.0 B  
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
$ docker pull traefik@sha256:8ac75422d559a55193d20df11116ea951ad962f7dcdf3bd76a51f81f460de821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:04c41c7c3ff03d006e93029fb6bce95a448a32900c47487cf2f54f4df2d42f56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25645268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb8c5f993e88b67da6b9d2b5ee0a09e7f6a576c70e19f8bd1031adae54418ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 18 Mar 2022 06:23:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 18 Mar 2022 06:23:24 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 18 Mar 2022 06:23:24 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Mar 2022 06:23:24 GMT
CMD ["traefik"]
# Fri, 18 Mar 2022 06:23:25 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9a06ba42895ffa47fb412ee9c0fe6cc5c33d4bf08ca4a76e74f7040bc82206`  
		Last Modified: Fri, 18 Mar 2022 06:24:42 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b266beb8763fa8eeb482f01673624fb468758ac98bb28cc16881d8f94e1f54c`  
		Last Modified: Fri, 18 Mar 2022 06:24:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:08be027ed453b435111cb912908324ee1f5f0d77db60b6d6f9f10003d2c62674
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23925625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fbe3dd0a206256fa43655ee4af71da94003b6377978bc54ccdb219452f1bcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 22:45:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 22:45:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 22:45:04 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:45:05 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 22:45:06 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244182210987061535c909a9a2aace43df0eb4ee95953b8813c3792dd4ba5b37`  
		Last Modified: Thu, 17 Mar 2022 22:47:55 GMT  
		Size: 20.6 MB (20623423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb981a93f73996a8309c5494870b9e83074dae0470e145590d2148af320281cf`  
		Last Modified: Thu, 17 Mar 2022 22:47:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1e7c544b79ed103ad6d22cd9941ca3416e02897a9cb7f75120f6fd5f1949d90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23515893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a718e3a556a699675cb6d5655875c7240cd58d718536719147125b9d171870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 21:06:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 21:06:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 21:06:55 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 21:06:57 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 21:06:58 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe57c71a6e6bc8b2eda9db22fd05c14079977728ba28062721c5d71106b23ab9`  
		Last Modified: Thu, 17 Mar 2022 21:08:21 GMT  
		Size: 20.1 MB (20131382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535366a8854793a298d798c23544e4ad0849c13ce51c5687ad00f9864bebe75a`  
		Last Modified: Thu, 17 Mar 2022 21:08:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:85ffe3d43fd4929a0e48d226e018af240fbbd8ea9a03685f74f1c78c432f85b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:67d210fa3d7dcb1ebc3b3b5f3bfdaac7d18195e1bb2b83fa2c1b1f48d09b08dd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738303983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ebd04310fbdd68b4e7225310f8a6f2dec3a0330af0d02b74a9a0e35b79945b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:53:09 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Mar 2022 18:53:10 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:53:11 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Mar 2022 18:53:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd63edc5d2bde654b771ee58c8e9bb78539127758e862053223f402d3eaea68`  
		Last Modified: Wed, 09 Mar 2022 18:54:50 GMT  
		Size: 22.8 MB (22845783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cefe3e1f9703a33ffdf92a9c03b8a4738222fe08ea99aded6416f848aa300e9`  
		Last Modified: Wed, 09 Mar 2022 18:54:27 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f3b18eb0ddb1cb4c6b01a2abc4127403c6a67c630a8c05c6be5f43ab74acc`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bcba10ab84d161e2dc32a48f6bc15da23d8aabdb22bbf4a89499ce18583d46`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:rocamadour`

```console
$ docker pull traefik@sha256:860fc052d2b48c0b05b76c47baeb6fdeea316b8950afc1e230e51f11e2b71157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:rocamadour` - linux; amd64

```console
$ docker pull traefik@sha256:b8ca739c8361611a964dfa5f023750de17f34e342997c50dbdfb5a38e3450edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30339417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0dc6675f5f00f8e256dd10f2ae3a6e9c72e101fefe340a7578c5cebef1e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:08 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:08 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4fa573d59a67acc4371181255191bdb4b7076976c4b419df716d42b807114`  
		Last Modified: Fri, 25 Mar 2022 01:37:01 GMT  
		Size: 26.9 MB (26856210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff15934093e3aba34a0e8ff6dc63870642eb043f5fa6a0601211910e54994d76`  
		Last Modified: Fri, 25 Mar 2022 01:36:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm variant v6

```console
$ docker pull traefik@sha256:473045fcf57e944e78c7985cd420f2aa74600a5c32625153a19763461403d67a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f6c8b8c1db1b0d145e6a3e42d9cf31d572968bafe60205235c70e31905e20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:49 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:50 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d15861ba3656bac0bf7350e50bc7965ab614fa0d0d2b2d2363d7c537272498`  
		Last Modified: Thu, 24 Mar 2022 23:05:53 GMT  
		Size: 25.2 MB (25213677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe35863b15e69b331cb86aec04d56420be2c4a8d2d7907fa5c6a5c924d682b`  
		Last Modified: Thu, 24 Mar 2022 23:05:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a4f13c83df426b98306e592a0c084a38eb6205329cd3a6c5d6961f855a4bf375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27885391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef507d0470ecf849d69dba8f5f48bbeb0aaef90c5fe1f2785b6ae52565f264e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:52 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:54 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bcc34080ce16bec6deac23ee8508c2109ec4b6ed36cc90d1ed88b86217f99`  
		Last Modified: Fri, 25 Mar 2022 02:27:21 GMT  
		Size: 24.5 MB (24500880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2737b6b44221cb2c0f986312da01294c49ccddef5a6cbcb23f7e4da0adc987`  
		Last Modified: Fri, 25 Mar 2022 02:27:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:rocamadour` - linux; s390x

```console
$ docker pull traefik@sha256:0ad3044a0cad96d56ddbc33d49951d1fba2dcd526648e4d8603a4ae5b982306b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29138079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c233c314a609dec253c443a92364cf96858016644c8212037d325faa58d0f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:58 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:58 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a795666c55ec202853627c2c7d338884cece42772fb6c12f0ac380ff558944`  
		Last Modified: Fri, 25 Mar 2022 00:32:00 GMT  
		Size: 25.9 MB (25860036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbf4dda32a155a274fd925f019944c1617ce43b9cc288bb3931e793acf041b`  
		Last Modified: Fri, 25 Mar 2022 00:31:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:rocamadour-windowsservercore-1809`

```console
$ docker pull traefik@sha256:65434d6814d7057964abe547d596828914443859613e8babbebc8256218a8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:rocamadour-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:8f74813cea5a837efd6b0233cc8f8e1ba58dbc017e9063dd6e0f41f0e337d3f2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742900692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de1050781331302a08d35b247b99ed30e38f7478ed59f9aaa3d5591766a7a5c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:17:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:17:35 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:17:36 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:17:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce6f4fdd887fab65f610dfbbd9047a42d1f5010d54dd773da1960e0be81d18c`  
		Last Modified: Thu, 24 Mar 2022 23:19:06 GMT  
		Size: 27.4 MB (27442514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194905ba9de641fb766068bd0d2adc5e44d3ad51a6895ac0769593315f272eda`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef3d84d9f2492e9648efc00341ac09f2f323c9cd87485bf58b0e2f520380b1`  
		Last Modified: Thu, 24 Mar 2022 23:19:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107216789aeb5347d5ac3e42177fae7ebfd271935c9b48bed8f8d78dddee204`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1427 bytes)  
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
$ docker pull traefik@sha256:8ac75422d559a55193d20df11116ea951ad962f7dcdf3bd76a51f81f460de821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:04c41c7c3ff03d006e93029fb6bce95a448a32900c47487cf2f54f4df2d42f56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25645268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb8c5f993e88b67da6b9d2b5ee0a09e7f6a576c70e19f8bd1031adae54418ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 18 Mar 2022 06:23:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 18 Mar 2022 06:23:24 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 18 Mar 2022 06:23:24 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Mar 2022 06:23:24 GMT
CMD ["traefik"]
# Fri, 18 Mar 2022 06:23:25 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9a06ba42895ffa47fb412ee9c0fe6cc5c33d4bf08ca4a76e74f7040bc82206`  
		Last Modified: Fri, 18 Mar 2022 06:24:42 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b266beb8763fa8eeb482f01673624fb468758ac98bb28cc16881d8f94e1f54c`  
		Last Modified: Fri, 18 Mar 2022 06:24:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:08be027ed453b435111cb912908324ee1f5f0d77db60b6d6f9f10003d2c62674
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23925625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fbe3dd0a206256fa43655ee4af71da94003b6377978bc54ccdb219452f1bcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 22:45:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 22:45:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 22:45:04 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:45:05 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 22:45:06 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244182210987061535c909a9a2aace43df0eb4ee95953b8813c3792dd4ba5b37`  
		Last Modified: Thu, 17 Mar 2022 22:47:55 GMT  
		Size: 20.6 MB (20623423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb981a93f73996a8309c5494870b9e83074dae0470e145590d2148af320281cf`  
		Last Modified: Thu, 17 Mar 2022 22:47:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1e7c544b79ed103ad6d22cd9941ca3416e02897a9cb7f75120f6fd5f1949d90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23515893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a718e3a556a699675cb6d5655875c7240cd58d718536719147125b9d171870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 21:06:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 21:06:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 21:06:55 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 21:06:57 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 21:06:58 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe57c71a6e6bc8b2eda9db22fd05c14079977728ba28062721c5d71106b23ab9`  
		Last Modified: Thu, 17 Mar 2022 21:08:21 GMT  
		Size: 20.1 MB (20131382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535366a8854793a298d798c23544e4ad0849c13ce51c5687ad00f9864bebe75a`  
		Last Modified: Thu, 17 Mar 2022 21:08:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:85ffe3d43fd4929a0e48d226e018af240fbbd8ea9a03685f74f1c78c432f85b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:67d210fa3d7dcb1ebc3b3b5f3bfdaac7d18195e1bb2b83fa2c1b1f48d09b08dd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738303983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ebd04310fbdd68b4e7225310f8a6f2dec3a0330af0d02b74a9a0e35b79945b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:53:09 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Mar 2022 18:53:10 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:53:11 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Mar 2022 18:53:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd63edc5d2bde654b771ee58c8e9bb78539127758e862053223f402d3eaea68`  
		Last Modified: Wed, 09 Mar 2022 18:54:50 GMT  
		Size: 22.8 MB (22845783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cefe3e1f9703a33ffdf92a9c03b8a4738222fe08ea99aded6416f848aa300e9`  
		Last Modified: Wed, 09 Mar 2022 18:54:27 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f3b18eb0ddb1cb4c6b01a2abc4127403c6a67c630a8c05c6be5f43ab74acc`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bcba10ab84d161e2dc32a48f6bc15da23d8aabdb22bbf4a89499ce18583d46`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1389 bytes)  
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
$ docker pull traefik@sha256:8ac75422d559a55193d20df11116ea951ad962f7dcdf3bd76a51f81f460de821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:04c41c7c3ff03d006e93029fb6bce95a448a32900c47487cf2f54f4df2d42f56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25645268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb8c5f993e88b67da6b9d2b5ee0a09e7f6a576c70e19f8bd1031adae54418ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 18 Mar 2022 06:23:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 18 Mar 2022 06:23:24 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 18 Mar 2022 06:23:24 GMT
EXPOSE 80
# Fri, 18 Mar 2022 06:23:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Mar 2022 06:23:24 GMT
CMD ["traefik"]
# Fri, 18 Mar 2022 06:23:25 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9a06ba42895ffa47fb412ee9c0fe6cc5c33d4bf08ca4a76e74f7040bc82206`  
		Last Modified: Fri, 18 Mar 2022 06:24:42 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b266beb8763fa8eeb482f01673624fb468758ac98bb28cc16881d8f94e1f54c`  
		Last Modified: Fri, 18 Mar 2022 06:24:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:08be027ed453b435111cb912908324ee1f5f0d77db60b6d6f9f10003d2c62674
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23925625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fbe3dd0a206256fa43655ee4af71da94003b6377978bc54ccdb219452f1bcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 22:45:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 22:45:03 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 22:45:04 GMT
EXPOSE 80
# Thu, 17 Mar 2022 22:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 22:45:05 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 22:45:06 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244182210987061535c909a9a2aace43df0eb4ee95953b8813c3792dd4ba5b37`  
		Last Modified: Thu, 17 Mar 2022 22:47:55 GMT  
		Size: 20.6 MB (20623423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb981a93f73996a8309c5494870b9e83074dae0470e145590d2148af320281cf`  
		Last Modified: Thu, 17 Mar 2022 22:47:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1e7c544b79ed103ad6d22cd9941ca3416e02897a9cb7f75120f6fd5f1949d90c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23515893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a718e3a556a699675cb6d5655875c7240cd58d718536719147125b9d171870`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 17 Mar 2022 21:06:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Thu, 17 Mar 2022 21:06:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 17 Mar 2022 21:06:55 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 21:06:57 GMT
CMD ["traefik"]
# Thu, 17 Mar 2022 21:06:58 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe57c71a6e6bc8b2eda9db22fd05c14079977728ba28062721c5d71106b23ab9`  
		Last Modified: Thu, 17 Mar 2022 21:08:21 GMT  
		Size: 20.1 MB (20131382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535366a8854793a298d798c23544e4ad0849c13ce51c5687ad00f9864bebe75a`  
		Last Modified: Thu, 17 Mar 2022 21:08:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:85ffe3d43fd4929a0e48d226e018af240fbbd8ea9a03685f74f1c78c432f85b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:v1.7.34-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:67d210fa3d7dcb1ebc3b3b5f3bfdaac7d18195e1bb2b83fa2c1b1f48d09b08dd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2738303983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ebd04310fbdd68b4e7225310f8a6f2dec3a0330af0d02b74a9a0e35b79945b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:53:09 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Wed, 09 Mar 2022 18:53:10 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:53:11 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Mar 2022 18:53:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd63edc5d2bde654b771ee58c8e9bb78539127758e862053223f402d3eaea68`  
		Last Modified: Wed, 09 Mar 2022 18:54:50 GMT  
		Size: 22.8 MB (22845783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cefe3e1f9703a33ffdf92a9c03b8a4738222fe08ea99aded6416f848aa300e9`  
		Last Modified: Wed, 09 Mar 2022 18:54:27 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f3b18eb0ddb1cb4c6b01a2abc4127403c6a67c630a8c05c6be5f43ab74acc`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bcba10ab84d161e2dc32a48f6bc15da23d8aabdb22bbf4a89499ce18583d46`  
		Last Modified: Wed, 09 Mar 2022 18:54:26 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6`

```console
$ docker pull traefik@sha256:860fc052d2b48c0b05b76c47baeb6fdeea316b8950afc1e230e51f11e2b71157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.6` - linux; amd64

```console
$ docker pull traefik@sha256:b8ca739c8361611a964dfa5f023750de17f34e342997c50dbdfb5a38e3450edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30339417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0dc6675f5f00f8e256dd10f2ae3a6e9c72e101fefe340a7578c5cebef1e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:08 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:08 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4fa573d59a67acc4371181255191bdb4b7076976c4b419df716d42b807114`  
		Last Modified: Fri, 25 Mar 2022 01:37:01 GMT  
		Size: 26.9 MB (26856210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff15934093e3aba34a0e8ff6dc63870642eb043f5fa6a0601211910e54994d76`  
		Last Modified: Fri, 25 Mar 2022 01:36:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:473045fcf57e944e78c7985cd420f2aa74600a5c32625153a19763461403d67a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f6c8b8c1db1b0d145e6a3e42d9cf31d572968bafe60205235c70e31905e20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:49 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:50 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d15861ba3656bac0bf7350e50bc7965ab614fa0d0d2b2d2363d7c537272498`  
		Last Modified: Thu, 24 Mar 2022 23:05:53 GMT  
		Size: 25.2 MB (25213677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe35863b15e69b331cb86aec04d56420be2c4a8d2d7907fa5c6a5c924d682b`  
		Last Modified: Thu, 24 Mar 2022 23:05:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a4f13c83df426b98306e592a0c084a38eb6205329cd3a6c5d6961f855a4bf375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27885391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef507d0470ecf849d69dba8f5f48bbeb0aaef90c5fe1f2785b6ae52565f264e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:52 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:54 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bcc34080ce16bec6deac23ee8508c2109ec4b6ed36cc90d1ed88b86217f99`  
		Last Modified: Fri, 25 Mar 2022 02:27:21 GMT  
		Size: 24.5 MB (24500880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2737b6b44221cb2c0f986312da01294c49ccddef5a6cbcb23f7e4da0adc987`  
		Last Modified: Fri, 25 Mar 2022 02:27:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6` - linux; s390x

```console
$ docker pull traefik@sha256:0ad3044a0cad96d56ddbc33d49951d1fba2dcd526648e4d8603a4ae5b982306b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29138079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c233c314a609dec253c443a92364cf96858016644c8212037d325faa58d0f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:58 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:58 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a795666c55ec202853627c2c7d338884cece42772fb6c12f0ac380ff558944`  
		Last Modified: Fri, 25 Mar 2022 00:32:00 GMT  
		Size: 25.9 MB (25860036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbf4dda32a155a274fd925f019944c1617ce43b9cc288bb3931e793acf041b`  
		Last Modified: Fri, 25 Mar 2022 00:31:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6-windowsservercore-1809`

```console
$ docker pull traefik@sha256:65434d6814d7057964abe547d596828914443859613e8babbebc8256218a8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:v2.6-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:8f74813cea5a837efd6b0233cc8f8e1ba58dbc017e9063dd6e0f41f0e337d3f2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742900692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de1050781331302a08d35b247b99ed30e38f7478ed59f9aaa3d5591766a7a5c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:17:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:17:35 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:17:36 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:17:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce6f4fdd887fab65f610dfbbd9047a42d1f5010d54dd773da1960e0be81d18c`  
		Last Modified: Thu, 24 Mar 2022 23:19:06 GMT  
		Size: 27.4 MB (27442514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194905ba9de641fb766068bd0d2adc5e44d3ad51a6895ac0769593315f272eda`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef3d84d9f2492e9648efc00341ac09f2f323c9cd87485bf58b0e2f520380b1`  
		Last Modified: Thu, 24 Mar 2022 23:19:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107216789aeb5347d5ac3e42177fae7ebfd271935c9b48bed8f8d78dddee204`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6.2`

```console
$ docker pull traefik@sha256:860fc052d2b48c0b05b76c47baeb6fdeea316b8950afc1e230e51f11e2b71157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.6.2` - linux; amd64

```console
$ docker pull traefik@sha256:b8ca739c8361611a964dfa5f023750de17f34e342997c50dbdfb5a38e3450edd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30339417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0dc6675f5f00f8e256dd10f2ae3a6e9c72e101fefe340a7578c5cebef1e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:08 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:08 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:08 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f4fa573d59a67acc4371181255191bdb4b7076976c4b419df716d42b807114`  
		Last Modified: Fri, 25 Mar 2022 01:37:01 GMT  
		Size: 26.9 MB (26856210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff15934093e3aba34a0e8ff6dc63870642eb043f5fa6a0601211910e54994d76`  
		Last Modified: Fri, 25 Mar 2022 01:36:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:473045fcf57e944e78c7985cd420f2aa74600a5c32625153a19763461403d67a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28515878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f6c8b8c1db1b0d145e6a3e42d9cf31d572968bafe60205235c70e31905e20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:49 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:49 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:50 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d15861ba3656bac0bf7350e50bc7965ab614fa0d0d2b2d2363d7c537272498`  
		Last Modified: Thu, 24 Mar 2022 23:05:53 GMT  
		Size: 25.2 MB (25213677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe35863b15e69b331cb86aec04d56420be2c4a8d2d7907fa5c6a5c924d682b`  
		Last Modified: Thu, 24 Mar 2022 23:05:36 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:a4f13c83df426b98306e592a0c084a38eb6205329cd3a6c5d6961f855a4bf375
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27885391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef507d0470ecf849d69dba8f5f48bbeb0aaef90c5fe1f2785b6ae52565f264e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:52 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:52 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:54 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bcc34080ce16bec6deac23ee8508c2109ec4b6ed36cc90d1ed88b86217f99`  
		Last Modified: Fri, 25 Mar 2022 02:27:21 GMT  
		Size: 24.5 MB (24500880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2737b6b44221cb2c0f986312da01294c49ccddef5a6cbcb23f7e4da0adc987`  
		Last Modified: Fri, 25 Mar 2022 02:27:17 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.6.2` - linux; s390x

```console
$ docker pull traefik@sha256:0ad3044a0cad96d56ddbc33d49951d1fba2dcd526648e4d8603a4ae5b982306b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29138079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c233c314a609dec253c443a92364cf96858016644c8212037d325faa58d0f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:58 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:58 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:58 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a795666c55ec202853627c2c7d338884cece42772fb6c12f0ac380ff558944`  
		Last Modified: Fri, 25 Mar 2022 00:32:00 GMT  
		Size: 25.9 MB (25860036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbf4dda32a155a274fd925f019944c1617ce43b9cc288bb3931e793acf041b`  
		Last Modified: Fri, 25 Mar 2022 00:31:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.6.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:65434d6814d7057964abe547d596828914443859613e8babbebc8256218a8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:v2.6.2-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:8f74813cea5a837efd6b0233cc8f8e1ba58dbc017e9063dd6e0f41f0e337d3f2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742900692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de1050781331302a08d35b247b99ed30e38f7478ed59f9aaa3d5591766a7a5c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:17:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:17:35 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:17:36 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:17:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce6f4fdd887fab65f610dfbbd9047a42d1f5010d54dd773da1960e0be81d18c`  
		Last Modified: Thu, 24 Mar 2022 23:19:06 GMT  
		Size: 27.4 MB (27442514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194905ba9de641fb766068bd0d2adc5e44d3ad51a6895ac0769593315f272eda`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef3d84d9f2492e9648efc00341ac09f2f323c9cd87485bf58b0e2f520380b1`  
		Last Modified: Thu, 24 Mar 2022 23:19:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107216789aeb5347d5ac3e42177fae7ebfd271935c9b48bed8f8d78dddee204`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.7`

```console
$ docker pull traefik@sha256:0c4ffaae9a318156d54fe26708819b61eaca3e024b52e899f0eaec25fc8c7e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.7` - linux; amd64

```console
$ docker pull traefik@sha256:20bfd389c3edae915394054bfe49f1d3aee4a806cbb6092f1c99b3add07bf1b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39992d581315a0b4b88f1e398c91dc4fc82ac4d5e4585f6b595c1ca74cd095c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:02 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:02 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdc75d2cb9ce1d3a6d44a3113d73337e408229f53699ccb417ca658b67a31bc`  
		Last Modified: Fri, 25 Mar 2022 01:36:41 GMT  
		Size: 27.4 MB (27394827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb17bd7149a04c28c3479b82ba24f491312b5e98d4f7fd7dd95d50685430be2`  
		Last Modified: Fri, 25 Mar 2022 01:36:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6559ba9320b3bc7bdbfacc86318d152c40350fb98bcccf8d9672844e15110426
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28985121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de721efb2e4bdc486928aaff68345cc5f0781bf7e3712aaf7a661c5bf0d550e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:24 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:26 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab9a8bb707f561dcd006c6c7e3d8b74f4010b711dbfc2b2cfe9922c7ce8975`  
		Last Modified: Thu, 24 Mar 2022 23:05:13 GMT  
		Size: 25.7 MB (25682919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef4ee5181ca8f86dc5e5543aa574a902b87e1fba760958cd65b77d177c2466`  
		Last Modified: Thu, 24 Mar 2022 23:04:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d857e522cbb1d2704be8e7455dae9d53943f304786171f2c1fa030d73121432e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28364399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985d429d196f31f082d4ce2802c33fed48027bf9ab84e6516926e53091e163`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:38 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:40 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d19cd8203c75d96b65bcb8e88efa57a03f46ae016db6f2bd9ae0834cc459bf`  
		Last Modified: Fri, 25 Mar 2022 02:26:56 GMT  
		Size: 25.0 MB (24979888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd8f6940877a3a5261afd917b904f04430958a88a70505509cde1772d4c50db`  
		Last Modified: Fri, 25 Mar 2022 02:26:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.7` - linux; s390x

```console
$ docker pull traefik@sha256:09f52f8e5cf8dc3b0b0d25c12a99525769fc1214b978c8c4c6f1046ce13378da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29651905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7669e71c0dd08df6a88e4fe7f4192dcd4316a3880160c55bff11932ba06b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:46 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:46 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d2f51aa128fa862dd0743f43958f7cd6f649bf5722880ca504c9dc31052475`  
		Last Modified: Fri, 25 Mar 2022 00:31:41 GMT  
		Size: 26.4 MB (26373860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625ffde3f2367f11b2beb2d81d847d0703e3960e1acda315768539670cb3d8b4`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:02cb9628336c1bf73cfac41139e2293027287239ae93ac5030aa9132aeda0d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:v2.7-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:47de1bfb0bae1a4ee272e93d523b8ba99781128c9c316dd2802432fe8b1aa300
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2743445028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d74c6ff9fd0ef0716d30ef3f47b96a6d81de3ee295920b148e8264be305842b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:16:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:16:23 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:16:24 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:16:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402d6b88042d7c0947353009ce4d477073e2736a9f31534244d33cf3420d459`  
		Last Modified: Thu, 24 Mar 2022 23:18:44 GMT  
		Size: 28.0 MB (27986759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76163e7d770a4111be892c0857a408bad2a2a6ab1acd826d443abe36b71d53cb`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfd6950346955cbf1855212200aaee09ed23996558944c2547f1c1f656d8c96`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15197f7b1ac7bc1c0ec20983eac3e25094ba3d991969d2785f3ae76e95f1345d`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.7.0-rc1`

```console
$ docker pull traefik@sha256:0c4ffaae9a318156d54fe26708819b61eaca3e024b52e899f0eaec25fc8c7e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.7.0-rc1` - linux; amd64

```console
$ docker pull traefik@sha256:20bfd389c3edae915394054bfe49f1d3aee4a806cbb6092f1c99b3add07bf1b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30878034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39992d581315a0b4b88f1e398c91dc4fc82ac4d5e4585f6b595c1ca74cd095c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 06:23:06 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 01:36:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 01:36:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 01:36:02 GMT
EXPOSE 80
# Fri, 25 Mar 2022 01:36:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 01:36:02 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 01:36:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f86d3f60579f394506161f82aafee52b414cd58c1060e18ca607a4fc9fbc4`  
		Last Modified: Fri, 18 Mar 2022 06:24:10 GMT  
		Size: 666.7 KB (666670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdc75d2cb9ce1d3a6d44a3113d73337e408229f53699ccb417ca658b67a31bc`  
		Last Modified: Fri, 25 Mar 2022 01:36:41 GMT  
		Size: 27.4 MB (27394827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb17bd7149a04c28c3479b82ba24f491312b5e98d4f7fd7dd95d50685430be2`  
		Last Modified: Fri, 25 Mar 2022 01:36:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.7.0-rc1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6559ba9320b3bc7bdbfacc86318d152c40350fb98bcccf8d9672844e15110426
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28985121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de721efb2e4bdc486928aaff68345cc5f0781bf7e3712aaf7a661c5bf0d550e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 22:44:31 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 24 Mar 2022 23:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 24 Mar 2022 23:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 24 Mar 2022 23:02:24 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Mar 2022 23:02:26 GMT
CMD ["traefik"]
# Thu, 24 Mar 2022 23:02:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc61b01c9ae829babc4ec995a57d752de240cbe8e3a8660191d3d21fc589a5f`  
		Last Modified: Thu, 17 Mar 2022 22:46:57 GMT  
		Size: 672.5 KB (672470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ab9a8bb707f561dcd006c6c7e3d8b74f4010b711dbfc2b2cfe9922c7ce8975`  
		Last Modified: Thu, 24 Mar 2022 23:05:13 GMT  
		Size: 25.7 MB (25682919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ef4ee5181ca8f86dc5e5543aa574a902b87e1fba760958cd65b77d177c2466`  
		Last Modified: Thu, 24 Mar 2022 23:04:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.7.0-rc1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d857e522cbb1d2704be8e7455dae9d53943f304786171f2c1fa030d73121432e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28364399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985d429d196f31f082d4ce2802c33fed48027bf9ab84e6516926e53091e163`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:06:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 02:25:36 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 02:25:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 02:25:38 GMT
EXPOSE 80
# Fri, 25 Mar 2022 02:25:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 02:25:40 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 02:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012a4d53d2ad42f0d1b24f774778f1ea2d1c67cfdd0a1611fb7652fac92fc9b`  
		Last Modified: Thu, 17 Mar 2022 21:07:51 GMT  
		Size: 668.3 KB (668255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d19cd8203c75d96b65bcb8e88efa57a03f46ae016db6f2bd9ae0834cc459bf`  
		Last Modified: Fri, 25 Mar 2022 02:26:56 GMT  
		Size: 25.0 MB (24979888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd8f6940877a3a5261afd917b904f04430958a88a70505509cde1772d4c50db`  
		Last Modified: Fri, 25 Mar 2022 02:26:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.7.0-rc1` - linux; s390x

```console
$ docker pull traefik@sha256:09f52f8e5cf8dc3b0b0d25c12a99525769fc1214b978c8c4c6f1046ce13378da
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29651905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7669e71c0dd08df6a88e4fe7f4192dcd4316a3880160c55bff11932ba06b08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Fri, 25 Mar 2022 00:30:41 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 25 Mar 2022 00:30:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 25 Mar 2022 00:30:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 25 Mar 2022 00:30:46 GMT
EXPOSE 80
# Fri, 25 Mar 2022 00:30:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 00:30:46 GMT
CMD ["traefik"]
# Fri, 25 Mar 2022 00:30:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f516f2bd18411ae6d3254b5fc966a99d4339d298a6439eb2784adaa71f2792b`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 672.5 KB (672468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d2f51aa128fa862dd0743f43958f7cd6f649bf5722880ca504c9dc31052475`  
		Last Modified: Fri, 25 Mar 2022 00:31:41 GMT  
		Size: 26.4 MB (26373860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625ffde3f2367f11b2beb2d81d847d0703e3960e1acda315768539670cb3d8b4`  
		Last Modified: Fri, 25 Mar 2022 00:31:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.7.0-rc1-windowsservercore-1809`

```console
$ docker pull traefik@sha256:02cb9628336c1bf73cfac41139e2293027287239ae93ac5030aa9132aeda0d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:v2.7.0-rc1-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:47de1bfb0bae1a4ee272e93d523b8ba99781128c9c316dd2802432fe8b1aa300
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2743445028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d74c6ff9fd0ef0716d30ef3f47b96a6d81de3ee295920b148e8264be305842b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:16:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.7.0-rc1/traefik_v2.7.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:16:23 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:16:24 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:16:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.7.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2402d6b88042d7c0947353009ce4d477073e2736a9f31534244d33cf3420d459`  
		Last Modified: Thu, 24 Mar 2022 23:18:44 GMT  
		Size: 28.0 MB (27986759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76163e7d770a4111be892c0857a408bad2a2a6ab1acd826d443abe36b71d53cb`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfd6950346955cbf1855212200aaee09ed23996558944c2547f1c1f656d8c96`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15197f7b1ac7bc1c0ec20983eac3e25094ba3d991969d2785f3ae76e95f1345d`  
		Last Modified: Thu, 24 Mar 2022 23:18:12 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:65434d6814d7057964abe547d596828914443859613e8babbebc8256218a8ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull traefik@sha256:8f74813cea5a837efd6b0233cc8f8e1ba58dbc017e9063dd6e0f41f0e337d3f2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742900692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de1050781331302a08d35b247b99ed30e38f7478ed59f9aaa3d5591766a7a5c`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 24 Mar 2022 23:17:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.6.2/traefik_v2.6.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 24 Mar 2022 23:17:35 GMT
EXPOSE 80
# Thu, 24 Mar 2022 23:17:36 GMT
ENTRYPOINT ["/traefik"]
# Thu, 24 Mar 2022 23:17:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.6.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce6f4fdd887fab65f610dfbbd9047a42d1f5010d54dd773da1960e0be81d18c`  
		Last Modified: Thu, 24 Mar 2022 23:19:06 GMT  
		Size: 27.4 MB (27442514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194905ba9de641fb766068bd0d2adc5e44d3ad51a6895ac0769593315f272eda`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef3d84d9f2492e9648efc00341ac09f2f323c9cd87485bf58b0e2f520380b1`  
		Last Modified: Thu, 24 Mar 2022 23:19:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1107216789aeb5347d5ac3e42177fae7ebfd271935c9b48bed8f8d78dddee204`  
		Last Modified: Thu, 24 Mar 2022 23:18:59 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
