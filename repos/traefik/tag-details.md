<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.29`](#traefik21129)
-	[`traefik:2.11.29-nanoserver-ltsc2022`](#traefik21129-nanoserver-ltsc2022)
-	[`traefik:2.11.29-windowsservercore-ltsc2022`](#traefik21129-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.5`](#traefik35)
-	[`traefik:3.5-nanoserver-ltsc2022`](#traefik35-nanoserver-ltsc2022)
-	[`traefik:3.5-windowsservercore-ltsc2022`](#traefik35-windowsservercore-ltsc2022)
-	[`traefik:3.5.3`](#traefik353)
-	[`traefik:3.5.3-nanoserver-ltsc2022`](#traefik353-nanoserver-ltsc2022)
-	[`traefik:3.5.3-windowsservercore-ltsc2022`](#traefik353-windowsservercore-ltsc2022)
-	[`traefik:chabichou`](#traefikchabichou)
-	[`traefik:chabichou-nanoserver-ltsc2022`](#traefikchabichou-nanoserver-ltsc2022)
-	[`traefik:chabichou-windowsservercore-ltsc2022`](#traefikchabichou-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.29`](#traefikv21129)
-	[`traefik:v2.11.29-nanoserver-ltsc2022`](#traefikv21129-nanoserver-ltsc2022)
-	[`traefik:v2.11.29-windowsservercore-ltsc2022`](#traefikv21129-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.5`](#traefikv35)
-	[`traefik:v3.5-nanoserver-ltsc2022`](#traefikv35-nanoserver-ltsc2022)
-	[`traefik:v3.5-windowsservercore-ltsc2022`](#traefikv35-windowsservercore-ltsc2022)
-	[`traefik:v3.5.3`](#traefikv353)
-	[`traefik:v3.5.3-nanoserver-ltsc2022`](#traefikv353-nanoserver-ltsc2022)
-	[`traefik:v3.5.3-windowsservercore-ltsc2022`](#traefikv353-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:5856b2381dcbf5e6b0ca81881a3a63cf75b1554889fab5aec843328655bd0fe2
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
$ docker pull traefik@sha256:10c68595a5716f05915f4d268f22da05168ac7ba6e397fd6be2a55c35463c55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48891106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f089b6d079e56196888f8ae298babc84919abed74e79b6a724cd8af6f426f11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace194ea058fa4d5892a892e1fd7b4b886f0408d98c61026f8977953a71f4d4c`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa864f1a2ba563e0af032c40b3c8e61269f4858eb8cdd7edadde3ab12ab419c`  
		Last Modified: Wed, 08 Oct 2025 23:32:52 GMT  
		Size: 44.6 MB (44631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b8dff630a77674c06491533b41967695401e58bad736fbfcf902fedc2206f`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:caddab0ba5406d19bcf97d051a5d84b9c48a90cecf3c5ccfe573300913f5b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ab89444ca88b71d7c3cb8684326b2b33f3798443241af36a27f2227b1be3a`

```dockerfile
```

-	Layers:
	-	`sha256:212e2939a6f92a43306023b844004cc0e62205dba1ae66d31211a5663d0aed15`  
		Last Modified: Thu, 09 Oct 2025 00:09:33 GMT  
		Size: 846.7 KB (846653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fa14d816df3e1c2cd4fda52ce5084605e3007790e128f0037f864dd067d0`  
		Last Modified: Thu, 09 Oct 2025 00:09:34 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:62139bf2068575a96511414601d747bbc381acef0d751b339f4537de689d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44713309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4abdfb90d5de05aa2fe4228dc79fa31757ad3bac4fd4112eb510215e269a76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07f1a83f5ca01436f1065b617a224df85b98f594db8406efb608986ed8d8a8`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127245637effe2cd5c0877929f6ffc01a251163b172e1ff06b222bebf9ef742`  
		Last Modified: Wed, 08 Oct 2025 22:10:12 GMT  
		Size: 40.8 MB (40751121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f87cacf0cabb971ea83173805a4269d07d1b895ef5f62d8320d0d85cd7c2cd`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c72988c31eec2887533432dd4ac2ff4f33d382baff1353fab242a9b40a14f2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacd1272261a03d3c7d5dd2cf48ce8df76029ada41f99c7751e1bcc5f48da1`

```dockerfile
```

-	Layers:
	-	`sha256:1cf126491ae9400b8bf590dbaba64f7e4d29c4301cef15fff2f31d547e392f46`  
		Last Modified: Thu, 09 Oct 2025 00:09:38 GMT  
		Size: 12.4 KB (12440 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b48ce8d73902c67f88b518b1c6aa6918cb0c0a6428f53f0154aaf4af873c106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb020d915e5655fae3f5060ff130a859abfe61a8ea91dfc1882124a58d14326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c35108c807e82173e970f056f3015e5dde837be289dc7933b119952bab0356`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e78658e7eb434fa7fc2370b328d875c80be35f21ab4ac93442933d4730264`  
		Last Modified: Wed, 08 Oct 2025 21:46:11 GMT  
		Size: 40.7 MB (40663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5828773411ee49f3139f8d2e872a67a4bbc6f3ee7d0dde4dcdd9773b5df89261`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:95826936a7213958cbc0d613beaf3e52553d3f80a68e685fc080c210da374482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0692264a94ea4145625fe77fec8feec1bdf451afb44d08f99bb7254cd0bca`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf31304a3d9020b59a7079496b3e887e74bd8243877363c84b185aedeb9502`  
		Last Modified: Thu, 09 Oct 2025 00:09:41 GMT  
		Size: 846.7 KB (846745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569fe3b0553180e02df23f9edf125bc49b2dfd4909414931a3fe1b428e9b4ec7`  
		Last Modified: Thu, 09 Oct 2025 00:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:27943b61f4cf7adb5a28b1428560453f3b221eddd1deb5597d5f66332ea9c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43260058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d0596d25069522159ee5f920821861d6fd636198d6f4909101f698978d1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9cbf796b10af40c247e0fc393162e272fd215b8afd8f9d3d514d3a91517185a2`  
		Last Modified: Thu, 09 Oct 2025 03:34:45 GMT  
		Size: 39.1 MB (39068022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d76833d79bcdee65dfacae22941644722559def5053c666a883f455eadf31f`  
		Last Modified: Thu, 09 Oct 2025 03:34:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a4a72fedd5ff7b13144b419eea765496f66a0e5e6c4f7392bd072c078a0615ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f38d822278db3f44c54fec63a2742f2ae8dc73a26cef1c72981c47fcdc08c70`

```dockerfile
```

-	Layers:
	-	`sha256:594712ef1bc83669370cead772ace625fe91e672eaa185bd8b318da38e47d35d`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 844.8 KB (844754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91d3789db5b665f6928567682693790c06ec8c365ba809aa88b47267841d5ea`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:543d7213524ac3a5b766bac7f62d67eeb3cd197bdbd2f0f168f978495a4b7689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ade4693856965b5e4711fbb27e663f7c51961d42ce95b0e5dc8e96b4030ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:75dfb592752d754af1c64c7dbd9015a2af5414f1e27100b1c1c984ff061bcd65`  
		Last Modified: Thu, 09 Oct 2025 02:28:20 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b010b67dd8d171e9c420f9627ae7d9979a95e634d2079874e4c257f8ce4abc12`  
		Last Modified: Thu, 09 Oct 2025 02:28:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:95f9d7b31c8f90b72c14ba6f425273db6204f76c41f6cecea61fbb508891ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.2 KB (857235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26cb7d048e0cdca0cebfa442468c96993718704c018f51f49cc78d9f1a852cb`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc98b90d01aa636ad8ad59bc0187c689a7e1066f306adc1712daab790480f3`  
		Last Modified: Thu, 09 Oct 2025 03:09:54 GMT  
		Size: 844.7 KB (844698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff43678d08ce6be10d3596b5376adc48089bef0e67225ad27117c6a95fe011d4`  
		Last Modified: Thu, 09 Oct 2025 03:09:55 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:5856b2381dcbf5e6b0ca81881a3a63cf75b1554889fab5aec843328655bd0fe2
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
$ docker pull traefik@sha256:10c68595a5716f05915f4d268f22da05168ac7ba6e397fd6be2a55c35463c55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48891106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f089b6d079e56196888f8ae298babc84919abed74e79b6a724cd8af6f426f11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace194ea058fa4d5892a892e1fd7b4b886f0408d98c61026f8977953a71f4d4c`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa864f1a2ba563e0af032c40b3c8e61269f4858eb8cdd7edadde3ab12ab419c`  
		Last Modified: Wed, 08 Oct 2025 23:32:52 GMT  
		Size: 44.6 MB (44631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b8dff630a77674c06491533b41967695401e58bad736fbfcf902fedc2206f`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:caddab0ba5406d19bcf97d051a5d84b9c48a90cecf3c5ccfe573300913f5b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ab89444ca88b71d7c3cb8684326b2b33f3798443241af36a27f2227b1be3a`

```dockerfile
```

-	Layers:
	-	`sha256:212e2939a6f92a43306023b844004cc0e62205dba1ae66d31211a5663d0aed15`  
		Last Modified: Thu, 09 Oct 2025 00:09:33 GMT  
		Size: 846.7 KB (846653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fa14d816df3e1c2cd4fda52ce5084605e3007790e128f0037f864dd067d0`  
		Last Modified: Thu, 09 Oct 2025 00:09:34 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:62139bf2068575a96511414601d747bbc381acef0d751b339f4537de689d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44713309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4abdfb90d5de05aa2fe4228dc79fa31757ad3bac4fd4112eb510215e269a76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07f1a83f5ca01436f1065b617a224df85b98f594db8406efb608986ed8d8a8`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127245637effe2cd5c0877929f6ffc01a251163b172e1ff06b222bebf9ef742`  
		Last Modified: Wed, 08 Oct 2025 22:10:12 GMT  
		Size: 40.8 MB (40751121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f87cacf0cabb971ea83173805a4269d07d1b895ef5f62d8320d0d85cd7c2cd`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c72988c31eec2887533432dd4ac2ff4f33d382baff1353fab242a9b40a14f2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacd1272261a03d3c7d5dd2cf48ce8df76029ada41f99c7751e1bcc5f48da1`

```dockerfile
```

-	Layers:
	-	`sha256:1cf126491ae9400b8bf590dbaba64f7e4d29c4301cef15fff2f31d547e392f46`  
		Last Modified: Thu, 09 Oct 2025 00:09:38 GMT  
		Size: 12.4 KB (12440 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b48ce8d73902c67f88b518b1c6aa6918cb0c0a6428f53f0154aaf4af873c106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb020d915e5655fae3f5060ff130a859abfe61a8ea91dfc1882124a58d14326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c35108c807e82173e970f056f3015e5dde837be289dc7933b119952bab0356`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e78658e7eb434fa7fc2370b328d875c80be35f21ab4ac93442933d4730264`  
		Last Modified: Wed, 08 Oct 2025 21:46:11 GMT  
		Size: 40.7 MB (40663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5828773411ee49f3139f8d2e872a67a4bbc6f3ee7d0dde4dcdd9773b5df89261`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95826936a7213958cbc0d613beaf3e52553d3f80a68e685fc080c210da374482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0692264a94ea4145625fe77fec8feec1bdf451afb44d08f99bb7254cd0bca`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf31304a3d9020b59a7079496b3e887e74bd8243877363c84b185aedeb9502`  
		Last Modified: Thu, 09 Oct 2025 00:09:41 GMT  
		Size: 846.7 KB (846745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569fe3b0553180e02df23f9edf125bc49b2dfd4909414931a3fe1b428e9b4ec7`  
		Last Modified: Thu, 09 Oct 2025 00:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:27943b61f4cf7adb5a28b1428560453f3b221eddd1deb5597d5f66332ea9c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43260058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d0596d25069522159ee5f920821861d6fd636198d6f4909101f698978d1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9cbf796b10af40c247e0fc393162e272fd215b8afd8f9d3d514d3a91517185a2`  
		Last Modified: Thu, 09 Oct 2025 03:34:45 GMT  
		Size: 39.1 MB (39068022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d76833d79bcdee65dfacae22941644722559def5053c666a883f455eadf31f`  
		Last Modified: Thu, 09 Oct 2025 03:34:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a4a72fedd5ff7b13144b419eea765496f66a0e5e6c4f7392bd072c078a0615ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f38d822278db3f44c54fec63a2742f2ae8dc73a26cef1c72981c47fcdc08c70`

```dockerfile
```

-	Layers:
	-	`sha256:594712ef1bc83669370cead772ace625fe91e672eaa185bd8b318da38e47d35d`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 844.8 KB (844754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91d3789db5b665f6928567682693790c06ec8c365ba809aa88b47267841d5ea`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:543d7213524ac3a5b766bac7f62d67eeb3cd197bdbd2f0f168f978495a4b7689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ade4693856965b5e4711fbb27e663f7c51961d42ce95b0e5dc8e96b4030ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:75dfb592752d754af1c64c7dbd9015a2af5414f1e27100b1c1c984ff061bcd65`  
		Last Modified: Thu, 09 Oct 2025 02:28:20 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b010b67dd8d171e9c420f9627ae7d9979a95e634d2079874e4c257f8ce4abc12`  
		Last Modified: Thu, 09 Oct 2025 02:28:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95f9d7b31c8f90b72c14ba6f425273db6204f76c41f6cecea61fbb508891ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.2 KB (857235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26cb7d048e0cdca0cebfa442468c96993718704c018f51f49cc78d9f1a852cb`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc98b90d01aa636ad8ad59bc0187c689a7e1066f306adc1712daab790480f3`  
		Last Modified: Thu, 09 Oct 2025 03:09:54 GMT  
		Size: 844.7 KB (844698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff43678d08ce6be10d3596b5376adc48089bef0e67225ad27117c6a95fe011d4`  
		Last Modified: Thu, 09 Oct 2025 03:09:55 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29`

```console
$ docker pull traefik@sha256:5856b2381dcbf5e6b0ca81881a3a63cf75b1554889fab5aec843328655bd0fe2
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

### `traefik:2.11.29` - linux; amd64

```console
$ docker pull traefik@sha256:10c68595a5716f05915f4d268f22da05168ac7ba6e397fd6be2a55c35463c55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48891106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f089b6d079e56196888f8ae298babc84919abed74e79b6a724cd8af6f426f11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace194ea058fa4d5892a892e1fd7b4b886f0408d98c61026f8977953a71f4d4c`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa864f1a2ba563e0af032c40b3c8e61269f4858eb8cdd7edadde3ab12ab419c`  
		Last Modified: Wed, 08 Oct 2025 23:32:52 GMT  
		Size: 44.6 MB (44631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b8dff630a77674c06491533b41967695401e58bad736fbfcf902fedc2206f`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:caddab0ba5406d19bcf97d051a5d84b9c48a90cecf3c5ccfe573300913f5b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ab89444ca88b71d7c3cb8684326b2b33f3798443241af36a27f2227b1be3a`

```dockerfile
```

-	Layers:
	-	`sha256:212e2939a6f92a43306023b844004cc0e62205dba1ae66d31211a5663d0aed15`  
		Last Modified: Thu, 09 Oct 2025 00:09:33 GMT  
		Size: 846.7 KB (846653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fa14d816df3e1c2cd4fda52ce5084605e3007790e128f0037f864dd067d0`  
		Last Modified: Thu, 09 Oct 2025 00:09:34 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; arm variant v6

```console
$ docker pull traefik@sha256:62139bf2068575a96511414601d747bbc381acef0d751b339f4537de689d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44713309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4abdfb90d5de05aa2fe4228dc79fa31757ad3bac4fd4112eb510215e269a76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07f1a83f5ca01436f1065b617a224df85b98f594db8406efb608986ed8d8a8`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127245637effe2cd5c0877929f6ffc01a251163b172e1ff06b222bebf9ef742`  
		Last Modified: Wed, 08 Oct 2025 22:10:12 GMT  
		Size: 40.8 MB (40751121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f87cacf0cabb971ea83173805a4269d07d1b895ef5f62d8320d0d85cd7c2cd`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:c72988c31eec2887533432dd4ac2ff4f33d382baff1353fab242a9b40a14f2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacd1272261a03d3c7d5dd2cf48ce8df76029ada41f99c7751e1bcc5f48da1`

```dockerfile
```

-	Layers:
	-	`sha256:1cf126491ae9400b8bf590dbaba64f7e4d29c4301cef15fff2f31d547e392f46`  
		Last Modified: Thu, 09 Oct 2025 00:09:38 GMT  
		Size: 12.4 KB (12440 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b48ce8d73902c67f88b518b1c6aa6918cb0c0a6428f53f0154aaf4af873c106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb020d915e5655fae3f5060ff130a859abfe61a8ea91dfc1882124a58d14326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c35108c807e82173e970f056f3015e5dde837be289dc7933b119952bab0356`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e78658e7eb434fa7fc2370b328d875c80be35f21ab4ac93442933d4730264`  
		Last Modified: Wed, 08 Oct 2025 21:46:11 GMT  
		Size: 40.7 MB (40663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5828773411ee49f3139f8d2e872a67a4bbc6f3ee7d0dde4dcdd9773b5df89261`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:95826936a7213958cbc0d613beaf3e52553d3f80a68e685fc080c210da374482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0692264a94ea4145625fe77fec8feec1bdf451afb44d08f99bb7254cd0bca`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf31304a3d9020b59a7079496b3e887e74bd8243877363c84b185aedeb9502`  
		Last Modified: Thu, 09 Oct 2025 00:09:41 GMT  
		Size: 846.7 KB (846745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569fe3b0553180e02df23f9edf125bc49b2dfd4909414931a3fe1b428e9b4ec7`  
		Last Modified: Thu, 09 Oct 2025 00:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; ppc64le

```console
$ docker pull traefik@sha256:27943b61f4cf7adb5a28b1428560453f3b221eddd1deb5597d5f66332ea9c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43260058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d0596d25069522159ee5f920821861d6fd636198d6f4909101f698978d1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9cbf796b10af40c247e0fc393162e272fd215b8afd8f9d3d514d3a91517185a2`  
		Last Modified: Thu, 09 Oct 2025 03:34:45 GMT  
		Size: 39.1 MB (39068022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d76833d79bcdee65dfacae22941644722559def5053c666a883f455eadf31f`  
		Last Modified: Thu, 09 Oct 2025 03:34:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:a4a72fedd5ff7b13144b419eea765496f66a0e5e6c4f7392bd072c078a0615ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f38d822278db3f44c54fec63a2742f2ae8dc73a26cef1c72981c47fcdc08c70`

```dockerfile
```

-	Layers:
	-	`sha256:594712ef1bc83669370cead772ace625fe91e672eaa185bd8b318da38e47d35d`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 844.8 KB (844754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91d3789db5b665f6928567682693790c06ec8c365ba809aa88b47267841d5ea`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; s390x

```console
$ docker pull traefik@sha256:543d7213524ac3a5b766bac7f62d67eeb3cd197bdbd2f0f168f978495a4b7689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ade4693856965b5e4711fbb27e663f7c51961d42ce95b0e5dc8e96b4030ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:75dfb592752d754af1c64c7dbd9015a2af5414f1e27100b1c1c984ff061bcd65`  
		Last Modified: Thu, 09 Oct 2025 02:28:20 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b010b67dd8d171e9c420f9627ae7d9979a95e634d2079874e4c257f8ce4abc12`  
		Last Modified: Thu, 09 Oct 2025 02:28:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:95f9d7b31c8f90b72c14ba6f425273db6204f76c41f6cecea61fbb508891ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.2 KB (857235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26cb7d048e0cdca0cebfa442468c96993718704c018f51f49cc78d9f1a852cb`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc98b90d01aa636ad8ad59bc0187c689a7e1066f306adc1712daab790480f3`  
		Last Modified: Thu, 09 Oct 2025 03:09:54 GMT  
		Size: 844.7 KB (844698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff43678d08ce6be10d3596b5376adc48089bef0e67225ad27117c6a95fe011d4`  
		Last Modified: Thu, 09 Oct 2025 03:09:55 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.29-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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

### `traefik:3.5` - linux; amd64

```console
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.3`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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

### `traefik:3.5.3` - linux; amd64

```console
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.5.3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5.3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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

### `traefik:chabichou` - linux; amd64

```console
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:chabichou-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:chabichou-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:5856b2381dcbf5e6b0ca81881a3a63cf75b1554889fab5aec843328655bd0fe2
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
$ docker pull traefik@sha256:10c68595a5716f05915f4d268f22da05168ac7ba6e397fd6be2a55c35463c55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48891106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f089b6d079e56196888f8ae298babc84919abed74e79b6a724cd8af6f426f11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace194ea058fa4d5892a892e1fd7b4b886f0408d98c61026f8977953a71f4d4c`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa864f1a2ba563e0af032c40b3c8e61269f4858eb8cdd7edadde3ab12ab419c`  
		Last Modified: Wed, 08 Oct 2025 23:32:52 GMT  
		Size: 44.6 MB (44631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b8dff630a77674c06491533b41967695401e58bad736fbfcf902fedc2206f`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:caddab0ba5406d19bcf97d051a5d84b9c48a90cecf3c5ccfe573300913f5b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ab89444ca88b71d7c3cb8684326b2b33f3798443241af36a27f2227b1be3a`

```dockerfile
```

-	Layers:
	-	`sha256:212e2939a6f92a43306023b844004cc0e62205dba1ae66d31211a5663d0aed15`  
		Last Modified: Thu, 09 Oct 2025 00:09:33 GMT  
		Size: 846.7 KB (846653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fa14d816df3e1c2cd4fda52ce5084605e3007790e128f0037f864dd067d0`  
		Last Modified: Thu, 09 Oct 2025 00:09:34 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:62139bf2068575a96511414601d747bbc381acef0d751b339f4537de689d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44713309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4abdfb90d5de05aa2fe4228dc79fa31757ad3bac4fd4112eb510215e269a76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07f1a83f5ca01436f1065b617a224df85b98f594db8406efb608986ed8d8a8`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127245637effe2cd5c0877929f6ffc01a251163b172e1ff06b222bebf9ef742`  
		Last Modified: Wed, 08 Oct 2025 22:10:12 GMT  
		Size: 40.8 MB (40751121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f87cacf0cabb971ea83173805a4269d07d1b895ef5f62d8320d0d85cd7c2cd`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c72988c31eec2887533432dd4ac2ff4f33d382baff1353fab242a9b40a14f2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacd1272261a03d3c7d5dd2cf48ce8df76029ada41f99c7751e1bcc5f48da1`

```dockerfile
```

-	Layers:
	-	`sha256:1cf126491ae9400b8bf590dbaba64f7e4d29c4301cef15fff2f31d547e392f46`  
		Last Modified: Thu, 09 Oct 2025 00:09:38 GMT  
		Size: 12.4 KB (12440 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b48ce8d73902c67f88b518b1c6aa6918cb0c0a6428f53f0154aaf4af873c106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb020d915e5655fae3f5060ff130a859abfe61a8ea91dfc1882124a58d14326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c35108c807e82173e970f056f3015e5dde837be289dc7933b119952bab0356`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e78658e7eb434fa7fc2370b328d875c80be35f21ab4ac93442933d4730264`  
		Last Modified: Wed, 08 Oct 2025 21:46:11 GMT  
		Size: 40.7 MB (40663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5828773411ee49f3139f8d2e872a67a4bbc6f3ee7d0dde4dcdd9773b5df89261`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:95826936a7213958cbc0d613beaf3e52553d3f80a68e685fc080c210da374482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0692264a94ea4145625fe77fec8feec1bdf451afb44d08f99bb7254cd0bca`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf31304a3d9020b59a7079496b3e887e74bd8243877363c84b185aedeb9502`  
		Last Modified: Thu, 09 Oct 2025 00:09:41 GMT  
		Size: 846.7 KB (846745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569fe3b0553180e02df23f9edf125bc49b2dfd4909414931a3fe1b428e9b4ec7`  
		Last Modified: Thu, 09 Oct 2025 00:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:27943b61f4cf7adb5a28b1428560453f3b221eddd1deb5597d5f66332ea9c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43260058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d0596d25069522159ee5f920821861d6fd636198d6f4909101f698978d1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9cbf796b10af40c247e0fc393162e272fd215b8afd8f9d3d514d3a91517185a2`  
		Last Modified: Thu, 09 Oct 2025 03:34:45 GMT  
		Size: 39.1 MB (39068022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d76833d79bcdee65dfacae22941644722559def5053c666a883f455eadf31f`  
		Last Modified: Thu, 09 Oct 2025 03:34:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a4a72fedd5ff7b13144b419eea765496f66a0e5e6c4f7392bd072c078a0615ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f38d822278db3f44c54fec63a2742f2ae8dc73a26cef1c72981c47fcdc08c70`

```dockerfile
```

-	Layers:
	-	`sha256:594712ef1bc83669370cead772ace625fe91e672eaa185bd8b318da38e47d35d`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 844.8 KB (844754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91d3789db5b665f6928567682693790c06ec8c365ba809aa88b47267841d5ea`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:543d7213524ac3a5b766bac7f62d67eeb3cd197bdbd2f0f168f978495a4b7689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ade4693856965b5e4711fbb27e663f7c51961d42ce95b0e5dc8e96b4030ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:75dfb592752d754af1c64c7dbd9015a2af5414f1e27100b1c1c984ff061bcd65`  
		Last Modified: Thu, 09 Oct 2025 02:28:20 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b010b67dd8d171e9c420f9627ae7d9979a95e634d2079874e4c257f8ce4abc12`  
		Last Modified: Thu, 09 Oct 2025 02:28:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:95f9d7b31c8f90b72c14ba6f425273db6204f76c41f6cecea61fbb508891ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.2 KB (857235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26cb7d048e0cdca0cebfa442468c96993718704c018f51f49cc78d9f1a852cb`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc98b90d01aa636ad8ad59bc0187c689a7e1066f306adc1712daab790480f3`  
		Last Modified: Thu, 09 Oct 2025 03:09:54 GMT  
		Size: 844.7 KB (844698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff43678d08ce6be10d3596b5376adc48089bef0e67225ad27117c6a95fe011d4`  
		Last Modified: Thu, 09 Oct 2025 03:09:55 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:5856b2381dcbf5e6b0ca81881a3a63cf75b1554889fab5aec843328655bd0fe2
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
$ docker pull traefik@sha256:10c68595a5716f05915f4d268f22da05168ac7ba6e397fd6be2a55c35463c55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48891106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f089b6d079e56196888f8ae298babc84919abed74e79b6a724cd8af6f426f11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace194ea058fa4d5892a892e1fd7b4b886f0408d98c61026f8977953a71f4d4c`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa864f1a2ba563e0af032c40b3c8e61269f4858eb8cdd7edadde3ab12ab419c`  
		Last Modified: Wed, 08 Oct 2025 23:32:52 GMT  
		Size: 44.6 MB (44631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b8dff630a77674c06491533b41967695401e58bad736fbfcf902fedc2206f`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:caddab0ba5406d19bcf97d051a5d84b9c48a90cecf3c5ccfe573300913f5b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ab89444ca88b71d7c3cb8684326b2b33f3798443241af36a27f2227b1be3a`

```dockerfile
```

-	Layers:
	-	`sha256:212e2939a6f92a43306023b844004cc0e62205dba1ae66d31211a5663d0aed15`  
		Last Modified: Thu, 09 Oct 2025 00:09:33 GMT  
		Size: 846.7 KB (846653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fa14d816df3e1c2cd4fda52ce5084605e3007790e128f0037f864dd067d0`  
		Last Modified: Thu, 09 Oct 2025 00:09:34 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:62139bf2068575a96511414601d747bbc381acef0d751b339f4537de689d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44713309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4abdfb90d5de05aa2fe4228dc79fa31757ad3bac4fd4112eb510215e269a76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07f1a83f5ca01436f1065b617a224df85b98f594db8406efb608986ed8d8a8`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127245637effe2cd5c0877929f6ffc01a251163b172e1ff06b222bebf9ef742`  
		Last Modified: Wed, 08 Oct 2025 22:10:12 GMT  
		Size: 40.8 MB (40751121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f87cacf0cabb971ea83173805a4269d07d1b895ef5f62d8320d0d85cd7c2cd`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c72988c31eec2887533432dd4ac2ff4f33d382baff1353fab242a9b40a14f2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacd1272261a03d3c7d5dd2cf48ce8df76029ada41f99c7751e1bcc5f48da1`

```dockerfile
```

-	Layers:
	-	`sha256:1cf126491ae9400b8bf590dbaba64f7e4d29c4301cef15fff2f31d547e392f46`  
		Last Modified: Thu, 09 Oct 2025 00:09:38 GMT  
		Size: 12.4 KB (12440 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b48ce8d73902c67f88b518b1c6aa6918cb0c0a6428f53f0154aaf4af873c106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb020d915e5655fae3f5060ff130a859abfe61a8ea91dfc1882124a58d14326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c35108c807e82173e970f056f3015e5dde837be289dc7933b119952bab0356`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e78658e7eb434fa7fc2370b328d875c80be35f21ab4ac93442933d4730264`  
		Last Modified: Wed, 08 Oct 2025 21:46:11 GMT  
		Size: 40.7 MB (40663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5828773411ee49f3139f8d2e872a67a4bbc6f3ee7d0dde4dcdd9773b5df89261`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:95826936a7213958cbc0d613beaf3e52553d3f80a68e685fc080c210da374482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0692264a94ea4145625fe77fec8feec1bdf451afb44d08f99bb7254cd0bca`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf31304a3d9020b59a7079496b3e887e74bd8243877363c84b185aedeb9502`  
		Last Modified: Thu, 09 Oct 2025 00:09:41 GMT  
		Size: 846.7 KB (846745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569fe3b0553180e02df23f9edf125bc49b2dfd4909414931a3fe1b428e9b4ec7`  
		Last Modified: Thu, 09 Oct 2025 00:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:27943b61f4cf7adb5a28b1428560453f3b221eddd1deb5597d5f66332ea9c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43260058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d0596d25069522159ee5f920821861d6fd636198d6f4909101f698978d1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9cbf796b10af40c247e0fc393162e272fd215b8afd8f9d3d514d3a91517185a2`  
		Last Modified: Thu, 09 Oct 2025 03:34:45 GMT  
		Size: 39.1 MB (39068022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d76833d79bcdee65dfacae22941644722559def5053c666a883f455eadf31f`  
		Last Modified: Thu, 09 Oct 2025 03:34:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a4a72fedd5ff7b13144b419eea765496f66a0e5e6c4f7392bd072c078a0615ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f38d822278db3f44c54fec63a2742f2ae8dc73a26cef1c72981c47fcdc08c70`

```dockerfile
```

-	Layers:
	-	`sha256:594712ef1bc83669370cead772ace625fe91e672eaa185bd8b318da38e47d35d`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 844.8 KB (844754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91d3789db5b665f6928567682693790c06ec8c365ba809aa88b47267841d5ea`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:543d7213524ac3a5b766bac7f62d67eeb3cd197bdbd2f0f168f978495a4b7689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ade4693856965b5e4711fbb27e663f7c51961d42ce95b0e5dc8e96b4030ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:75dfb592752d754af1c64c7dbd9015a2af5414f1e27100b1c1c984ff061bcd65`  
		Last Modified: Thu, 09 Oct 2025 02:28:20 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b010b67dd8d171e9c420f9627ae7d9979a95e634d2079874e4c257f8ce4abc12`  
		Last Modified: Thu, 09 Oct 2025 02:28:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:95f9d7b31c8f90b72c14ba6f425273db6204f76c41f6cecea61fbb508891ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.2 KB (857235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26cb7d048e0cdca0cebfa442468c96993718704c018f51f49cc78d9f1a852cb`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc98b90d01aa636ad8ad59bc0187c689a7e1066f306adc1712daab790480f3`  
		Last Modified: Thu, 09 Oct 2025 03:09:54 GMT  
		Size: 844.7 KB (844698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff43678d08ce6be10d3596b5376adc48089bef0e67225ad27117c6a95fe011d4`  
		Last Modified: Thu, 09 Oct 2025 03:09:55 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:5856b2381dcbf5e6b0ca81881a3a63cf75b1554889fab5aec843328655bd0fe2
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
$ docker pull traefik@sha256:10c68595a5716f05915f4d268f22da05168ac7ba6e397fd6be2a55c35463c55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48891106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f089b6d079e56196888f8ae298babc84919abed74e79b6a724cd8af6f426f11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace194ea058fa4d5892a892e1fd7b4b886f0408d98c61026f8977953a71f4d4c`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa864f1a2ba563e0af032c40b3c8e61269f4858eb8cdd7edadde3ab12ab419c`  
		Last Modified: Wed, 08 Oct 2025 23:32:52 GMT  
		Size: 44.6 MB (44631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b8dff630a77674c06491533b41967695401e58bad736fbfcf902fedc2206f`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:caddab0ba5406d19bcf97d051a5d84b9c48a90cecf3c5ccfe573300913f5b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ab89444ca88b71d7c3cb8684326b2b33f3798443241af36a27f2227b1be3a`

```dockerfile
```

-	Layers:
	-	`sha256:212e2939a6f92a43306023b844004cc0e62205dba1ae66d31211a5663d0aed15`  
		Last Modified: Thu, 09 Oct 2025 00:09:33 GMT  
		Size: 846.7 KB (846653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fa14d816df3e1c2cd4fda52ce5084605e3007790e128f0037f864dd067d0`  
		Last Modified: Thu, 09 Oct 2025 00:09:34 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:62139bf2068575a96511414601d747bbc381acef0d751b339f4537de689d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44713309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4abdfb90d5de05aa2fe4228dc79fa31757ad3bac4fd4112eb510215e269a76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07f1a83f5ca01436f1065b617a224df85b98f594db8406efb608986ed8d8a8`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127245637effe2cd5c0877929f6ffc01a251163b172e1ff06b222bebf9ef742`  
		Last Modified: Wed, 08 Oct 2025 22:10:12 GMT  
		Size: 40.8 MB (40751121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f87cacf0cabb971ea83173805a4269d07d1b895ef5f62d8320d0d85cd7c2cd`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c72988c31eec2887533432dd4ac2ff4f33d382baff1353fab242a9b40a14f2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacd1272261a03d3c7d5dd2cf48ce8df76029ada41f99c7751e1bcc5f48da1`

```dockerfile
```

-	Layers:
	-	`sha256:1cf126491ae9400b8bf590dbaba64f7e4d29c4301cef15fff2f31d547e392f46`  
		Last Modified: Thu, 09 Oct 2025 00:09:38 GMT  
		Size: 12.4 KB (12440 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b48ce8d73902c67f88b518b1c6aa6918cb0c0a6428f53f0154aaf4af873c106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb020d915e5655fae3f5060ff130a859abfe61a8ea91dfc1882124a58d14326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c35108c807e82173e970f056f3015e5dde837be289dc7933b119952bab0356`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e78658e7eb434fa7fc2370b328d875c80be35f21ab4ac93442933d4730264`  
		Last Modified: Wed, 08 Oct 2025 21:46:11 GMT  
		Size: 40.7 MB (40663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5828773411ee49f3139f8d2e872a67a4bbc6f3ee7d0dde4dcdd9773b5df89261`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95826936a7213958cbc0d613beaf3e52553d3f80a68e685fc080c210da374482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0692264a94ea4145625fe77fec8feec1bdf451afb44d08f99bb7254cd0bca`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf31304a3d9020b59a7079496b3e887e74bd8243877363c84b185aedeb9502`  
		Last Modified: Thu, 09 Oct 2025 00:09:41 GMT  
		Size: 846.7 KB (846745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569fe3b0553180e02df23f9edf125bc49b2dfd4909414931a3fe1b428e9b4ec7`  
		Last Modified: Thu, 09 Oct 2025 00:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:27943b61f4cf7adb5a28b1428560453f3b221eddd1deb5597d5f66332ea9c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43260058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d0596d25069522159ee5f920821861d6fd636198d6f4909101f698978d1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9cbf796b10af40c247e0fc393162e272fd215b8afd8f9d3d514d3a91517185a2`  
		Last Modified: Thu, 09 Oct 2025 03:34:45 GMT  
		Size: 39.1 MB (39068022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d76833d79bcdee65dfacae22941644722559def5053c666a883f455eadf31f`  
		Last Modified: Thu, 09 Oct 2025 03:34:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a4a72fedd5ff7b13144b419eea765496f66a0e5e6c4f7392bd072c078a0615ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f38d822278db3f44c54fec63a2742f2ae8dc73a26cef1c72981c47fcdc08c70`

```dockerfile
```

-	Layers:
	-	`sha256:594712ef1bc83669370cead772ace625fe91e672eaa185bd8b318da38e47d35d`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 844.8 KB (844754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91d3789db5b665f6928567682693790c06ec8c365ba809aa88b47267841d5ea`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:543d7213524ac3a5b766bac7f62d67eeb3cd197bdbd2f0f168f978495a4b7689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ade4693856965b5e4711fbb27e663f7c51961d42ce95b0e5dc8e96b4030ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:75dfb592752d754af1c64c7dbd9015a2af5414f1e27100b1c1c984ff061bcd65`  
		Last Modified: Thu, 09 Oct 2025 02:28:20 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b010b67dd8d171e9c420f9627ae7d9979a95e634d2079874e4c257f8ce4abc12`  
		Last Modified: Thu, 09 Oct 2025 02:28:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:95f9d7b31c8f90b72c14ba6f425273db6204f76c41f6cecea61fbb508891ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.2 KB (857235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26cb7d048e0cdca0cebfa442468c96993718704c018f51f49cc78d9f1a852cb`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc98b90d01aa636ad8ad59bc0187c689a7e1066f306adc1712daab790480f3`  
		Last Modified: Thu, 09 Oct 2025 03:09:54 GMT  
		Size: 844.7 KB (844698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff43678d08ce6be10d3596b5376adc48089bef0e67225ad27117c6a95fe011d4`  
		Last Modified: Thu, 09 Oct 2025 03:09:55 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29`

```console
$ docker pull traefik@sha256:5856b2381dcbf5e6b0ca81881a3a63cf75b1554889fab5aec843328655bd0fe2
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

### `traefik:v2.11.29` - linux; amd64

```console
$ docker pull traefik@sha256:10c68595a5716f05915f4d268f22da05168ac7ba6e397fd6be2a55c35463c55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48891106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f089b6d079e56196888f8ae298babc84919abed74e79b6a724cd8af6f426f11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace194ea058fa4d5892a892e1fd7b4b886f0408d98c61026f8977953a71f4d4c`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 456.9 KB (456923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa864f1a2ba563e0af032c40b3c8e61269f4858eb8cdd7edadde3ab12ab419c`  
		Last Modified: Wed, 08 Oct 2025 23:32:52 GMT  
		Size: 44.6 MB (44631362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7b8dff630a77674c06491533b41967695401e58bad736fbfcf902fedc2206f`  
		Last Modified: Wed, 08 Oct 2025 23:32:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:caddab0ba5406d19bcf97d051a5d84b9c48a90cecf3c5ccfe573300913f5b8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.2 KB (859191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463ab89444ca88b71d7c3cb8684326b2b33f3798443241af36a27f2227b1be3a`

```dockerfile
```

-	Layers:
	-	`sha256:212e2939a6f92a43306023b844004cc0e62205dba1ae66d31211a5663d0aed15`  
		Last Modified: Thu, 09 Oct 2025 00:09:33 GMT  
		Size: 846.7 KB (846653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a187fa14d816df3e1c2cd4fda52ce5084605e3007790e128f0037f864dd067d0`  
		Last Modified: Thu, 09 Oct 2025 00:09:34 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; arm variant v6

```console
$ docker pull traefik@sha256:62139bf2068575a96511414601d747bbc381acef0d751b339f4537de689d955c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44713309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4abdfb90d5de05aa2fe4228dc79fa31757ad3bac4fd4112eb510215e269a76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07f1a83f5ca01436f1065b617a224df85b98f594db8406efb608986ed8d8a8`  
		Last Modified: Wed, 08 Oct 2025 22:10:06 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127245637effe2cd5c0877929f6ffc01a251163b172e1ff06b222bebf9ef742`  
		Last Modified: Wed, 08 Oct 2025 22:10:12 GMT  
		Size: 40.8 MB (40751121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f87cacf0cabb971ea83173805a4269d07d1b895ef5f62d8320d0d85cd7c2cd`  
		Last Modified: Wed, 08 Oct 2025 22:10:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:c72988c31eec2887533432dd4ac2ff4f33d382baff1353fab242a9b40a14f2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacd1272261a03d3c7d5dd2cf48ce8df76029ada41f99c7751e1bcc5f48da1`

```dockerfile
```

-	Layers:
	-	`sha256:1cf126491ae9400b8bf590dbaba64f7e4d29c4301cef15fff2f31d547e392f46`  
		Last Modified: Thu, 09 Oct 2025 00:09:38 GMT  
		Size: 12.4 KB (12440 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:b48ce8d73902c67f88b518b1c6aa6918cb0c0a6428f53f0154aaf4af873c106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45260578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb020d915e5655fae3f5060ff130a859abfe61a8ea91dfc1882124a58d14326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c35108c807e82173e970f056f3015e5dde837be289dc7933b119952bab0356`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e78658e7eb434fa7fc2370b328d875c80be35f21ab4ac93442933d4730264`  
		Last Modified: Wed, 08 Oct 2025 21:46:11 GMT  
		Size: 40.7 MB (40663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5828773411ee49f3139f8d2e872a67a4bbc6f3ee7d0dde4dcdd9773b5df89261`  
		Last Modified: Wed, 08 Oct 2025 21:46:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:95826936a7213958cbc0d613beaf3e52553d3f80a68e685fc080c210da374482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **859.4 KB (859438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e0692264a94ea4145625fe77fec8feec1bdf451afb44d08f99bb7254cd0bca`

```dockerfile
```

-	Layers:
	-	`sha256:8dcf31304a3d9020b59a7079496b3e887e74bd8243877363c84b185aedeb9502`  
		Last Modified: Thu, 09 Oct 2025 00:09:41 GMT  
		Size: 846.7 KB (846745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569fe3b0553180e02df23f9edf125bc49b2dfd4909414931a3fe1b428e9b4ec7`  
		Last Modified: Thu, 09 Oct 2025 00:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; ppc64le

```console
$ docker pull traefik@sha256:27943b61f4cf7adb5a28b1428560453f3b221eddd1deb5597d5f66332ea9c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43260058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d0596d25069522159ee5f920821861d6fd636198d6f4909101f698978d1f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9cbf796b10af40c247e0fc393162e272fd215b8afd8f9d3d514d3a91517185a2`  
		Last Modified: Thu, 09 Oct 2025 03:34:45 GMT  
		Size: 39.1 MB (39068022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d76833d79bcdee65dfacae22941644722559def5053c666a883f455eadf31f`  
		Last Modified: Thu, 09 Oct 2025 03:34:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:a4a72fedd5ff7b13144b419eea765496f66a0e5e6c4f7392bd072c078a0615ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f38d822278db3f44c54fec63a2742f2ae8dc73a26cef1c72981c47fcdc08c70`

```dockerfile
```

-	Layers:
	-	`sha256:594712ef1bc83669370cead772ace625fe91e672eaa185bd8b318da38e47d35d`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 844.8 KB (844754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91d3789db5b665f6928567682693790c06ec8c365ba809aa88b47267841d5ea`  
		Last Modified: Thu, 09 Oct 2025 06:09:38 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; s390x

```console
$ docker pull traefik@sha256:543d7213524ac3a5b766bac7f62d67eeb3cd197bdbd2f0f168f978495a4b7689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47359458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ade4693856965b5e4711fbb27e663f7c51961d42ce95b0e5dc8e96b4030ff1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:75dfb592752d754af1c64c7dbd9015a2af5414f1e27100b1c1c984ff061bcd65`  
		Last Modified: Thu, 09 Oct 2025 02:28:20 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b010b67dd8d171e9c420f9627ae7d9979a95e634d2079874e4c257f8ce4abc12`  
		Last Modified: Thu, 09 Oct 2025 02:28:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:95f9d7b31c8f90b72c14ba6f425273db6204f76c41f6cecea61fbb508891ddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.2 KB (857235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26cb7d048e0cdca0cebfa442468c96993718704c018f51f49cc78d9f1a852cb`

```dockerfile
```

-	Layers:
	-	`sha256:1cfc98b90d01aa636ad8ad59bc0187c689a7e1066f306adc1712daab790480f3`  
		Last Modified: Thu, 09 Oct 2025 03:09:54 GMT  
		Size: 844.7 KB (844698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff43678d08ce6be10d3596b5376adc48089bef0e67225ad27117c6a95fe011d4`  
		Last Modified: Thu, 09 Oct 2025 03:09:55 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.29-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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

### `traefik:v3.5` - linux; amd64

```console
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.3`

```console
$ docker pull traefik@sha256:76ac93e6ff8c749c9b68e31698e93d3af38c6a6d10a6b989eeef97bf0b9887f8
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

### `traefik:v3.5.3` - linux; amd64

```console
$ docker pull traefik@sha256:c8bcb479c8057a29b05b1f3a5dcfb580fa67bc6adc41e48eabb168512c6a8c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49716109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14917e96c7b0b37131205ca71d9093f78a6cfd8a27e646b313ab56682f9a8f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bd0179750832e9de97b0bac2c192cc2aac92d69311b90e432bb29c37c1298`  
		Last Modified: Wed, 08 Oct 2025 22:58:25 GMT  
		Size: 456.9 KB (456931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4fbf871756efcb092111e7946dc1bbbdf030ea64c516f1cccfe7e772b715e`  
		Last Modified: Wed, 08 Oct 2025 22:58:29 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787b8e1b941cb587cbf08cdf29c385157166e21d37cf668d4b56cbc91642f799`  
		Last Modified: Wed, 08 Oct 2025 22:58:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5b4132eae9b80ba12a41844dcfc3b66c69ac45dff5b9e326c6925d51db47dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07450bfea175729ad964e8769c503f32e5293a0b7677a513abe8e4d277fbbc7e`

```dockerfile
```

-	Layers:
	-	`sha256:5e130619b49b7bea032b20657be97af5874372a4a96db1bbb7daa21f5f4cb804`  
		Last Modified: Thu, 09 Oct 2025 00:09:51 GMT  
		Size: 832.5 KB (832528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454e9247bee7930c12c6577fe31b6d37ad010e6d02ef14c2aeae701604b630ae`  
		Last Modified: Thu, 09 Oct 2025 00:09:52 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:bf75588f33488c4cc243964fb1b67210dd404a4e886fc792c52b399365eabc31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45184463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef92b3c92a6da0d39e60b89b88b4d780191a2c650b24a3723a27dfd727e61337`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869385d7119069c74bbfbe63b503bb726b0b3986076fb543301c4ad7e297443`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95f2a38018606192d6fc71eff8c393365bbba883843a1486078354a1f8060d6`  
		Last Modified: Wed, 08 Oct 2025 22:10:09 GMT  
		Size: 41.2 MB (41222269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c0690641ab41dbe76d29a30e41d14c0a28dc2ff8bd479afe7be302a3e44cc`  
		Last Modified: Wed, 08 Oct 2025 22:10:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:eb05c706a69710ed8d23ce58d355019e5bc5b4e06c262e6c35495535f23b9fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedd7f847b2f814318dfe6ca7f1c9ee025651a5bf329af4c9131b782d79a849`

```dockerfile
```

-	Layers:
	-	`sha256:b772db1f54ff9967cc2fd2af95f0134adac505a5b147113d572c74456db815b9`  
		Last Modified: Thu, 09 Oct 2025 00:09:55 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:bf34d2e927fe9d597b16923ae8e02ae8a03e551b506d9156947839c4a51364e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1ebb00fd8580bde9307a7a5770b331235d4febfd4ac074fb065a8d63eea8b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1125d4f30d7169bf0b30f923c7790c6186cd0538ab745a66d65e270d6d99eeb0`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 459.0 KB (459009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87081c37c56560398697106435ec570586660952c459611bf7f5bc3c18b8199a`  
		Last Modified: Wed, 08 Oct 2025 21:46:19 GMT  
		Size: 41.4 MB (41381100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654569a9ab029105fbddae97e5d19452e765c3452153a7fcc0d0507edeceb2c`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:903c02e7c353d5f0c8cfae486f424b15398a3fec2b0fa6e7de9c2e8a7da65976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.6 KB (845609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8cde3914b44e301264e0e27c00ff499f30b8ddc870c9000fbe43ecb78a525b`

```dockerfile
```

-	Layers:
	-	`sha256:5040026c4e1987267e0059d6b4780b7fd3892e73d4caf6a5cbef13bd908955b3`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 832.6 KB (832632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa9e46bfc2b7751e7c5c3e2c7f49012294fd2b8c5b2aeda1a2327086a811e16`  
		Last Modified: Thu, 09 Oct 2025 00:09:59 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; ppc64le

```console
$ docker pull traefik@sha256:b1fa6e84ec23d7dcf2b28da8c955eba32244fcf7cfc132e7697cf973c40a4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43638246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a537b543e3cd8f3019f6494e25e75d16634e3706bf477485b38c4d76b48e60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a36497d8a28bc91245a70bb25feddaec17391f2c509649ab447fb88c8d63224a`  
		Last Modified: Thu, 09 Oct 2025 03:33:25 GMT  
		Size: 39.4 MB (39446209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eb8adcabf277380b63dc1490c1be2a52bd0a3be7229104726be4902e230a2f`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:7003af7d2325ad02a4485d0c28c809f581121f225ff0f538c28b75fe11b74260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bee0f53011f70f40b06023e3e2340ba21762c0a67ddfa267b0b47af3cb1577f`

```dockerfile
```

-	Layers:
	-	`sha256:f3b8e2a37d993945f9a7d3698aa1e1d61c3bde1da11cc5e5195833e6f088df5a`  
		Last Modified: Thu, 09 Oct 2025 06:09:52 GMT  
		Size: 830.6 KB (830635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1f307c74c425de33fe21a5cdf011e0fa7f3ee96442396e2f0f9a103d31357`  
		Last Modified: Thu, 09 Oct 2025 06:09:53 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; s390x

```console
$ docker pull traefik@sha256:76eef4c4ee493ff4f2f6e8c1589e9bee463d97edac18a2714dd206d6a6f93ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47762061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b55631f8c8fb2ca753a17b15aa64ad63c8bfb43551f5c6f59027b210ce6f63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5f642442ff1303190ae0f27194f279b9d2d9d7fcb6fdb558b86bd91ddc6ce95b`  
		Last Modified: Thu, 09 Oct 2025 02:27:14 GMT  
		Size: 43.7 MB (43654543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ea1e119a867b4e74ba44a3a7d3a8b738f50b97a51047efe7afc353658dd0`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:92e774666e65ee5ab2a77f2485d3002c4706377f75e0bd3d3f9cf7ab4cb22c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f57e5a76956fb80c51fc8e7eef412e89c4a648794f640130e57ff0ee8872d`

```dockerfile
```

-	Layers:
	-	`sha256:be9720d0019d02b61df9e393288130d4f95c5ca66c4cc4467d4bef0f80411b7c`  
		Last Modified: Thu, 09 Oct 2025 03:10:04 GMT  
		Size: 830.6 KB (830577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1ff995839dfd509296629c05eea8f3b49014b508816e951ee10065775a2c5`  
		Last Modified: Thu, 09 Oct 2025 03:10:05 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.5.3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5.3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
