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
$ docker pull traefik@sha256:20be0efb184e9ef56927aa52c3c4b14783314d0da1515a15796e60877399dc2a
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
$ docker pull traefik@sha256:5ca4c5b63ac0826c920e1fc00a5a7fc09e6e43fe3eecad9cfa545237da6f5847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47287831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c32b60cc476b8576b66d8909e400eca182ccd954b65f14112cfe4b53cb535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c1fd8b4550f4e38f53b4f321cb2fa01a695e628e22541d9fb69ed42fb157d`  
		Last Modified: Fri, 10 Oct 2025 21:01:33 GMT  
		Size: 43.3 MB (43314949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a87fa5a1beb0c774120d8b856366a5abaef23842d2dd736c1b469ece4c99c`  
		Last Modified: Fri, 10 Oct 2025 21:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:a046244b3f26e51541875e367e773a04e1b51f2fe1cc52c288a30396a2380edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919502ae56c96821c85607970e18002499a7c99ce110bebb77a4aa1f7cc7c2e`

```dockerfile
```

-	Layers:
	-	`sha256:b2397c9011c10606a3b2354959c77a2310245c0845622cc490aed8e58668033f`  
		Last Modified: Fri, 10 Oct 2025 21:09:56 GMT  
		Size: 844.8 KB (844750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206958e24603f7f124045eca2ab6c435e14db0257c1c5381c4d9f981e39df024`  
		Last Modified: Fri, 10 Oct 2025 21:09:57 GMT  
		Size: 12.6 KB (12602 bytes)  
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
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8b12138c7587583ad978f6e20dcd02c1b2f07e5be8cad0fd7406879f192b4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8a101f10b24acaa0e23c0c867b63ff273e59b4edce6509fa63ab928aab09913a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1623232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80aeb67a00b1afba5df925e0c8aba1b3e1e39b54f306b20dfe0d536b51e6fb46`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:36 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:36 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8fc9685f839dd92c4d1d53b23867b093485643ea9d6826fee7e8edee0d6850`  
		Last Modified: Fri, 24 Oct 2025 18:22:24 GMT  
		Size: 46.0 MB (46034220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de74a6848534cdf597c00ebf1ee0751bb2f89354551331ef83971fdc68905d`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18b13e03b88056baaadae568b0d426138a4633e536238ea7b1f08c4455db6c`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61856ba4e0382718973ce3c7e57203b52e5832f0a50fdd368934569b774e87c8`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:20be0efb184e9ef56927aa52c3c4b14783314d0da1515a15796e60877399dc2a
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
$ docker pull traefik@sha256:5ca4c5b63ac0826c920e1fc00a5a7fc09e6e43fe3eecad9cfa545237da6f5847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47287831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c32b60cc476b8576b66d8909e400eca182ccd954b65f14112cfe4b53cb535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c1fd8b4550f4e38f53b4f321cb2fa01a695e628e22541d9fb69ed42fb157d`  
		Last Modified: Fri, 10 Oct 2025 21:01:33 GMT  
		Size: 43.3 MB (43314949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a87fa5a1beb0c774120d8b856366a5abaef23842d2dd736c1b469ece4c99c`  
		Last Modified: Fri, 10 Oct 2025 21:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a046244b3f26e51541875e367e773a04e1b51f2fe1cc52c288a30396a2380edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919502ae56c96821c85607970e18002499a7c99ce110bebb77a4aa1f7cc7c2e`

```dockerfile
```

-	Layers:
	-	`sha256:b2397c9011c10606a3b2354959c77a2310245c0845622cc490aed8e58668033f`  
		Last Modified: Fri, 10 Oct 2025 21:09:56 GMT  
		Size: 844.8 KB (844750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206958e24603f7f124045eca2ab6c435e14db0257c1c5381c4d9f981e39df024`  
		Last Modified: Fri, 10 Oct 2025 21:09:57 GMT  
		Size: 12.6 KB (12602 bytes)  
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
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8b12138c7587583ad978f6e20dcd02c1b2f07e5be8cad0fd7406879f192b4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8a101f10b24acaa0e23c0c867b63ff273e59b4edce6509fa63ab928aab09913a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1623232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80aeb67a00b1afba5df925e0c8aba1b3e1e39b54f306b20dfe0d536b51e6fb46`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:36 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:36 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8fc9685f839dd92c4d1d53b23867b093485643ea9d6826fee7e8edee0d6850`  
		Last Modified: Fri, 24 Oct 2025 18:22:24 GMT  
		Size: 46.0 MB (46034220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de74a6848534cdf597c00ebf1ee0751bb2f89354551331ef83971fdc68905d`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18b13e03b88056baaadae568b0d426138a4633e536238ea7b1f08c4455db6c`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61856ba4e0382718973ce3c7e57203b52e5832f0a50fdd368934569b774e87c8`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29`

```console
$ docker pull traefik@sha256:20be0efb184e9ef56927aa52c3c4b14783314d0da1515a15796e60877399dc2a
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
$ docker pull traefik@sha256:5ca4c5b63ac0826c920e1fc00a5a7fc09e6e43fe3eecad9cfa545237da6f5847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47287831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c32b60cc476b8576b66d8909e400eca182ccd954b65f14112cfe4b53cb535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c1fd8b4550f4e38f53b4f321cb2fa01a695e628e22541d9fb69ed42fb157d`  
		Last Modified: Fri, 10 Oct 2025 21:01:33 GMT  
		Size: 43.3 MB (43314949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a87fa5a1beb0c774120d8b856366a5abaef23842d2dd736c1b469ece4c99c`  
		Last Modified: Fri, 10 Oct 2025 21:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:a046244b3f26e51541875e367e773a04e1b51f2fe1cc52c288a30396a2380edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919502ae56c96821c85607970e18002499a7c99ce110bebb77a4aa1f7cc7c2e`

```dockerfile
```

-	Layers:
	-	`sha256:b2397c9011c10606a3b2354959c77a2310245c0845622cc490aed8e58668033f`  
		Last Modified: Fri, 10 Oct 2025 21:09:56 GMT  
		Size: 844.8 KB (844750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206958e24603f7f124045eca2ab6c435e14db0257c1c5381c4d9f981e39df024`  
		Last Modified: Fri, 10 Oct 2025 21:09:57 GMT  
		Size: 12.6 KB (12602 bytes)  
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
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8b12138c7587583ad978f6e20dcd02c1b2f07e5be8cad0fd7406879f192b4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8a101f10b24acaa0e23c0c867b63ff273e59b4edce6509fa63ab928aab09913a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1623232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80aeb67a00b1afba5df925e0c8aba1b3e1e39b54f306b20dfe0d536b51e6fb46`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:36 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:36 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8fc9685f839dd92c4d1d53b23867b093485643ea9d6826fee7e8edee0d6850`  
		Last Modified: Fri, 24 Oct 2025 18:22:24 GMT  
		Size: 46.0 MB (46034220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de74a6848534cdf597c00ebf1ee0751bb2f89354551331ef83971fdc68905d`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18b13e03b88056baaadae568b0d426138a4633e536238ea7b1f08c4455db6c`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61856ba4e0382718973ce3c7e57203b52e5832f0a50fdd368934569b774e87c8`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.3`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:3.5.3-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:3.5.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:chabichou-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:20be0efb184e9ef56927aa52c3c4b14783314d0da1515a15796e60877399dc2a
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
$ docker pull traefik@sha256:5ca4c5b63ac0826c920e1fc00a5a7fc09e6e43fe3eecad9cfa545237da6f5847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47287831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c32b60cc476b8576b66d8909e400eca182ccd954b65f14112cfe4b53cb535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c1fd8b4550f4e38f53b4f321cb2fa01a695e628e22541d9fb69ed42fb157d`  
		Last Modified: Fri, 10 Oct 2025 21:01:33 GMT  
		Size: 43.3 MB (43314949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a87fa5a1beb0c774120d8b856366a5abaef23842d2dd736c1b469ece4c99c`  
		Last Modified: Fri, 10 Oct 2025 21:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:a046244b3f26e51541875e367e773a04e1b51f2fe1cc52c288a30396a2380edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919502ae56c96821c85607970e18002499a7c99ce110bebb77a4aa1f7cc7c2e`

```dockerfile
```

-	Layers:
	-	`sha256:b2397c9011c10606a3b2354959c77a2310245c0845622cc490aed8e58668033f`  
		Last Modified: Fri, 10 Oct 2025 21:09:56 GMT  
		Size: 844.8 KB (844750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206958e24603f7f124045eca2ab6c435e14db0257c1c5381c4d9f981e39df024`  
		Last Modified: Fri, 10 Oct 2025 21:09:57 GMT  
		Size: 12.6 KB (12602 bytes)  
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
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8b12138c7587583ad978f6e20dcd02c1b2f07e5be8cad0fd7406879f192b4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8a101f10b24acaa0e23c0c867b63ff273e59b4edce6509fa63ab928aab09913a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1623232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80aeb67a00b1afba5df925e0c8aba1b3e1e39b54f306b20dfe0d536b51e6fb46`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:36 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:36 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8fc9685f839dd92c4d1d53b23867b093485643ea9d6826fee7e8edee0d6850`  
		Last Modified: Fri, 24 Oct 2025 18:22:24 GMT  
		Size: 46.0 MB (46034220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de74a6848534cdf597c00ebf1ee0751bb2f89354551331ef83971fdc68905d`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18b13e03b88056baaadae568b0d426138a4633e536238ea7b1f08c4455db6c`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61856ba4e0382718973ce3c7e57203b52e5832f0a50fdd368934569b774e87c8`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:20be0efb184e9ef56927aa52c3c4b14783314d0da1515a15796e60877399dc2a
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
$ docker pull traefik@sha256:5ca4c5b63ac0826c920e1fc00a5a7fc09e6e43fe3eecad9cfa545237da6f5847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47287831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c32b60cc476b8576b66d8909e400eca182ccd954b65f14112cfe4b53cb535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c1fd8b4550f4e38f53b4f321cb2fa01a695e628e22541d9fb69ed42fb157d`  
		Last Modified: Fri, 10 Oct 2025 21:01:33 GMT  
		Size: 43.3 MB (43314949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a87fa5a1beb0c774120d8b856366a5abaef23842d2dd736c1b469ece4c99c`  
		Last Modified: Fri, 10 Oct 2025 21:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:a046244b3f26e51541875e367e773a04e1b51f2fe1cc52c288a30396a2380edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919502ae56c96821c85607970e18002499a7c99ce110bebb77a4aa1f7cc7c2e`

```dockerfile
```

-	Layers:
	-	`sha256:b2397c9011c10606a3b2354959c77a2310245c0845622cc490aed8e58668033f`  
		Last Modified: Fri, 10 Oct 2025 21:09:56 GMT  
		Size: 844.8 KB (844750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206958e24603f7f124045eca2ab6c435e14db0257c1c5381c4d9f981e39df024`  
		Last Modified: Fri, 10 Oct 2025 21:09:57 GMT  
		Size: 12.6 KB (12602 bytes)  
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
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8b12138c7587583ad978f6e20dcd02c1b2f07e5be8cad0fd7406879f192b4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8a101f10b24acaa0e23c0c867b63ff273e59b4edce6509fa63ab928aab09913a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1623232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80aeb67a00b1afba5df925e0c8aba1b3e1e39b54f306b20dfe0d536b51e6fb46`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:36 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:36 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8fc9685f839dd92c4d1d53b23867b093485643ea9d6826fee7e8edee0d6850`  
		Last Modified: Fri, 24 Oct 2025 18:22:24 GMT  
		Size: 46.0 MB (46034220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de74a6848534cdf597c00ebf1ee0751bb2f89354551331ef83971fdc68905d`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18b13e03b88056baaadae568b0d426138a4633e536238ea7b1f08c4455db6c`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61856ba4e0382718973ce3c7e57203b52e5832f0a50fdd368934569b774e87c8`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:20be0efb184e9ef56927aa52c3c4b14783314d0da1515a15796e60877399dc2a
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
$ docker pull traefik@sha256:5ca4c5b63ac0826c920e1fc00a5a7fc09e6e43fe3eecad9cfa545237da6f5847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47287831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c32b60cc476b8576b66d8909e400eca182ccd954b65f14112cfe4b53cb535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c1fd8b4550f4e38f53b4f321cb2fa01a695e628e22541d9fb69ed42fb157d`  
		Last Modified: Fri, 10 Oct 2025 21:01:33 GMT  
		Size: 43.3 MB (43314949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a87fa5a1beb0c774120d8b856366a5abaef23842d2dd736c1b469ece4c99c`  
		Last Modified: Fri, 10 Oct 2025 21:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:a046244b3f26e51541875e367e773a04e1b51f2fe1cc52c288a30396a2380edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919502ae56c96821c85607970e18002499a7c99ce110bebb77a4aa1f7cc7c2e`

```dockerfile
```

-	Layers:
	-	`sha256:b2397c9011c10606a3b2354959c77a2310245c0845622cc490aed8e58668033f`  
		Last Modified: Fri, 10 Oct 2025 21:09:56 GMT  
		Size: 844.8 KB (844750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206958e24603f7f124045eca2ab6c435e14db0257c1c5381c4d9f981e39df024`  
		Last Modified: Fri, 10 Oct 2025 21:09:57 GMT  
		Size: 12.6 KB (12602 bytes)  
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
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8b12138c7587583ad978f6e20dcd02c1b2f07e5be8cad0fd7406879f192b4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8a101f10b24acaa0e23c0c867b63ff273e59b4edce6509fa63ab928aab09913a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1623232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80aeb67a00b1afba5df925e0c8aba1b3e1e39b54f306b20dfe0d536b51e6fb46`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:36 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:36 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8fc9685f839dd92c4d1d53b23867b093485643ea9d6826fee7e8edee0d6850`  
		Last Modified: Fri, 24 Oct 2025 18:22:24 GMT  
		Size: 46.0 MB (46034220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de74a6848534cdf597c00ebf1ee0751bb2f89354551331ef83971fdc68905d`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18b13e03b88056baaadae568b0d426138a4633e536238ea7b1f08c4455db6c`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61856ba4e0382718973ce3c7e57203b52e5832f0a50fdd368934569b774e87c8`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29`

```console
$ docker pull traefik@sha256:20be0efb184e9ef56927aa52c3c4b14783314d0da1515a15796e60877399dc2a
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
$ docker pull traefik@sha256:5ca4c5b63ac0826c920e1fc00a5a7fc09e6e43fe3eecad9cfa545237da6f5847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47287831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c32b60cc476b8576b66d8909e400eca182ccd954b65f14112cfe4b53cb535`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 26 Aug 2025 13:14:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13c1fd8b4550f4e38f53b4f321cb2fa01a695e628e22541d9fb69ed42fb157d`  
		Last Modified: Fri, 10 Oct 2025 21:01:33 GMT  
		Size: 43.3 MB (43314949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a87fa5a1beb0c774120d8b856366a5abaef23842d2dd736c1b469ece4c99c`  
		Last Modified: Fri, 10 Oct 2025 21:01:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:a046244b3f26e51541875e367e773a04e1b51f2fe1cc52c288a30396a2380edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **857.4 KB (857352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919502ae56c96821c85607970e18002499a7c99ce110bebb77a4aa1f7cc7c2e`

```dockerfile
```

-	Layers:
	-	`sha256:b2397c9011c10606a3b2354959c77a2310245c0845622cc490aed8e58668033f`  
		Last Modified: Fri, 10 Oct 2025 21:09:56 GMT  
		Size: 844.8 KB (844750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206958e24603f7f124045eca2ab6c435e14db0257c1c5381c4d9f981e39df024`  
		Last Modified: Fri, 10 Oct 2025 21:09:57 GMT  
		Size: 12.6 KB (12602 bytes)  
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
$ docker pull traefik@sha256:a51f3666b0610e751e7e5685b8d4f57bf481ad938077496d9deefad0b3642b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:32b8e5f4a0242786c11b700df1b84d4f3fd163a23753d5acc3ba5ee777c65938
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168082643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8cacaf9491647e22ca70caa76e1f350071eda1bbb64a36b820be44762143d4`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:16 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Fri, 24 Oct 2025 19:21:18 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:21:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:21:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e2a8d499c28b84bedad6991db6967fb6123023c25c1ce2d22beae0d9b3ad8`  
		Last Modified: Fri, 24 Oct 2025 19:22:29 GMT  
		Size: 45.4 MB (45395392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610f792c72c16eb1185a26d7c3886854f07c9b82f0fd8827e40be067e21dc62c`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133df68841803c33b0ee03535841502452b801f7619a2a70b4f08f73beb87135`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c280db07b28481e3eacdf673dd8caf97459b6fa99517bc2b3605ced691203186`  
		Last Modified: Fri, 24 Oct 2025 19:22:18 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8b12138c7587583ad978f6e20dcd02c1b2f07e5be8cad0fd7406879f192b4b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:8a101f10b24acaa0e23c0c867b63ff273e59b4edce6509fa63ab928aab09913a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1623232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80aeb67a00b1afba5df925e0c8aba1b3e1e39b54f306b20dfe0d536b51e6fb46`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:21:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:36 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:36 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e969c09e3393939c9e6a500d472036f493ca065945e74c4ac359749c0216ff`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8fc9685f839dd92c4d1d53b23867b093485643ea9d6826fee7e8edee0d6850`  
		Last Modified: Fri, 24 Oct 2025 18:22:24 GMT  
		Size: 46.0 MB (46034220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6de74a6848534cdf597c00ebf1ee0751bb2f89354551331ef83971fdc68905d`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea18b13e03b88056baaadae568b0d426138a4633e536238ea7b1f08c4455db6c`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61856ba4e0382718973ce3c7e57203b52e5832f0a50fdd368934569b774e87c8`  
		Last Modified: Fri, 24 Oct 2025 18:22:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.3`

```console
$ docker pull traefik@sha256:d6be8725d21b45bdd84b93ea01438256e0e3c94aa8fa51834fe87f37cd5d4af8
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
$ docker pull traefik@sha256:533b88704a28de92a0093e0be45db300418c06842bc226d9faf6b56abe2e7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47782519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54194530fda53b48ca7712597d957ef68727a59a075f51153733a3be2d3f292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Sep 2025 09:31:02 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018263c158e9a8273ae549999fb21be08a91bdf3b745e9dfcef3687ee69ae42e`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 457.3 KB (457272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfad31b5d766aad82fec2961e7ed074a4be0dfa8c15beaadde9fb3e24f979fd`  
		Last Modified: Fri, 10 Oct 2025 20:56:11 GMT  
		Size: 43.8 MB (43809638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc3bfa476a92caa1213a55317274525f2daf0045149b63fd38ecfb923c4f16`  
		Last Modified: Fri, 10 Oct 2025 20:56:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:9f2e1cd031774fe1c786d3db5e826f9d2f9f1be1254364c9ab3d2268e3ee6b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.5 KB (843512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0af71bd7fb00d620bca754ae3d09f5844ba5e722c6113bcd87111837c9ed8b`

```dockerfile
```

-	Layers:
	-	`sha256:e66433c4d916d0d4bccc5c1d2400f9c26bdee599b13a39bcc4f3de80f4798d8c`  
		Last Modified: Fri, 10 Oct 2025 21:10:07 GMT  
		Size: 830.6 KB (830631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869a7ec1846b233642b1ceeaecef085ed6be737cb88e2344415e7a0698919fb9`  
		Last Modified: Fri, 10 Oct 2025 21:10:08 GMT  
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
$ docker pull traefik@sha256:8de652f6bcb5ee8b2a93af9517f50bf595dc771b527213da17a39682a3813acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v3.5.3-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:19d1b86e24803f343ea932a77a1eee10488ed7845c968b9d59e36ec00f901e20
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168904640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47857e9dc64e1373545383d830acb79477c78ad618185c31e5a91b911504be45`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:18:17 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 24 Oct 2025 19:18:19 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 19:18:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b29ca6c2223fd0dba9dacd8c81ffc5784482424d569057883b99829e166ed7`  
		Last Modified: Fri, 24 Oct 2025 19:18:53 GMT  
		Size: 46.2 MB (46217386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbb4eea59fe79343a9e791c3eeb8876a26300f17f61e24e90716348c3436abd`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084ed331675e3d52476819355331467d24983c960ffc150380d02603ecf5c9c9`  
		Last Modified: Fri, 24 Oct 2025 19:18:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dbff7c41d910fd1dc98efbc324ae763b57b5763d82990c645ed09fcd9b8622`  
		Last Modified: Fri, 24 Oct 2025 19:18:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:v3.5.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:507ae5b4f78222d164509e590ef87702e37f485593758014f3fa20d020a8e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull traefik@sha256:aabc85d60009a7baf9f3dbf8a9e8e20bc77f026a1162a4fed602fd7e297053e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1624065734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d89ab91ad08e600f759283a61e8fa3cbaa3b868ef55ad56cf05582b49c66791`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 24 Oct 2025 18:21:21 GMT
EXPOSE 80
# Fri, 24 Oct 2025 18:21:22 GMT
ENTRYPOINT ["/traefik"]
# Fri, 24 Oct 2025 18:21:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43dbb168232cf2c6ae8ec8131b97368efd3d1e9b08f5bcf6401182e363534890`  
		Last Modified: Fri, 24 Oct 2025 18:22:23 GMT  
		Size: 46.9 MB (46867533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfc301ccd9bfd2e46645a828288f984b0de9a2813c062e6d7a4eb64bf6bf031`  
		Last Modified: Fri, 24 Oct 2025 18:22:17 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7619f6d8257f5d5207878286ad98e3c5a667738d98fbc9887887164538c233e`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0b9bd7a5477478de578c2881b826e65a7e4854f4e0d0a55f0c3c0512e24ce1`  
		Last Modified: Fri, 24 Oct 2025 18:22:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
