## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:52aee798462232c976ee82afb2407f6ed06b73bdfdb3c05bb81fd9c86c64eccf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0c0e427274c7c11718147649fcaf54d24efafd84be81c16b95929228e2b9d681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113353190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5feb76ed14b3faa46ad2a37e17ce8fbda10d69d227ca9bff22d0b5423b4376c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4430.tar --tag 26.04
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4430.tar
# Wed, 15 Apr 2026 20:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f528443f34699bfec0f2308065cd6e3542906dc651e44adcbc224911a068119`  
		Last Modified: Mon, 13 Apr 2026 04:42:47 GMT  
		Size: 41.5 MB (41456182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7db96ef8a1ff29f593a12f085ddc564d16b3924f6213bb6c978b9dbe40b304`  
		Last Modified: Mon, 13 Apr 2026 04:42:50 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c119d0c66c27f7d34953d535ece957fc04cc295f72889f2b773ff2b7ce656f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:13 GMT  
		Size: 22.5 MB (22470928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0b629e25426934d573e59d216b907cd4ca93f9451c2a889cadc5f7f1ce8c3`  
		Last Modified: Wed, 15 Apr 2026 21:27:36 GMT  
		Size: 49.4 MB (49425688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:826e37fa8ce25c51a5a449173a13febe418677369e0647464e1387978f1f8528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8ee98541d8894c73f6a845b1de5d8f1cd43a37049c7bd688961d73e61fbe72`

```dockerfile
```

-	Layers:
	-	`sha256:3d41a54caeea4185bc78fe8a4cf85fcc11cf96bb85774c579abb7012a5fe3aa6`  
		Last Modified: Wed, 15 Apr 2026 21:27:35 GMT  
		Size: 7.2 MB (7219885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9cbd53cf771324fd071db27e5c641c5a9f5434d93014c08b30c093b5cfbaf83`  
		Last Modified: Wed, 15 Apr 2026 21:27:34 GMT  
		Size: 7.6 KB (7589 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f332f9b7f07b7d3ad4733751a0337a10161ea7158acb49607152856b1473e855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110889703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd04f1dd633e54b1c6158fc75296b7459501d4465897a4e2479e01fa71b73c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:21 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4467.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4467.tar
# Wed, 15 Apr 2026 20:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ad4da938cf0c0570f3f7d460c11d9db8ebf696978ae9b30e56bbbce569cbf516`  
		Last Modified: Mon, 13 Apr 2026 04:43:18 GMT  
		Size: 38.6 MB (38638847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86038324bc4115f9a18bd6bdea151513582b60ca3c9de1a881935f1beab04dcb`  
		Last Modified: Mon, 13 Apr 2026 04:43:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29851844ca92a399541c3a7a70f5c076de781b7bf6acd8369d547689815e304`  
		Last Modified: Wed, 15 Apr 2026 20:16:55 GMT  
		Size: 20.0 MB (20001894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ee8fd48bf93f1544ca6dc0eb0f51d4f4047c2986dbc7bb3dd7236a88ed8649`  
		Last Modified: Wed, 15 Apr 2026 21:32:49 GMT  
		Size: 52.2 MB (52248555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75c809f2a2c46a182d63d98154072c75a6ffa9715c40b44ad3f81eb0cd68e214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1285c9580662086b3fda21e1219f2f3fe3849f46683c0a2c63b2b8ff70cfeab`

```dockerfile
```

-	Layers:
	-	`sha256:3d0704526fc5b0fc2d8d2f8a8ae4f13e720be4255637847d029f28f8f36d859d`  
		Last Modified: Wed, 15 Apr 2026 21:32:47 GMT  
		Size: 7.2 MB (7220390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4b52eb5c9a7a0eafcb29e348c6e7e7c50703852aa89305a4c57a5b036a9fce`  
		Last Modified: Wed, 15 Apr 2026 21:32:47 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a45c873f9319c99eeb114cae9cc114cb3296b88d110e04443fdea0e79c329514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112067739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf74b04a83ab77562fef158bc0cc5ec58271a96e30db3694d032880a6ca8d7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4512.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4512.tar
# Wed, 15 Apr 2026 20:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86973008df0f4d84f186cd417b697dd89ad0500783a74fbdf846af4e31defe9d`  
		Last Modified: Mon, 13 Apr 2026 04:42:57 GMT  
		Size: 40.7 MB (40683787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d2ed58370ae479dbd99563da5d88c6adecad662d756c0dbce31ca40162b95`  
		Last Modified: Mon, 13 Apr 2026 04:43:00 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9312fd14283f97d0c5f184b060bf26f1bb507d6cfd80927c5d04bbd3cf5d9d`  
		Last Modified: Wed, 15 Apr 2026 20:24:43 GMT  
		Size: 22.4 MB (22362393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ec7c74949ed1d1147300d1277cb82b4bc3f8ceec48ec61ca2e9f0457e0449d`  
		Last Modified: Wed, 15 Apr 2026 21:36:31 GMT  
		Size: 49.0 MB (49021170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:47f2eb1fd27be2c32c2d5ddea900024f8b03267bc3000d6a427aa40f28084626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7233943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82dc521ef47035b6adbec1663cccd34c3e64c7181f812702a5e1347d17cd5fc`

```dockerfile
```

-	Layers:
	-	`sha256:3a6ad92fa2bc363a445858b7d880465255b58d97409111af019ed77443442b91`  
		Last Modified: Wed, 15 Apr 2026 21:36:29 GMT  
		Size: 7.2 MB (7226275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d17a9fad02aa4a2235fdae4a62e6dfade2d364471feb3cd942d40726e5bafe4`  
		Last Modified: Wed, 15 Apr 2026 21:36:29 GMT  
		Size: 7.7 KB (7668 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9e4287cb5cf075bc18bcdc55d3729c6d25fd4cc25e7a11d14ffd0faebfe9fd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124197215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea13ad9c0d204fce5b7d6c2da0328f64dfe83d3fc6aa9c3e2bfd70156c1bbe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.4420.tar --tag 26.04
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.control_data.4420.tar
# Tue, 07 Apr 2026 04:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:58:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0db7ebb2f8444a7effc07cc060085d3ebb0c3b962818809de2885138fa645def`  
		Last Modified: Sat, 04 Apr 2026 05:27:38 GMT  
		Size: 46.7 MB (46739906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250b37d4175277ba214b7494c79a05938f8c42cb3deff8c57b2eb4d7951bfbc`  
		Last Modified: Sat, 04 Apr 2026 05:27:40 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c404c821f83acd9c9ffb53162181be6e1ceab2de93b8b1a7f8de617f8c0383`  
		Last Modified: Tue, 07 Apr 2026 04:25:28 GMT  
		Size: 22.0 MB (21990388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d483f13091e34784b72a22ab7d97877821d8d9ed739fc2a369fd01b53e3d1b46`  
		Last Modified: Tue, 07 Apr 2026 09:59:00 GMT  
		Size: 55.5 MB (55466530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20128bb0cfae39e6ba4cb6386b870c6f7b6807f5eea579aff5243e4876f84bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7237800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192a112092df40b991ca60ac20f67b32acb6c2344c0ebc92943984dca08ecf18`

```dockerfile
```

-	Layers:
	-	`sha256:b00a65729e038a9404b322a71a59f44ba16366287612a9b8a036f5960d61773a`  
		Last Modified: Tue, 07 Apr 2026 09:58:59 GMT  
		Size: 7.2 MB (7230179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099705b07c2fd02f8da6ee8dbd753570d569ed37ddfbfff81dc73bcf1d915dd2`  
		Last Modified: Tue, 07 Apr 2026 09:58:58 GMT  
		Size: 7.6 KB (7621 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5405174ef21fd4e69ca353ffd98030740392f14d291ee95ce6bf815f416bbb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114335802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bd7241991a5f28be04fd946fbc34af194b0bf7a815eca13afb5dd6682f10e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4487.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4487.tar
# Wed, 15 Apr 2026 20:43:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 23:51:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a7f3c6c466d8b59f9a103cde6bc7628a0057e9d800bfdd5f06ee656d07ed9a7`  
		Last Modified: Mon, 13 Apr 2026 04:43:37 GMT  
		Size: 41.1 MB (41145053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f07b4f43f880fa2a19a5b25906c31b8fa10386bda422165111b0fa1f377c5`  
		Last Modified: Mon, 13 Apr 2026 04:43:39 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8ce8e664329b3e5cce2e99d01feecb396d0a720b4aadb5f84e0007779982f2`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 22.6 MB (22597584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff452ea2b8aa8fc6b12e19cebad9c32d2a9859675517d9ef48fdedde178002d2`  
		Last Modified: Wed, 15 Apr 2026 23:51:38 GMT  
		Size: 50.6 MB (50592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3758525685fff25710a5be8fb865dc01db20b829ed24eaddf95330edf493d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517f4eb7f92f628a42a6166b21fb1d79c76b9c329c4c4a9189b557a3578a54c5`

```dockerfile
```

-	Layers:
	-	`sha256:02bcabbbf19929e93b6fc4716f55e3d48ae4c36827bf0b0a6da4ec75011d8f83`  
		Last Modified: Wed, 15 Apr 2026 23:51:37 GMT  
		Size: 7.2 MB (7220614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9249682a25d4566be498954c822a965ab2bf5297c2e904b5baaff3cdab01ae9`  
		Last Modified: Wed, 15 Apr 2026 23:51:36 GMT  
		Size: 7.6 KB (7589 bytes)  
		MIME: application/vnd.in-toto+json
