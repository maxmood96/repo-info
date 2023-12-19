## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:e4f879dbbe50179453be8206c8f324fd6128ea827681f8dc7d2025356fa99f77
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e0d5e41352ab8cf617b9920e2249a5a53258e38c0a21a33e2c18993575ab51e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142062356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a979ddc17b1169bcd0e7d369cee427e20e75db30073643f8df8f9d1443751d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:05 GMT
ADD file:0e0fcf0b6bc9c9794502332cd0f45625ac991c8a06ab284afd8673f8d5ab789c in / 
# Tue, 19 Dec 2023 01:22:06 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:37:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:efe9565a064a4e2c8d2e24ea50bb5793fd5453d880cc1268075d4c95136016c2`  
		Last Modified: Tue, 19 Dec 2023 04:44:29 GMT  
		Size: 66.0 MB (66049037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:eda7ad1c9adf08141546487b4ca131c7c951de47acff64152d95db04680b52af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135854704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd629151c9a68becd2cd8cecc176f909736db356d0d4889c5700cbd713dcf67d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:00 GMT
ADD file:cd6b2b4b3b0e27503b12f67c0901ed5145dc3891d490c198b6ea77c5429c7ad7 in / 
# Tue, 19 Dec 2023 01:56:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:26:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:42019878fcdad4a69934727cbee368f7e012c1b035b52d0baa848cfaf64c288e`  
		Last Modified: Tue, 19 Dec 2023 05:34:01 GMT  
		Size: 63.7 MB (63677008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e92555b16e2fc8e0aafab18ce41f5ce4be40a2a97800a1eb331b9958d6db9683
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130016032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab9986a51458daa2e9af10223109393a92da8e9e53d4809afcc14f922d57699`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:12 GMT
ADD file:5e0189fc7402da5b92ea3c0f1e4cde0f5f56258cfb29bbf3fa29767c1d430c76 in / 
# Tue, 19 Dec 2023 02:09:12 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:01:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d56a0b12321836cb81d9731b0251034aa0aca0333c7b777bf5565787fd9c86a6`  
		Last Modified: Tue, 19 Dec 2023 08:09:42 GMT  
		Size: 61.0 MB (61025413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5a72b0d80e775202e4637daa12333eb46351c5a626aaa055df78bc26bec51c1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141823279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57b09fc98a3aa247da6b784c2e7d996c51a0bf6f7436d60367b9c2533fd1b1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:13 GMT
ADD file:b95bf5556d43a8a1d79a2dbf26ab8a4a912869d65cc1b76a372ca80259a65b7b in / 
# Tue, 19 Dec 2023 01:42:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:38:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:38:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:591136ec6e5960d51ec4ac04b638e9bb1afe645fd53be0f002e76e7d236d522b`  
		Last Modified: Tue, 19 Dec 2023 11:45:12 GMT  
		Size: 66.1 MB (66149784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b403e321a12af49825b52173de020258f34e044645d5b4c7e407638600344d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145812346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c0378b636a237178ce1710b59568f8522ef9de3399ff88454c0edb618c2d03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:40:47 GMT
ADD file:736d4b14c103f5161855a9c14b05565523005af03b61bcfb3d6bfaddee9431f3 in / 
# Tue, 19 Dec 2023 01:40:47 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:31:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:98e5706d82a57d517f5b2faa92178f9346b9a474417ad5a9158a842164e920a6`  
		Last Modified: Tue, 19 Dec 2023 03:40:36 GMT  
		Size: 67.8 MB (67809651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7d6b57ec0772da03f76089453b7948af8001f2b7c4cd6275133e62771f6c4842
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140362504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268dd58b533640c04942005a5685b8022869bd3c3cf19a393c854217f467a20f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:16:40 GMT
ADD file:92ddd4cc9e70e469a6b3b98c2281b2b6c642d6709639b0c1950eda80325d474c in / 
# Tue, 19 Dec 2023 02:16:46 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:08:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0539b334e5a1b4f830e2cb90767d1d6bd23065595b3d40e6cd589ec973f33276`  
		Last Modified: Tue, 19 Dec 2023 03:26:15 GMT  
		Size: 64.9 MB (64877294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4df51f25e0e066e317211b0c8f337d1595123b1695efa23d860d40760ad29520
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154000490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9524f0ad342c674364fbd23da2814fe7a9512b65c6534904c954bb9a5b09dd3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:00 GMT
ADD file:ebe2bb6638a51888bf27d1bb5ca609a91df94474b4abf70f874e60b653885a2e in / 
# Tue, 19 Dec 2023 01:23:03 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 12:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 12:02:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:91bcb9d372effc2b9eed2bc00b534deeaf705ecf5a3705a53bce008b65768d0a`  
		Last Modified: Tue, 19 Dec 2023 12:25:37 GMT  
		Size: 71.6 MB (71584185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cab57db4abded03a615cdeb1b61f19d471f83b61cd62d49fe9248e47afd5ddfa
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139309835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b18f767be5d0b44739d653a26034dce3433781c850d7429a89e91f08e6aee7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:09:57 GMT
ADD file:3562591665655b4a3f3484846dabe4d93498b3b3216abd802cc9678912880a41 in / 
# Tue, 19 Dec 2023 02:09:59 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:ebe6c23c39483f54e5cc09f3805cbea29d02f6bbc773bf62d752dbdc74d194e3`  
		Last Modified: Tue, 19 Dec 2023 02:43:08 GMT  
		Size: 65.3 MB (65295558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6da1236508da6d38595a2124e425541438417f0003015b2daf2c758f2960c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143450498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e456831f71a7d08f94bee3f7efecca81ea1bdf9aab3c0d9875e65862688e05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:58 GMT
ADD file:787d19e6a77aebb4de0df132b1de8d62f9d4c2c2d0181bd2c57d043a742aba66 in / 
# Tue, 19 Dec 2023 01:44:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:47:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:966a7cc784826f7ec8c32d88dd36bc8a9262f3b9612fd9916ba143c8e3362629`  
		Last Modified: Tue, 19 Dec 2023 07:55:28 GMT  
		Size: 67.1 MB (67083999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
