## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:1eeb97bcba838179337f8a23b9be7aa5a53bfe252cbcab6a806ae1a64b3b01fa
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
$ docker pull buildpack-deps@sha256:c506c9a4be6710ea11f6f9e651b299b2923321eb160bb25bf1d1e072cda99e99
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72078916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f91c17165e09e37563417b4384a281bd5f9a34451345ed1e380530c62e936f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:25:11 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
# Tue, 23 Jul 2024 05:25:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83f204115f2d8f0a8c57a70da31bf65c2c885bd0d5f75a66abdfd1d38169bbe`  
		Last Modified: Tue, 23 Jul 2024 06:15:13 GMT  
		Size: 19.3 MB (19296959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6b5b91dd8563b6c83f9f292f47b4f4dbe9be84f6e6132701121dc0133e988f57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68071420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b80c1c593db8ba05c984a51879cef29a28366f43e1fb6396f1eb08e2ab6422`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:01 GMT
ADD file:95d0230b78af5d334bd0243ce6197c2140ec2471924e5ef4413707038e18e143 in / 
# Mon, 22 Jul 2024 23:58:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec2b125127e6f8d49325b626aa909fcd3b43a8d6c77bc97a74c5f2018c245546`  
		Last Modified: Tue, 23 Jul 2024 00:03:01 GMT  
		Size: 49.8 MB (49828856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b117c2153e64301fab367eee4a7771746dee9588d142dbd0e4791dc9a32239c3`  
		Last Modified: Tue, 23 Jul 2024 03:54:47 GMT  
		Size: 18.2 MB (18242564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bfa97ce73cde95032209696321352612680db764c680a1b0951f78188c543fc2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64920297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d9f5d5f12b39b29e168914b6f8c8975fdcee316b9e697f402b0b3c5137032b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:04:00 GMT
ADD file:31576c5cd1d1e13e2a728f71cf07534ba5b1b2ab9de9793a31cc07fcc990c347 in / 
# Tue, 23 Jul 2024 03:04:04 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fa7817dbf291482bb88d91e0e917de78192dae47dd05161de99a0ed32a21527e`  
		Last Modified: Tue, 23 Jul 2024 03:08:25 GMT  
		Size: 47.3 MB (47311981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dd4c3d5aa06a66cbc690f7dfe97a6c3194299eeb4d8911e0fc8c5a62f49d50`  
		Last Modified: Tue, 23 Jul 2024 03:49:38 GMT  
		Size: 17.6 MB (17608316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b4457f66928512d5f7e7e272b2860a1570c42bd987dc1a19752da630fb0cbf5b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72094583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd70e123fa323cf6fb7aa18f6e1d8a9c1df8bd0c99a4449f0382ebffe20c314`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:28 GMT
ADD file:368e6d1d2999bc62054217cfec29bdcf59fe672d1d5db07c2f2c2939222c4a42 in / 
# Tue, 23 Jul 2024 04:18:29 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:88161cad314c45536b001a7558a18c0a54c991650605a6212e9720f7ac3bbc4a`  
		Last Modified: Tue, 23 Jul 2024 04:21:45 GMT  
		Size: 53.1 MB (53060158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b68eb8ee2aecf040cd7b1e4e851a71e9d804cc97278c9794ee8ae286ecdac8`  
		Last Modified: Tue, 23 Jul 2024 08:11:50 GMT  
		Size: 19.0 MB (19034425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:04c2515d0b3ac31ffd91e42f38e369e1bff2641c2728fd0621aedc407df1b678
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74055569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad98ccf705d644b38203f371bfff8ec7f09a2c081edea59d84db557b6519f68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:55:07 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
# Tue, 23 Jul 2024 03:55:08 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30d4c408d4b13b5bbb6ad75101f14733d7889301ed646e770751250019d74f`  
		Last Modified: Tue, 23 Jul 2024 04:51:15 GMT  
		Size: 20.4 MB (20354821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e7fa6ef8eb669a3a49a45a66f8cc69d7f09d1b83c63555825932c55ae4e2220
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71416344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfba9f25abc92be9a113bf2def9775d340036cb7b23d08e40a068554fb1d56c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:41:03 GMT
ADD file:4c5b8a467710d6b46f986172bbe029a8628d9b5e288ce89ae0d2507c9c6a4f0d in / 
# Tue, 23 Jul 2024 00:41:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:547554521a86f8be7b55003b426c5518e59d2cad10d4457d287f4456f5b47111`  
		Last Modified: Tue, 23 Jul 2024 00:52:35 GMT  
		Size: 51.6 MB (51646553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c0a36f24cc092af4605ed4efcf52aa8a41e0c0da13688560a4403d8ba28144`  
		Last Modified: Tue, 23 Jul 2024 02:05:09 GMT  
		Size: 19.8 MB (19769791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:597bffbfd546b0553a21404706d32d58cb0aff05e5d1c007c50f45820a980671
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78023351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e74849ee887deb1ee055850655ecbc96c46bfe4cdabff05dbcb2e34bf9a2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:28:02 GMT
ADD file:585b8dcf2e4526cdaba5e616b7761a5b74b918d3740bb07d4bae9a885dd726a3 in / 
# Tue, 23 Jul 2024 01:28:05 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bba0decf595ccf1bd757b6cf34465cdaa54fd8173ae0936ea4365d416401a52f`  
		Last Modified: Tue, 23 Jul 2024 01:32:48 GMT  
		Size: 56.7 MB (56726468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df406a521d8c92d349441aa62ad3b1bf57ec4505884acf3abaa7d36e0ea51411`  
		Last Modified: Tue, 23 Jul 2024 02:44:13 GMT  
		Size: 21.3 MB (21296883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9bc2ea4d38c6b0ac29be1de344a525e9d0b19dddcd16d68afe5f75dcf15192a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70079293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd66d8fceec4fdc27c23b33db01a245076b992eadc7ab6e8fbebedf1fe5499a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 17:00:16 GMT
ADD file:e50db9eb289cfb812a6695f6e40f3a10aaa2f9e38ad4a6d70af6494e43ed5371 in / 
# Tue, 23 Jul 2024 17:00:19 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 17:25:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d76d9ab5752f2093439bfad28138755ba4fefb84ed483e2759ad849339595f30`  
		Last Modified: Tue, 23 Jul 2024 17:03:10 GMT  
		Size: 51.1 MB (51106330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ad85b635ea630a6c98fc3100c738528a1fa21b6f8ac73630d6cbc2a17c333b`  
		Last Modified: Tue, 23 Jul 2024 17:33:53 GMT  
		Size: 19.0 MB (18972963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f1fbd779f4eb589e092c27e36df4ce7691bba7800c279e8aa9588ed295da8f17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72913514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30203e2370c0857b26cbd63c6d17b0d5cb59f4f69da9eca5b30f41fc7f5143eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:29:15 GMT
ADD file:95a4cfad52ad69897cc13b974c9594de964886d46c30d9631ea74926a2fa92d0 in / 
# Tue, 23 Jul 2024 02:29:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:09:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c8768a7d57cf906ef686ceb35e7a6f68642e12ce3f36244a42bfd313f55747dc`  
		Last Modified: Tue, 23 Jul 2024 02:33:50 GMT  
		Size: 52.4 MB (52435495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc02aad785807afd931690639de0be3fec099b62e37f4be13347783597758be`  
		Last Modified: Tue, 23 Jul 2024 03:16:04 GMT  
		Size: 20.5 MB (20478019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
