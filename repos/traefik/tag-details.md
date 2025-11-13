<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.31`](#traefik21131)
-	[`traefik:2.11.31-nanoserver-ltsc2022`](#traefik21131-nanoserver-ltsc2022)
-	[`traefik:2.11.31-windowsservercore-ltsc2022`](#traefik21131-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.1`](#traefik361)
-	[`traefik:3.6.1-nanoserver-ltsc2022`](#traefik361-nanoserver-ltsc2022)
-	[`traefik:3.6.1-windowsservercore-ltsc2022`](#traefik361-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:ramequin`](#traefikramequin)
-	[`traefik:ramequin-nanoserver-ltsc2022`](#traefikramequin-nanoserver-ltsc2022)
-	[`traefik:ramequin-windowsservercore-ltsc2022`](#traefikramequin-windowsservercore-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.31`](#traefikv21131)
-	[`traefik:v2.11.31-nanoserver-ltsc2022`](#traefikv21131-nanoserver-ltsc2022)
-	[`traefik:v2.11.31-windowsservercore-ltsc2022`](#traefikv21131-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.1`](#traefikv361)
-	[`traefik:v3.6.1-nanoserver-ltsc2022`](#traefikv361-nanoserver-ltsc2022)
-	[`traefik:v3.6.1-windowsservercore-ltsc2022`](#traefikv361-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:badb2650cbabae8263ebed0a979475c66c31edc92b24535a519b1ebe5cd1c877
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2` - linux; amd64

```console
$ docker pull traefik@sha256:1332aeea1523caaac64bc7406c29fc64251fa094ceb7bfb07bc2cb0b8f529f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50910385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dbee76cdc4979751996a427018d29e2c47cbec3969f6531ffc657a85877568`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:45 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97737d16fc287bff426b9fcc31e25545fa851f22fd8ddafe89247d215a75ad`  
		Last Modified: Tue, 28 Oct 2025 17:47:50 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84707add128ffb7f94431606938b253c3801170834ff69ffe34f357c2e4c7a13`  
		Last Modified: Tue, 28 Oct 2025 17:48:24 GMT  
		Size: 46.7 MB (46650641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f36d2f6d74a2a636fdbf7dd1aca511bf3fc1c22d696d4e6f1663f4898ea093`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:cb43b5450457a56aa9616d67acd9cadc442dac847f0d1251b6f1e71838358d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964ad9164c17fa2c3b892a2616aeea20142f4ea9ead7854fc1de56230d9e617d`

```dockerfile
```

-	Layers:
	-	`sha256:363044314e3b4bdfe2bf8e8e39d23c486c2135feb6fde6b2433dbecbe05587e0`  
		Last Modified: Tue, 28 Oct 2025 18:10:18 GMT  
		Size: 855.0 KB (854969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0337a010506479073a18b774ec9f78438b31f8adb57be84fe6f18b96df693639`  
		Last Modified: Tue, 28 Oct 2025 18:10:20 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fb0937ebe0301624689d25e9b98446767f3f6a4c5d50103f5fecc33f2d16994c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46664295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabf0acac9bd919187522e3e8bfee4e0ef390322cdbac29f185b0bc7f771a06a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:56 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45540fa3a8d3d091a7310092722247dfa5a86e242b3eb49cf653df1cc2ead`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 457.7 KB (457734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d911210d3431c2962574b7b9991f46aee9b03593cdcbf28c8c6fb83209d9c`  
		Last Modified: Tue, 28 Oct 2025 17:48:22 GMT  
		Size: 42.7 MB (42702112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ea1d8666f65ee215e321ebb26eccb50d4a7884ed90d91fdfc926319262506`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:7c0532eda99388f549249be5763638fc35eda61a5257c12f890fc9587698b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d2903526cd5d4cbbf402e83879fe4ad3027cacb1c5ab3c2299ba6caa43460`

```dockerfile
```

-	Layers:
	-	`sha256:3d07b4e5c28f4ddbde7c6c86862bdc9d9a0164275ab22e3df66097a83268e9be`  
		Last Modified: Tue, 28 Oct 2025 18:10:23 GMT  
		Size: 12.4 KB (12395 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ab418a79e147f0c147f20d9d60f533da7c525373ed4bd1d164c63f8bca9ce9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f644e134d254c5450d3c76a3c9080fcf32358fb5e5850f5c2a2c594668d811ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:46:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:26 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505aca7b2af80fb1238e95cc1e84ea0b413f871a2a32aa0aa56987bccbe0a7f`  
		Last Modified: Tue, 28 Oct 2025 17:47:44 GMT  
		Size: 459.0 KB (459024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea70b51c2f64913cfef44574bfec1feb51f974e81e8555b3c0ba4d7a746368`  
		Last Modified: Tue, 28 Oct 2025 17:48:19 GMT  
		Size: 42.6 MB (42556661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442542845355acb4759bb19a01eb66b5d0fcc819bf28217f2d78fa9ae0100a3`  
		Last Modified: Tue, 28 Oct 2025 17:48:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:350601070db30fa37739fd111f5cd43143082917a5e665466821c1526813fe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1e0f4f6e44232018f2fb26877162717a685dfbb4a8440c887e7994d48eb55d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5cf79ab6d112724f8cdea87c8b0c3b4f82014dd1d5038d03db5d3edc52cf6e`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 855.1 KB (855061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b918ca010d1776d51e7f6600cda1169389ae4805f6b81200fcafdd02a0234d6`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:8b78cc9c02e03d2b9c7d664b64e35836dc1dd52a0ecb9e0155e9e84c64e86d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d9034e795d7d490437d617256a97871e1d843787c30c6a9b29aceb83c0d9ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 03:32:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:49:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:49:14 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:49:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476383bb2bb2988acf2098cf20bed14bd4441bc69c2acd614a2184dbd44d8a8`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 459.4 KB (459426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e962222239ca1db0946eb95f2639a631db0d2b7e384c4e51914825a43ebc82eb`  
		Last Modified: Tue, 28 Oct 2025 17:50:23 GMT  
		Size: 40.9 MB (40872840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7f46011584a53acf7b7061f713e6e84bf026644e2f99a0cee25ea98f590bf3`  
		Last Modified: Tue, 28 Oct 2025 17:50:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:8e7817f72ca1a8412416e686715efee169d32c0da5b663902081a195cb2b0f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fdec5acfb4b5a22c5bc9e0e5ba8bfa7965c7bbbefbc5af5dbc48a2a9e4de40`

```dockerfile
```

-	Layers:
	-	`sha256:d46ffd6881cb514082c44dc74abde240e3d7451d0eda7f67841363a1d9692b45`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 853.1 KB (853070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658821108ec994a7bdbbcbc0ca7dbae2c4d97e9d1a84b2ac716148769052974f`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:47808be40092a8f0eadfd3423422c5a9fd6644b6a67fd556f98891512c7d8ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49224580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8d8c2005c13f7aef9ccb20b88ffb6d250ee9d82de95ed5fa93c4cade0f3b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 15:02:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 Oct 2025 15:14:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Oct 2025 15:14:26 GMT
CMD ["traefik"]
# Wed, 29 Oct 2025 15:14:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3734c19de58da4f3bd4df579f0943d0967f596e3a1e2aa541e119d14638340`  
		Last Modified: Wed, 29 Oct 2025 15:08:21 GMT  
		Size: 457.3 KB (457265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7431aec009fbc1aed617baba72815f470a8edbbcdd89275198e9fa611d614`  
		Last Modified: Wed, 29 Oct 2025 15:19:51 GMT  
		Size: 45.3 MB (45251707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d2683b6ac01afc5a6e6b8607e99964916b1674d9cabb34e6c97694a0668d5`  
		Last Modified: Wed, 29 Oct 2025 15:19:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:72d8db8a45e182f730c763c34e92a9ccf27e5823dc91027da64913be1a140e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d101f19f639bae0f2f3d218b38bcd0feb283e86210762a217e6add3d33adf`

```dockerfile
```

-	Layers:
	-	`sha256:eed804f401f8645370ee55c500d178dac6eb42935ad10fea6f2f1e57ee24dd32`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 853.1 KB (853066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18cb9eac7c2ca078418ff431acaae16fb87ddcd871256e4442b498b4fa80507`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:62793241ab3d3fa28e30f6a4d3b92d2f0e49c2fb0c3474b8350eb6c0a08c990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f46a2e0f3bd40e068adbfa338d31864ffe512c1a4b7cb0f3e22d282a7d8ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 02:26:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:52:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:52:24 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:52:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6155014a1d77a7bc8a35aaadb5baad965e9e640c5be73a93d70e92988712af6d`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b402204d5299e98a2674e31dfe76c1067b611238b2d27bc1455a180b10691b9`  
		Last Modified: Tue, 28 Oct 2025 17:53:22 GMT  
		Size: 45.2 MB (45191097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c03dd8190a9e7c30c473a99dde70793acdd87c0fa553c36466cdae626ae73`  
		Last Modified: Tue, 28 Oct 2025 17:53:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c9c848a281277a91c6d12862355ff4eb93759e0929b211a37e22656ec66def60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c792e2b12f36bd90717549db7ad4a26ceffbb37e31f176c55791379ef7b181d1`

```dockerfile
```

-	Layers:
	-	`sha256:eac88704671328544f3d2394f32b7c94060cfd6e83999c53573fbddedc9a23ce`  
		Last Modified: Tue, 28 Oct 2025 18:10:42 GMT  
		Size: 853.0 KB (853014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5c84a0048b551af6d027b04bc271d0152fa1b3a3e91a2f965461c4139f1db7`  
		Last Modified: Tue, 28 Oct 2025 18:10:43 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:60724e738c7ed9116b0cca972040b6aafd2762d2f572afaa54a40552a9fb62f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e2f55045c64078c084ef9e53f08adf1623aa8e844c0f61ac976e59ef978d66be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173790001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8318d8f6e397d73cc19da9686cd752741b871ca5e5f2833e0a36abe8a9cc2547`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:6cfeac02f7657e0f21bec793858fed4418e5818930327326190bd6ff11a7fa98 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae60a04a76082373387efad417e4554a5a8af770bbbcc040b0811829cdfbdb`  
		Last Modified: Tue, 11 Nov 2025 20:10:44 GMT  
		Size: 47.4 MB (47437742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36572591302f3f4ec803657efd9cf2a5635c524bf86800891e48499c6c83100d`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39e8d7bce4b204cc12e1d9ec388767ee42407e17c5751b6174c90b12e16df7`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ff038bfba1a92d3ca14cb7a8d0ee8597c094e3ef37614449e15e15bd0bd287`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4113e8c54c253277cdcdd6584f3d094a65d2abf18765de6d30b0abb1bec248cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:7dac490b602f9587776991ffdb54c35d0b697c37dc645387d0890ceca4188306
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818021605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719b1f153be2e7f51d90cedd318244af304cf70e951822e773ee7b73f549277f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:20 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:21 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f462a0a30c68120954a26c242c266ecc7cf71abf17249112775238e61ca66c56`  
		Last Modified: Tue, 11 Nov 2025 19:22:26 GMT  
		Size: 48.1 MB (48054851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311fafd46778b18455cef771ee101f5fdc2fa5d7722610a7acd8e984621d252d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d7f0a3bf57c22d8952d3d2c8b835ad28012ad0e732cc1286b6774abdfbf778`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb0dc8595b4ccc82bf97d01c80ab263d5c15fadb2711cf1c1649a8c49c61f98`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:badb2650cbabae8263ebed0a979475c66c31edc92b24535a519b1ebe5cd1c877
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11` - linux; amd64

```console
$ docker pull traefik@sha256:1332aeea1523caaac64bc7406c29fc64251fa094ceb7bfb07bc2cb0b8f529f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50910385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dbee76cdc4979751996a427018d29e2c47cbec3969f6531ffc657a85877568`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:45 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97737d16fc287bff426b9fcc31e25545fa851f22fd8ddafe89247d215a75ad`  
		Last Modified: Tue, 28 Oct 2025 17:47:50 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84707add128ffb7f94431606938b253c3801170834ff69ffe34f357c2e4c7a13`  
		Last Modified: Tue, 28 Oct 2025 17:48:24 GMT  
		Size: 46.7 MB (46650641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f36d2f6d74a2a636fdbf7dd1aca511bf3fc1c22d696d4e6f1663f4898ea093`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cb43b5450457a56aa9616d67acd9cadc442dac847f0d1251b6f1e71838358d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964ad9164c17fa2c3b892a2616aeea20142f4ea9ead7854fc1de56230d9e617d`

```dockerfile
```

-	Layers:
	-	`sha256:363044314e3b4bdfe2bf8e8e39d23c486c2135feb6fde6b2433dbecbe05587e0`  
		Last Modified: Tue, 28 Oct 2025 18:10:18 GMT  
		Size: 855.0 KB (854969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0337a010506479073a18b774ec9f78438b31f8adb57be84fe6f18b96df693639`  
		Last Modified: Tue, 28 Oct 2025 18:10:20 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fb0937ebe0301624689d25e9b98446767f3f6a4c5d50103f5fecc33f2d16994c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46664295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabf0acac9bd919187522e3e8bfee4e0ef390322cdbac29f185b0bc7f771a06a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:56 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45540fa3a8d3d091a7310092722247dfa5a86e242b3eb49cf653df1cc2ead`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 457.7 KB (457734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d911210d3431c2962574b7b9991f46aee9b03593cdcbf28c8c6fb83209d9c`  
		Last Modified: Tue, 28 Oct 2025 17:48:22 GMT  
		Size: 42.7 MB (42702112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ea1d8666f65ee215e321ebb26eccb50d4a7884ed90d91fdfc926319262506`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7c0532eda99388f549249be5763638fc35eda61a5257c12f890fc9587698b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d2903526cd5d4cbbf402e83879fe4ad3027cacb1c5ab3c2299ba6caa43460`

```dockerfile
```

-	Layers:
	-	`sha256:3d07b4e5c28f4ddbde7c6c86862bdc9d9a0164275ab22e3df66097a83268e9be`  
		Last Modified: Tue, 28 Oct 2025 18:10:23 GMT  
		Size: 12.4 KB (12395 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ab418a79e147f0c147f20d9d60f533da7c525373ed4bd1d164c63f8bca9ce9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f644e134d254c5450d3c76a3c9080fcf32358fb5e5850f5c2a2c594668d811ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:46:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:26 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505aca7b2af80fb1238e95cc1e84ea0b413f871a2a32aa0aa56987bccbe0a7f`  
		Last Modified: Tue, 28 Oct 2025 17:47:44 GMT  
		Size: 459.0 KB (459024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea70b51c2f64913cfef44574bfec1feb51f974e81e8555b3c0ba4d7a746368`  
		Last Modified: Tue, 28 Oct 2025 17:48:19 GMT  
		Size: 42.6 MB (42556661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442542845355acb4759bb19a01eb66b5d0fcc819bf28217f2d78fa9ae0100a3`  
		Last Modified: Tue, 28 Oct 2025 17:48:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:350601070db30fa37739fd111f5cd43143082917a5e665466821c1526813fe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1e0f4f6e44232018f2fb26877162717a685dfbb4a8440c887e7994d48eb55d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5cf79ab6d112724f8cdea87c8b0c3b4f82014dd1d5038d03db5d3edc52cf6e`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 855.1 KB (855061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b918ca010d1776d51e7f6600cda1169389ae4805f6b81200fcafdd02a0234d6`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:8b78cc9c02e03d2b9c7d664b64e35836dc1dd52a0ecb9e0155e9e84c64e86d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d9034e795d7d490437d617256a97871e1d843787c30c6a9b29aceb83c0d9ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 03:32:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:49:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:49:14 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:49:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476383bb2bb2988acf2098cf20bed14bd4441bc69c2acd614a2184dbd44d8a8`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 459.4 KB (459426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e962222239ca1db0946eb95f2639a631db0d2b7e384c4e51914825a43ebc82eb`  
		Last Modified: Tue, 28 Oct 2025 17:50:23 GMT  
		Size: 40.9 MB (40872840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7f46011584a53acf7b7061f713e6e84bf026644e2f99a0cee25ea98f590bf3`  
		Last Modified: Tue, 28 Oct 2025 17:50:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:8e7817f72ca1a8412416e686715efee169d32c0da5b663902081a195cb2b0f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fdec5acfb4b5a22c5bc9e0e5ba8bfa7965c7bbbefbc5af5dbc48a2a9e4de40`

```dockerfile
```

-	Layers:
	-	`sha256:d46ffd6881cb514082c44dc74abde240e3d7451d0eda7f67841363a1d9692b45`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 853.1 KB (853070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658821108ec994a7bdbbcbc0ca7dbae2c4d97e9d1a84b2ac716148769052974f`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:47808be40092a8f0eadfd3423422c5a9fd6644b6a67fd556f98891512c7d8ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49224580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8d8c2005c13f7aef9ccb20b88ffb6d250ee9d82de95ed5fa93c4cade0f3b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 15:02:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 Oct 2025 15:14:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Oct 2025 15:14:26 GMT
CMD ["traefik"]
# Wed, 29 Oct 2025 15:14:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3734c19de58da4f3bd4df579f0943d0967f596e3a1e2aa541e119d14638340`  
		Last Modified: Wed, 29 Oct 2025 15:08:21 GMT  
		Size: 457.3 KB (457265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7431aec009fbc1aed617baba72815f470a8edbbcdd89275198e9fa611d614`  
		Last Modified: Wed, 29 Oct 2025 15:19:51 GMT  
		Size: 45.3 MB (45251707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d2683b6ac01afc5a6e6b8607e99964916b1674d9cabb34e6c97694a0668d5`  
		Last Modified: Wed, 29 Oct 2025 15:19:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:72d8db8a45e182f730c763c34e92a9ccf27e5823dc91027da64913be1a140e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d101f19f639bae0f2f3d218b38bcd0feb283e86210762a217e6add3d33adf`

```dockerfile
```

-	Layers:
	-	`sha256:eed804f401f8645370ee55c500d178dac6eb42935ad10fea6f2f1e57ee24dd32`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 853.1 KB (853066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18cb9eac7c2ca078418ff431acaae16fb87ddcd871256e4442b498b4fa80507`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:62793241ab3d3fa28e30f6a4d3b92d2f0e49c2fb0c3474b8350eb6c0a08c990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f46a2e0f3bd40e068adbfa338d31864ffe512c1a4b7cb0f3e22d282a7d8ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 02:26:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:52:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:52:24 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:52:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6155014a1d77a7bc8a35aaadb5baad965e9e640c5be73a93d70e92988712af6d`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b402204d5299e98a2674e31dfe76c1067b611238b2d27bc1455a180b10691b9`  
		Last Modified: Tue, 28 Oct 2025 17:53:22 GMT  
		Size: 45.2 MB (45191097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c03dd8190a9e7c30c473a99dde70793acdd87c0fa553c36466cdae626ae73`  
		Last Modified: Tue, 28 Oct 2025 17:53:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c9c848a281277a91c6d12862355ff4eb93759e0929b211a37e22656ec66def60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c792e2b12f36bd90717549db7ad4a26ceffbb37e31f176c55791379ef7b181d1`

```dockerfile
```

-	Layers:
	-	`sha256:eac88704671328544f3d2394f32b7c94060cfd6e83999c53573fbddedc9a23ce`  
		Last Modified: Tue, 28 Oct 2025 18:10:42 GMT  
		Size: 853.0 KB (853014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5c84a0048b551af6d027b04bc271d0152fa1b3a3e91a2f965461c4139f1db7`  
		Last Modified: Tue, 28 Oct 2025 18:10:43 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:60724e738c7ed9116b0cca972040b6aafd2762d2f572afaa54a40552a9fb62f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e2f55045c64078c084ef9e53f08adf1623aa8e844c0f61ac976e59ef978d66be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173790001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8318d8f6e397d73cc19da9686cd752741b871ca5e5f2833e0a36abe8a9cc2547`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:6cfeac02f7657e0f21bec793858fed4418e5818930327326190bd6ff11a7fa98 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae60a04a76082373387efad417e4554a5a8af770bbbcc040b0811829cdfbdb`  
		Last Modified: Tue, 11 Nov 2025 20:10:44 GMT  
		Size: 47.4 MB (47437742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36572591302f3f4ec803657efd9cf2a5635c524bf86800891e48499c6c83100d`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39e8d7bce4b204cc12e1d9ec388767ee42407e17c5751b6174c90b12e16df7`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ff038bfba1a92d3ca14cb7a8d0ee8597c094e3ef37614449e15e15bd0bd287`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4113e8c54c253277cdcdd6584f3d094a65d2abf18765de6d30b0abb1bec248cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:7dac490b602f9587776991ffdb54c35d0b697c37dc645387d0890ceca4188306
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818021605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719b1f153be2e7f51d90cedd318244af304cf70e951822e773ee7b73f549277f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:20 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:21 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f462a0a30c68120954a26c242c266ecc7cf71abf17249112775238e61ca66c56`  
		Last Modified: Tue, 11 Nov 2025 19:22:26 GMT  
		Size: 48.1 MB (48054851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311fafd46778b18455cef771ee101f5fdc2fa5d7722610a7acd8e984621d252d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d7f0a3bf57c22d8952d3d2c8b835ad28012ad0e732cc1286b6774abdfbf778`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb0dc8595b4ccc82bf97d01c80ab263d5c15fadb2711cf1c1649a8c49c61f98`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.31`

**does not exist** (yet?)

## `traefik:2.11.31-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:2.11.31-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:3`

```console
$ docker pull traefik@sha256:18112aed2bfe3dfb8534f1045622390c3316596cff0cefab64f44e43d23e1640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3` - linux; amd64

```console
$ docker pull traefik@sha256:c1d367d01066413216bde351c64076358928d36c39128bc84b8d77bcf625fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7065ee8303e5acc80a10479c1aa70594eeada0ef33a531d51481b781027646d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:09 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a551e6e94e8d6b0eadbaff71fc30d07e795156757222a3275f23d2fbe886d`  
		Last Modified: Sat, 08 Nov 2025 17:49:39 GMT  
		Size: 456.9 KB (456920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746bd391ec3f05e8f1670234a30e9f9e3f1384f6d6b90e790b1506a91d8f49e`  
		Last Modified: Sat, 08 Nov 2025 17:49:50 GMT  
		Size: 47.6 MB (47647053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9148c3d019cdbb699b0399feb4b8bde49b33225180951c29b3ac484301e8c1fa`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:49404ec90da14b81d5730b4b92bbdce9d9811a0408a65be8821375eff72491d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9f51aa35a7c3f928f92e8b57ef8f73af9296c773ba68a0d01d32968376ef0b`

```dockerfile
```

-	Layers:
	-	`sha256:9a176a130ca26a66b3626af56aa085f2084647a4286c40f2fe92cdde1ea2a18e`  
		Last Modified: Sat, 08 Nov 2025 19:14:36 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cdbd3e4ed32c8605e2e181edd1bdb10825ad3e337119cc8de65279a3e120eda`  
		Last Modified: Sat, 08 Nov 2025 19:14:41 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8c1f9170cd49bd260f86260fa4f9931e1996627b40be511205f4522dfd884ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47122068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911b660733057f37aaf382a62cdd30f37f0aebfd90479c60c17f7789f4439bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:23 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d32af4def2314aeda5fa7c2d5cddb469a0666f2ab64a8999fb4b9d4678b785`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 457.7 KB (457735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa665f047b6aacaefa7c1b5ec28299ef9b34e27197765850c8492fba633ecb2`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 43.2 MB (43159884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142b8a33d16cfda6f921981607a855bc41e11eec7bd904f79c7fd704cbc2d33`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:8176e73ed6e3e37b50fdcf150a77cef959812c1ad9cc4487b6ab25066d695a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a5674fbf0c0b32f1ff7104201f8e2e2cb4f1614fd0aa1ca9a84280ec9a75b1`

```dockerfile
```

-	Layers:
	-	`sha256:90c3e9765b391851fbd5622c83ea675c05c4e54ba07c219dd524c3a2b76f2df1`  
		Last Modified: Sat, 08 Nov 2025 19:15:13 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:932e4f4c53902c8620d64199dffb4c6ef2efcd799137c76bf06312c0291e060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47952858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08927b02f26a06024f9cf1324adf4d4fa6d4302fa35895d3fc55d09de68e8b9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:47 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcfcadb61884e632ee6855fc9d05acdcac92ea38f3baf49360df256678d6c4`  
		Last Modified: Sat, 08 Nov 2025 17:49:25 GMT  
		Size: 459.0 KB (459025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6133c1595dad94916b16df346dba0c3674ee62cd6e8d48575401b932e0a5af`  
		Last Modified: Sat, 08 Nov 2025 17:49:28 GMT  
		Size: 43.4 MB (43355395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e688a415944a77f89aff4bfb8501253f3e5f2070bc106ee762f607015d954`  
		Last Modified: Sat, 08 Nov 2025 17:49:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:b958dfd5bb43ec9a4b595bf8f8da8c2569c2bc6fb5630fdb015c8c871125dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76b4b1bbd51072fb33c96875d3537bceac06c87d22047b6b3a6575ce8b5723`

```dockerfile
```

-	Layers:
	-	`sha256:b9287959e40047244875219eccfc9a62c79f3464f225bb9a6a839f429de903e4`  
		Last Modified: Sat, 08 Nov 2025 19:15:16 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dc0ebacd5097f6f54c735e6db91e5b34108d5ffa7c2dc587f22ab4917a5057`  
		Last Modified: Sat, 08 Nov 2025 19:15:17 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:d8a89c65c0466dbaf521dfee4394549e4d813e5e112bb31efa5c5d21380b6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45528880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e7f93130630c77319d3ad4f4acd6e0f940863cc36847e3ee44c583095f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:06 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed7ef67f69c2b5a0caa2013b8451255932b057923b9f18ef138e1bac3fe202`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 459.4 KB (459431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a635055d916db706f9ac32e427eda46e90cd856045aa0fffb8c0a4dc3935c`  
		Last Modified: Sat, 08 Nov 2025 17:49:10 GMT  
		Size: 41.3 MB (41336840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf09a848ab17c82ae94532e3cf46cff03e322c1a70998c68b85f5ee140ed63d`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:f3e919e7b8655274f12133697480e98e440215a5356a8c7ede337538155e129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd9a8ed72756542deae52401b02bb5b1a8591a5d6e9a3e9b827e31fa765a82`

```dockerfile
```

-	Layers:
	-	`sha256:33a73882bd6d35e47d0c8d12e1582d660da8fe3bebb4965e80a15c450edd764e`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a1f979a9028a3050a78bf693f450e4a9a661201036dba695172ce07ca6582c`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:9d945497f1e0e0315abc0a52f853239338f08e713a86b22942e9eb55a3fd9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49896389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8753fb4db640d360a2b5e1fb0ec9946738292c1e981455888d7fc665d05a860e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
COPY entrypoint.sh / # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
EXPOSE map[80/tcp:{}]
# Sun, 09 Nov 2025 21:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 09 Nov 2025 21:37:43 GMT
CMD ["traefik"]
# Sun, 09 Nov 2025 21:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b6e207f69d2afa9c62f16c53bac3661f79667ed248dbb86188fa53be5a0fc`  
		Last Modified: Sun, 09 Nov 2025 21:42:58 GMT  
		Size: 45.9 MB (45923504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc33070eac1e0dfbffe3befc315859cc7adfa74df7e1746110f3f9eda17bb`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:4d7cb2aeb1a9fb763a9cc257178350c0a6d8f7a2975d563d19e0832e018d1e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198a484789301f44968e04d7f83eb867c272a217e81bfa34fbf49cc9d0809ba6`

```dockerfile
```

-	Layers:
	-	`sha256:165bd089fae0d63962bc1db2a74722d6fba1d131b94f525f12dc91f8ca589e00`  
		Last Modified: Sun, 09 Nov 2025 22:09:29 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f258816c82e54e07b68a06537658018cd2a88d81ab9d8fdfac714731b69551b`  
		Last Modified: Sun, 09 Nov 2025 22:09:30 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:4faefd84b7c54d68b276c9451c76d83991f446ae6e5c21d61ffc23976820008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49899862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906574974acf76b8f05d02292abaac804c08d05909cd1a0a0ac0fa1545d97f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:47:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:04 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba992a90373c6f9649b17857d1fe6894ed01c492f0c3f8314218f3bf8ac6725`  
		Last Modified: Sat, 08 Nov 2025 17:49:02 GMT  
		Size: 457.9 KB (457910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808795fe98794b5559426ab0b77bf9109a6b2572c67e673d3cc2b4323aef9df8`  
		Last Modified: Sat, 08 Nov 2025 17:49:06 GMT  
		Size: 45.8 MB (45792340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94b29e8468df4e2b75502b1484f121021c6b11e808ea65af2b920c14129bfb`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:3ec8fd1cc7a3434e45bc24f365f23be261d08218078d8fa71d09ce90d0b5dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43660154f83526b4ecc46d1f468cafdcccad1ab2cd10356fb4174b8da31316b4`

```dockerfile
```

-	Layers:
	-	`sha256:5229dda88366c5ad5993f82a43d495c8bd119544e12e3b26fa98ef6c6cfd09a0`  
		Last Modified: Sat, 08 Nov 2025 19:15:26 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79fb299eb71e31887ab98cc994b995c2943b800c28b8e947bbc9db38525c876`  
		Last Modified: Sat, 08 Nov 2025 19:15:27 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:58bdbd714aaf63369efd43293de2e246e328d76d1c052079f230a069ba147170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e0d382c02836adbce8db53819da77bbed076352af93eab870a5c2d3f2ff1705f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174739638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606f2520cf13e92129dcc7d2d7c2e23f565940998eaa134012ea4050340ad44`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:fa7d458e5035cd7257a4fcca892af645f6a7bff0167a9a36ee2be323cba3aea8 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9080590026898dc45cb4ce39ea66b413cc59161c14bbb40e928d5d2936339bb`  
		Last Modified: Tue, 11 Nov 2025 20:11:00 GMT  
		Size: 48.4 MB (48387349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef94a0710093125c521f9c5feedf55499ec5cd192da6a680877f99e37c7886e1`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922dc6de5393d74f7b8c06fb66486fe7d1329f8d8eb7725e590f63de72359ea`  
		Last Modified: Tue, 11 Nov 2025 20:10:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e291f81a41d1e29a6a1208c05d403fdf7ab5816a3ca4d177558b2bc6a9a08e3`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:047d63ab1573e82a1136a4411117bd2346d5021076eddc80f6bc4bee8a529e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e8af3c304a96ec32fc62478b50dcd7cbc370fcb7ec1bc73fbb1427b00f40490b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818993276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d7a9e86f9609ce347f37946711c412653be1364ec950f24251da914b8bb987`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:01 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:01 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef226535da45dbfa8a4d7f70609bddf8ca912461ba29fffbb5f4a6c343342bad`  
		Last Modified: Tue, 11 Nov 2025 19:22:25 GMT  
		Size: 49.0 MB (49026478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8441ed2b6b03f2592848998903b7b2048dc3fd90a58cc751691c8b350c9624e`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eef944fba1dc3cb2e6c0db849ee7cf49cb25a8f5718ff1f805e546ec4d79d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f944678203d9badbe57ca7c5ed0d295e0c697fc5a46c855fb1f53b2417de9`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:18112aed2bfe3dfb8534f1045622390c3316596cff0cefab64f44e43d23e1640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3.6` - linux; amd64

```console
$ docker pull traefik@sha256:c1d367d01066413216bde351c64076358928d36c39128bc84b8d77bcf625fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7065ee8303e5acc80a10479c1aa70594eeada0ef33a531d51481b781027646d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:09 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a551e6e94e8d6b0eadbaff71fc30d07e795156757222a3275f23d2fbe886d`  
		Last Modified: Sat, 08 Nov 2025 17:49:39 GMT  
		Size: 456.9 KB (456920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746bd391ec3f05e8f1670234a30e9f9e3f1384f6d6b90e790b1506a91d8f49e`  
		Last Modified: Sat, 08 Nov 2025 17:49:50 GMT  
		Size: 47.6 MB (47647053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9148c3d019cdbb699b0399feb4b8bde49b33225180951c29b3ac484301e8c1fa`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:49404ec90da14b81d5730b4b92bbdce9d9811a0408a65be8821375eff72491d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9f51aa35a7c3f928f92e8b57ef8f73af9296c773ba68a0d01d32968376ef0b`

```dockerfile
```

-	Layers:
	-	`sha256:9a176a130ca26a66b3626af56aa085f2084647a4286c40f2fe92cdde1ea2a18e`  
		Last Modified: Sat, 08 Nov 2025 19:14:36 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cdbd3e4ed32c8605e2e181edd1bdb10825ad3e337119cc8de65279a3e120eda`  
		Last Modified: Sat, 08 Nov 2025 19:14:41 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8c1f9170cd49bd260f86260fa4f9931e1996627b40be511205f4522dfd884ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47122068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911b660733057f37aaf382a62cdd30f37f0aebfd90479c60c17f7789f4439bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:23 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d32af4def2314aeda5fa7c2d5cddb469a0666f2ab64a8999fb4b9d4678b785`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 457.7 KB (457735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa665f047b6aacaefa7c1b5ec28299ef9b34e27197765850c8492fba633ecb2`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 43.2 MB (43159884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142b8a33d16cfda6f921981607a855bc41e11eec7bd904f79c7fd704cbc2d33`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8176e73ed6e3e37b50fdcf150a77cef959812c1ad9cc4487b6ab25066d695a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a5674fbf0c0b32f1ff7104201f8e2e2cb4f1614fd0aa1ca9a84280ec9a75b1`

```dockerfile
```

-	Layers:
	-	`sha256:90c3e9765b391851fbd5622c83ea675c05c4e54ba07c219dd524c3a2b76f2df1`  
		Last Modified: Sat, 08 Nov 2025 19:15:13 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:932e4f4c53902c8620d64199dffb4c6ef2efcd799137c76bf06312c0291e060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47952858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08927b02f26a06024f9cf1324adf4d4fa6d4302fa35895d3fc55d09de68e8b9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:47 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcfcadb61884e632ee6855fc9d05acdcac92ea38f3baf49360df256678d6c4`  
		Last Modified: Sat, 08 Nov 2025 17:49:25 GMT  
		Size: 459.0 KB (459025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6133c1595dad94916b16df346dba0c3674ee62cd6e8d48575401b932e0a5af`  
		Last Modified: Sat, 08 Nov 2025 17:49:28 GMT  
		Size: 43.4 MB (43355395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e688a415944a77f89aff4bfb8501253f3e5f2070bc106ee762f607015d954`  
		Last Modified: Sat, 08 Nov 2025 17:49:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b958dfd5bb43ec9a4b595bf8f8da8c2569c2bc6fb5630fdb015c8c871125dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76b4b1bbd51072fb33c96875d3537bceac06c87d22047b6b3a6575ce8b5723`

```dockerfile
```

-	Layers:
	-	`sha256:b9287959e40047244875219eccfc9a62c79f3464f225bb9a6a839f429de903e4`  
		Last Modified: Sat, 08 Nov 2025 19:15:16 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dc0ebacd5097f6f54c735e6db91e5b34108d5ffa7c2dc587f22ab4917a5057`  
		Last Modified: Sat, 08 Nov 2025 19:15:17 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:d8a89c65c0466dbaf521dfee4394549e4d813e5e112bb31efa5c5d21380b6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45528880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e7f93130630c77319d3ad4f4acd6e0f940863cc36847e3ee44c583095f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:06 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed7ef67f69c2b5a0caa2013b8451255932b057923b9f18ef138e1bac3fe202`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 459.4 KB (459431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a635055d916db706f9ac32e427eda46e90cd856045aa0fffb8c0a4dc3935c`  
		Last Modified: Sat, 08 Nov 2025 17:49:10 GMT  
		Size: 41.3 MB (41336840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf09a848ab17c82ae94532e3cf46cff03e322c1a70998c68b85f5ee140ed63d`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f3e919e7b8655274f12133697480e98e440215a5356a8c7ede337538155e129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd9a8ed72756542deae52401b02bb5b1a8591a5d6e9a3e9b827e31fa765a82`

```dockerfile
```

-	Layers:
	-	`sha256:33a73882bd6d35e47d0c8d12e1582d660da8fe3bebb4965e80a15c450edd764e`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a1f979a9028a3050a78bf693f450e4a9a661201036dba695172ce07ca6582c`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:9d945497f1e0e0315abc0a52f853239338f08e713a86b22942e9eb55a3fd9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49896389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8753fb4db640d360a2b5e1fb0ec9946738292c1e981455888d7fc665d05a860e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
COPY entrypoint.sh / # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
EXPOSE map[80/tcp:{}]
# Sun, 09 Nov 2025 21:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 09 Nov 2025 21:37:43 GMT
CMD ["traefik"]
# Sun, 09 Nov 2025 21:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b6e207f69d2afa9c62f16c53bac3661f79667ed248dbb86188fa53be5a0fc`  
		Last Modified: Sun, 09 Nov 2025 21:42:58 GMT  
		Size: 45.9 MB (45923504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc33070eac1e0dfbffe3befc315859cc7adfa74df7e1746110f3f9eda17bb`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4d7cb2aeb1a9fb763a9cc257178350c0a6d8f7a2975d563d19e0832e018d1e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198a484789301f44968e04d7f83eb867c272a217e81bfa34fbf49cc9d0809ba6`

```dockerfile
```

-	Layers:
	-	`sha256:165bd089fae0d63962bc1db2a74722d6fba1d131b94f525f12dc91f8ca589e00`  
		Last Modified: Sun, 09 Nov 2025 22:09:29 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f258816c82e54e07b68a06537658018cd2a88d81ab9d8fdfac714731b69551b`  
		Last Modified: Sun, 09 Nov 2025 22:09:30 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:4faefd84b7c54d68b276c9451c76d83991f446ae6e5c21d61ffc23976820008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49899862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906574974acf76b8f05d02292abaac804c08d05909cd1a0a0ac0fa1545d97f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:47:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:04 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba992a90373c6f9649b17857d1fe6894ed01c492f0c3f8314218f3bf8ac6725`  
		Last Modified: Sat, 08 Nov 2025 17:49:02 GMT  
		Size: 457.9 KB (457910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808795fe98794b5559426ab0b77bf9109a6b2572c67e673d3cc2b4323aef9df8`  
		Last Modified: Sat, 08 Nov 2025 17:49:06 GMT  
		Size: 45.8 MB (45792340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94b29e8468df4e2b75502b1484f121021c6b11e808ea65af2b920c14129bfb`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:3ec8fd1cc7a3434e45bc24f365f23be261d08218078d8fa71d09ce90d0b5dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43660154f83526b4ecc46d1f468cafdcccad1ab2cd10356fb4174b8da31316b4`

```dockerfile
```

-	Layers:
	-	`sha256:5229dda88366c5ad5993f82a43d495c8bd119544e12e3b26fa98ef6c6cfd09a0`  
		Last Modified: Sat, 08 Nov 2025 19:15:26 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79fb299eb71e31887ab98cc994b995c2943b800c28b8e947bbc9db38525c876`  
		Last Modified: Sat, 08 Nov 2025 19:15:27 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:58bdbd714aaf63369efd43293de2e246e328d76d1c052079f230a069ba147170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e0d382c02836adbce8db53819da77bbed076352af93eab870a5c2d3f2ff1705f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174739638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606f2520cf13e92129dcc7d2d7c2e23f565940998eaa134012ea4050340ad44`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:fa7d458e5035cd7257a4fcca892af645f6a7bff0167a9a36ee2be323cba3aea8 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9080590026898dc45cb4ce39ea66b413cc59161c14bbb40e928d5d2936339bb`  
		Last Modified: Tue, 11 Nov 2025 20:11:00 GMT  
		Size: 48.4 MB (48387349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef94a0710093125c521f9c5feedf55499ec5cd192da6a680877f99e37c7886e1`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922dc6de5393d74f7b8c06fb66486fe7d1329f8d8eb7725e590f63de72359ea`  
		Last Modified: Tue, 11 Nov 2025 20:10:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e291f81a41d1e29a6a1208c05d403fdf7ab5816a3ca4d177558b2bc6a9a08e3`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:047d63ab1573e82a1136a4411117bd2346d5021076eddc80f6bc4bee8a529e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e8af3c304a96ec32fc62478b50dcd7cbc370fcb7ec1bc73fbb1427b00f40490b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818993276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d7a9e86f9609ce347f37946711c412653be1364ec950f24251da914b8bb987`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:01 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:01 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef226535da45dbfa8a4d7f70609bddf8ca912461ba29fffbb5f4a6c343342bad`  
		Last Modified: Tue, 11 Nov 2025 19:22:25 GMT  
		Size: 49.0 MB (49026478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8441ed2b6b03f2592848998903b7b2048dc3fd90a58cc751691c8b350c9624e`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eef944fba1dc3cb2e6c0db849ee7cf49cb25a8f5718ff1f805e546ec4d79d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f944678203d9badbe57ca7c5ed0d295e0c697fc5a46c855fb1f53b2417de9`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.1`

**does not exist** (yet?)

## `traefik:3.6.1-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:3.6.1-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:latest`

```console
$ docker pull traefik@sha256:18112aed2bfe3dfb8534f1045622390c3316596cff0cefab64f44e43d23e1640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:c1d367d01066413216bde351c64076358928d36c39128bc84b8d77bcf625fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7065ee8303e5acc80a10479c1aa70594eeada0ef33a531d51481b781027646d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:09 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a551e6e94e8d6b0eadbaff71fc30d07e795156757222a3275f23d2fbe886d`  
		Last Modified: Sat, 08 Nov 2025 17:49:39 GMT  
		Size: 456.9 KB (456920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746bd391ec3f05e8f1670234a30e9f9e3f1384f6d6b90e790b1506a91d8f49e`  
		Last Modified: Sat, 08 Nov 2025 17:49:50 GMT  
		Size: 47.6 MB (47647053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9148c3d019cdbb699b0399feb4b8bde49b33225180951c29b3ac484301e8c1fa`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:49404ec90da14b81d5730b4b92bbdce9d9811a0408a65be8821375eff72491d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9f51aa35a7c3f928f92e8b57ef8f73af9296c773ba68a0d01d32968376ef0b`

```dockerfile
```

-	Layers:
	-	`sha256:9a176a130ca26a66b3626af56aa085f2084647a4286c40f2fe92cdde1ea2a18e`  
		Last Modified: Sat, 08 Nov 2025 19:14:36 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cdbd3e4ed32c8605e2e181edd1bdb10825ad3e337119cc8de65279a3e120eda`  
		Last Modified: Sat, 08 Nov 2025 19:14:41 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8c1f9170cd49bd260f86260fa4f9931e1996627b40be511205f4522dfd884ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47122068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911b660733057f37aaf382a62cdd30f37f0aebfd90479c60c17f7789f4439bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:23 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d32af4def2314aeda5fa7c2d5cddb469a0666f2ab64a8999fb4b9d4678b785`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 457.7 KB (457735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa665f047b6aacaefa7c1b5ec28299ef9b34e27197765850c8492fba633ecb2`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 43.2 MB (43159884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142b8a33d16cfda6f921981607a855bc41e11eec7bd904f79c7fd704cbc2d33`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8176e73ed6e3e37b50fdcf150a77cef959812c1ad9cc4487b6ab25066d695a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a5674fbf0c0b32f1ff7104201f8e2e2cb4f1614fd0aa1ca9a84280ec9a75b1`

```dockerfile
```

-	Layers:
	-	`sha256:90c3e9765b391851fbd5622c83ea675c05c4e54ba07c219dd524c3a2b76f2df1`  
		Last Modified: Sat, 08 Nov 2025 19:15:13 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:932e4f4c53902c8620d64199dffb4c6ef2efcd799137c76bf06312c0291e060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47952858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08927b02f26a06024f9cf1324adf4d4fa6d4302fa35895d3fc55d09de68e8b9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:47 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcfcadb61884e632ee6855fc9d05acdcac92ea38f3baf49360df256678d6c4`  
		Last Modified: Sat, 08 Nov 2025 17:49:25 GMT  
		Size: 459.0 KB (459025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6133c1595dad94916b16df346dba0c3674ee62cd6e8d48575401b932e0a5af`  
		Last Modified: Sat, 08 Nov 2025 17:49:28 GMT  
		Size: 43.4 MB (43355395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e688a415944a77f89aff4bfb8501253f3e5f2070bc106ee762f607015d954`  
		Last Modified: Sat, 08 Nov 2025 17:49:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:b958dfd5bb43ec9a4b595bf8f8da8c2569c2bc6fb5630fdb015c8c871125dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76b4b1bbd51072fb33c96875d3537bceac06c87d22047b6b3a6575ce8b5723`

```dockerfile
```

-	Layers:
	-	`sha256:b9287959e40047244875219eccfc9a62c79f3464f225bb9a6a839f429de903e4`  
		Last Modified: Sat, 08 Nov 2025 19:15:16 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dc0ebacd5097f6f54c735e6db91e5b34108d5ffa7c2dc587f22ab4917a5057`  
		Last Modified: Sat, 08 Nov 2025 19:15:17 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:d8a89c65c0466dbaf521dfee4394549e4d813e5e112bb31efa5c5d21380b6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45528880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e7f93130630c77319d3ad4f4acd6e0f940863cc36847e3ee44c583095f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:06 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed7ef67f69c2b5a0caa2013b8451255932b057923b9f18ef138e1bac3fe202`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 459.4 KB (459431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a635055d916db706f9ac32e427eda46e90cd856045aa0fffb8c0a4dc3935c`  
		Last Modified: Sat, 08 Nov 2025 17:49:10 GMT  
		Size: 41.3 MB (41336840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf09a848ab17c82ae94532e3cf46cff03e322c1a70998c68b85f5ee140ed63d`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:f3e919e7b8655274f12133697480e98e440215a5356a8c7ede337538155e129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd9a8ed72756542deae52401b02bb5b1a8591a5d6e9a3e9b827e31fa765a82`

```dockerfile
```

-	Layers:
	-	`sha256:33a73882bd6d35e47d0c8d12e1582d660da8fe3bebb4965e80a15c450edd764e`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a1f979a9028a3050a78bf693f450e4a9a661201036dba695172ce07ca6582c`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:9d945497f1e0e0315abc0a52f853239338f08e713a86b22942e9eb55a3fd9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49896389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8753fb4db640d360a2b5e1fb0ec9946738292c1e981455888d7fc665d05a860e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
COPY entrypoint.sh / # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
EXPOSE map[80/tcp:{}]
# Sun, 09 Nov 2025 21:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 09 Nov 2025 21:37:43 GMT
CMD ["traefik"]
# Sun, 09 Nov 2025 21:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b6e207f69d2afa9c62f16c53bac3661f79667ed248dbb86188fa53be5a0fc`  
		Last Modified: Sun, 09 Nov 2025 21:42:58 GMT  
		Size: 45.9 MB (45923504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc33070eac1e0dfbffe3befc315859cc7adfa74df7e1746110f3f9eda17bb`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4d7cb2aeb1a9fb763a9cc257178350c0a6d8f7a2975d563d19e0832e018d1e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198a484789301f44968e04d7f83eb867c272a217e81bfa34fbf49cc9d0809ba6`

```dockerfile
```

-	Layers:
	-	`sha256:165bd089fae0d63962bc1db2a74722d6fba1d131b94f525f12dc91f8ca589e00`  
		Last Modified: Sun, 09 Nov 2025 22:09:29 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f258816c82e54e07b68a06537658018cd2a88d81ab9d8fdfac714731b69551b`  
		Last Modified: Sun, 09 Nov 2025 22:09:30 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:4faefd84b7c54d68b276c9451c76d83991f446ae6e5c21d61ffc23976820008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49899862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906574974acf76b8f05d02292abaac804c08d05909cd1a0a0ac0fa1545d97f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:47:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:04 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba992a90373c6f9649b17857d1fe6894ed01c492f0c3f8314218f3bf8ac6725`  
		Last Modified: Sat, 08 Nov 2025 17:49:02 GMT  
		Size: 457.9 KB (457910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808795fe98794b5559426ab0b77bf9109a6b2572c67e673d3cc2b4323aef9df8`  
		Last Modified: Sat, 08 Nov 2025 17:49:06 GMT  
		Size: 45.8 MB (45792340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94b29e8468df4e2b75502b1484f121021c6b11e808ea65af2b920c14129bfb`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:3ec8fd1cc7a3434e45bc24f365f23be261d08218078d8fa71d09ce90d0b5dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43660154f83526b4ecc46d1f468cafdcccad1ab2cd10356fb4174b8da31316b4`

```dockerfile
```

-	Layers:
	-	`sha256:5229dda88366c5ad5993f82a43d495c8bd119544e12e3b26fa98ef6c6cfd09a0`  
		Last Modified: Sat, 08 Nov 2025 19:15:26 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79fb299eb71e31887ab98cc994b995c2943b800c28b8e947bbc9db38525c876`  
		Last Modified: Sat, 08 Nov 2025 19:15:27 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:badb2650cbabae8263ebed0a979475c66c31edc92b24535a519b1ebe5cd1c877
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:1332aeea1523caaac64bc7406c29fc64251fa094ceb7bfb07bc2cb0b8f529f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50910385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dbee76cdc4979751996a427018d29e2c47cbec3969f6531ffc657a85877568`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:45 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97737d16fc287bff426b9fcc31e25545fa851f22fd8ddafe89247d215a75ad`  
		Last Modified: Tue, 28 Oct 2025 17:47:50 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84707add128ffb7f94431606938b253c3801170834ff69ffe34f357c2e4c7a13`  
		Last Modified: Tue, 28 Oct 2025 17:48:24 GMT  
		Size: 46.7 MB (46650641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f36d2f6d74a2a636fdbf7dd1aca511bf3fc1c22d696d4e6f1663f4898ea093`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:cb43b5450457a56aa9616d67acd9cadc442dac847f0d1251b6f1e71838358d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964ad9164c17fa2c3b892a2616aeea20142f4ea9ead7854fc1de56230d9e617d`

```dockerfile
```

-	Layers:
	-	`sha256:363044314e3b4bdfe2bf8e8e39d23c486c2135feb6fde6b2433dbecbe05587e0`  
		Last Modified: Tue, 28 Oct 2025 18:10:18 GMT  
		Size: 855.0 KB (854969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0337a010506479073a18b774ec9f78438b31f8adb57be84fe6f18b96df693639`  
		Last Modified: Tue, 28 Oct 2025 18:10:20 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fb0937ebe0301624689d25e9b98446767f3f6a4c5d50103f5fecc33f2d16994c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46664295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabf0acac9bd919187522e3e8bfee4e0ef390322cdbac29f185b0bc7f771a06a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:56 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45540fa3a8d3d091a7310092722247dfa5a86e242b3eb49cf653df1cc2ead`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 457.7 KB (457734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d911210d3431c2962574b7b9991f46aee9b03593cdcbf28c8c6fb83209d9c`  
		Last Modified: Tue, 28 Oct 2025 17:48:22 GMT  
		Size: 42.7 MB (42702112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ea1d8666f65ee215e321ebb26eccb50d4a7884ed90d91fdfc926319262506`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:7c0532eda99388f549249be5763638fc35eda61a5257c12f890fc9587698b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d2903526cd5d4cbbf402e83879fe4ad3027cacb1c5ab3c2299ba6caa43460`

```dockerfile
```

-	Layers:
	-	`sha256:3d07b4e5c28f4ddbde7c6c86862bdc9d9a0164275ab22e3df66097a83268e9be`  
		Last Modified: Tue, 28 Oct 2025 18:10:23 GMT  
		Size: 12.4 KB (12395 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ab418a79e147f0c147f20d9d60f533da7c525373ed4bd1d164c63f8bca9ce9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f644e134d254c5450d3c76a3c9080fcf32358fb5e5850f5c2a2c594668d811ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:46:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:26 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505aca7b2af80fb1238e95cc1e84ea0b413f871a2a32aa0aa56987bccbe0a7f`  
		Last Modified: Tue, 28 Oct 2025 17:47:44 GMT  
		Size: 459.0 KB (459024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea70b51c2f64913cfef44574bfec1feb51f974e81e8555b3c0ba4d7a746368`  
		Last Modified: Tue, 28 Oct 2025 17:48:19 GMT  
		Size: 42.6 MB (42556661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442542845355acb4759bb19a01eb66b5d0fcc819bf28217f2d78fa9ae0100a3`  
		Last Modified: Tue, 28 Oct 2025 17:48:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:350601070db30fa37739fd111f5cd43143082917a5e665466821c1526813fe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1e0f4f6e44232018f2fb26877162717a685dfbb4a8440c887e7994d48eb55d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5cf79ab6d112724f8cdea87c8b0c3b4f82014dd1d5038d03db5d3edc52cf6e`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 855.1 KB (855061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b918ca010d1776d51e7f6600cda1169389ae4805f6b81200fcafdd02a0234d6`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:8b78cc9c02e03d2b9c7d664b64e35836dc1dd52a0ecb9e0155e9e84c64e86d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d9034e795d7d490437d617256a97871e1d843787c30c6a9b29aceb83c0d9ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 03:32:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:49:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:49:14 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:49:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476383bb2bb2988acf2098cf20bed14bd4441bc69c2acd614a2184dbd44d8a8`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 459.4 KB (459426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e962222239ca1db0946eb95f2639a631db0d2b7e384c4e51914825a43ebc82eb`  
		Last Modified: Tue, 28 Oct 2025 17:50:23 GMT  
		Size: 40.9 MB (40872840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7f46011584a53acf7b7061f713e6e84bf026644e2f99a0cee25ea98f590bf3`  
		Last Modified: Tue, 28 Oct 2025 17:50:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:8e7817f72ca1a8412416e686715efee169d32c0da5b663902081a195cb2b0f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fdec5acfb4b5a22c5bc9e0e5ba8bfa7965c7bbbefbc5af5dbc48a2a9e4de40`

```dockerfile
```

-	Layers:
	-	`sha256:d46ffd6881cb514082c44dc74abde240e3d7451d0eda7f67841363a1d9692b45`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 853.1 KB (853070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658821108ec994a7bdbbcbc0ca7dbae2c4d97e9d1a84b2ac716148769052974f`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:47808be40092a8f0eadfd3423422c5a9fd6644b6a67fd556f98891512c7d8ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49224580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8d8c2005c13f7aef9ccb20b88ffb6d250ee9d82de95ed5fa93c4cade0f3b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 15:02:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 Oct 2025 15:14:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Oct 2025 15:14:26 GMT
CMD ["traefik"]
# Wed, 29 Oct 2025 15:14:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3734c19de58da4f3bd4df579f0943d0967f596e3a1e2aa541e119d14638340`  
		Last Modified: Wed, 29 Oct 2025 15:08:21 GMT  
		Size: 457.3 KB (457265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7431aec009fbc1aed617baba72815f470a8edbbcdd89275198e9fa611d614`  
		Last Modified: Wed, 29 Oct 2025 15:19:51 GMT  
		Size: 45.3 MB (45251707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d2683b6ac01afc5a6e6b8607e99964916b1674d9cabb34e6c97694a0668d5`  
		Last Modified: Wed, 29 Oct 2025 15:19:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:72d8db8a45e182f730c763c34e92a9ccf27e5823dc91027da64913be1a140e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d101f19f639bae0f2f3d218b38bcd0feb283e86210762a217e6add3d33adf`

```dockerfile
```

-	Layers:
	-	`sha256:eed804f401f8645370ee55c500d178dac6eb42935ad10fea6f2f1e57ee24dd32`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 853.1 KB (853066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18cb9eac7c2ca078418ff431acaae16fb87ddcd871256e4442b498b4fa80507`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:62793241ab3d3fa28e30f6a4d3b92d2f0e49c2fb0c3474b8350eb6c0a08c990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f46a2e0f3bd40e068adbfa338d31864ffe512c1a4b7cb0f3e22d282a7d8ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 02:26:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:52:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:52:24 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:52:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6155014a1d77a7bc8a35aaadb5baad965e9e640c5be73a93d70e92988712af6d`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b402204d5299e98a2674e31dfe76c1067b611238b2d27bc1455a180b10691b9`  
		Last Modified: Tue, 28 Oct 2025 17:53:22 GMT  
		Size: 45.2 MB (45191097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c03dd8190a9e7c30c473a99dde70793acdd87c0fa553c36466cdae626ae73`  
		Last Modified: Tue, 28 Oct 2025 17:53:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c9c848a281277a91c6d12862355ff4eb93759e0929b211a37e22656ec66def60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c792e2b12f36bd90717549db7ad4a26ceffbb37e31f176c55791379ef7b181d1`

```dockerfile
```

-	Layers:
	-	`sha256:eac88704671328544f3d2394f32b7c94060cfd6e83999c53573fbddedc9a23ce`  
		Last Modified: Tue, 28 Oct 2025 18:10:42 GMT  
		Size: 853.0 KB (853014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5c84a0048b551af6d027b04bc271d0152fa1b3a3e91a2f965461c4139f1db7`  
		Last Modified: Tue, 28 Oct 2025 18:10:43 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:60724e738c7ed9116b0cca972040b6aafd2762d2f572afaa54a40552a9fb62f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e2f55045c64078c084ef9e53f08adf1623aa8e844c0f61ac976e59ef978d66be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173790001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8318d8f6e397d73cc19da9686cd752741b871ca5e5f2833e0a36abe8a9cc2547`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:6cfeac02f7657e0f21bec793858fed4418e5818930327326190bd6ff11a7fa98 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae60a04a76082373387efad417e4554a5a8af770bbbcc040b0811829cdfbdb`  
		Last Modified: Tue, 11 Nov 2025 20:10:44 GMT  
		Size: 47.4 MB (47437742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36572591302f3f4ec803657efd9cf2a5635c524bf86800891e48499c6c83100d`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39e8d7bce4b204cc12e1d9ec388767ee42407e17c5751b6174c90b12e16df7`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ff038bfba1a92d3ca14cb7a8d0ee8597c094e3ef37614449e15e15bd0bd287`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4113e8c54c253277cdcdd6584f3d094a65d2abf18765de6d30b0abb1bec248cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:7dac490b602f9587776991ffdb54c35d0b697c37dc645387d0890ceca4188306
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818021605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719b1f153be2e7f51d90cedd318244af304cf70e951822e773ee7b73f549277f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:20 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:21 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f462a0a30c68120954a26c242c266ecc7cf71abf17249112775238e61ca66c56`  
		Last Modified: Tue, 11 Nov 2025 19:22:26 GMT  
		Size: 48.1 MB (48054851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311fafd46778b18455cef771ee101f5fdc2fa5d7722610a7acd8e984621d252d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d7f0a3bf57c22d8952d3d2c8b835ad28012ad0e732cc1286b6774abdfbf778`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb0dc8595b4ccc82bf97d01c80ab263d5c15fadb2711cf1c1649a8c49c61f98`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:58bdbd714aaf63369efd43293de2e246e328d76d1c052079f230a069ba147170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e0d382c02836adbce8db53819da77bbed076352af93eab870a5c2d3f2ff1705f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174739638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606f2520cf13e92129dcc7d2d7c2e23f565940998eaa134012ea4050340ad44`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:fa7d458e5035cd7257a4fcca892af645f6a7bff0167a9a36ee2be323cba3aea8 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9080590026898dc45cb4ce39ea66b413cc59161c14bbb40e928d5d2936339bb`  
		Last Modified: Tue, 11 Nov 2025 20:11:00 GMT  
		Size: 48.4 MB (48387349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef94a0710093125c521f9c5feedf55499ec5cd192da6a680877f99e37c7886e1`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922dc6de5393d74f7b8c06fb66486fe7d1329f8d8eb7725e590f63de72359ea`  
		Last Modified: Tue, 11 Nov 2025 20:10:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e291f81a41d1e29a6a1208c05d403fdf7ab5816a3ca4d177558b2bc6a9a08e3`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:18112aed2bfe3dfb8534f1045622390c3316596cff0cefab64f44e43d23e1640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:ramequin` - linux; amd64

```console
$ docker pull traefik@sha256:c1d367d01066413216bde351c64076358928d36c39128bc84b8d77bcf625fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7065ee8303e5acc80a10479c1aa70594eeada0ef33a531d51481b781027646d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:09 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a551e6e94e8d6b0eadbaff71fc30d07e795156757222a3275f23d2fbe886d`  
		Last Modified: Sat, 08 Nov 2025 17:49:39 GMT  
		Size: 456.9 KB (456920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746bd391ec3f05e8f1670234a30e9f9e3f1384f6d6b90e790b1506a91d8f49e`  
		Last Modified: Sat, 08 Nov 2025 17:49:50 GMT  
		Size: 47.6 MB (47647053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9148c3d019cdbb699b0399feb4b8bde49b33225180951c29b3ac484301e8c1fa`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:49404ec90da14b81d5730b4b92bbdce9d9811a0408a65be8821375eff72491d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9f51aa35a7c3f928f92e8b57ef8f73af9296c773ba68a0d01d32968376ef0b`

```dockerfile
```

-	Layers:
	-	`sha256:9a176a130ca26a66b3626af56aa085f2084647a4286c40f2fe92cdde1ea2a18e`  
		Last Modified: Sat, 08 Nov 2025 19:14:36 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cdbd3e4ed32c8605e2e181edd1bdb10825ad3e337119cc8de65279a3e120eda`  
		Last Modified: Sat, 08 Nov 2025 19:14:41 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8c1f9170cd49bd260f86260fa4f9931e1996627b40be511205f4522dfd884ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47122068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911b660733057f37aaf382a62cdd30f37f0aebfd90479c60c17f7789f4439bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:23 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d32af4def2314aeda5fa7c2d5cddb469a0666f2ab64a8999fb4b9d4678b785`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 457.7 KB (457735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa665f047b6aacaefa7c1b5ec28299ef9b34e27197765850c8492fba633ecb2`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 43.2 MB (43159884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142b8a33d16cfda6f921981607a855bc41e11eec7bd904f79c7fd704cbc2d33`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:8176e73ed6e3e37b50fdcf150a77cef959812c1ad9cc4487b6ab25066d695a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a5674fbf0c0b32f1ff7104201f8e2e2cb4f1614fd0aa1ca9a84280ec9a75b1`

```dockerfile
```

-	Layers:
	-	`sha256:90c3e9765b391851fbd5622c83ea675c05c4e54ba07c219dd524c3a2b76f2df1`  
		Last Modified: Sat, 08 Nov 2025 19:15:13 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:932e4f4c53902c8620d64199dffb4c6ef2efcd799137c76bf06312c0291e060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47952858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08927b02f26a06024f9cf1324adf4d4fa6d4302fa35895d3fc55d09de68e8b9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:47 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcfcadb61884e632ee6855fc9d05acdcac92ea38f3baf49360df256678d6c4`  
		Last Modified: Sat, 08 Nov 2025 17:49:25 GMT  
		Size: 459.0 KB (459025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6133c1595dad94916b16df346dba0c3674ee62cd6e8d48575401b932e0a5af`  
		Last Modified: Sat, 08 Nov 2025 17:49:28 GMT  
		Size: 43.4 MB (43355395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e688a415944a77f89aff4bfb8501253f3e5f2070bc106ee762f607015d954`  
		Last Modified: Sat, 08 Nov 2025 17:49:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:b958dfd5bb43ec9a4b595bf8f8da8c2569c2bc6fb5630fdb015c8c871125dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76b4b1bbd51072fb33c96875d3537bceac06c87d22047b6b3a6575ce8b5723`

```dockerfile
```

-	Layers:
	-	`sha256:b9287959e40047244875219eccfc9a62c79f3464f225bb9a6a839f429de903e4`  
		Last Modified: Sat, 08 Nov 2025 19:15:16 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dc0ebacd5097f6f54c735e6db91e5b34108d5ffa7c2dc587f22ab4917a5057`  
		Last Modified: Sat, 08 Nov 2025 19:15:17 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:d8a89c65c0466dbaf521dfee4394549e4d813e5e112bb31efa5c5d21380b6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45528880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e7f93130630c77319d3ad4f4acd6e0f940863cc36847e3ee44c583095f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:06 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed7ef67f69c2b5a0caa2013b8451255932b057923b9f18ef138e1bac3fe202`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 459.4 KB (459431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a635055d916db706f9ac32e427eda46e90cd856045aa0fffb8c0a4dc3935c`  
		Last Modified: Sat, 08 Nov 2025 17:49:10 GMT  
		Size: 41.3 MB (41336840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf09a848ab17c82ae94532e3cf46cff03e322c1a70998c68b85f5ee140ed63d`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:f3e919e7b8655274f12133697480e98e440215a5356a8c7ede337538155e129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd9a8ed72756542deae52401b02bb5b1a8591a5d6e9a3e9b827e31fa765a82`

```dockerfile
```

-	Layers:
	-	`sha256:33a73882bd6d35e47d0c8d12e1582d660da8fe3bebb4965e80a15c450edd764e`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a1f979a9028a3050a78bf693f450e4a9a661201036dba695172ce07ca6582c`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:9d945497f1e0e0315abc0a52f853239338f08e713a86b22942e9eb55a3fd9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49896389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8753fb4db640d360a2b5e1fb0ec9946738292c1e981455888d7fc665d05a860e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
COPY entrypoint.sh / # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
EXPOSE map[80/tcp:{}]
# Sun, 09 Nov 2025 21:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 09 Nov 2025 21:37:43 GMT
CMD ["traefik"]
# Sun, 09 Nov 2025 21:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b6e207f69d2afa9c62f16c53bac3661f79667ed248dbb86188fa53be5a0fc`  
		Last Modified: Sun, 09 Nov 2025 21:42:58 GMT  
		Size: 45.9 MB (45923504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc33070eac1e0dfbffe3befc315859cc7adfa74df7e1746110f3f9eda17bb`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:4d7cb2aeb1a9fb763a9cc257178350c0a6d8f7a2975d563d19e0832e018d1e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198a484789301f44968e04d7f83eb867c272a217e81bfa34fbf49cc9d0809ba6`

```dockerfile
```

-	Layers:
	-	`sha256:165bd089fae0d63962bc1db2a74722d6fba1d131b94f525f12dc91f8ca589e00`  
		Last Modified: Sun, 09 Nov 2025 22:09:29 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f258816c82e54e07b68a06537658018cd2a88d81ab9d8fdfac714731b69551b`  
		Last Modified: Sun, 09 Nov 2025 22:09:30 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:4faefd84b7c54d68b276c9451c76d83991f446ae6e5c21d61ffc23976820008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49899862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906574974acf76b8f05d02292abaac804c08d05909cd1a0a0ac0fa1545d97f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:47:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:04 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba992a90373c6f9649b17857d1fe6894ed01c492f0c3f8314218f3bf8ac6725`  
		Last Modified: Sat, 08 Nov 2025 17:49:02 GMT  
		Size: 457.9 KB (457910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808795fe98794b5559426ab0b77bf9109a6b2572c67e673d3cc2b4323aef9df8`  
		Last Modified: Sat, 08 Nov 2025 17:49:06 GMT  
		Size: 45.8 MB (45792340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94b29e8468df4e2b75502b1484f121021c6b11e808ea65af2b920c14129bfb`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:3ec8fd1cc7a3434e45bc24f365f23be261d08218078d8fa71d09ce90d0b5dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43660154f83526b4ecc46d1f468cafdcccad1ab2cd10356fb4174b8da31316b4`

```dockerfile
```

-	Layers:
	-	`sha256:5229dda88366c5ad5993f82a43d495c8bd119544e12e3b26fa98ef6c6cfd09a0`  
		Last Modified: Sat, 08 Nov 2025 19:15:26 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79fb299eb71e31887ab98cc994b995c2943b800c28b8e947bbc9db38525c876`  
		Last Modified: Sat, 08 Nov 2025 19:15:27 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:58bdbd714aaf63369efd43293de2e246e328d76d1c052079f230a069ba147170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e0d382c02836adbce8db53819da77bbed076352af93eab870a5c2d3f2ff1705f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174739638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606f2520cf13e92129dcc7d2d7c2e23f565940998eaa134012ea4050340ad44`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:fa7d458e5035cd7257a4fcca892af645f6a7bff0167a9a36ee2be323cba3aea8 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9080590026898dc45cb4ce39ea66b413cc59161c14bbb40e928d5d2936339bb`  
		Last Modified: Tue, 11 Nov 2025 20:11:00 GMT  
		Size: 48.4 MB (48387349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef94a0710093125c521f9c5feedf55499ec5cd192da6a680877f99e37c7886e1`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922dc6de5393d74f7b8c06fb66486fe7d1329f8d8eb7725e590f63de72359ea`  
		Last Modified: Tue, 11 Nov 2025 20:10:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e291f81a41d1e29a6a1208c05d403fdf7ab5816a3ca4d177558b2bc6a9a08e3`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:047d63ab1573e82a1136a4411117bd2346d5021076eddc80f6bc4bee8a529e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e8af3c304a96ec32fc62478b50dcd7cbc370fcb7ec1bc73fbb1427b00f40490b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818993276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d7a9e86f9609ce347f37946711c412653be1364ec950f24251da914b8bb987`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:01 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:01 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef226535da45dbfa8a4d7f70609bddf8ca912461ba29fffbb5f4a6c343342bad`  
		Last Modified: Tue, 11 Nov 2025 19:22:25 GMT  
		Size: 49.0 MB (49026478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8441ed2b6b03f2592848998903b7b2048dc3fd90a58cc751691c8b350c9624e`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eef944fba1dc3cb2e6c0db849ee7cf49cb25a8f5718ff1f805e546ec4d79d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f944678203d9badbe57ca7c5ed0d295e0c697fc5a46c855fb1f53b2417de9`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:badb2650cbabae8263ebed0a979475c66c31edc92b24535a519b1ebe5cd1c877
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2` - linux; amd64

```console
$ docker pull traefik@sha256:1332aeea1523caaac64bc7406c29fc64251fa094ceb7bfb07bc2cb0b8f529f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50910385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dbee76cdc4979751996a427018d29e2c47cbec3969f6531ffc657a85877568`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:45 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97737d16fc287bff426b9fcc31e25545fa851f22fd8ddafe89247d215a75ad`  
		Last Modified: Tue, 28 Oct 2025 17:47:50 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84707add128ffb7f94431606938b253c3801170834ff69ffe34f357c2e4c7a13`  
		Last Modified: Tue, 28 Oct 2025 17:48:24 GMT  
		Size: 46.7 MB (46650641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f36d2f6d74a2a636fdbf7dd1aca511bf3fc1c22d696d4e6f1663f4898ea093`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:cb43b5450457a56aa9616d67acd9cadc442dac847f0d1251b6f1e71838358d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964ad9164c17fa2c3b892a2616aeea20142f4ea9ead7854fc1de56230d9e617d`

```dockerfile
```

-	Layers:
	-	`sha256:363044314e3b4bdfe2bf8e8e39d23c486c2135feb6fde6b2433dbecbe05587e0`  
		Last Modified: Tue, 28 Oct 2025 18:10:18 GMT  
		Size: 855.0 KB (854969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0337a010506479073a18b774ec9f78438b31f8adb57be84fe6f18b96df693639`  
		Last Modified: Tue, 28 Oct 2025 18:10:20 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fb0937ebe0301624689d25e9b98446767f3f6a4c5d50103f5fecc33f2d16994c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46664295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabf0acac9bd919187522e3e8bfee4e0ef390322cdbac29f185b0bc7f771a06a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:56 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45540fa3a8d3d091a7310092722247dfa5a86e242b3eb49cf653df1cc2ead`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 457.7 KB (457734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d911210d3431c2962574b7b9991f46aee9b03593cdcbf28c8c6fb83209d9c`  
		Last Modified: Tue, 28 Oct 2025 17:48:22 GMT  
		Size: 42.7 MB (42702112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ea1d8666f65ee215e321ebb26eccb50d4a7884ed90d91fdfc926319262506`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:7c0532eda99388f549249be5763638fc35eda61a5257c12f890fc9587698b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d2903526cd5d4cbbf402e83879fe4ad3027cacb1c5ab3c2299ba6caa43460`

```dockerfile
```

-	Layers:
	-	`sha256:3d07b4e5c28f4ddbde7c6c86862bdc9d9a0164275ab22e3df66097a83268e9be`  
		Last Modified: Tue, 28 Oct 2025 18:10:23 GMT  
		Size: 12.4 KB (12395 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ab418a79e147f0c147f20d9d60f533da7c525373ed4bd1d164c63f8bca9ce9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f644e134d254c5450d3c76a3c9080fcf32358fb5e5850f5c2a2c594668d811ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:46:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:26 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505aca7b2af80fb1238e95cc1e84ea0b413f871a2a32aa0aa56987bccbe0a7f`  
		Last Modified: Tue, 28 Oct 2025 17:47:44 GMT  
		Size: 459.0 KB (459024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea70b51c2f64913cfef44574bfec1feb51f974e81e8555b3c0ba4d7a746368`  
		Last Modified: Tue, 28 Oct 2025 17:48:19 GMT  
		Size: 42.6 MB (42556661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442542845355acb4759bb19a01eb66b5d0fcc819bf28217f2d78fa9ae0100a3`  
		Last Modified: Tue, 28 Oct 2025 17:48:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:350601070db30fa37739fd111f5cd43143082917a5e665466821c1526813fe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1e0f4f6e44232018f2fb26877162717a685dfbb4a8440c887e7994d48eb55d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5cf79ab6d112724f8cdea87c8b0c3b4f82014dd1d5038d03db5d3edc52cf6e`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 855.1 KB (855061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b918ca010d1776d51e7f6600cda1169389ae4805f6b81200fcafdd02a0234d6`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:8b78cc9c02e03d2b9c7d664b64e35836dc1dd52a0ecb9e0155e9e84c64e86d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d9034e795d7d490437d617256a97871e1d843787c30c6a9b29aceb83c0d9ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 03:32:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:49:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:49:14 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:49:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476383bb2bb2988acf2098cf20bed14bd4441bc69c2acd614a2184dbd44d8a8`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 459.4 KB (459426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e962222239ca1db0946eb95f2639a631db0d2b7e384c4e51914825a43ebc82eb`  
		Last Modified: Tue, 28 Oct 2025 17:50:23 GMT  
		Size: 40.9 MB (40872840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7f46011584a53acf7b7061f713e6e84bf026644e2f99a0cee25ea98f590bf3`  
		Last Modified: Tue, 28 Oct 2025 17:50:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:8e7817f72ca1a8412416e686715efee169d32c0da5b663902081a195cb2b0f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fdec5acfb4b5a22c5bc9e0e5ba8bfa7965c7bbbefbc5af5dbc48a2a9e4de40`

```dockerfile
```

-	Layers:
	-	`sha256:d46ffd6881cb514082c44dc74abde240e3d7451d0eda7f67841363a1d9692b45`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 853.1 KB (853070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658821108ec994a7bdbbcbc0ca7dbae2c4d97e9d1a84b2ac716148769052974f`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:47808be40092a8f0eadfd3423422c5a9fd6644b6a67fd556f98891512c7d8ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49224580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8d8c2005c13f7aef9ccb20b88ffb6d250ee9d82de95ed5fa93c4cade0f3b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 15:02:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 Oct 2025 15:14:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Oct 2025 15:14:26 GMT
CMD ["traefik"]
# Wed, 29 Oct 2025 15:14:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3734c19de58da4f3bd4df579f0943d0967f596e3a1e2aa541e119d14638340`  
		Last Modified: Wed, 29 Oct 2025 15:08:21 GMT  
		Size: 457.3 KB (457265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7431aec009fbc1aed617baba72815f470a8edbbcdd89275198e9fa611d614`  
		Last Modified: Wed, 29 Oct 2025 15:19:51 GMT  
		Size: 45.3 MB (45251707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d2683b6ac01afc5a6e6b8607e99964916b1674d9cabb34e6c97694a0668d5`  
		Last Modified: Wed, 29 Oct 2025 15:19:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:72d8db8a45e182f730c763c34e92a9ccf27e5823dc91027da64913be1a140e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d101f19f639bae0f2f3d218b38bcd0feb283e86210762a217e6add3d33adf`

```dockerfile
```

-	Layers:
	-	`sha256:eed804f401f8645370ee55c500d178dac6eb42935ad10fea6f2f1e57ee24dd32`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 853.1 KB (853066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18cb9eac7c2ca078418ff431acaae16fb87ddcd871256e4442b498b4fa80507`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:62793241ab3d3fa28e30f6a4d3b92d2f0e49c2fb0c3474b8350eb6c0a08c990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f46a2e0f3bd40e068adbfa338d31864ffe512c1a4b7cb0f3e22d282a7d8ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 02:26:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:52:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:52:24 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:52:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6155014a1d77a7bc8a35aaadb5baad965e9e640c5be73a93d70e92988712af6d`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b402204d5299e98a2674e31dfe76c1067b611238b2d27bc1455a180b10691b9`  
		Last Modified: Tue, 28 Oct 2025 17:53:22 GMT  
		Size: 45.2 MB (45191097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c03dd8190a9e7c30c473a99dde70793acdd87c0fa553c36466cdae626ae73`  
		Last Modified: Tue, 28 Oct 2025 17:53:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c9c848a281277a91c6d12862355ff4eb93759e0929b211a37e22656ec66def60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c792e2b12f36bd90717549db7ad4a26ceffbb37e31f176c55791379ef7b181d1`

```dockerfile
```

-	Layers:
	-	`sha256:eac88704671328544f3d2394f32b7c94060cfd6e83999c53573fbddedc9a23ce`  
		Last Modified: Tue, 28 Oct 2025 18:10:42 GMT  
		Size: 853.0 KB (853014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5c84a0048b551af6d027b04bc271d0152fa1b3a3e91a2f965461c4139f1db7`  
		Last Modified: Tue, 28 Oct 2025 18:10:43 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:60724e738c7ed9116b0cca972040b6aafd2762d2f572afaa54a40552a9fb62f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e2f55045c64078c084ef9e53f08adf1623aa8e844c0f61ac976e59ef978d66be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173790001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8318d8f6e397d73cc19da9686cd752741b871ca5e5f2833e0a36abe8a9cc2547`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:6cfeac02f7657e0f21bec793858fed4418e5818930327326190bd6ff11a7fa98 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae60a04a76082373387efad417e4554a5a8af770bbbcc040b0811829cdfbdb`  
		Last Modified: Tue, 11 Nov 2025 20:10:44 GMT  
		Size: 47.4 MB (47437742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36572591302f3f4ec803657efd9cf2a5635c524bf86800891e48499c6c83100d`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39e8d7bce4b204cc12e1d9ec388767ee42407e17c5751b6174c90b12e16df7`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ff038bfba1a92d3ca14cb7a8d0ee8597c094e3ef37614449e15e15bd0bd287`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4113e8c54c253277cdcdd6584f3d094a65d2abf18765de6d30b0abb1bec248cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:7dac490b602f9587776991ffdb54c35d0b697c37dc645387d0890ceca4188306
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818021605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719b1f153be2e7f51d90cedd318244af304cf70e951822e773ee7b73f549277f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:20 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:21 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f462a0a30c68120954a26c242c266ecc7cf71abf17249112775238e61ca66c56`  
		Last Modified: Tue, 11 Nov 2025 19:22:26 GMT  
		Size: 48.1 MB (48054851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311fafd46778b18455cef771ee101f5fdc2fa5d7722610a7acd8e984621d252d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d7f0a3bf57c22d8952d3d2c8b835ad28012ad0e732cc1286b6774abdfbf778`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb0dc8595b4ccc82bf97d01c80ab263d5c15fadb2711cf1c1649a8c49c61f98`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:badb2650cbabae8263ebed0a979475c66c31edc92b24535a519b1ebe5cd1c877
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11` - linux; amd64

```console
$ docker pull traefik@sha256:1332aeea1523caaac64bc7406c29fc64251fa094ceb7bfb07bc2cb0b8f529f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50910385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dbee76cdc4979751996a427018d29e2c47cbec3969f6531ffc657a85877568`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:10 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:45 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97737d16fc287bff426b9fcc31e25545fa851f22fd8ddafe89247d215a75ad`  
		Last Modified: Tue, 28 Oct 2025 17:47:50 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84707add128ffb7f94431606938b253c3801170834ff69ffe34f357c2e4c7a13`  
		Last Modified: Tue, 28 Oct 2025 17:48:24 GMT  
		Size: 46.7 MB (46650641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f36d2f6d74a2a636fdbf7dd1aca511bf3fc1c22d696d4e6f1663f4898ea093`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:cb43b5450457a56aa9616d67acd9cadc442dac847f0d1251b6f1e71838358d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964ad9164c17fa2c3b892a2616aeea20142f4ea9ead7854fc1de56230d9e617d`

```dockerfile
```

-	Layers:
	-	`sha256:363044314e3b4bdfe2bf8e8e39d23c486c2135feb6fde6b2433dbecbe05587e0`  
		Last Modified: Tue, 28 Oct 2025 18:10:18 GMT  
		Size: 855.0 KB (854969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0337a010506479073a18b774ec9f78438b31f8adb57be84fe6f18b96df693639`  
		Last Modified: Tue, 28 Oct 2025 18:10:20 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fb0937ebe0301624689d25e9b98446767f3f6a4c5d50103f5fecc33f2d16994c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46664295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabf0acac9bd919187522e3e8bfee4e0ef390322cdbac29f185b0bc7f771a06a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:56 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45540fa3a8d3d091a7310092722247dfa5a86e242b3eb49cf653df1cc2ead`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 457.7 KB (457734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d911210d3431c2962574b7b9991f46aee9b03593cdcbf28c8c6fb83209d9c`  
		Last Modified: Tue, 28 Oct 2025 17:48:22 GMT  
		Size: 42.7 MB (42702112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ea1d8666f65ee215e321ebb26eccb50d4a7884ed90d91fdfc926319262506`  
		Last Modified: Tue, 28 Oct 2025 17:48:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7c0532eda99388f549249be5763638fc35eda61a5257c12f890fc9587698b145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284d2903526cd5d4cbbf402e83879fe4ad3027cacb1c5ab3c2299ba6caa43460`

```dockerfile
```

-	Layers:
	-	`sha256:3d07b4e5c28f4ddbde7c6c86862bdc9d9a0164275ab22e3df66097a83268e9be`  
		Last Modified: Tue, 28 Oct 2025 18:10:23 GMT  
		Size: 12.4 KB (12395 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:ab418a79e147f0c147f20d9d60f533da7c525373ed4bd1d164c63f8bca9ce9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f644e134d254c5450d3c76a3c9080fcf32358fb5e5850f5c2a2c594668d811ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:46:46 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:26 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505aca7b2af80fb1238e95cc1e84ea0b413f871a2a32aa0aa56987bccbe0a7f`  
		Last Modified: Tue, 28 Oct 2025 17:47:44 GMT  
		Size: 459.0 KB (459024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea70b51c2f64913cfef44574bfec1feb51f974e81e8555b3c0ba4d7a746368`  
		Last Modified: Tue, 28 Oct 2025 17:48:19 GMT  
		Size: 42.6 MB (42556661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442542845355acb4759bb19a01eb66b5d0fcc819bf28217f2d78fa9ae0100a3`  
		Last Modified: Tue, 28 Oct 2025 17:48:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:350601070db30fa37739fd111f5cd43143082917a5e665466821c1526813fe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1e0f4f6e44232018f2fb26877162717a685dfbb4a8440c887e7994d48eb55d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5cf79ab6d112724f8cdea87c8b0c3b4f82014dd1d5038d03db5d3edc52cf6e`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 855.1 KB (855061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b918ca010d1776d51e7f6600cda1169389ae4805f6b81200fcafdd02a0234d6`  
		Last Modified: Tue, 28 Oct 2025 18:10:27 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:8b78cc9c02e03d2b9c7d664b64e35836dc1dd52a0ecb9e0155e9e84c64e86d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45064875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d9034e795d7d490437d617256a97871e1d843787c30c6a9b29aceb83c0d9ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 03:32:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:49:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:49:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:49:14 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:49:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476383bb2bb2988acf2098cf20bed14bd4441bc69c2acd614a2184dbd44d8a8`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 459.4 KB (459426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e962222239ca1db0946eb95f2639a631db0d2b7e384c4e51914825a43ebc82eb`  
		Last Modified: Tue, 28 Oct 2025 17:50:23 GMT  
		Size: 40.9 MB (40872840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7f46011584a53acf7b7061f713e6e84bf026644e2f99a0cee25ea98f590bf3`  
		Last Modified: Tue, 28 Oct 2025 17:50:18 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:8e7817f72ca1a8412416e686715efee169d32c0da5b663902081a195cb2b0f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fdec5acfb4b5a22c5bc9e0e5ba8bfa7965c7bbbefbc5af5dbc48a2a9e4de40`

```dockerfile
```

-	Layers:
	-	`sha256:d46ffd6881cb514082c44dc74abde240e3d7451d0eda7f67841363a1d9692b45`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 853.1 KB (853070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658821108ec994a7bdbbcbc0ca7dbae2c4d97e9d1a84b2ac716148769052974f`  
		Last Modified: Tue, 28 Oct 2025 18:10:37 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:47808be40092a8f0eadfd3423422c5a9fd6644b6a67fd556f98891512c7d8ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49224580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab8d8c2005c13f7aef9ccb20b88ffb6d250ee9d82de95ed5fa93c4cade0f3b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 15:02:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
COPY entrypoint.sh / # buildkit
# Wed, 29 Oct 2025 15:14:26 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 Oct 2025 15:14:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Oct 2025 15:14:26 GMT
CMD ["traefik"]
# Wed, 29 Oct 2025 15:14:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3734c19de58da4f3bd4df579f0943d0967f596e3a1e2aa541e119d14638340`  
		Last Modified: Wed, 29 Oct 2025 15:08:21 GMT  
		Size: 457.3 KB (457265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7431aec009fbc1aed617baba72815f470a8edbbcdd89275198e9fa611d614`  
		Last Modified: Wed, 29 Oct 2025 15:19:51 GMT  
		Size: 45.3 MB (45251707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d2683b6ac01afc5a6e6b8607e99964916b1674d9cabb34e6c97694a0668d5`  
		Last Modified: Wed, 29 Oct 2025 15:19:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:72d8db8a45e182f730c763c34e92a9ccf27e5823dc91027da64913be1a140e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.6 KB (865625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4d101f19f639bae0f2f3d218b38bcd0feb283e86210762a217e6add3d33adf`

```dockerfile
```

-	Layers:
	-	`sha256:eed804f401f8645370ee55c500d178dac6eb42935ad10fea6f2f1e57ee24dd32`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 853.1 KB (853066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18cb9eac7c2ca078418ff431acaae16fb87ddcd871256e4442b498b4fa80507`  
		Last Modified: Wed, 29 Oct 2025 18:09:30 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:62793241ab3d3fa28e30f6a4d3b92d2f0e49c2fb0c3474b8350eb6c0a08c990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f46a2e0f3bd40e068adbfa338d31864ffe512c1a4b7cb0f3e22d282a7d8ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 02:26:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:52:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:52:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:52:24 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:52:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6155014a1d77a7bc8a35aaadb5baad965e9e640c5be73a93d70e92988712af6d`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b402204d5299e98a2674e31dfe76c1067b611238b2d27bc1455a180b10691b9`  
		Last Modified: Tue, 28 Oct 2025 17:53:22 GMT  
		Size: 45.2 MB (45191097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c03dd8190a9e7c30c473a99dde70793acdd87c0fa553c36466cdae626ae73`  
		Last Modified: Tue, 28 Oct 2025 17:53:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c9c848a281277a91c6d12862355ff4eb93759e0929b211a37e22656ec66def60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.5 KB (865509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c792e2b12f36bd90717549db7ad4a26ceffbb37e31f176c55791379ef7b181d1`

```dockerfile
```

-	Layers:
	-	`sha256:eac88704671328544f3d2394f32b7c94060cfd6e83999c53573fbddedc9a23ce`  
		Last Modified: Tue, 28 Oct 2025 18:10:42 GMT  
		Size: 853.0 KB (853014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5c84a0048b551af6d027b04bc271d0152fa1b3a3e91a2f965461c4139f1db7`  
		Last Modified: Tue, 28 Oct 2025 18:10:43 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:60724e738c7ed9116b0cca972040b6aafd2762d2f572afaa54a40552a9fb62f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e2f55045c64078c084ef9e53f08adf1623aa8e844c0f61ac976e59ef978d66be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173790001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8318d8f6e397d73cc19da9686cd752741b871ca5e5f2833e0a36abe8a9cc2547`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:6cfeac02f7657e0f21bec793858fed4418e5818930327326190bd6ff11a7fa98 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ae60a04a76082373387efad417e4554a5a8af770bbbcc040b0811829cdfbdb`  
		Last Modified: Tue, 11 Nov 2025 20:10:44 GMT  
		Size: 47.4 MB (47437742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36572591302f3f4ec803657efd9cf2a5635c524bf86800891e48499c6c83100d`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad39e8d7bce4b204cc12e1d9ec388767ee42407e17c5751b6174c90b12e16df7`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ff038bfba1a92d3ca14cb7a8d0ee8597c094e3ef37614449e15e15bd0bd287`  
		Last Modified: Tue, 11 Nov 2025 20:10:40 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:4113e8c54c253277cdcdd6584f3d094a65d2abf18765de6d30b0abb1bec248cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:7dac490b602f9587776991ffdb54c35d0b697c37dc645387d0890ceca4188306
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818021605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719b1f153be2e7f51d90cedd318244af304cf70e951822e773ee7b73f549277f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.30/traefik_v2.11.30_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:20 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:21 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:21 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.30 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442760c8d26f9c34d441d655bfed0213774e9ee1491b0a9d451ba3951353bd99`  
		Last Modified: Tue, 11 Nov 2025 19:18:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f462a0a30c68120954a26c242c266ecc7cf71abf17249112775238e61ca66c56`  
		Last Modified: Tue, 11 Nov 2025 19:22:26 GMT  
		Size: 48.1 MB (48054851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311fafd46778b18455cef771ee101f5fdc2fa5d7722610a7acd8e984621d252d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d7f0a3bf57c22d8952d3d2c8b835ad28012ad0e732cc1286b6774abdfbf778`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb0dc8595b4ccc82bf97d01c80ab263d5c15fadb2711cf1c1649a8c49c61f98`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.31`

**does not exist** (yet?)

## `traefik:v2.11.31-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:v2.11.31-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:v3`

```console
$ docker pull traefik@sha256:18112aed2bfe3dfb8534f1045622390c3316596cff0cefab64f44e43d23e1640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3` - linux; amd64

```console
$ docker pull traefik@sha256:c1d367d01066413216bde351c64076358928d36c39128bc84b8d77bcf625fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7065ee8303e5acc80a10479c1aa70594eeada0ef33a531d51481b781027646d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:09 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a551e6e94e8d6b0eadbaff71fc30d07e795156757222a3275f23d2fbe886d`  
		Last Modified: Sat, 08 Nov 2025 17:49:39 GMT  
		Size: 456.9 KB (456920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746bd391ec3f05e8f1670234a30e9f9e3f1384f6d6b90e790b1506a91d8f49e`  
		Last Modified: Sat, 08 Nov 2025 17:49:50 GMT  
		Size: 47.6 MB (47647053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9148c3d019cdbb699b0399feb4b8bde49b33225180951c29b3ac484301e8c1fa`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:49404ec90da14b81d5730b4b92bbdce9d9811a0408a65be8821375eff72491d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9f51aa35a7c3f928f92e8b57ef8f73af9296c773ba68a0d01d32968376ef0b`

```dockerfile
```

-	Layers:
	-	`sha256:9a176a130ca26a66b3626af56aa085f2084647a4286c40f2fe92cdde1ea2a18e`  
		Last Modified: Sat, 08 Nov 2025 19:14:36 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cdbd3e4ed32c8605e2e181edd1bdb10825ad3e337119cc8de65279a3e120eda`  
		Last Modified: Sat, 08 Nov 2025 19:14:41 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8c1f9170cd49bd260f86260fa4f9931e1996627b40be511205f4522dfd884ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47122068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911b660733057f37aaf382a62cdd30f37f0aebfd90479c60c17f7789f4439bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:23 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d32af4def2314aeda5fa7c2d5cddb469a0666f2ab64a8999fb4b9d4678b785`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 457.7 KB (457735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa665f047b6aacaefa7c1b5ec28299ef9b34e27197765850c8492fba633ecb2`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 43.2 MB (43159884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142b8a33d16cfda6f921981607a855bc41e11eec7bd904f79c7fd704cbc2d33`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:8176e73ed6e3e37b50fdcf150a77cef959812c1ad9cc4487b6ab25066d695a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a5674fbf0c0b32f1ff7104201f8e2e2cb4f1614fd0aa1ca9a84280ec9a75b1`

```dockerfile
```

-	Layers:
	-	`sha256:90c3e9765b391851fbd5622c83ea675c05c4e54ba07c219dd524c3a2b76f2df1`  
		Last Modified: Sat, 08 Nov 2025 19:15:13 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:932e4f4c53902c8620d64199dffb4c6ef2efcd799137c76bf06312c0291e060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47952858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08927b02f26a06024f9cf1324adf4d4fa6d4302fa35895d3fc55d09de68e8b9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:47 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcfcadb61884e632ee6855fc9d05acdcac92ea38f3baf49360df256678d6c4`  
		Last Modified: Sat, 08 Nov 2025 17:49:25 GMT  
		Size: 459.0 KB (459025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6133c1595dad94916b16df346dba0c3674ee62cd6e8d48575401b932e0a5af`  
		Last Modified: Sat, 08 Nov 2025 17:49:28 GMT  
		Size: 43.4 MB (43355395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e688a415944a77f89aff4bfb8501253f3e5f2070bc106ee762f607015d954`  
		Last Modified: Sat, 08 Nov 2025 17:49:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:b958dfd5bb43ec9a4b595bf8f8da8c2569c2bc6fb5630fdb015c8c871125dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76b4b1bbd51072fb33c96875d3537bceac06c87d22047b6b3a6575ce8b5723`

```dockerfile
```

-	Layers:
	-	`sha256:b9287959e40047244875219eccfc9a62c79f3464f225bb9a6a839f429de903e4`  
		Last Modified: Sat, 08 Nov 2025 19:15:16 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dc0ebacd5097f6f54c735e6db91e5b34108d5ffa7c2dc587f22ab4917a5057`  
		Last Modified: Sat, 08 Nov 2025 19:15:17 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:d8a89c65c0466dbaf521dfee4394549e4d813e5e112bb31efa5c5d21380b6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45528880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e7f93130630c77319d3ad4f4acd6e0f940863cc36847e3ee44c583095f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:06 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed7ef67f69c2b5a0caa2013b8451255932b057923b9f18ef138e1bac3fe202`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 459.4 KB (459431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a635055d916db706f9ac32e427eda46e90cd856045aa0fffb8c0a4dc3935c`  
		Last Modified: Sat, 08 Nov 2025 17:49:10 GMT  
		Size: 41.3 MB (41336840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf09a848ab17c82ae94532e3cf46cff03e322c1a70998c68b85f5ee140ed63d`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:f3e919e7b8655274f12133697480e98e440215a5356a8c7ede337538155e129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd9a8ed72756542deae52401b02bb5b1a8591a5d6e9a3e9b827e31fa765a82`

```dockerfile
```

-	Layers:
	-	`sha256:33a73882bd6d35e47d0c8d12e1582d660da8fe3bebb4965e80a15c450edd764e`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a1f979a9028a3050a78bf693f450e4a9a661201036dba695172ce07ca6582c`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:9d945497f1e0e0315abc0a52f853239338f08e713a86b22942e9eb55a3fd9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49896389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8753fb4db640d360a2b5e1fb0ec9946738292c1e981455888d7fc665d05a860e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
COPY entrypoint.sh / # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
EXPOSE map[80/tcp:{}]
# Sun, 09 Nov 2025 21:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 09 Nov 2025 21:37:43 GMT
CMD ["traefik"]
# Sun, 09 Nov 2025 21:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b6e207f69d2afa9c62f16c53bac3661f79667ed248dbb86188fa53be5a0fc`  
		Last Modified: Sun, 09 Nov 2025 21:42:58 GMT  
		Size: 45.9 MB (45923504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc33070eac1e0dfbffe3befc315859cc7adfa74df7e1746110f3f9eda17bb`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:4d7cb2aeb1a9fb763a9cc257178350c0a6d8f7a2975d563d19e0832e018d1e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198a484789301f44968e04d7f83eb867c272a217e81bfa34fbf49cc9d0809ba6`

```dockerfile
```

-	Layers:
	-	`sha256:165bd089fae0d63962bc1db2a74722d6fba1d131b94f525f12dc91f8ca589e00`  
		Last Modified: Sun, 09 Nov 2025 22:09:29 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f258816c82e54e07b68a06537658018cd2a88d81ab9d8fdfac714731b69551b`  
		Last Modified: Sun, 09 Nov 2025 22:09:30 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:4faefd84b7c54d68b276c9451c76d83991f446ae6e5c21d61ffc23976820008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49899862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906574974acf76b8f05d02292abaac804c08d05909cd1a0a0ac0fa1545d97f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:47:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:04 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba992a90373c6f9649b17857d1fe6894ed01c492f0c3f8314218f3bf8ac6725`  
		Last Modified: Sat, 08 Nov 2025 17:49:02 GMT  
		Size: 457.9 KB (457910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808795fe98794b5559426ab0b77bf9109a6b2572c67e673d3cc2b4323aef9df8`  
		Last Modified: Sat, 08 Nov 2025 17:49:06 GMT  
		Size: 45.8 MB (45792340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94b29e8468df4e2b75502b1484f121021c6b11e808ea65af2b920c14129bfb`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:3ec8fd1cc7a3434e45bc24f365f23be261d08218078d8fa71d09ce90d0b5dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43660154f83526b4ecc46d1f468cafdcccad1ab2cd10356fb4174b8da31316b4`

```dockerfile
```

-	Layers:
	-	`sha256:5229dda88366c5ad5993f82a43d495c8bd119544e12e3b26fa98ef6c6cfd09a0`  
		Last Modified: Sat, 08 Nov 2025 19:15:26 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79fb299eb71e31887ab98cc994b995c2943b800c28b8e947bbc9db38525c876`  
		Last Modified: Sat, 08 Nov 2025 19:15:27 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:58bdbd714aaf63369efd43293de2e246e328d76d1c052079f230a069ba147170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e0d382c02836adbce8db53819da77bbed076352af93eab870a5c2d3f2ff1705f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174739638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606f2520cf13e92129dcc7d2d7c2e23f565940998eaa134012ea4050340ad44`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:fa7d458e5035cd7257a4fcca892af645f6a7bff0167a9a36ee2be323cba3aea8 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9080590026898dc45cb4ce39ea66b413cc59161c14bbb40e928d5d2936339bb`  
		Last Modified: Tue, 11 Nov 2025 20:11:00 GMT  
		Size: 48.4 MB (48387349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef94a0710093125c521f9c5feedf55499ec5cd192da6a680877f99e37c7886e1`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922dc6de5393d74f7b8c06fb66486fe7d1329f8d8eb7725e590f63de72359ea`  
		Last Modified: Tue, 11 Nov 2025 20:10:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e291f81a41d1e29a6a1208c05d403fdf7ab5816a3ca4d177558b2bc6a9a08e3`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:047d63ab1573e82a1136a4411117bd2346d5021076eddc80f6bc4bee8a529e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e8af3c304a96ec32fc62478b50dcd7cbc370fcb7ec1bc73fbb1427b00f40490b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818993276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d7a9e86f9609ce347f37946711c412653be1364ec950f24251da914b8bb987`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:01 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:01 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef226535da45dbfa8a4d7f70609bddf8ca912461ba29fffbb5f4a6c343342bad`  
		Last Modified: Tue, 11 Nov 2025 19:22:25 GMT  
		Size: 49.0 MB (49026478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8441ed2b6b03f2592848998903b7b2048dc3fd90a58cc751691c8b350c9624e`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eef944fba1dc3cb2e6c0db849ee7cf49cb25a8f5718ff1f805e546ec4d79d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f944678203d9badbe57ca7c5ed0d295e0c697fc5a46c855fb1f53b2417de9`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:18112aed2bfe3dfb8534f1045622390c3316596cff0cefab64f44e43d23e1640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3.6` - linux; amd64

```console
$ docker pull traefik@sha256:c1d367d01066413216bde351c64076358928d36c39128bc84b8d77bcf625fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51906793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7065ee8303e5acc80a10479c1aa70594eeada0ef33a531d51481b781027646d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:09 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:09 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365a551e6e94e8d6b0eadbaff71fc30d07e795156757222a3275f23d2fbe886d`  
		Last Modified: Sat, 08 Nov 2025 17:49:39 GMT  
		Size: 456.9 KB (456920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1746bd391ec3f05e8f1670234a30e9f9e3f1384f6d6b90e790b1506a91d8f49e`  
		Last Modified: Sat, 08 Nov 2025 17:49:50 GMT  
		Size: 47.6 MB (47647053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9148c3d019cdbb699b0399feb4b8bde49b33225180951c29b3ac484301e8c1fa`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:49404ec90da14b81d5730b4b92bbdce9d9811a0408a65be8821375eff72491d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.3 KB (854265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9f51aa35a7c3f928f92e8b57ef8f73af9296c773ba68a0d01d32968376ef0b`

```dockerfile
```

-	Layers:
	-	`sha256:9a176a130ca26a66b3626af56aa085f2084647a4286c40f2fe92cdde1ea2a18e`  
		Last Modified: Sat, 08 Nov 2025 19:14:36 GMT  
		Size: 841.5 KB (841499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cdbd3e4ed32c8605e2e181edd1bdb10825ad3e337119cc8de65279a3e120eda`  
		Last Modified: Sat, 08 Nov 2025 19:14:41 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8c1f9170cd49bd260f86260fa4f9931e1996627b40be511205f4522dfd884ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47122068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911b660733057f37aaf382a62cdd30f37f0aebfd90479c60c17f7789f4439bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:49:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:49:23 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:49:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:49:23 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:49:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d32af4def2314aeda5fa7c2d5cddb469a0666f2ab64a8999fb4b9d4678b785`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 457.7 KB (457735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa665f047b6aacaefa7c1b5ec28299ef9b34e27197765850c8492fba633ecb2`  
		Last Modified: Sat, 08 Nov 2025 17:49:40 GMT  
		Size: 43.2 MB (43159884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142b8a33d16cfda6f921981607a855bc41e11eec7bd904f79c7fd704cbc2d33`  
		Last Modified: Sat, 08 Nov 2025 17:49:37 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:8176e73ed6e3e37b50fdcf150a77cef959812c1ad9cc4487b6ab25066d695a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a5674fbf0c0b32f1ff7104201f8e2e2cb4f1614fd0aa1ca9a84280ec9a75b1`

```dockerfile
```

-	Layers:
	-	`sha256:90c3e9765b391851fbd5622c83ea675c05c4e54ba07c219dd524c3a2b76f2df1`  
		Last Modified: Sat, 08 Nov 2025 19:15:13 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:932e4f4c53902c8620d64199dffb4c6ef2efcd799137c76bf06312c0291e060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47952858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08927b02f26a06024f9cf1324adf4d4fa6d4302fa35895d3fc55d09de68e8b9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:47 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:47 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcfcadb61884e632ee6855fc9d05acdcac92ea38f3baf49360df256678d6c4`  
		Last Modified: Sat, 08 Nov 2025 17:49:25 GMT  
		Size: 459.0 KB (459025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6133c1595dad94916b16df346dba0c3674ee62cd6e8d48575401b932e0a5af`  
		Last Modified: Sat, 08 Nov 2025 17:49:28 GMT  
		Size: 43.4 MB (43355395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e688a415944a77f89aff4bfb8501253f3e5f2070bc106ee762f607015d954`  
		Last Modified: Sat, 08 Nov 2025 17:49:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:b958dfd5bb43ec9a4b595bf8f8da8c2569c2bc6fb5630fdb015c8c871125dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.5 KB (854536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c76b4b1bbd51072fb33c96875d3537bceac06c87d22047b6b3a6575ce8b5723`

```dockerfile
```

-	Layers:
	-	`sha256:b9287959e40047244875219eccfc9a62c79f3464f225bb9a6a839f429de903e4`  
		Last Modified: Sat, 08 Nov 2025 19:15:16 GMT  
		Size: 841.6 KB (841603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dc0ebacd5097f6f54c735e6db91e5b34108d5ffa7c2dc587f22ab4917a5057`  
		Last Modified: Sat, 08 Nov 2025 19:15:17 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:d8a89c65c0466dbaf521dfee4394549e4d813e5e112bb31efa5c5d21380b6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45528880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4e7f93130630c77319d3ad4f4acd6e0f940863cc36847e3ee44c583095f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:48:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:06 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:06 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed7ef67f69c2b5a0caa2013b8451255932b057923b9f18ef138e1bac3fe202`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 459.4 KB (459431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41a635055d916db706f9ac32e427eda46e90cd856045aa0fffb8c0a4dc3935c`  
		Last Modified: Sat, 08 Nov 2025 17:49:10 GMT  
		Size: 41.3 MB (41336840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf09a848ab17c82ae94532e3cf46cff03e322c1a70998c68b85f5ee140ed63d`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:f3e919e7b8655274f12133697480e98e440215a5356a8c7ede337538155e129e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49fd9a8ed72756542deae52401b02bb5b1a8591a5d6e9a3e9b827e31fa765a82`

```dockerfile
```

-	Layers:
	-	`sha256:33a73882bd6d35e47d0c8d12e1582d660da8fe3bebb4965e80a15c450edd764e`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 839.6 KB (839606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a1f979a9028a3050a78bf693f450e4a9a661201036dba695172ce07ca6582c`  
		Last Modified: Sat, 08 Nov 2025 19:15:21 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:9d945497f1e0e0315abc0a52f853239338f08e713a86b22942e9eb55a3fd9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49896389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8753fb4db640d360a2b5e1fb0ec9946738292c1e981455888d7fc665d05a860e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sun, 09 Nov 2025 21:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
COPY entrypoint.sh / # buildkit
# Sun, 09 Nov 2025 21:37:43 GMT
EXPOSE map[80/tcp:{}]
# Sun, 09 Nov 2025 21:37:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 09 Nov 2025 21:37:43 GMT
CMD ["traefik"]
# Sun, 09 Nov 2025 21:37:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af791cbe18cccde54cc961a13cf4c5891ced4cdef67b44389ccf9e891855e8d5`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 457.3 KB (457276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b6e207f69d2afa9c62f16c53bac3661f79667ed248dbb86188fa53be5a0fc`  
		Last Modified: Sun, 09 Nov 2025 21:42:58 GMT  
		Size: 45.9 MB (45923504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc33070eac1e0dfbffe3befc315859cc7adfa74df7e1746110f3f9eda17bb`  
		Last Modified: Sun, 09 Nov 2025 21:42:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4d7cb2aeb1a9fb763a9cc257178350c0a6d8f7a2975d563d19e0832e018d1e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.4 KB (852438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198a484789301f44968e04d7f83eb867c272a217e81bfa34fbf49cc9d0809ba6`

```dockerfile
```

-	Layers:
	-	`sha256:165bd089fae0d63962bc1db2a74722d6fba1d131b94f525f12dc91f8ca589e00`  
		Last Modified: Sun, 09 Nov 2025 22:09:29 GMT  
		Size: 839.6 KB (839602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f258816c82e54e07b68a06537658018cd2a88d81ab9d8fdfac714731b69551b`  
		Last Modified: Sun, 09 Nov 2025 22:09:30 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:4faefd84b7c54d68b276c9451c76d83991f446ae6e5c21d61ffc23976820008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49899862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906574974acf76b8f05d02292abaac804c08d05909cd1a0a0ac0fa1545d97f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:47:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
COPY entrypoint.sh / # buildkit
# Sat, 08 Nov 2025 17:48:04 GMT
EXPOSE map[80/tcp:{}]
# Sat, 08 Nov 2025 17:48:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 08 Nov 2025 17:48:04 GMT
CMD ["traefik"]
# Sat, 08 Nov 2025 17:48:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba992a90373c6f9649b17857d1fe6894ed01c492f0c3f8314218f3bf8ac6725`  
		Last Modified: Sat, 08 Nov 2025 17:49:02 GMT  
		Size: 457.9 KB (457910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808795fe98794b5559426ab0b77bf9109a6b2572c67e673d3cc2b4323aef9df8`  
		Last Modified: Sat, 08 Nov 2025 17:49:06 GMT  
		Size: 45.8 MB (45792340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94b29e8468df4e2b75502b1484f121021c6b11e808ea65af2b920c14129bfb`  
		Last Modified: Sat, 08 Nov 2025 17:49:04 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:3ec8fd1cc7a3434e45bc24f365f23be261d08218078d8fa71d09ce90d0b5dc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **852.3 KB (852314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43660154f83526b4ecc46d1f468cafdcccad1ab2cd10356fb4174b8da31316b4`

```dockerfile
```

-	Layers:
	-	`sha256:5229dda88366c5ad5993f82a43d495c8bd119544e12e3b26fa98ef6c6cfd09a0`  
		Last Modified: Sat, 08 Nov 2025 19:15:26 GMT  
		Size: 839.5 KB (839548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79fb299eb71e31887ab98cc994b995c2943b800c28b8e947bbc9db38525c876`  
		Last Modified: Sat, 08 Nov 2025 19:15:27 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:58bdbd714aaf63369efd43293de2e246e328d76d1c052079f230a069ba147170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e0d382c02836adbce8db53819da77bbed076352af93eab870a5c2d3f2ff1705f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174739638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606f2520cf13e92129dcc7d2d7c2e23f565940998eaa134012ea4050340ad44`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:10:15 GMT
RUN cmd /S /C #(nop) COPY file:fa7d458e5035cd7257a4fcca892af645f6a7bff0167a9a36ee2be323cba3aea8 in \ 
# Tue, 11 Nov 2025 20:10:17 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 20:10:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9080590026898dc45cb4ce39ea66b413cc59161c14bbb40e928d5d2936339bb`  
		Last Modified: Tue, 11 Nov 2025 20:11:00 GMT  
		Size: 48.4 MB (48387349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef94a0710093125c521f9c5feedf55499ec5cd192da6a680877f99e37c7886e1`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4922dc6de5393d74f7b8c06fb66486fe7d1329f8d8eb7725e590f63de72359ea`  
		Last Modified: Tue, 11 Nov 2025 20:10:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e291f81a41d1e29a6a1208c05d403fdf7ab5816a3ca4d177558b2bc6a9a08e3`  
		Last Modified: Tue, 11 Nov 2025 20:10:56 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:047d63ab1573e82a1136a4411117bd2346d5021076eddc80f6bc4bee8a529e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e8af3c304a96ec32fc62478b50dcd7cbc370fcb7ec1bc73fbb1427b00f40490b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818993276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d7a9e86f9609ce347f37946711c412653be1364ec950f24251da914b8bb987`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:01 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:01 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef226535da45dbfa8a4d7f70609bddf8ca912461ba29fffbb5f4a6c343342bad`  
		Last Modified: Tue, 11 Nov 2025 19:22:25 GMT  
		Size: 49.0 MB (49026478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8441ed2b6b03f2592848998903b7b2048dc3fd90a58cc751691c8b350c9624e`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eef944fba1dc3cb2e6c0db849ee7cf49cb25a8f5718ff1f805e546ec4d79d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f944678203d9badbe57ca7c5ed0d295e0c697fc5a46c855fb1f53b2417de9`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.1`

**does not exist** (yet?)

## `traefik:v3.6.1-nanoserver-ltsc2022`

**does not exist** (yet?)

## `traefik:v3.6.1-windowsservercore-ltsc2022`

**does not exist** (yet?)

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:047d63ab1573e82a1136a4411117bd2346d5021076eddc80f6bc4bee8a529e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:e8af3c304a96ec32fc62478b50dcd7cbc370fcb7ec1bc73fbb1427b00f40490b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818993276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d7a9e86f9609ce347f37946711c412653be1364ec950f24251da914b8bb987`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.0/traefik_v3.6.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 11 Nov 2025 19:20:01 GMT
EXPOSE 80
# Tue, 11 Nov 2025 19:20:01 GMT
ENTRYPOINT ["/traefik"]
# Tue, 11 Nov 2025 19:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef226535da45dbfa8a4d7f70609bddf8ca912461ba29fffbb5f4a6c343342bad`  
		Last Modified: Tue, 11 Nov 2025 19:22:25 GMT  
		Size: 49.0 MB (49026478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8441ed2b6b03f2592848998903b7b2048dc3fd90a58cc751691c8b350c9624e`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eef944fba1dc3cb2e6c0db849ee7cf49cb25a8f5718ff1f805e546ec4d79d`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f944678203d9badbe57ca7c5ed0d295e0c697fc5a46c855fb1f53b2417de9`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
