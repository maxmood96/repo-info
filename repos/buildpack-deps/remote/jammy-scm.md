## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:fb086168f02bf0eeb30506554fd023b41cdb60408979582773228d6fd6f68065
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
$ docker pull buildpack-deps@sha256:d8949b2a51fba36ee65a9b205ae804c2c9f452a5a3e324edc26dafdf60158cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76329965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199f92403c329219e5aff4900b615a385631490920192859de3d264aeca37250`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:04:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678f5d5bd853ac3377b342817069c80171f8554b28f23a90374f267e96ca3b6`  
		Last Modified: Wed, 01 Apr 2026 20:05:00 GMT  
		Size: 7.1 MB (7105295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea596a0024b4f21c48bd688bc647b96f1041da01cf615c25cfe8e5b4d8165804`  
		Last Modified: Wed, 01 Apr 2026 20:25:28 GMT  
		Size: 39.5 MB (39488257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:748dbea62f0087d72720e67c5f4efb645aa35414c33f4b94b6380f67b36f74c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5819979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10830b9bf417de0f7e01b18ae50320bb333c6905d5314813a541d6bd8580d8ca`

```dockerfile
```

-	Layers:
	-	`sha256:90d8e4b17b78395839e9c7207805e351b9e550322f9dbf6127ed589d1368734d`  
		Last Modified: Wed, 01 Apr 2026 20:25:27 GMT  
		Size: 5.8 MB (5812698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53f9bdc8a094fde9618a76717632e603d9c4f2744da35768f862ed005e53fe3`  
		Last Modified: Wed, 01 Apr 2026 20:25:27 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9238d07841bde34556f2f889ad71fb69e3600611eb96d407cafd59da613538c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76121294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21e938a190f2e2546db0d9587b51caa1bbaa068acb71efebc7a1a9d1e620a79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:eaa1e345a925acc7b826effa9fb4c3dfb4aebe47807533938898d49afe7561cb in / 
# Sun, 22 Mar 2026 18:14:12 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e7c88f36edd2a67246005d083413bd656459d3b63bab8e6a05a1018c7658daae`  
		Last Modified: Sun, 22 Mar 2026 18:43:39 GMT  
		Size: 26.8 MB (26842286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea32eae6e70821cf7c87d1558f27873f18b23a676f23d22ea0004e4ffdc5f34b`  
		Last Modified: Wed, 01 Apr 2026 20:07:12 GMT  
		Size: 7.0 MB (7009221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627d4bae11c9e08e9baced9969c31850c54260b3e95ee4758efd2d2a173915a`  
		Last Modified: Wed, 01 Apr 2026 21:04:34 GMT  
		Size: 42.3 MB (42269787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1434574566d4922da2a2deb25897655868b726bfa9632219aaf477cadd43a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7463895765f257d00c7bf5823f6ef083158995e71288317e6d3c50864c946b`

```dockerfile
```

-	Layers:
	-	`sha256:8b97d118663c3cb73d371acd40a554efca046c04de467a78f05bb994b54df688`  
		Last Modified: Wed, 01 Apr 2026 21:04:33 GMT  
		Size: 5.8 MB (5813978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ccdff0fdf839a40b1b00ec1af26b4e2fddb663bc46f470fed672907d0846a8f`  
		Last Modified: Wed, 01 Apr 2026 21:04:34 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b054b98dc721d00b84f89c423a20356a6ea1541e709a853c831f62444836d65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74077606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b0c150900754b9ce1f3a56d12716223d15768d2e2cf195da7c59167b828f80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9b1f87458950c0fcd1b5032f566542c2039fc1ae78138539563c4ff4c9be88`  
		Last Modified: Wed, 01 Apr 2026 20:05:12 GMT  
		Size: 7.1 MB (7059304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0539ec4146d528c8266d57fd46154d1a94c1986f84ac826d7944ff6762689b0`  
		Last Modified: Wed, 01 Apr 2026 20:22:53 GMT  
		Size: 39.4 MB (39411359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:427d09f659a58b720241f2811c3ce8e0cbd5c435197a2690fd709f2548dc47a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9456bafab2834d5af27f8ecf6c4ada6d00645f7b44f8dc060433793e19efc0b`

```dockerfile
```

-	Layers:
	-	`sha256:18d128e3ec20234bdd69913f2169f2347b6d1eacea841a9335a35318c505147c`  
		Last Modified: Wed, 01 Apr 2026 20:22:52 GMT  
		Size: 5.8 MB (5819092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb028a2262b08c37c36fd88e57328d57e5a2b1b1c8a3c4e9a3679328e582fd15`  
		Last Modified: Wed, 01 Apr 2026 20:22:52 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6284e17a62746574bf000eb29ac49db1b74ee451ce8cb6952d2eb53e0538d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86610853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c272623921fc2a395ba18243ac7cfca46a9fe2daec2de2705ef36d4cdeabccf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:17:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:04:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0601ddb68d9444803d7b9a76e5d2436faf60ed8c2386c2a288e3a6cf2c5b1bd8`  
		Last Modified: Wed, 01 Apr 2026 20:18:04 GMT  
		Size: 8.2 MB (8184752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe312746e23513aa8b501b29df5132b1a06d932842a57ac9f30bb4e031303f82`  
		Last Modified: Wed, 01 Apr 2026 21:05:02 GMT  
		Size: 43.8 MB (43776441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1de8d0727ac4f61db2049fff00f098bb1eb43b022b46bccc261c76a9b08e6421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34116265a7830ddc0defce60ffceaea1e3c4b71a5f125a248cd7cd5eba7cce8`

```dockerfile
```

-	Layers:
	-	`sha256:fbeabab7343f1171e0f7a64d35f9c4cfacaf3655d85e34c68d60654595bd1818`  
		Last Modified: Wed, 01 Apr 2026 21:05:00 GMT  
		Size: 5.8 MB (5820542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12f01171feab1f583f4f0912406efd60384ef681b5c072d9313d4c31f84ad7a`  
		Last Modified: Wed, 01 Apr 2026 21:04:59 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:95133ecf20198d3562f4621061446a8097faf9f4ce4de52bfdb21ad9a05adba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76667870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3587668bc9e2c8106fe9894da2a980d52de143d1c9779c548da0d62ffebd100`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:32:30 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:32:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:32:31 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:33:10 GMT
ADD file:cef4de62251709bb7b835e063bc33adeb6a0fff04ccc75dc4822972fe4b3c892 in / 
# Sun, 22 Mar 2026 18:33:14 GMT
CMD ["/bin/bash"]
# Thu, 02 Apr 2026 16:14:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Apr 2026 17:13:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8b5ae14641591653bb3f51ef85e2794ecf70f68429e0388fc2292269c97d806c`  
		Last Modified: Sun, 22 Mar 2026 18:43:53 GMT  
		Size: 27.2 MB (27241072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b600eb68ff8d6a9d6795092227c9b7a3b32cfbe3f5f5592dbec2c7605106cabf`  
		Last Modified: Thu, 02 Apr 2026 16:15:16 GMT  
		Size: 7.1 MB (7118638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c2144835325c38a77d02e8c16c5fff64c4d763f84d7f9d6dde3d41f2be94ed`  
		Last Modified: Thu, 02 Apr 2026 17:16:05 GMT  
		Size: 42.3 MB (42308160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51b0d1d1a2b4e1e045a5a21f87fd251943a707d134b8f183e80f0781b78ac8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62f6f9b61d6ed021449c801fce29e843af609a83db4a08d1e2dae80f8711b21`

```dockerfile
```

-	Layers:
	-	`sha256:0d6cd30d1e1ce95dd6de3636196bb8b3ae3154a74acc947687b00c7e27bd3398`  
		Last Modified: Thu, 02 Apr 2026 17:15:59 GMT  
		Size: 5.8 MB (5803084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84d0eeb921ca10a3ee3006b7bbee76c5b77ec60e4d173cde95215ec8dfc9a5a`  
		Last Modified: Thu, 02 Apr 2026 17:15:58 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b927893f7bb4e8c9b425a5473247ff75513bde17b048b8654e6bdb7645653692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74635279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323475b89d67564ab7a7f73f0a573576c94ab0804bf93f94c9ba189bfc6c0722`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:12:49 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:12:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:12:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:12:50 GMT
ADD file:e6d9716e3c60256d600998c1e662d7bc5ced705020e73df5a8f8327ed250efa1 in / 
# Sun, 22 Mar 2026 18:12:51 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 21:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7db076360428795a3bedb94abf5c7d3527328da728852f1fa3e28cc99bb96eba`  
		Last Modified: Sun, 22 Mar 2026 18:44:00 GMT  
		Size: 28.2 MB (28202727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390ee8e0bfba66d347e5a4dfdf7c3593fa25dad79673b32e42c9804ef0045bf7`  
		Last Modified: Wed, 01 Apr 2026 20:08:46 GMT  
		Size: 7.0 MB (7017251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a823e8aff4afaeef54bc758462fe7878f439191257bf21fccd213dec6b7a1c93`  
		Last Modified: Wed, 01 Apr 2026 21:08:40 GMT  
		Size: 39.4 MB (39415301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e2f4db7fb0b8ef77052eb8a7fdd821daf2cdcabb4f2057c258ce67913cdec33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9108e699530c57ab7a1ee5dfd408579a5c7e1b81125dab7e9e34f23a501acf7c`

```dockerfile
```

-	Layers:
	-	`sha256:86361af3759fe785732398445a8ea0c7d52959d0f7f7978657fc5b628fa1ebcc`  
		Last Modified: Wed, 01 Apr 2026 21:08:33 GMT  
		Size: 5.8 MB (5813617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e272ca5dd339ba0e8ae27ed52e58b83ebaf6abda87484d2daea5a9a95ff9e620`  
		Last Modified: Wed, 01 Apr 2026 21:08:29 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
