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
-	[`traefik:2.9.8`](#traefik298)
-	[`traefik:2.9.8-windowsservercore-1809`](#traefik298-windowsservercore-1809)
-	[`traefik:3.0`](#traefik30)
-	[`traefik:3.0-windowsservercore-1809`](#traefik30-windowsservercore-1809)
-	[`traefik:3.0.0-beta2`](#traefik300-beta2)
-	[`traefik:3.0.0-beta2-windowsservercore-1809`](#traefik300-beta2-windowsservercore-1809)
-	[`traefik:banon`](#traefikbanon)
-	[`traefik:banon-windowsservercore-1809`](#traefikbanon-windowsservercore-1809)
-	[`traefik:beaufort`](#traefikbeaufort)
-	[`traefik:beaufort-windowsservercore-1809`](#traefikbeaufort-windowsservercore-1809)
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
-	[`traefik:v2.9.8`](#traefikv298)
-	[`traefik:v2.9.8-windowsservercore-1809`](#traefikv298-windowsservercore-1809)
-	[`traefik:v3.0`](#traefikv30)
-	[`traefik:v3.0-windowsservercore-1809`](#traefikv30-windowsservercore-1809)
-	[`traefik:v3.0.0-beta2`](#traefikv300-beta2)
-	[`traefik:v3.0.0-beta2-windowsservercore-1809`](#traefikv300-beta2-windowsservercore-1809)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)

## `traefik:1.7`

```console
$ docker pull traefik@sha256:4bd2fbfb20b5ddb03ef8cf9f77d9726da942d92ebc206abca1865824d352cf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7` - linux; amd64

```console
$ docker pull traefik@sha256:a37a3469b7bd1e58d95ab5918f31f3a8aada1bdfa90f8d963eb78e8bae37d025
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22594315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b06305d2e0eca68d66088b5290a28c31dd73722f3f8e33c764bd60faf17edd7`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 11 Feb 2023 14:05:58 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Sat, 11 Feb 2023 14:05:59 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Sat, 11 Feb 2023 14:05:59 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:59 GMT
VOLUME [/tmp]
# Sat, 11 Feb 2023 14:05:59 GMT
ENTRYPOINT ["/traefik"]
# Sat, 11 Feb 2023 14:05:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b232dbde1f095d758c59886ecc24a42610dd35fd72116f3bf04738104e1cfa`  
		Last Modified: Sat, 11 Feb 2023 14:07:25 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066ff3631f4c0a13ebb72826195f8332b28aa6c9945865b1c07076fad46fb81b`  
		Last Modified: Sat, 11 Feb 2023 14:07:29 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ed51daf51f75bf5735027eed93829bc2ddc8cab5f7d2c92661e9ae240a812647
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21055568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35629440895fbdc6144fd69e6ddccee4de8aa7785af39e4804683304ac4f2df1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:59:12 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:59:13 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 11 Nov 2022 11:59:14 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:59:14 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:59:14 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:59:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0efdacb2b2ba042055ea537001460b2cff92ff305869705801b66bc44dc8565`  
		Last Modified: Fri, 11 Nov 2022 12:01:04 GMT  
		Size: 308.7 KB (308749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ebe6d2d943e776e37535f360e7b0f3745d625ee69f6ee5fe1eecee5487ce1`  
		Last Modified: Fri, 11 Nov 2022 12:01:08 GMT  
		Size: 20.6 MB (20623281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ac5b287132e97dc27bbd96791a25701e051ddce973d6ee70eda1c87138e3c299
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20563697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d5da1bea8e1a3e20b83ceca6e486a1e881451b1e304a0281d936d5e51f418d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:00:57 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:00:58 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 11 Nov 2022 11:00:58 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:00:58 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:00:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:00:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f6a6b590d30fda524213974a86d6ca01981b3ab4154a359b9c2e3fa3262c6`  
		Last Modified: Fri, 11 Nov 2022 11:02:04 GMT  
		Size: 308.8 KB (308813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af8a7d805d81cf74f58f3793659f76132259201bea15bbb7a0edc6191f8edfa`  
		Last Modified: Fri, 11 Nov 2022 11:02:07 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-alpine`

```console
$ docker pull traefik@sha256:40749b8ddac52c036c1e70f65175304503ec9a0e5afd2f06f855c45e6b6e9556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:6a5bf0d59212a73927e18da4a5b85ff7d02fb566283bcd10b3c307b8a39627a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25653523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299327139165b0025a883c7a11747b5d04c4bc72f053601c0f763fee0ed761a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:46 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:51 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:52 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:52 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fab313a1ca0ee79d027587c5edad5ff243a08e1cbd263abe2a17503c316d8b`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 661.5 KB (661461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e550be36e43026c7c9214cf16b3b866de5ce1da12f14fcef46658c0def1d4a7`  
		Last Modified: Sat, 11 Feb 2023 14:07:12 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4561714fba29bd0d410fa9813afc75479ffef93714ffdad849a7943771d73544`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c877680359edeb36e0f7b0749fbb09a801a680d177cda3b4cfbb42c8562ab55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23928217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7628e269edbd96b0ce234c48ad415c771aae9f62ea77226d2902180116cd4388`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:41 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Fri, 10 Feb 2023 20:49:41 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:41 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:41 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d249d387e6c91bac13ecc5746b760ce33da5956b1857574c15c4ba2b5002a4`  
		Last Modified: Sat, 11 Feb 2023 07:31:47 GMT  
		Size: 666.3 KB (666280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4a0aee18eee90e65c8dc3e3cf8ceb25a9aee2aef1b26d1322d7a7b2392295f`  
		Last Modified: Sat, 11 Feb 2023 07:31:50 GMT  
		Size: 20.6 MB (20623417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5e05661e72c78c68ccdc37047515cc68b8aafff48c76185f4381a9c0954cf0`  
		Last Modified: Sat, 11 Feb 2023 07:31:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e23b8edb3c8a7f4a5ce7b2697e304f8e31d845474dccdbcd15b86e831c7bc69b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23519920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dbaffc2f8e74c9ed9aa7a99d590e792ba2b318e8562992180335ba122958e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:46 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:46 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:46 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5c8dd85906c92d3445ffeb0481950055e77c854095c4cbbd854f6951242a3c`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 663.2 KB (663163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994ad8baa5503f4c667ced5bb36b643eba7642f9791e4bf7975527de9f2c2ed`  
		Last Modified: Sat, 11 Feb 2023 06:41:57 GMT  
		Size: 20.1 MB (20131363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6a5a822a3369f9999a4da4bcb9718729d386c2dbf108fb8a8a52056eacc8d2`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f8223de1afb5c0d3c84ac73737d280550d6c118d326dda320af3d6c84a1cc42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:1.7-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:608c9a5abd6dcd8831958380ec03bf2b6d756d151ff8bef7c387ff157223a3c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1730802068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789e7cee983ab7e7e598355f69c9db141fd644d2e5c467b9d49f0750c561a887`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:11:17 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 12 Jan 2023 08:11:18 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:11:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:11:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1c4961b4b546f722e4a1e76673f9e32be91d74d2f8afbcc97fa90b491357f7`  
		Last Modified: Thu, 12 Jan 2023 08:12:40 GMT  
		Size: 22.9 MB (22852479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8695c3b7b24056e2113dcc6735b59d46b4d0b13567be65bd3a89a4e96f052`  
		Last Modified: Thu, 12 Jan 2023 08:12:34 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ae219d0779fe8847f8e1d50e8e35f27c0ea05e783a1d06bb67a0c1446b46e`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0a9394409e220db17e543bcb32779dbb83a4a71063bd777206ee09133c69e2`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34`

```console
$ docker pull traefik@sha256:4bd2fbfb20b5ddb03ef8cf9f77d9726da942d92ebc206abca1865824d352cf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:a37a3469b7bd1e58d95ab5918f31f3a8aada1bdfa90f8d963eb78e8bae37d025
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22594315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b06305d2e0eca68d66088b5290a28c31dd73722f3f8e33c764bd60faf17edd7`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 11 Feb 2023 14:05:58 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Sat, 11 Feb 2023 14:05:59 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Sat, 11 Feb 2023 14:05:59 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:59 GMT
VOLUME [/tmp]
# Sat, 11 Feb 2023 14:05:59 GMT
ENTRYPOINT ["/traefik"]
# Sat, 11 Feb 2023 14:05:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b232dbde1f095d758c59886ecc24a42610dd35fd72116f3bf04738104e1cfa`  
		Last Modified: Sat, 11 Feb 2023 14:07:25 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066ff3631f4c0a13ebb72826195f8332b28aa6c9945865b1c07076fad46fb81b`  
		Last Modified: Sat, 11 Feb 2023 14:07:29 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ed51daf51f75bf5735027eed93829bc2ddc8cab5f7d2c92661e9ae240a812647
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21055568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35629440895fbdc6144fd69e6ddccee4de8aa7785af39e4804683304ac4f2df1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:59:12 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:59:13 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 11 Nov 2022 11:59:14 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:59:14 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:59:14 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:59:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0efdacb2b2ba042055ea537001460b2cff92ff305869705801b66bc44dc8565`  
		Last Modified: Fri, 11 Nov 2022 12:01:04 GMT  
		Size: 308.7 KB (308749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ebe6d2d943e776e37535f360e7b0f3745d625ee69f6ee5fe1eecee5487ce1`  
		Last Modified: Fri, 11 Nov 2022 12:01:08 GMT  
		Size: 20.6 MB (20623281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ac5b287132e97dc27bbd96791a25701e051ddce973d6ee70eda1c87138e3c299
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20563697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d5da1bea8e1a3e20b83ceca6e486a1e881451b1e304a0281d936d5e51f418d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:00:57 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:00:58 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 11 Nov 2022 11:00:58 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:00:58 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:00:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:00:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f6a6b590d30fda524213974a86d6ca01981b3ab4154a359b9c2e3fa3262c6`  
		Last Modified: Fri, 11 Nov 2022 11:02:04 GMT  
		Size: 308.8 KB (308813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af8a7d805d81cf74f58f3793659f76132259201bea15bbb7a0edc6191f8edfa`  
		Last Modified: Fri, 11 Nov 2022 11:02:07 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-alpine`

```console
$ docker pull traefik@sha256:40749b8ddac52c036c1e70f65175304503ec9a0e5afd2f06f855c45e6b6e9556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:6a5bf0d59212a73927e18da4a5b85ff7d02fb566283bcd10b3c307b8a39627a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25653523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299327139165b0025a883c7a11747b5d04c4bc72f053601c0f763fee0ed761a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:46 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:51 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:52 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:52 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fab313a1ca0ee79d027587c5edad5ff243a08e1cbd263abe2a17503c316d8b`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 661.5 KB (661461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e550be36e43026c7c9214cf16b3b866de5ce1da12f14fcef46658c0def1d4a7`  
		Last Modified: Sat, 11 Feb 2023 14:07:12 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4561714fba29bd0d410fa9813afc75479ffef93714ffdad849a7943771d73544`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c877680359edeb36e0f7b0749fbb09a801a680d177cda3b4cfbb42c8562ab55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23928217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7628e269edbd96b0ce234c48ad415c771aae9f62ea77226d2902180116cd4388`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:41 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Fri, 10 Feb 2023 20:49:41 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:41 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:41 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d249d387e6c91bac13ecc5746b760ce33da5956b1857574c15c4ba2b5002a4`  
		Last Modified: Sat, 11 Feb 2023 07:31:47 GMT  
		Size: 666.3 KB (666280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4a0aee18eee90e65c8dc3e3cf8ceb25a9aee2aef1b26d1322d7a7b2392295f`  
		Last Modified: Sat, 11 Feb 2023 07:31:50 GMT  
		Size: 20.6 MB (20623417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5e05661e72c78c68ccdc37047515cc68b8aafff48c76185f4381a9c0954cf0`  
		Last Modified: Sat, 11 Feb 2023 07:31:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e23b8edb3c8a7f4a5ce7b2697e304f8e31d845474dccdbcd15b86e831c7bc69b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23519920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dbaffc2f8e74c9ed9aa7a99d590e792ba2b318e8562992180335ba122958e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:46 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:46 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:46 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5c8dd85906c92d3445ffeb0481950055e77c854095c4cbbd854f6951242a3c`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 663.2 KB (663163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994ad8baa5503f4c667ced5bb36b643eba7642f9791e4bf7975527de9f2c2ed`  
		Last Modified: Sat, 11 Feb 2023 06:41:57 GMT  
		Size: 20.1 MB (20131363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6a5a822a3369f9999a4da4bcb9718729d386c2dbf108fb8a8a52056eacc8d2`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f8223de1afb5c0d3c84ac73737d280550d6c118d326dda320af3d6c84a1cc42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:1.7.34-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:608c9a5abd6dcd8831958380ec03bf2b6d756d151ff8bef7c387ff157223a3c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1730802068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789e7cee983ab7e7e598355f69c9db141fd644d2e5c467b9d49f0750c561a887`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:11:17 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 12 Jan 2023 08:11:18 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:11:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:11:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1c4961b4b546f722e4a1e76673f9e32be91d74d2f8afbcc97fa90b491357f7`  
		Last Modified: Thu, 12 Jan 2023 08:12:40 GMT  
		Size: 22.9 MB (22852479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8695c3b7b24056e2113dcc6735b59d46b4d0b13567be65bd3a89a4e96f052`  
		Last Modified: Thu, 12 Jan 2023 08:12:34 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ae219d0779fe8847f8e1d50e8e35f27c0ea05e783a1d06bb67a0c1446b46e`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0a9394409e220db17e543bcb32779dbb83a4a71063bd777206ee09133c69e2`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9`

```console
$ docker pull traefik@sha256:7a4fb968173b583bcf4aae0fea180cd6cd95001be686494d339da35809897cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:2.9` - linux; amd64

```console
$ docker pull traefik@sha256:1f614d9645242cdd8eef1fd9e344fa1c9bd0ed5a5a30de4dbc41506f327d7420
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38771266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0e86397f2b094403ade8b63c70cc37fc6b46e9d62685b36a189139daa02b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 02:44:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 02:44:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 02:44:07 GMT
EXPOSE 80
# Wed, 15 Feb 2023 02:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 02:44:07 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 02:44:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee56f1b8420e11a19285128414fe8b580c55ae0344fec9a25689a2b9bb15ef4`  
		Last Modified: Wed, 15 Feb 2023 02:44:41 GMT  
		Size: 35.3 MB (35282705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a93139c311e646d9d7a0d54cd6b9d4d4dd63f01826b3e1ca43278f6ed78590`  
		Last Modified: Wed, 15 Feb 2023 02:44:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:23f7873a5b093e4fd79f8c73e07104359cd8414049d745689255e75576297701
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36621938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adde262bc17f9052ef4bf0278302876519d1963197a6e4e1926a156266f9794a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Feb 2023 23:45:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Feb 2023 23:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Feb 2023 23:45:40 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:45:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Feb 2023 23:45:40 GMT
CMD ["traefik"]
# Tue, 14 Feb 2023 23:45:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200d375a7d2d15bb2f36b51b82ed256c5e93e8a74fe02dcf40631638f0904a3c`  
		Last Modified: Tue, 14 Feb 2023 23:47:00 GMT  
		Size: 33.3 MB (33321544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ca36f9053054cd9568d42bfe631c966de835fb248a43afac60392966162d42`  
		Last Modified: Tue, 14 Feb 2023 23:46:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4fea093c218e9879dc904d6259ccf1c37b6c598131094237ef9315b5e655cab7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35755082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25591b4c17d6f05e5ae4c39fba11549f8423c773595e4d05afd7babfff6bef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 03:00:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 03:00:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 03:00:15 GMT
EXPOSE 80
# Wed, 15 Feb 2023 03:00:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 03:00:15 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 03:00:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b59175297242976fbda9978b9bb91d21dfc03087ade15af211ef03974dec93`  
		Last Modified: Wed, 15 Feb 2023 03:00:55 GMT  
		Size: 32.4 MB (32370006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e163b4ad7fced3b65af29248927428f8e5a32542f07a622633dd64c25393b8`  
		Last Modified: Wed, 15 Feb 2023 03:00:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.9` - linux; s390x

```console
$ docker pull traefik@sha256:07885187fc52fd8ff0a452b7d717d1a903ebf5da9cf520dc76e91dd8d33c97ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37422861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f61b3fb75835c977ba4c7708081a6ccf524c05037f4887dfd00f22595fd3bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 01:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 01:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 01:15:33 GMT
EXPOSE 80
# Wed, 15 Feb 2023 01:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 01:15:33 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 01:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d8313315918fc17d3ece316f1d4d8120d45cd6a5890513eb9c0b2e4b71241`  
		Last Modified: Wed, 15 Feb 2023 01:16:11 GMT  
		Size: 34.1 MB (34145842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b9c9537c81a395883a12f8ce134f9ac80dfa0af0cfa9965ef2d11818b53f9c`  
		Last Modified: Wed, 15 Feb 2023 01:16:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:215ef7bc4716a538be92bf07e8a2cde01d843bd97f103d1926fc291e72d0359f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:2.9-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:a66fe3285811d47b416d52cff1039a2be1272ef65911e5d4408a5abe80d9c395
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1743763194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55c1fc2d695137bcb70e5e160edfeb678ff3b32ba7d1ee39ad5188fc3062181`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 23:31:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Feb 2023 23:31:53 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:31:54 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Feb 2023 23:31:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808cf7622e268fdf6b4b307ecfed6fc1202a1fe72ba4ba7c5b2d4158c2a4c11e`  
		Last Modified: Tue, 14 Feb 2023 23:32:42 GMT  
		Size: 35.8 MB (35813657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea9822173d84ad1124265a8bb5b13842edd3838a19ba9a6f9457068b69d3c27`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afac8a1dc53167b33acaa33afd475d8c3c210190a3286ccb2814bd3ec611fc7`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce789abd0db635843e66b061f366caa2b6631bf7676b637ecfe2c1614e4cf2`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.9.8`

```console
$ docker pull traefik@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `traefik:2.9.8-windowsservercore-1809`

```console
$ docker pull traefik@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `traefik:3.0`

```console
$ docker pull traefik@sha256:2ee635d5a3f9ab51ac38e4f1c23b81aa032caebddc0c4a17fef4b0ce67a0c5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0` - linux; amd64

```console
$ docker pull traefik@sha256:bf822393b55095bc13f7699ae1fa1b56bbe2e072bc2ae283bffd3a4dadd98d7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40563449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ad70784035ddea0808eeb76e7f8a6bc64e2cb867b63c6513f8f4e853f1133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:33 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:33 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc32ef302c3bee4df8ba7b31c8717d000beefd7e66fbdcc07450792441ad67`  
		Last Modified: Sat, 11 Feb 2023 14:06:28 GMT  
		Size: 37.1 MB (37074888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f96cb39092b375e76e59ca53f161a1777975c9c58ea5d46e480812addb564`  
		Last Modified: Sat, 11 Feb 2023 14:06:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:38a72f51da3516567e454612ebf9c705505d81d7c6a128023c6e78eac79d7133
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38289710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd914e7e9ec33c8b17a562f98d7938a2c3cf1b28b15c57175d58e9ac58c47f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:15 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:16 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b17904232ad841e1008a38d3198e139f7c1dc9623cf4ec7a1ea4befe331e`  
		Last Modified: Sat, 11 Feb 2023 07:30:56 GMT  
		Size: 35.0 MB (34989317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8978277a0c0a32ed1141dbed8a27b2d62173b22c5ec97e74d14da614e29318`  
		Last Modified: Sat, 11 Feb 2023 07:30:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:49b2e1db6ca60eae983dab7632ed2ea3997c698d05dd6789eeac4de13c94ea14
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37408591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b18449b8e63bade321e2c66ff5674dd5d7e3a36154f012db7b37c3c668a53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:30 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:30 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1381066f019ec8bedc5c9e8c8dcae4ed86e75cb46d22c461d5a87a060f23a`  
		Last Modified: Sat, 11 Feb 2023 06:41:17 GMT  
		Size: 34.0 MB (34023515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac00a09db30fc81aca200d38461e38fcc368b57e9878c1f51bb832b235e287d`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:c50bbeaf64f9b8a1d4a6f4ec10ff476e2066ac2dc59230bf8f02ce77f9cb4f5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39132486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d71fc91baad09e19cde42a2c649d7dc4a303b86b94d97f988e69e7da9222d76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 05:21:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 05:21:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 05:21:37 GMT
EXPOSE 80
# Sat, 11 Feb 2023 05:21:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:21:37 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 05:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1f663552d308b8665c6af4376a263f91e8bf072db5dce19d544e897af5aa9`  
		Last Modified: Sat, 11 Feb 2023 05:22:30 GMT  
		Size: 35.9 MB (35855467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a80fe50e1182c4db36fc9b9c0c0ed898c4e2745f7b16e7a2654fa5a403a2d`  
		Last Modified: Sat, 11 Feb 2023 05:22:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4e4873c46e1405633ba807d466905287ba16748a64f0ef5d62bb638487770888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:0812d9fa20ee998bd80da2264dd751babce5c77c51c578d9396860130d5c01ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1745532327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ae00dec5210bb28052cf25de60e9ecfc714b8e21523f5185b414e7f85eacfc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:09:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 12 Jan 2023 08:09:37 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:09:38 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:09:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d503c8b525fe53b864daad518042ee97e12921ace8b41afc4726c356773bcd06`  
		Last Modified: Thu, 12 Jan 2023 08:11:54 GMT  
		Size: 37.6 MB (37582767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0478827f4dbc2809903391adcc658352dc2eaf714eb55f55ca9de6054c77`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ef5b83460aa4bef81cc5f121d7aa09e66e20640e36f680ce98f7179cb6d66b`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7253d7c7c3290a1f980222ce35b9a66f0241f0eb0cb83d1cface350deb5ab`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta2`

```console
$ docker pull traefik@sha256:2ee635d5a3f9ab51ac38e4f1c23b81aa032caebddc0c4a17fef4b0ce67a0c5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:3.0.0-beta2` - linux; amd64

```console
$ docker pull traefik@sha256:bf822393b55095bc13f7699ae1fa1b56bbe2e072bc2ae283bffd3a4dadd98d7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40563449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ad70784035ddea0808eeb76e7f8a6bc64e2cb867b63c6513f8f4e853f1133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:33 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:33 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc32ef302c3bee4df8ba7b31c8717d000beefd7e66fbdcc07450792441ad67`  
		Last Modified: Sat, 11 Feb 2023 14:06:28 GMT  
		Size: 37.1 MB (37074888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f96cb39092b375e76e59ca53f161a1777975c9c58ea5d46e480812addb564`  
		Last Modified: Sat, 11 Feb 2023 14:06:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:38a72f51da3516567e454612ebf9c705505d81d7c6a128023c6e78eac79d7133
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38289710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd914e7e9ec33c8b17a562f98d7938a2c3cf1b28b15c57175d58e9ac58c47f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:15 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:16 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b17904232ad841e1008a38d3198e139f7c1dc9623cf4ec7a1ea4befe331e`  
		Last Modified: Sat, 11 Feb 2023 07:30:56 GMT  
		Size: 35.0 MB (34989317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8978277a0c0a32ed1141dbed8a27b2d62173b22c5ec97e74d14da614e29318`  
		Last Modified: Sat, 11 Feb 2023 07:30:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:49b2e1db6ca60eae983dab7632ed2ea3997c698d05dd6789eeac4de13c94ea14
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37408591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b18449b8e63bade321e2c66ff5674dd5d7e3a36154f012db7b37c3c668a53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:30 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:30 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1381066f019ec8bedc5c9e8c8dcae4ed86e75cb46d22c461d5a87a060f23a`  
		Last Modified: Sat, 11 Feb 2023 06:41:17 GMT  
		Size: 34.0 MB (34023515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac00a09db30fc81aca200d38461e38fcc368b57e9878c1f51bb832b235e287d`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-beta2` - linux; s390x

```console
$ docker pull traefik@sha256:c50bbeaf64f9b8a1d4a6f4ec10ff476e2066ac2dc59230bf8f02ce77f9cb4f5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39132486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d71fc91baad09e19cde42a2c649d7dc4a303b86b94d97f988e69e7da9222d76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 05:21:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 05:21:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 05:21:37 GMT
EXPOSE 80
# Sat, 11 Feb 2023 05:21:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:21:37 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 05:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1f663552d308b8665c6af4376a263f91e8bf072db5dce19d544e897af5aa9`  
		Last Modified: Sat, 11 Feb 2023 05:22:30 GMT  
		Size: 35.9 MB (35855467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a80fe50e1182c4db36fc9b9c0c0ed898c4e2745f7b16e7a2654fa5a403a2d`  
		Last Modified: Sat, 11 Feb 2023 05:22:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-beta2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4e4873c46e1405633ba807d466905287ba16748a64f0ef5d62bb638487770888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:3.0.0-beta2-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:0812d9fa20ee998bd80da2264dd751babce5c77c51c578d9396860130d5c01ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1745532327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ae00dec5210bb28052cf25de60e9ecfc714b8e21523f5185b414e7f85eacfc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:09:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 12 Jan 2023 08:09:37 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:09:38 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:09:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d503c8b525fe53b864daad518042ee97e12921ace8b41afc4726c356773bcd06`  
		Last Modified: Thu, 12 Jan 2023 08:11:54 GMT  
		Size: 37.6 MB (37582767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0478827f4dbc2809903391adcc658352dc2eaf714eb55f55ca9de6054c77`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ef5b83460aa4bef81cc5f121d7aa09e66e20640e36f680ce98f7179cb6d66b`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7253d7c7c3290a1f980222ce35b9a66f0241f0eb0cb83d1cface350deb5ab`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:banon`

```console
$ docker pull traefik@sha256:7a4fb968173b583bcf4aae0fea180cd6cd95001be686494d339da35809897cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:banon` - linux; amd64

```console
$ docker pull traefik@sha256:1f614d9645242cdd8eef1fd9e344fa1c9bd0ed5a5a30de4dbc41506f327d7420
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38771266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0e86397f2b094403ade8b63c70cc37fc6b46e9d62685b36a189139daa02b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 02:44:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 02:44:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 02:44:07 GMT
EXPOSE 80
# Wed, 15 Feb 2023 02:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 02:44:07 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 02:44:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee56f1b8420e11a19285128414fe8b580c55ae0344fec9a25689a2b9bb15ef4`  
		Last Modified: Wed, 15 Feb 2023 02:44:41 GMT  
		Size: 35.3 MB (35282705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a93139c311e646d9d7a0d54cd6b9d4d4dd63f01826b3e1ca43278f6ed78590`  
		Last Modified: Wed, 15 Feb 2023 02:44:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; arm variant v6

```console
$ docker pull traefik@sha256:23f7873a5b093e4fd79f8c73e07104359cd8414049d745689255e75576297701
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36621938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adde262bc17f9052ef4bf0278302876519d1963197a6e4e1926a156266f9794a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Feb 2023 23:45:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Feb 2023 23:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Feb 2023 23:45:40 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:45:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Feb 2023 23:45:40 GMT
CMD ["traefik"]
# Tue, 14 Feb 2023 23:45:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200d375a7d2d15bb2f36b51b82ed256c5e93e8a74fe02dcf40631638f0904a3c`  
		Last Modified: Tue, 14 Feb 2023 23:47:00 GMT  
		Size: 33.3 MB (33321544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ca36f9053054cd9568d42bfe631c966de835fb248a43afac60392966162d42`  
		Last Modified: Tue, 14 Feb 2023 23:46:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4fea093c218e9879dc904d6259ccf1c37b6c598131094237ef9315b5e655cab7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35755082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25591b4c17d6f05e5ae4c39fba11549f8423c773595e4d05afd7babfff6bef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 03:00:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 03:00:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 03:00:15 GMT
EXPOSE 80
# Wed, 15 Feb 2023 03:00:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 03:00:15 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 03:00:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b59175297242976fbda9978b9bb91d21dfc03087ade15af211ef03974dec93`  
		Last Modified: Wed, 15 Feb 2023 03:00:55 GMT  
		Size: 32.4 MB (32370006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e163b4ad7fced3b65af29248927428f8e5a32542f07a622633dd64c25393b8`  
		Last Modified: Wed, 15 Feb 2023 03:00:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:banon` - linux; s390x

```console
$ docker pull traefik@sha256:07885187fc52fd8ff0a452b7d717d1a903ebf5da9cf520dc76e91dd8d33c97ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37422861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f61b3fb75835c977ba4c7708081a6ccf524c05037f4887dfd00f22595fd3bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 01:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 01:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 01:15:33 GMT
EXPOSE 80
# Wed, 15 Feb 2023 01:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 01:15:33 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 01:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d8313315918fc17d3ece316f1d4d8120d45cd6a5890513eb9c0b2e4b71241`  
		Last Modified: Wed, 15 Feb 2023 01:16:11 GMT  
		Size: 34.1 MB (34145842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b9c9537c81a395883a12f8ce134f9ac80dfa0af0cfa9965ef2d11818b53f9c`  
		Last Modified: Wed, 15 Feb 2023 01:16:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:banon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:215ef7bc4716a538be92bf07e8a2cde01d843bd97f103d1926fc291e72d0359f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:banon-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:a66fe3285811d47b416d52cff1039a2be1272ef65911e5d4408a5abe80d9c395
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1743763194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55c1fc2d695137bcb70e5e160edfeb678ff3b32ba7d1ee39ad5188fc3062181`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 23:31:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Feb 2023 23:31:53 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:31:54 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Feb 2023 23:31:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808cf7622e268fdf6b4b307ecfed6fc1202a1fe72ba4ba7c5b2d4158c2a4c11e`  
		Last Modified: Tue, 14 Feb 2023 23:32:42 GMT  
		Size: 35.8 MB (35813657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea9822173d84ad1124265a8bb5b13842edd3838a19ba9a6f9457068b69d3c27`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afac8a1dc53167b33acaa33afd475d8c3c210190a3286ccb2814bd3ec611fc7`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce789abd0db635843e66b061f366caa2b6631bf7676b637ecfe2c1614e4cf2`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:2ee635d5a3f9ab51ac38e4f1c23b81aa032caebddc0c4a17fef4b0ce67a0c5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:bf822393b55095bc13f7699ae1fa1b56bbe2e072bc2ae283bffd3a4dadd98d7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40563449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ad70784035ddea0808eeb76e7f8a6bc64e2cb867b63c6513f8f4e853f1133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:33 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:33 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc32ef302c3bee4df8ba7b31c8717d000beefd7e66fbdcc07450792441ad67`  
		Last Modified: Sat, 11 Feb 2023 14:06:28 GMT  
		Size: 37.1 MB (37074888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f96cb39092b375e76e59ca53f161a1777975c9c58ea5d46e480812addb564`  
		Last Modified: Sat, 11 Feb 2023 14:06:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:38a72f51da3516567e454612ebf9c705505d81d7c6a128023c6e78eac79d7133
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38289710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd914e7e9ec33c8b17a562f98d7938a2c3cf1b28b15c57175d58e9ac58c47f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:15 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:16 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b17904232ad841e1008a38d3198e139f7c1dc9623cf4ec7a1ea4befe331e`  
		Last Modified: Sat, 11 Feb 2023 07:30:56 GMT  
		Size: 35.0 MB (34989317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8978277a0c0a32ed1141dbed8a27b2d62173b22c5ec97e74d14da614e29318`  
		Last Modified: Sat, 11 Feb 2023 07:30:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:49b2e1db6ca60eae983dab7632ed2ea3997c698d05dd6789eeac4de13c94ea14
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37408591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b18449b8e63bade321e2c66ff5674dd5d7e3a36154f012db7b37c3c668a53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:30 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:30 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1381066f019ec8bedc5c9e8c8dcae4ed86e75cb46d22c461d5a87a060f23a`  
		Last Modified: Sat, 11 Feb 2023 06:41:17 GMT  
		Size: 34.0 MB (34023515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac00a09db30fc81aca200d38461e38fcc368b57e9878c1f51bb832b235e287d`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:c50bbeaf64f9b8a1d4a6f4ec10ff476e2066ac2dc59230bf8f02ce77f9cb4f5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39132486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d71fc91baad09e19cde42a2c649d7dc4a303b86b94d97f988e69e7da9222d76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 05:21:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 05:21:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 05:21:37 GMT
EXPOSE 80
# Sat, 11 Feb 2023 05:21:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:21:37 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 05:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1f663552d308b8665c6af4376a263f91e8bf072db5dce19d544e897af5aa9`  
		Last Modified: Sat, 11 Feb 2023 05:22:30 GMT  
		Size: 35.9 MB (35855467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a80fe50e1182c4db36fc9b9c0c0ed898c4e2745f7b16e7a2654fa5a403a2d`  
		Last Modified: Sat, 11 Feb 2023 05:22:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4e4873c46e1405633ba807d466905287ba16748a64f0ef5d62bb638487770888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:0812d9fa20ee998bd80da2264dd751babce5c77c51c578d9396860130d5c01ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1745532327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ae00dec5210bb28052cf25de60e9ecfc714b8e21523f5185b414e7f85eacfc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:09:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 12 Jan 2023 08:09:37 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:09:38 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:09:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d503c8b525fe53b864daad518042ee97e12921ace8b41afc4726c356773bcd06`  
		Last Modified: Thu, 12 Jan 2023 08:11:54 GMT  
		Size: 37.6 MB (37582767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0478827f4dbc2809903391adcc658352dc2eaf714eb55f55ca9de6054c77`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ef5b83460aa4bef81cc5f121d7aa09e66e20640e36f680ce98f7179cb6d66b`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7253d7c7c3290a1f980222ce35b9a66f0241f0eb0cb83d1cface350deb5ab`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:7a4fb968173b583bcf4aae0fea180cd6cd95001be686494d339da35809897cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:1f614d9645242cdd8eef1fd9e344fa1c9bd0ed5a5a30de4dbc41506f327d7420
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38771266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0e86397f2b094403ade8b63c70cc37fc6b46e9d62685b36a189139daa02b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 02:44:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 02:44:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 02:44:07 GMT
EXPOSE 80
# Wed, 15 Feb 2023 02:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 02:44:07 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 02:44:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee56f1b8420e11a19285128414fe8b580c55ae0344fec9a25689a2b9bb15ef4`  
		Last Modified: Wed, 15 Feb 2023 02:44:41 GMT  
		Size: 35.3 MB (35282705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a93139c311e646d9d7a0d54cd6b9d4d4dd63f01826b3e1ca43278f6ed78590`  
		Last Modified: Wed, 15 Feb 2023 02:44:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:23f7873a5b093e4fd79f8c73e07104359cd8414049d745689255e75576297701
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36621938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adde262bc17f9052ef4bf0278302876519d1963197a6e4e1926a156266f9794a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Feb 2023 23:45:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Feb 2023 23:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Feb 2023 23:45:40 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:45:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Feb 2023 23:45:40 GMT
CMD ["traefik"]
# Tue, 14 Feb 2023 23:45:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200d375a7d2d15bb2f36b51b82ed256c5e93e8a74fe02dcf40631638f0904a3c`  
		Last Modified: Tue, 14 Feb 2023 23:47:00 GMT  
		Size: 33.3 MB (33321544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ca36f9053054cd9568d42bfe631c966de835fb248a43afac60392966162d42`  
		Last Modified: Tue, 14 Feb 2023 23:46:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4fea093c218e9879dc904d6259ccf1c37b6c598131094237ef9315b5e655cab7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35755082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25591b4c17d6f05e5ae4c39fba11549f8423c773595e4d05afd7babfff6bef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 03:00:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 03:00:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 03:00:15 GMT
EXPOSE 80
# Wed, 15 Feb 2023 03:00:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 03:00:15 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 03:00:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b59175297242976fbda9978b9bb91d21dfc03087ade15af211ef03974dec93`  
		Last Modified: Wed, 15 Feb 2023 03:00:55 GMT  
		Size: 32.4 MB (32370006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e163b4ad7fced3b65af29248927428f8e5a32542f07a622633dd64c25393b8`  
		Last Modified: Wed, 15 Feb 2023 03:00:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:07885187fc52fd8ff0a452b7d717d1a903ebf5da9cf520dc76e91dd8d33c97ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37422861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f61b3fb75835c977ba4c7708081a6ccf524c05037f4887dfd00f22595fd3bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 01:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 01:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 01:15:33 GMT
EXPOSE 80
# Wed, 15 Feb 2023 01:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 01:15:33 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 01:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d8313315918fc17d3ece316f1d4d8120d45cd6a5890513eb9c0b2e4b71241`  
		Last Modified: Wed, 15 Feb 2023 01:16:11 GMT  
		Size: 34.1 MB (34145842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b9c9537c81a395883a12f8ce134f9ac80dfa0af0cfa9965ef2d11818b53f9c`  
		Last Modified: Wed, 15 Feb 2023 01:16:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles`

```console
$ docker pull traefik@sha256:4bd2fbfb20b5ddb03ef8cf9f77d9726da942d92ebc206abca1865824d352cf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:a37a3469b7bd1e58d95ab5918f31f3a8aada1bdfa90f8d963eb78e8bae37d025
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22594315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b06305d2e0eca68d66088b5290a28c31dd73722f3f8e33c764bd60faf17edd7`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 11 Feb 2023 14:05:58 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Sat, 11 Feb 2023 14:05:59 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Sat, 11 Feb 2023 14:05:59 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:59 GMT
VOLUME [/tmp]
# Sat, 11 Feb 2023 14:05:59 GMT
ENTRYPOINT ["/traefik"]
# Sat, 11 Feb 2023 14:05:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b232dbde1f095d758c59886ecc24a42610dd35fd72116f3bf04738104e1cfa`  
		Last Modified: Sat, 11 Feb 2023 14:07:25 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066ff3631f4c0a13ebb72826195f8332b28aa6c9945865b1c07076fad46fb81b`  
		Last Modified: Sat, 11 Feb 2023 14:07:29 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ed51daf51f75bf5735027eed93829bc2ddc8cab5f7d2c92661e9ae240a812647
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21055568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35629440895fbdc6144fd69e6ddccee4de8aa7785af39e4804683304ac4f2df1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:59:12 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:59:13 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 11 Nov 2022 11:59:14 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:59:14 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:59:14 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:59:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0efdacb2b2ba042055ea537001460b2cff92ff305869705801b66bc44dc8565`  
		Last Modified: Fri, 11 Nov 2022 12:01:04 GMT  
		Size: 308.7 KB (308749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ebe6d2d943e776e37535f360e7b0f3745d625ee69f6ee5fe1eecee5487ce1`  
		Last Modified: Fri, 11 Nov 2022 12:01:08 GMT  
		Size: 20.6 MB (20623281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ac5b287132e97dc27bbd96791a25701e051ddce973d6ee70eda1c87138e3c299
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20563697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d5da1bea8e1a3e20b83ceca6e486a1e881451b1e304a0281d936d5e51f418d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:00:57 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:00:58 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 11 Nov 2022 11:00:58 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:00:58 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:00:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:00:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f6a6b590d30fda524213974a86d6ca01981b3ab4154a359b9c2e3fa3262c6`  
		Last Modified: Fri, 11 Nov 2022 11:02:04 GMT  
		Size: 308.8 KB (308813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af8a7d805d81cf74f58f3793659f76132259201bea15bbb7a0edc6191f8edfa`  
		Last Modified: Fri, 11 Nov 2022 11:02:07 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:40749b8ddac52c036c1e70f65175304503ec9a0e5afd2f06f855c45e6b6e9556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:6a5bf0d59212a73927e18da4a5b85ff7d02fb566283bcd10b3c307b8a39627a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25653523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299327139165b0025a883c7a11747b5d04c4bc72f053601c0f763fee0ed761a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:46 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:51 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:52 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:52 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fab313a1ca0ee79d027587c5edad5ff243a08e1cbd263abe2a17503c316d8b`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 661.5 KB (661461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e550be36e43026c7c9214cf16b3b866de5ce1da12f14fcef46658c0def1d4a7`  
		Last Modified: Sat, 11 Feb 2023 14:07:12 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4561714fba29bd0d410fa9813afc75479ffef93714ffdad849a7943771d73544`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c877680359edeb36e0f7b0749fbb09a801a680d177cda3b4cfbb42c8562ab55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23928217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7628e269edbd96b0ce234c48ad415c771aae9f62ea77226d2902180116cd4388`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:41 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Fri, 10 Feb 2023 20:49:41 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:41 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:41 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d249d387e6c91bac13ecc5746b760ce33da5956b1857574c15c4ba2b5002a4`  
		Last Modified: Sat, 11 Feb 2023 07:31:47 GMT  
		Size: 666.3 KB (666280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4a0aee18eee90e65c8dc3e3cf8ceb25a9aee2aef1b26d1322d7a7b2392295f`  
		Last Modified: Sat, 11 Feb 2023 07:31:50 GMT  
		Size: 20.6 MB (20623417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5e05661e72c78c68ccdc37047515cc68b8aafff48c76185f4381a9c0954cf0`  
		Last Modified: Sat, 11 Feb 2023 07:31:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e23b8edb3c8a7f4a5ce7b2697e304f8e31d845474dccdbcd15b86e831c7bc69b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23519920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dbaffc2f8e74c9ed9aa7a99d590e792ba2b318e8562992180335ba122958e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:46 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:46 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:46 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5c8dd85906c92d3445ffeb0481950055e77c854095c4cbbd854f6951242a3c`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 663.2 KB (663163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994ad8baa5503f4c667ced5bb36b643eba7642f9791e4bf7975527de9f2c2ed`  
		Last Modified: Sat, 11 Feb 2023 06:41:57 GMT  
		Size: 20.1 MB (20131363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6a5a822a3369f9999a4da4bcb9718729d386c2dbf108fb8a8a52056eacc8d2`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f8223de1afb5c0d3c84ac73737d280550d6c118d326dda320af3d6c84a1cc42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:608c9a5abd6dcd8831958380ec03bf2b6d756d151ff8bef7c387ff157223a3c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1730802068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789e7cee983ab7e7e598355f69c9db141fd644d2e5c467b9d49f0750c561a887`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:11:17 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 12 Jan 2023 08:11:18 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:11:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:11:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1c4961b4b546f722e4a1e76673f9e32be91d74d2f8afbcc97fa90b491357f7`  
		Last Modified: Thu, 12 Jan 2023 08:12:40 GMT  
		Size: 22.9 MB (22852479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8695c3b7b24056e2113dcc6735b59d46b4d0b13567be65bd3a89a4e96f052`  
		Last Modified: Thu, 12 Jan 2023 08:12:34 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ae219d0779fe8847f8e1d50e8e35f27c0ea05e783a1d06bb67a0c1446b46e`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0a9394409e220db17e543bcb32779dbb83a4a71063bd777206ee09133c69e2`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7`

```console
$ docker pull traefik@sha256:4bd2fbfb20b5ddb03ef8cf9f77d9726da942d92ebc206abca1865824d352cf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7` - linux; amd64

```console
$ docker pull traefik@sha256:a37a3469b7bd1e58d95ab5918f31f3a8aada1bdfa90f8d963eb78e8bae37d025
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22594315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b06305d2e0eca68d66088b5290a28c31dd73722f3f8e33c764bd60faf17edd7`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 11 Feb 2023 14:05:58 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Sat, 11 Feb 2023 14:05:59 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Sat, 11 Feb 2023 14:05:59 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:59 GMT
VOLUME [/tmp]
# Sat, 11 Feb 2023 14:05:59 GMT
ENTRYPOINT ["/traefik"]
# Sat, 11 Feb 2023 14:05:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b232dbde1f095d758c59886ecc24a42610dd35fd72116f3bf04738104e1cfa`  
		Last Modified: Sat, 11 Feb 2023 14:07:25 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066ff3631f4c0a13ebb72826195f8332b28aa6c9945865b1c07076fad46fb81b`  
		Last Modified: Sat, 11 Feb 2023 14:07:29 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ed51daf51f75bf5735027eed93829bc2ddc8cab5f7d2c92661e9ae240a812647
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21055568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35629440895fbdc6144fd69e6ddccee4de8aa7785af39e4804683304ac4f2df1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:59:12 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:59:13 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 11 Nov 2022 11:59:14 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:59:14 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:59:14 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:59:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0efdacb2b2ba042055ea537001460b2cff92ff305869705801b66bc44dc8565`  
		Last Modified: Fri, 11 Nov 2022 12:01:04 GMT  
		Size: 308.7 KB (308749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ebe6d2d943e776e37535f360e7b0f3745d625ee69f6ee5fe1eecee5487ce1`  
		Last Modified: Fri, 11 Nov 2022 12:01:08 GMT  
		Size: 20.6 MB (20623281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ac5b287132e97dc27bbd96791a25701e051ddce973d6ee70eda1c87138e3c299
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20563697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d5da1bea8e1a3e20b83ceca6e486a1e881451b1e304a0281d936d5e51f418d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:00:57 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:00:58 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 11 Nov 2022 11:00:58 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:00:58 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:00:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:00:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f6a6b590d30fda524213974a86d6ca01981b3ab4154a359b9c2e3fa3262c6`  
		Last Modified: Fri, 11 Nov 2022 11:02:04 GMT  
		Size: 308.8 KB (308813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af8a7d805d81cf74f58f3793659f76132259201bea15bbb7a0edc6191f8edfa`  
		Last Modified: Fri, 11 Nov 2022 11:02:07 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-alpine`

```console
$ docker pull traefik@sha256:40749b8ddac52c036c1e70f65175304503ec9a0e5afd2f06f855c45e6b6e9556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:6a5bf0d59212a73927e18da4a5b85ff7d02fb566283bcd10b3c307b8a39627a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25653523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299327139165b0025a883c7a11747b5d04c4bc72f053601c0f763fee0ed761a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:46 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:51 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:52 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:52 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fab313a1ca0ee79d027587c5edad5ff243a08e1cbd263abe2a17503c316d8b`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 661.5 KB (661461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e550be36e43026c7c9214cf16b3b866de5ce1da12f14fcef46658c0def1d4a7`  
		Last Modified: Sat, 11 Feb 2023 14:07:12 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4561714fba29bd0d410fa9813afc75479ffef93714ffdad849a7943771d73544`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c877680359edeb36e0f7b0749fbb09a801a680d177cda3b4cfbb42c8562ab55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23928217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7628e269edbd96b0ce234c48ad415c771aae9f62ea77226d2902180116cd4388`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:41 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Fri, 10 Feb 2023 20:49:41 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:41 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:41 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d249d387e6c91bac13ecc5746b760ce33da5956b1857574c15c4ba2b5002a4`  
		Last Modified: Sat, 11 Feb 2023 07:31:47 GMT  
		Size: 666.3 KB (666280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4a0aee18eee90e65c8dc3e3cf8ceb25a9aee2aef1b26d1322d7a7b2392295f`  
		Last Modified: Sat, 11 Feb 2023 07:31:50 GMT  
		Size: 20.6 MB (20623417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5e05661e72c78c68ccdc37047515cc68b8aafff48c76185f4381a9c0954cf0`  
		Last Modified: Sat, 11 Feb 2023 07:31:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e23b8edb3c8a7f4a5ce7b2697e304f8e31d845474dccdbcd15b86e831c7bc69b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23519920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dbaffc2f8e74c9ed9aa7a99d590e792ba2b318e8562992180335ba122958e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:46 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:46 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:46 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5c8dd85906c92d3445ffeb0481950055e77c854095c4cbbd854f6951242a3c`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 663.2 KB (663163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994ad8baa5503f4c667ced5bb36b643eba7642f9791e4bf7975527de9f2c2ed`  
		Last Modified: Sat, 11 Feb 2023 06:41:57 GMT  
		Size: 20.1 MB (20131363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6a5a822a3369f9999a4da4bcb9718729d386c2dbf108fb8a8a52056eacc8d2`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f8223de1afb5c0d3c84ac73737d280550d6c118d326dda320af3d6c84a1cc42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:v1.7-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:608c9a5abd6dcd8831958380ec03bf2b6d756d151ff8bef7c387ff157223a3c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1730802068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789e7cee983ab7e7e598355f69c9db141fd644d2e5c467b9d49f0750c561a887`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:11:17 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 12 Jan 2023 08:11:18 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:11:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:11:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1c4961b4b546f722e4a1e76673f9e32be91d74d2f8afbcc97fa90b491357f7`  
		Last Modified: Thu, 12 Jan 2023 08:12:40 GMT  
		Size: 22.9 MB (22852479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8695c3b7b24056e2113dcc6735b59d46b4d0b13567be65bd3a89a4e96f052`  
		Last Modified: Thu, 12 Jan 2023 08:12:34 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ae219d0779fe8847f8e1d50e8e35f27c0ea05e783a1d06bb67a0c1446b46e`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0a9394409e220db17e543bcb32779dbb83a4a71063bd777206ee09133c69e2`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34`

```console
$ docker pull traefik@sha256:4bd2fbfb20b5ddb03ef8cf9f77d9726da942d92ebc206abca1865824d352cf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34` - linux; amd64

```console
$ docker pull traefik@sha256:a37a3469b7bd1e58d95ab5918f31f3a8aada1bdfa90f8d963eb78e8bae37d025
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22594315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b06305d2e0eca68d66088b5290a28c31dd73722f3f8e33c764bd60faf17edd7`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 11 Feb 2023 14:05:58 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Sat, 11 Feb 2023 14:05:59 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Sat, 11 Feb 2023 14:05:59 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:59 GMT
VOLUME [/tmp]
# Sat, 11 Feb 2023 14:05:59 GMT
ENTRYPOINT ["/traefik"]
# Sat, 11 Feb 2023 14:05:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b232dbde1f095d758c59886ecc24a42610dd35fd72116f3bf04738104e1cfa`  
		Last Modified: Sat, 11 Feb 2023 14:07:25 GMT  
		Size: 308.8 KB (308823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066ff3631f4c0a13ebb72826195f8332b28aa6c9945865b1c07076fad46fb81b`  
		Last Modified: Sat, 11 Feb 2023 14:07:29 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ed51daf51f75bf5735027eed93829bc2ddc8cab5f7d2c92661e9ae240a812647
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21055568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35629440895fbdc6144fd69e6ddccee4de8aa7785af39e4804683304ac4f2df1`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 28 Oct 2022 00:15:28 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:59:12 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:59:13 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Fri, 11 Nov 2022 11:59:14 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:59:14 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:59:14 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:59:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93432fb5c46fdb5c83e424ff85db4e06a08e5ac2ec96ce9e11f1c60f5a86d29b`  
		Last Modified: Fri, 28 Oct 2022 00:17:20 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0efdacb2b2ba042055ea537001460b2cff92ff305869705801b66bc44dc8565`  
		Last Modified: Fri, 11 Nov 2022 12:01:04 GMT  
		Size: 308.7 KB (308749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849ebe6d2d943e776e37535f360e7b0f3745d625ee69f6ee5fe1eecee5487ce1`  
		Last Modified: Fri, 11 Nov 2022 12:01:08 GMT  
		Size: 20.6 MB (20623281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ac5b287132e97dc27bbd96791a25701e051ddce973d6ee70eda1c87138e3c299
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20563697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d5da1bea8e1a3e20b83ceca6e486a1e881451b1e304a0281d936d5e51f418d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 11 Nov 2022 11:00:57 GMT
COPY dir:3b1b1d8650d4180b42ead5fd074947c16b0405195b425df367fbf007be68841d in /usr/share/ 
# Fri, 11 Nov 2022 11:00:58 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 11 Nov 2022 11:00:58 GMT
EXPOSE 80
# Fri, 11 Nov 2022 11:00:58 GMT
VOLUME [/tmp]
# Fri, 11 Nov 2022 11:00:58 GMT
ENTRYPOINT ["/traefik"]
# Fri, 11 Nov 2022 11:00:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f6a6b590d30fda524213974a86d6ca01981b3ab4154a359b9c2e3fa3262c6`  
		Last Modified: Fri, 11 Nov 2022 11:02:04 GMT  
		Size: 308.8 KB (308813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af8a7d805d81cf74f58f3793659f76132259201bea15bbb7a0edc6191f8edfa`  
		Last Modified: Fri, 11 Nov 2022 11:02:07 GMT  
		Size: 20.1 MB (20131346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-alpine`

```console
$ docker pull traefik@sha256:40749b8ddac52c036c1e70f65175304503ec9a0e5afd2f06f855c45e6b6e9556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:v1.7.34-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:6a5bf0d59212a73927e18da4a5b85ff7d02fb566283bcd10b3c307b8a39627a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25653523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299327139165b0025a883c7a11747b5d04c4bc72f053601c0f763fee0ed761a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:46 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:51 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:51 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:52 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:52 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fab313a1ca0ee79d027587c5edad5ff243a08e1cbd263abe2a17503c316d8b`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 661.5 KB (661461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e550be36e43026c7c9214cf16b3b866de5ce1da12f14fcef46658c0def1d4a7`  
		Last Modified: Sat, 11 Feb 2023 14:07:12 GMT  
		Size: 22.2 MB (22162062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4561714fba29bd0d410fa9813afc75479ffef93714ffdad849a7943771d73544`  
		Last Modified: Sat, 11 Feb 2023 14:07:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c877680359edeb36e0f7b0749fbb09a801a680d177cda3b4cfbb42c8562ab55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23928217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7628e269edbd96b0ce234c48ad415c771aae9f62ea77226d2902180116cd4388`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:41 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Fri, 10 Feb 2023 20:49:41 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:35 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:41 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:41 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:41 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d249d387e6c91bac13ecc5746b760ce33da5956b1857574c15c4ba2b5002a4`  
		Last Modified: Sat, 11 Feb 2023 07:31:47 GMT  
		Size: 666.3 KB (666280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4a0aee18eee90e65c8dc3e3cf8ceb25a9aee2aef1b26d1322d7a7b2392295f`  
		Last Modified: Sat, 11 Feb 2023 07:31:50 GMT  
		Size: 20.6 MB (20623417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5e05661e72c78c68ccdc37047515cc68b8aafff48c76185f4381a9c0954cf0`  
		Last Modified: Sat, 11 Feb 2023 07:31:46 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v1.7.34-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e23b8edb3c8a7f4a5ce7b2697e304f8e31d845474dccdbcd15b86e831c7bc69b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23519920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dbaffc2f8e74c9ed9aa7a99d590e792ba2b318e8562992180335ba122958e3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:46 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:46 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:46 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5c8dd85906c92d3445ffeb0481950055e77c854095c4cbbd854f6951242a3c`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 663.2 KB (663163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0994ad8baa5503f4c667ced5bb36b643eba7642f9791e4bf7975527de9f2c2ed`  
		Last Modified: Sat, 11 Feb 2023 06:41:57 GMT  
		Size: 20.1 MB (20131363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6a5a822a3369f9999a4da4bcb9718729d386c2dbf108fb8a8a52056eacc8d2`  
		Last Modified: Sat, 11 Feb 2023 06:41:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v1.7.34-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f8223de1afb5c0d3c84ac73737d280550d6c118d326dda320af3d6c84a1cc42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:v1.7.34-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:608c9a5abd6dcd8831958380ec03bf2b6d756d151ff8bef7c387ff157223a3c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1730802068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789e7cee983ab7e7e598355f69c9db141fd644d2e5c467b9d49f0750c561a887`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:11:17 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Thu, 12 Jan 2023 08:11:18 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:11:19 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:11:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1c4961b4b546f722e4a1e76673f9e32be91d74d2f8afbcc97fa90b491357f7`  
		Last Modified: Thu, 12 Jan 2023 08:12:40 GMT  
		Size: 22.9 MB (22852479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8695c3b7b24056e2113dcc6735b59d46b4d0b13567be65bd3a89a4e96f052`  
		Last Modified: Thu, 12 Jan 2023 08:12:34 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507ae219d0779fe8847f8e1d50e8e35f27c0ea05e783a1d06bb67a0c1446b46e`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0a9394409e220db17e543bcb32779dbb83a4a71063bd777206ee09133c69e2`  
		Last Modified: Thu, 12 Jan 2023 08:12:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9`

```console
$ docker pull traefik@sha256:7a4fb968173b583bcf4aae0fea180cd6cd95001be686494d339da35809897cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v2.9` - linux; amd64

```console
$ docker pull traefik@sha256:1f614d9645242cdd8eef1fd9e344fa1c9bd0ed5a5a30de4dbc41506f327d7420
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38771266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0e86397f2b094403ade8b63c70cc37fc6b46e9d62685b36a189139daa02b7b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 02:44:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 02:44:07 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 02:44:07 GMT
EXPOSE 80
# Wed, 15 Feb 2023 02:44:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 02:44:07 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 02:44:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee56f1b8420e11a19285128414fe8b580c55ae0344fec9a25689a2b9bb15ef4`  
		Last Modified: Wed, 15 Feb 2023 02:44:41 GMT  
		Size: 35.3 MB (35282705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a93139c311e646d9d7a0d54cd6b9d4d4dd63f01826b3e1ca43278f6ed78590`  
		Last Modified: Wed, 15 Feb 2023 02:44:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.9` - linux; arm variant v6

```console
$ docker pull traefik@sha256:23f7873a5b093e4fd79f8c73e07104359cd8414049d745689255e75576297701
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36621938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adde262bc17f9052ef4bf0278302876519d1963197a6e4e1926a156266f9794a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 14 Feb 2023 23:45:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 14 Feb 2023 23:45:40 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 14 Feb 2023 23:45:40 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:45:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Feb 2023 23:45:40 GMT
CMD ["traefik"]
# Tue, 14 Feb 2023 23:45:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200d375a7d2d15bb2f36b51b82ed256c5e93e8a74fe02dcf40631638f0904a3c`  
		Last Modified: Tue, 14 Feb 2023 23:47:00 GMT  
		Size: 33.3 MB (33321544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ca36f9053054cd9568d42bfe631c966de835fb248a43afac60392966162d42`  
		Last Modified: Tue, 14 Feb 2023 23:46:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.9` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4fea093c218e9879dc904d6259ccf1c37b6c598131094237ef9315b5e655cab7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35755082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25591b4c17d6f05e5ae4c39fba11549f8423c773595e4d05afd7babfff6bef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 03:00:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 03:00:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 03:00:15 GMT
EXPOSE 80
# Wed, 15 Feb 2023 03:00:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 03:00:15 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 03:00:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b59175297242976fbda9978b9bb91d21dfc03087ade15af211ef03974dec93`  
		Last Modified: Wed, 15 Feb 2023 03:00:55 GMT  
		Size: 32.4 MB (32370006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e163b4ad7fced3b65af29248927428f8e5a32542f07a622633dd64c25393b8`  
		Last Modified: Wed, 15 Feb 2023 03:00:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.9` - linux; s390x

```console
$ docker pull traefik@sha256:07885187fc52fd8ff0a452b7d717d1a903ebf5da9cf520dc76e91dd8d33c97ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37422861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f61b3fb75835c977ba4c7708081a6ccf524c05037f4887dfd00f22595fd3bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 15 Feb 2023 01:15:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 15 Feb 2023 01:15:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 15 Feb 2023 01:15:33 GMT
EXPOSE 80
# Wed, 15 Feb 2023 01:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Feb 2023 01:15:33 GMT
CMD ["traefik"]
# Wed, 15 Feb 2023 01:15:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d8313315918fc17d3ece316f1d4d8120d45cd6a5890513eb9c0b2e4b71241`  
		Last Modified: Wed, 15 Feb 2023 01:16:11 GMT  
		Size: 34.1 MB (34145842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b9c9537c81a395883a12f8ce134f9ac80dfa0af0cfa9965ef2d11818b53f9c`  
		Last Modified: Wed, 15 Feb 2023 01:16:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9-windowsservercore-1809`

```console
$ docker pull traefik@sha256:215ef7bc4716a538be92bf07e8a2cde01d843bd97f103d1926fc291e72d0359f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:v2.9-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:a66fe3285811d47b416d52cff1039a2be1272ef65911e5d4408a5abe80d9c395
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1743763194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55c1fc2d695137bcb70e5e160edfeb678ff3b32ba7d1ee39ad5188fc3062181`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 23:31:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Feb 2023 23:31:53 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:31:54 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Feb 2023 23:31:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808cf7622e268fdf6b4b307ecfed6fc1202a1fe72ba4ba7c5b2d4158c2a4c11e`  
		Last Modified: Tue, 14 Feb 2023 23:32:42 GMT  
		Size: 35.8 MB (35813657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea9822173d84ad1124265a8bb5b13842edd3838a19ba9a6f9457068b69d3c27`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afac8a1dc53167b33acaa33afd475d8c3c210190a3286ccb2814bd3ec611fc7`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce789abd0db635843e66b061f366caa2b6631bf7676b637ecfe2c1614e4cf2`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.9.8`

```console
$ docker pull traefik@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `traefik:v2.9.8-windowsservercore-1809`

```console
$ docker pull traefik@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:2ee635d5a3f9ab51ac38e4f1c23b81aa032caebddc0c4a17fef4b0ce67a0c5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0` - linux; amd64

```console
$ docker pull traefik@sha256:bf822393b55095bc13f7699ae1fa1b56bbe2e072bc2ae283bffd3a4dadd98d7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40563449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ad70784035ddea0808eeb76e7f8a6bc64e2cb867b63c6513f8f4e853f1133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:33 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:33 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc32ef302c3bee4df8ba7b31c8717d000beefd7e66fbdcc07450792441ad67`  
		Last Modified: Sat, 11 Feb 2023 14:06:28 GMT  
		Size: 37.1 MB (37074888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f96cb39092b375e76e59ca53f161a1777975c9c58ea5d46e480812addb564`  
		Last Modified: Sat, 11 Feb 2023 14:06:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:38a72f51da3516567e454612ebf9c705505d81d7c6a128023c6e78eac79d7133
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38289710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd914e7e9ec33c8b17a562f98d7938a2c3cf1b28b15c57175d58e9ac58c47f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:15 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:16 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b17904232ad841e1008a38d3198e139f7c1dc9623cf4ec7a1ea4befe331e`  
		Last Modified: Sat, 11 Feb 2023 07:30:56 GMT  
		Size: 35.0 MB (34989317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8978277a0c0a32ed1141dbed8a27b2d62173b22c5ec97e74d14da614e29318`  
		Last Modified: Sat, 11 Feb 2023 07:30:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:49b2e1db6ca60eae983dab7632ed2ea3997c698d05dd6789eeac4de13c94ea14
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37408591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b18449b8e63bade321e2c66ff5674dd5d7e3a36154f012db7b37c3c668a53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:30 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:30 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1381066f019ec8bedc5c9e8c8dcae4ed86e75cb46d22c461d5a87a060f23a`  
		Last Modified: Sat, 11 Feb 2023 06:41:17 GMT  
		Size: 34.0 MB (34023515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac00a09db30fc81aca200d38461e38fcc368b57e9878c1f51bb832b235e287d`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:c50bbeaf64f9b8a1d4a6f4ec10ff476e2066ac2dc59230bf8f02ce77f9cb4f5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39132486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d71fc91baad09e19cde42a2c649d7dc4a303b86b94d97f988e69e7da9222d76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 05:21:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 05:21:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 05:21:37 GMT
EXPOSE 80
# Sat, 11 Feb 2023 05:21:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:21:37 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 05:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1f663552d308b8665c6af4376a263f91e8bf072db5dce19d544e897af5aa9`  
		Last Modified: Sat, 11 Feb 2023 05:22:30 GMT  
		Size: 35.9 MB (35855467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a80fe50e1182c4db36fc9b9c0c0ed898c4e2745f7b16e7a2654fa5a403a2d`  
		Last Modified: Sat, 11 Feb 2023 05:22:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4e4873c46e1405633ba807d466905287ba16748a64f0ef5d62bb638487770888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:0812d9fa20ee998bd80da2264dd751babce5c77c51c578d9396860130d5c01ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1745532327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ae00dec5210bb28052cf25de60e9ecfc714b8e21523f5185b414e7f85eacfc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:09:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 12 Jan 2023 08:09:37 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:09:38 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:09:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d503c8b525fe53b864daad518042ee97e12921ace8b41afc4726c356773bcd06`  
		Last Modified: Thu, 12 Jan 2023 08:11:54 GMT  
		Size: 37.6 MB (37582767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0478827f4dbc2809903391adcc658352dc2eaf714eb55f55ca9de6054c77`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ef5b83460aa4bef81cc5f121d7aa09e66e20640e36f680ce98f7179cb6d66b`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7253d7c7c3290a1f980222ce35b9a66f0241f0eb0cb83d1cface350deb5ab`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta2`

```console
$ docker pull traefik@sha256:2ee635d5a3f9ab51ac38e4f1c23b81aa032caebddc0c4a17fef4b0ce67a0c5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:v3.0.0-beta2` - linux; amd64

```console
$ docker pull traefik@sha256:bf822393b55095bc13f7699ae1fa1b56bbe2e072bc2ae283bffd3a4dadd98d7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40563449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ad70784035ddea0808eeb76e7f8a6bc64e2cb867b63c6513f8f4e853f1133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:54 GMT
ADD file:cdac18271416ac5bf6876b7ea9af1129108d03f9813589dfda113e5f09d6b80b in / 
# Sat, 11 Feb 2023 04:46:55 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 14:05:27 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 14:05:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 14:05:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 14:05:33 GMT
EXPOSE 80
# Sat, 11 Feb 2023 14:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 14:05:33 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 14:05:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:895e193edb5191bf66fb5ccb29f5d3659e05eec5953255180cbdd66520e7c517`  
		Last Modified: Sat, 11 Feb 2023 04:47:40 GMT  
		Size: 2.8 MB (2826146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3655af1bbd56df1bcfec44686273a57d30cc0b69f6e501f87ec67712913b8b55`  
		Last Modified: Sat, 11 Feb 2023 14:06:23 GMT  
		Size: 662.0 KB (662047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cc32ef302c3bee4df8ba7b31c8717d000beefd7e66fbdcc07450792441ad67`  
		Last Modified: Sat, 11 Feb 2023 14:06:28 GMT  
		Size: 37.1 MB (37074888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f96cb39092b375e76e59ca53f161a1777975c9c58ea5d46e480812addb564`  
		Last Modified: Sat, 11 Feb 2023 14:06:22 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:38a72f51da3516567e454612ebf9c705505d81d7c6a128023c6e78eac79d7133
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38289710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd914e7e9ec33c8b17a562f98d7938a2c3cf1b28b15c57175d58e9ac58c47f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:29:09 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 07:29:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 07:29:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 07:29:15 GMT
EXPOSE 80
# Sat, 11 Feb 2023 07:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 07:29:16 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 07:29:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ab2c963984fccd926abab14ca2d152973ee20d445747e4a9ec4139b02dc43e`  
		Last Modified: Sat, 11 Feb 2023 07:30:48 GMT  
		Size: 666.4 KB (666376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9b17904232ad841e1008a38d3198e139f7c1dc9623cf4ec7a1ea4befe331e`  
		Last Modified: Sat, 11 Feb 2023 07:30:56 GMT  
		Size: 35.0 MB (34989317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8978277a0c0a32ed1141dbed8a27b2d62173b22c5ec97e74d14da614e29318`  
		Last Modified: Sat, 11 Feb 2023 07:30:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:49b2e1db6ca60eae983dab7632ed2ea3997c698d05dd6789eeac4de13c94ea14
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37408591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b18449b8e63bade321e2c66ff5674dd5d7e3a36154f012db7b37c3c668a53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:40:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 06:40:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 06:40:30 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 06:40:30 GMT
EXPOSE 80
# Sat, 11 Feb 2023 06:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:40:30 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 06:40:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57456bf9239ae8d2b09ba33d1227b60a493b664b0a0558a09a614e08aedf0438`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 663.2 KB (663152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e1381066f019ec8bedc5c9e8c8dcae4ed86e75cb46d22c461d5a87a060f23a`  
		Last Modified: Sat, 11 Feb 2023 06:41:17 GMT  
		Size: 34.0 MB (34023515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac00a09db30fc81aca200d38461e38fcc368b57e9878c1f51bb832b235e287d`  
		Last Modified: Sat, 11 Feb 2023 06:41:13 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-beta2` - linux; s390x

```console
$ docker pull traefik@sha256:c50bbeaf64f9b8a1d4a6f4ec10ff476e2066ac2dc59230bf8f02ce77f9cb4f5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39132486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d71fc91baad09e19cde42a2c649d7dc4a303b86b94d97f988e69e7da9222d76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:37 GMT
ADD file:8a7d887c96c361c6ae19ca804030a0d79a1984b9e32b6c3767ede695c6613909 in / 
# Fri, 10 Feb 2023 21:41:37 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:21:30 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 11 Feb 2023 05:21:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 11 Feb 2023 05:21:37 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 11 Feb 2023 05:21:37 GMT
EXPOSE 80
# Sat, 11 Feb 2023 05:21:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 05:21:37 GMT
CMD ["traefik"]
# Sat, 11 Feb 2023 05:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0d71e9a79f477719291f0a25b6a2462917f2e396325883144c1f1e59fbc56f21`  
		Last Modified: Fri, 10 Feb 2023 21:42:33 GMT  
		Size: 2.6 MB (2610267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e10f8aa3cb11731ad3d5cea5740b9baa80c4652f810b4efd47d507984fa8d8`  
		Last Modified: Sat, 11 Feb 2023 05:22:25 GMT  
		Size: 666.4 KB (666384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f1f663552d308b8665c6af4376a263f91e8bf072db5dce19d544e897af5aa9`  
		Last Modified: Sat, 11 Feb 2023 05:22:30 GMT  
		Size: 35.9 MB (35855467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6a80fe50e1182c4db36fc9b9c0c0ed898c4e2745f7b16e7a2654fa5a403a2d`  
		Last Modified: Sat, 11 Feb 2023 05:22:24 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-beta2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:4e4873c46e1405633ba807d466905287ba16748a64f0ef5d62bb638487770888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:v3.0.0-beta2-windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:0812d9fa20ee998bd80da2264dd751babce5c77c51c578d9396860130d5c01ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1745532327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ae00dec5210bb28052cf25de60e9ecfc714b8e21523f5185b414e7f85eacfc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 08:09:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-beta2/traefik_v3.0.0-beta2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 12 Jan 2023 08:09:37 GMT
EXPOSE 80
# Thu, 12 Jan 2023 08:09:38 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Jan 2023 08:09:39 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-beta2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d503c8b525fe53b864daad518042ee97e12921ace8b41afc4726c356773bcd06`  
		Last Modified: Thu, 12 Jan 2023 08:11:54 GMT  
		Size: 37.6 MB (37582767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e0478827f4dbc2809903391adcc658352dc2eaf714eb55f55ca9de6054c77`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ef5b83460aa4bef81cc5f121d7aa09e66e20640e36f680ce98f7179cb6d66b`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf7253d7c7c3290a1f980222ce35b9a66f0241f0eb0cb83d1cface350deb5ab`  
		Last Modified: Thu, 12 Jan 2023 08:11:45 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:215ef7bc4716a538be92bf07e8a2cde01d843bd97f103d1926fc291e72d0359f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.3887; amd64

```console
$ docker pull traefik@sha256:a66fe3285811d47b416d52cff1039a2be1272ef65911e5d4408a5abe80d9c395
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1743763194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55c1fc2d695137bcb70e5e160edfeb678ff3b32ba7d1ee39ad5188fc3062181`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Feb 2023 23:31:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.7/traefik_v2.9.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Feb 2023 23:31:53 GMT
EXPOSE 80
# Tue, 14 Feb 2023 23:31:54 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Feb 2023 23:31:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808cf7622e268fdf6b4b307ecfed6fc1202a1fe72ba4ba7c5b2d4158c2a4c11e`  
		Last Modified: Tue, 14 Feb 2023 23:32:42 GMT  
		Size: 35.8 MB (35813657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea9822173d84ad1124265a8bb5b13842edd3838a19ba9a6f9457068b69d3c27`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afac8a1dc53167b33acaa33afd475d8c3c210190a3286ccb2814bd3ec611fc7`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fce789abd0db635843e66b061f366caa2b6631bf7676b637ecfe2c1614e4cf2`  
		Last Modified: Tue, 14 Feb 2023 23:32:33 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
