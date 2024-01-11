## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:d883c0f1946f3f8079d96405d2f108ec462c552455566d5e54b1fa39ddd55ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7fd071471c070146e579b6e18e3385299f6bd90fcdac5376a06e689a769d5e9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76013319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c938c72d716541c88f972961bbd785d121eb6be6212ee7519eb38483bf81aff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:716f2525263989014ccf51727e00b6ee9f74018b7b13e996b0e06409e58a44a3`  
		Last Modified: Tue, 19 Dec 2023 01:27:57 GMT  
		Size: 52.2 MB (52246819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562138d694fb5f355036844c413debe243407688e2d5d831cf2333c434a0bb40`  
		Last Modified: Tue, 19 Dec 2023 04:44:12 GMT  
		Size: 23.8 MB (23766500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6619eb9db222bd053555e7cb22ca730e3186bd13c78473a06b5c617036fabc6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72177696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be421aff42b9b42179286525e3b47418aaf1a1c3514b8d81c7da8f912e66bfd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5110329ab47599ddb3bc004401c37c9cde68589c2b2734abaaef4fd51bb0f3c`  
		Last Modified: Tue, 19 Dec 2023 02:00:24 GMT  
		Size: 47.3 MB (47266091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4217a8fea4bbcabeb43f96e627c8788aed8b7f524c41838c7b4e9aeb229a6572`  
		Last Modified: Tue, 19 Dec 2023 05:33:42 GMT  
		Size: 24.9 MB (24911605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:66b64ed00e48532ae240a99a44fa667324a2f4390f412883ed00b62dd4f077b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68990619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4b2b56694995ef3bf428c090588656a55850b9b9b0192bb4af9c7f56c74b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:12 GMT
ADD file:5e0189fc7402da5b92ea3c0f1e4cde0f5f56258cfb29bbf3fa29767c1d430c76 in / 
# Tue, 19 Dec 2023 02:09:12 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ad57ea9eca16d7e9ee7827f31dfc15f264b708ab11728a7935b2f23ec3f42d3`  
		Last Modified: Tue, 19 Dec 2023 02:14:36 GMT  
		Size: 44.9 MB (44898763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd55d116127ea8cdc765d3307e52ea259fb1ac1a89e4303e4ae51e5781e544d6`  
		Last Modified: Tue, 19 Dec 2023 08:09:24 GMT  
		Size: 24.1 MB (24091856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee9608c6d0266b7f3821338d936434e46b4ef863c603f645337b25bc523ee34e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75673495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836b7e01ae3a85d4eecef46b61178478eea2f0cb77a25b76bc7ad15cc8b2e0a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:13 GMT
ADD file:b95bf5556d43a8a1d79a2dbf26ab8a4a912869d65cc1b76a372ca80259a65b7b in / 
# Tue, 19 Dec 2023 01:42:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:38:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f38ee39d2143cc6781c8d40b267519e59c558f7902df442f2e5ecfcefb01689`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 49.7 MB (49689786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec939d1d3b6574ac3482db9be62850fd83b1612f01d44fb296af8ed464c33f1f`  
		Last Modified: Tue, 19 Dec 2023 11:44:56 GMT  
		Size: 26.0 MB (25983709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f5bce5b2a812ac3e4d477ded664ef22b441a4e04cf273a87c312d5ebef7ee6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78002695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0b69328536bca8f709bb9cbc16648970c323d17878bc58bf9d30c585881148`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:567001fd97421e53b722a950bba83f44d7635056bc895f0b4f77b68d779fc15e`  
		Last Modified: Tue, 19 Dec 2023 01:46:59 GMT  
		Size: 50.6 MB (50559243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be94f97dfece4691341230f320f14599076c4363c331188ce540fae76670a04`  
		Last Modified: Tue, 19 Dec 2023 03:40:12 GMT  
		Size: 27.4 MB (27443452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1e5bcd2de6aac0d979e9e3ac7288764dc6ba5531745b4ea398fcf254dc899375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75485210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6422bcdcce20e3e6dcea181aea6a3ae12e19f7ed14a04a35cd8c79a1f6a07330`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2d66d60497a4bd908c27fcfb1927b93e2c8404b82c72ec7b1f6256da631680a`  
		Last Modified: Tue, 19 Dec 2023 02:28:04 GMT  
		Size: 49.3 MB (49347836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d78f2105a2a8a1a33a9d6d37906b39d31cf3ebbff970baecabceb1a81716e9`  
		Last Modified: Tue, 19 Dec 2023 03:25:22 GMT  
		Size: 26.1 MB (26137374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f1a2435281af5fe27f3051d6e9b32118aa57ff0e36622ea60497983843bf2aa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82416305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c991fc02d8428c72153f6eeb492bd10f4e8f6159c5f818a43266c9d5d90f42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:00 GMT
ADD file:ebe2bb6638a51888bf27d1bb5ca609a91df94474b4abf70f874e60b653885a2e in / 
# Tue, 19 Dec 2023 01:23:03 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:97954753acf4d5cb589b2a49219ffbc5c86834cb864ed80f516370017ea3c569`  
		Last Modified: Tue, 19 Dec 2023 01:28:17 GMT  
		Size: 53.5 MB (53455717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf9bc2559c9bc0dde88b00d18449e9a40dea5919313c9dba6b3a432f24542e4`  
		Last Modified: Tue, 19 Dec 2023 12:25:16 GMT  
		Size: 29.0 MB (28960588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a1d2845e03db5e718840f2e80e44a25e52659aaf135321d76515b5ab9289975c
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73951260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5c628c68b3456f42af22d7bb5fca78fe956af7b2308df19b7c735a9f988c21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:08:57 GMT
ADD file:2425f95373d17e6fdcc9fa7f49bb6c7911f6b90dc27b013c125e09c38c1691de in / 
# Thu, 11 Jan 2024 02:08:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c4051c39033b0cb21a5a8e11e0cc7f40eaa9806ddc6699457c2f509128c3a492`  
		Last Modified: Thu, 11 Jan 2024 02:11:46 GMT  
		Size: 50.5 MB (50487871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680ecbf0470fdf287fdea90380971756e9423f13d45445f3c9b23000a0ace9db`  
		Last Modified: Thu, 11 Jan 2024 02:41:54 GMT  
		Size: 23.5 MB (23463389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f033afe3d217b2be035f73914cc7f6d1ebc5228cd50a06fe2811587a4db3d431
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76522710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48aa36fe76e09fee873a89a00d59adfe21f36e58081e4bf48c0e7e9c6a64a996`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:46:39 GMT
ADD file:8031754126dba92ceeddd0be53523bca85fa55f5859c83eaa57be2b0ba8f8046 in / 
# Thu, 11 Jan 2024 01:46:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce6f2c0c05e382af54def5b355ea9bda0f36bd689f9f43fdcd74463778010bc5`  
		Last Modified: Thu, 11 Jan 2024 01:51:57 GMT  
		Size: 51.7 MB (51672176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccdf962076103e72329069bf48fa3112a100d8a6deee506176beb22e27789a0`  
		Last Modified: Thu, 11 Jan 2024 02:22:51 GMT  
		Size: 24.9 MB (24850534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
