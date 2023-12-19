## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:e6281f9b311234395836fbffe9dafbdf47e602aecf826795545108ab4c7718f4
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
$ docker pull buildpack-deps@sha256:7d94a1efff10fcb19fbd83cfb66d8d450a7ed085c20a21d34777ddeea944d677
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76614270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84f666bba1d3f33d489b7f1ca30183b36b1949707e4cfcc5b70fad6f28dfe30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:10 GMT
ADD file:b7e79bb3e80d19e670364baeded7d6093bed7726e664bf3e7a2c821d334ca2a7 in / 
# Tue, 21 Nov 2023 06:28:10 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:02:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f10682f9151129c7a80c2164b36358fc8ab4fad6515f194b50035e08ff0e5d7`  
		Last Modified: Tue, 21 Nov 2023 06:33:04 GMT  
		Size: 49.6 MB (49637809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308844503dea1813b99b0e18b34377690a3c37b34548a792e2ba1ae2dd7044c1`  
		Last Modified: Tue, 21 Nov 2023 08:08:42 GMT  
		Size: 27.0 MB (26976461 bytes)  
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
$ docker pull buildpack-deps@sha256:bf7b2c6f20aeaa97efb86336a12338247f96a743fa032cbb6e848100e365d25e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83434831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e185b08bc814b3731dcb7aa4ef80f272175c6d3715e08afb5a280d02f76715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:25:27 GMT
ADD file:a20f125b82438597a2805558ad08c66dbc68ff26fb4af210ce31e903d1d46127 in / 
# Tue, 21 Nov 2023 04:25:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:700801ea1c1b3b29b8d88a2f8f9405af55e151c6a84cab4b448b09ce5f2e432c`  
		Last Modified: Tue, 21 Nov 2023 04:30:48 GMT  
		Size: 53.4 MB (53423841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978542d765f76211993ce7a733e45289127bc6a8dcd47683860c44cd31e03925`  
		Last Modified: Tue, 21 Nov 2023 07:09:13 GMT  
		Size: 30.0 MB (30010990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e2b661dc9029e826be1456b9abde55f5a23438a6f9f7ac222510e045a0d9f8a
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74014277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b585177a3343949dae98f8d0e2e5591bb16fa3a41b44d130e49941538583ed42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:847370bc2768a9e226e456b3801dcd33d1e866f32c8776dd5d447eca46270972`  
		Last Modified: Tue, 19 Dec 2023 02:12:47 GMT  
		Size: 48.2 MB (48232544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789991b71e44f6b60185366eca5b60f17c4ff7f66b5a0c174e178d81ca5ca22a`  
		Last Modified: Tue, 19 Dec 2023 02:41:52 GMT  
		Size: 25.8 MB (25781733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bb33554e8e7d6d9e77a54cc1a8086dd7f73cf431861f425c04e7cc3a00e5ed03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76366499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5cf6a3a3c2d4a9cde0e41314e1c95e517eb7786b4c8e6c66ef2b14ec0019b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:58 GMT
ADD file:787d19e6a77aebb4de0df132b1de8d62f9d4c2c2d0181bd2c57d043a742aba66 in / 
# Tue, 19 Dec 2023 01:44:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:81a71db9a04e29cf0934e3f04c4935c1dad336d34d53ea6877240b19747c865e`  
		Last Modified: Tue, 19 Dec 2023 01:48:45 GMT  
		Size: 49.3 MB (49328178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f2e8658adec6b0269494f8fb2af7c207978a293ef3251001e591960530e6fd`  
		Last Modified: Tue, 19 Dec 2023 07:55:14 GMT  
		Size: 27.0 MB (27038321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
