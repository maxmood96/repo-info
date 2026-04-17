## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:b796f36d2fba0cc258963d2ed401eab917270511687dc4578ccd9d1fe5bf68f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5a423134e0791c2d59a832a5569902731e444f8d4185289f92673d6a163ba5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76330781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d7c12f6883819605ebb8f8fa1aa8ff5e206a89319f0ada2ffe6a97f56536fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:26:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecec50759c3bd60116bddbffcebabb3dcd76303cf36ce83784b5ba0cf93040`  
		Last Modified: Wed, 15 Apr 2026 20:24:53 GMT  
		Size: 7.1 MB (7106390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e4958bba254d5b20b93d40bc57b4d2e5d5db9d885840d5f7405d3da91fb59`  
		Last Modified: Wed, 15 Apr 2026 21:27:09 GMT  
		Size: 39.5 MB (39487893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0892dd6c841802abac05f6387b324b40729157c48934d28d70f61e19b1eaf27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5819978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da997e131ed88d78cd851e29e41152ef21644ae3a1e33c56cd1e3de60a2264a`

```dockerfile
```

-	Layers:
	-	`sha256:44dddf1ab21c2d9048ccb133d63bc4d7b9bfc834b231d97c9d088594be92a923`  
		Last Modified: Wed, 15 Apr 2026 21:27:08 GMT  
		Size: 5.8 MB (5812698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d660ef314e25b38ca015e2032f0a5bf88991230a9f3aa4253fc0a8b64fe078ad`  
		Last Modified: Wed, 15 Apr 2026 21:27:07 GMT  
		Size: 7.3 KB (7280 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:44db0c22ec312a0cb8cb880717598c6f0fcbdd4c7d9680abe6a8b3f80e6b26f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76121660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6034b0159f77214eb3dafc46d97270ea2b67358de1f56c6908f98093865b95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:44:44 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:44:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:44:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:44:47 GMT
ADD file:cf79b3b81bc9aa60d93ec4cfb803894aca6ed3d1e7c9ed02435158c6c0de400b in / 
# Fri, 10 Apr 2026 09:44:47 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:32:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f1c61368409f262f2b51173bb83056489f63f356da65ec1d7227c4451afc7ff0`  
		Last Modified: Fri, 10 Apr 2026 11:01:03 GMT  
		Size: 26.8 MB (26841687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ea175a59e4f7f510d8b43574403d0483cfe07a859f9c54ff97760dc3b0b09e`  
		Last Modified: Wed, 15 Apr 2026 20:31:20 GMT  
		Size: 7.0 MB (7010549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a03bc9e8dd1d1fa48ff01cdf2bcc6457fb722e8d6ec9fc5d5681fe7bb742fba`  
		Last Modified: Wed, 15 Apr 2026 21:32:27 GMT  
		Size: 42.3 MB (42269424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8dc2c4b577f0b4d7404d19c133c129ad2d1ba41a024d8f12f496a2567a66a71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45edb8740395d4f5a5063c0585f5ee1e13f7c29633ec2ca4ea122a93286593b2`

```dockerfile
```

-	Layers:
	-	`sha256:626d20efd57c28e1573e6e07585a16047d22ec71463d0a790891e66b0c7954e3`  
		Last Modified: Wed, 15 Apr 2026 21:32:26 GMT  
		Size: 5.8 MB (5813978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c2394060adb286e3ee40ca189a43748c66f3f636ccc435a15f3a378a1d65e3`  
		Last Modified: Wed, 15 Apr 2026 21:32:26 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bbb764971211442890d876f60666d2c0fb4592842a9dde5ca42acef9d9da0195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74078807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4081d7d6947925dfb0d86eaeb6e045aaf6e60307b2689fedfcb1a318bbaca291`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:40:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a5bc53c1a6e7cc1735f8944574d4921d9d23f26d4b1025adf1c324ad2b07b6`  
		Last Modified: Wed, 15 Apr 2026 20:24:21 GMT  
		Size: 7.1 MB (7061127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbcb8f28dc46ee2582e5ed090a59d48662855ba06861fbb05e006c6efc2f612`  
		Last Modified: Wed, 15 Apr 2026 21:40:17 GMT  
		Size: 39.4 MB (39411137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38a59919f8ddfdbea388d13e1755c58b766629473b855233d6abe0ad36ae3777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbaeb1549b842ffa8b61ed56920175d55b81af7447f2adcec0df824c015887c`

```dockerfile
```

-	Layers:
	-	`sha256:24248d61a946cd9c1da41a010a50a47901cc79d5e5fa778dbae4163cc2d33a9e`  
		Last Modified: Wed, 15 Apr 2026 21:40:16 GMT  
		Size: 5.8 MB (5819092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd7587283ac0c6803014f93ead41f56d9c18f02adb11654c42ddc1787c26ec9`  
		Last Modified: Wed, 15 Apr 2026 21:40:15 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:692f80188a162b713761e228bcbefc9ea54bcb7c6bca2de8ad07eeec65188173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86610909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bb837d2f68b6239e37bb14da519a810e92e4c7f3688aa74cbc25a2f15343df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 00:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934dcd0d71e03d90a927f281153e6d3ea266863de69f95adc0ac8dc3ddc9e4e`  
		Last Modified: Wed, 15 Apr 2026 21:11:30 GMT  
		Size: 8.2 MB (8186214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d1ad4a4ff321f644d76bbef785a0d592a87d54674d9faa63d42df9d16e983`  
		Last Modified: Thu, 16 Apr 2026 00:11:00 GMT  
		Size: 43.8 MB (43776297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e2a592a562143b35465f2253ecd28d5003503626d74f200f8c185a30b6683983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d618d0392df22e32ec13ac2c42115bb8cad6c6abb64f5266ab226dcfaa075`

```dockerfile
```

-	Layers:
	-	`sha256:37d71e5ee87220d084b7ce8a6ad815e5edd7e665f8f38013450e056ffc72658d`  
		Last Modified: Thu, 16 Apr 2026 00:10:59 GMT  
		Size: 5.8 MB (5820542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:323931b791e632eded559f90a832c5e1a5d360a83e8fc5bb205b181013d82cd6`  
		Last Modified: Thu, 16 Apr 2026 00:10:59 GMT  
		Size: 7.3 KB (7312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c98adebb61dd9dd7795bc9fc49fe4100b0dfe25a87bdd1b8e9e9d02bfa1f2f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76666913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b945a7dcee5c5fd6f8b40fd9382cb85a5de9bc412b4e0adebeb2771fa5ce1b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 10:46:30 GMT
ARG RELEASE
# Fri, 10 Apr 2026 10:46:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 10:46:31 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 10:47:09 GMT
ADD file:7ae2692e9ead2e53576d53cdb893209a70fe6f0a62ff35308c9fe5c855c10e94 in / 
# Fri, 10 Apr 2026 10:47:13 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 16:40:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 Apr 2026 15:18:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:116177a8ef78c1de97a5262550388dc00d9881fcb4c367e06e4e52bbdb5a832b`  
		Last Modified: Fri, 10 Apr 2026 11:01:22 GMT  
		Size: 27.2 MB (27240349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74ddabbfbd66006e6d36799950a3c7e93532654f0837cde6fe2521d8c52ee83`  
		Last Modified: Thu, 16 Apr 2026 16:41:28 GMT  
		Size: 7.1 MB (7118338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144adc2ee8321b5f81e7424187eca2a7ced16978dd9f89b2dca14b113fd47f46`  
		Last Modified: Fri, 17 Apr 2026 15:20:34 GMT  
		Size: 42.3 MB (42308226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f16094003f760a9e9fc891233ecea3b14dd22911afa378652b1408493995d8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49466e97547cde357a1d665a1001a5ed2cf1702a8122d61e8ba03f35a904ce63`

```dockerfile
```

-	Layers:
	-	`sha256:2976657b94217663302085dba94a516dc6f9f639a84fb8c269ecfbc79643a2aa`  
		Last Modified: Fri, 17 Apr 2026 15:20:28 GMT  
		Size: 5.8 MB (5803084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aed84cbfc42961307e4c9484b6f941b5d93310180763ef10f9b198ed9c85b62`  
		Last Modified: Fri, 17 Apr 2026 15:20:27 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bc9c853fbd508e2a3831682577b609874f98f4973f2519e3a6b4d5572652411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74635842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586afb38cd23d39c83c59c215ea75dc985d8a90660d3d436cb05e96bb6741909`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:50:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb2def34f87e70db8ee4787df628a5479c6cdb42d140cd23cb1cfc202317d9`  
		Last Modified: Wed, 15 Apr 2026 20:43:23 GMT  
		Size: 7.0 MB (7019135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f2f17fa2aa4d3f3d7ffad88a6e820e36144fc3f9f9de46504012f45065a9d8`  
		Last Modified: Wed, 15 Apr 2026 23:51:03 GMT  
		Size: 39.4 MB (39414408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b650571fc7fe0c0236cf94e7a89e410d98c27b83244d0dbc5a31153c38e9ca39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbffabefd545f894d2c8df14555265f3ac3fe113e226a9923619efb2452645e4`

```dockerfile
```

-	Layers:
	-	`sha256:1c7c24b407ea3a9140c1b420f5934d23a00f9e336ef64df34189c53ede586016`  
		Last Modified: Wed, 15 Apr 2026 23:51:02 GMT  
		Size: 5.8 MB (5813617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aead8436488d581391b814324f971807109c55fcc11740ed1db976638f149920`  
		Last Modified: Wed, 15 Apr 2026 23:51:02 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
