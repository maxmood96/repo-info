## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:156bbc18c945cc15e57a53005229b6c26dd09f60d7247a2033a3e801e2f5cacc
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fba312212535595ce8df4bf4364eb2c4a83c82d53acdfcdad11673285c4f073c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43336598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4af34cc749c7026753d4f237a806226a0bc2e3a614ad04a917240f70927af2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1521653fda6cd0a5792ccce948424ec895da66a78dd341dd761cf5d863079a6c`  
		Last Modified: Tue, 03 Jun 2025 04:15:43 GMT  
		Size: 13.6 MB (13621261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4fad6e2aed581ddb8ef0027508d46377a69d1c1b6dc1370f363db2039ecf0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2492279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927b48055b9a6e56158b09982cd1b58c2f5ccc3aefc0630bbfc1bb46c95ff9c7`

```dockerfile
```

-	Layers:
	-	`sha256:92165cd154cbd2f019da31dbb01949073784213b8b4d0fca60e3912b24304c8d`  
		Last Modified: Tue, 03 Jun 2025 04:15:42 GMT  
		Size: 2.5 MB (2485320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14f47ed7d17eda788cbfde54067c0a67b876e02b71630a8f51679bac7af72f4`  
		Last Modified: Tue, 03 Jun 2025 04:15:42 GMT  
		Size: 7.0 KB (6959 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f3192ba8c82ad2c4ffe5d3f718a444b30fab76cc74099d3917eb7098af7974de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39622789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34d60f48f6ad02053c45ee94cbb022ef419a5eeee321d60b0f019534b4059c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f5b71e3353c1f92a265c88e163d98b6fc00235db4d001763328933c4838f3576 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76393e3f1626a318c4984c6e6d91f17fe6888451b277b6cc175eab3a1032ebf5`  
		Last Modified: Thu, 29 May 2025 06:11:44 GMT  
		Size: 26.8 MB (26842221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca74547492ebc6726e0a1ef9887a16bf144497b7eff9f2f4d1b9b96fd524d65`  
		Last Modified: Tue, 03 Jun 2025 04:16:36 GMT  
		Size: 12.8 MB (12780568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72f179f4b14bbbffd1fd7cf070cf6d071d08e207068b7ed155bf3e396bcfe6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a7ea161697b5cf2afe72060c9da794edd1061d27c6499dd595c49982161de2`

```dockerfile
```

-	Layers:
	-	`sha256:be1fba116274223bb22b3c0c9b114786129d05e3f01ee5bad87633cdf1fc3ba3`  
		Last Modified: Tue, 03 Jun 2025 04:16:35 GMT  
		Size: 2.5 MB (2487624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4a3fe4050198c96e5730f5890e4ac25aa8a9f46c8de76c31dc04f8617e02d9`  
		Last Modified: Tue, 03 Jun 2025 04:16:35 GMT  
		Size: 7.0 KB (7019 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:97c5a349f3ac105edb2c473f014ec844a937379f5024ddbf5f7ea004b48f136d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42308134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc0537eeb2fb0d19ad30c489cbc16808696439c59eda36584b8ca1f98068e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b69317717db81c94bb0365bd720346e2a43a6b03173cf89d340cc19a993286`  
		Last Modified: Tue, 03 Jun 2025 04:17:41 GMT  
		Size: 13.5 MB (13456235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4750fec23bd664a1b466f61a7d41fc154f2ae70c67b9b596c7f977306e8166be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2493417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2450525ccc2c74307bfd44386247eea106e240c19dcc198e70a3af65cd556b94`

```dockerfile
```

-	Layers:
	-	`sha256:708e8ebd7ed65e5c66edd99ac2dba35659ea5e58a30342ba42a888f6ee714a9b`  
		Last Modified: Tue, 03 Jun 2025 04:17:41 GMT  
		Size: 2.5 MB (2486378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4feccb7c4fa74f6806332c05059dfcd893f81803db2964e09027805365c7e083`  
		Last Modified: Tue, 03 Jun 2025 04:17:40 GMT  
		Size: 7.0 KB (7039 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:207696ff78cf8f387646484c417d105098635a3799e66fa711e8ae46f9fe2c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50279393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f444900fcd09987294249991d4897f47835d02ba5ffa4e7eb842dd9d6598aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Thu, 29 May 2025 06:11:52 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b8bfbc006efc56c6755ed0088bc7e2319e113b78600a3ddbd68b5426fba260`  
		Last Modified: Tue, 03 Jun 2025 04:17:18 GMT  
		Size: 16.0 MB (15954183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a78989cc3b05d4a560de87fb5a3713a70963a39684eb7d141bf29f130785ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a327497f269020b011dc1775464520de753f94daaaf4d9dc329d57faf14f648`

```dockerfile
```

-	Layers:
	-	`sha256:0e1b1d27762021877de895ffb4ebdb9854bbad0107b5073a40a194d34abd3886`  
		Last Modified: Tue, 03 Jun 2025 04:17:18 GMT  
		Size: 2.5 MB (2489939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0dbaa80d518ce0a0af1df4ca49115275d7d229415c0e146c3d6fd769942fee`  
		Last Modified: Tue, 03 Jun 2025 04:17:18 GMT  
		Size: 7.0 KB (6990 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c1f076925d9bc7c4028b0ebf22d9c9219a9965ba14d688eb9b347f5c6dd87ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45275482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7f40fe90822b4443eb7c0b35f63e242a551bfd1c1db08cc588cb3bc6e4d84f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Thu, 29 May 2025 06:11:59 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f34a9ec93701ff69dabbd7cfb519ee4f1c3aea72d284f88712f56d2d510da2`  
		Last Modified: Tue, 03 Jun 2025 04:20:54 GMT  
		Size: 14.3 MB (14327998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5f2360d612b6a8400d38125b1aa7fbb4b5b53b036bfb676ee57bbe499d80789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d667de38360c0ecf1733d40ab5f23bf77e2b8fb463378893a82599a8ad7bc319`

```dockerfile
```

-	Layers:
	-	`sha256:f139a6b9f18cd922638cf021bb0fdef19330426bcb9ecc26e9b916cead5e212d`  
		Last Modified: Tue, 03 Jun 2025 04:20:52 GMT  
		Size: 2.5 MB (2479219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bcdf24c48956f74adb318b3afa245ad0dd3f22ea47b6cbd27ead0c0b04e2031`  
		Last Modified: Tue, 03 Jun 2025 04:20:51 GMT  
		Size: 7.0 KB (6991 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d82c5aff1800a2f8c723bf605918ef3370d8f1c4c2d22c96ea03cd112d70a81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44868041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e32a19f01416b94efc5ae2e42d3f67ffba68d999c4fb0a345f786ac7d05e672`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Thu, 29 May 2025 06:12:06 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de52c2fdeab987f45f86ba773c7a796e45606740580a41f52ad841cf7937f80`  
		Last Modified: Tue, 03 Jun 2025 04:16:39 GMT  
		Size: 14.9 MB (14937985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa6aef7c07e9800d8cbb5c09a765ccebe0ebfe44575af32b8580ab72e41dedf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c4d6f2ffb37d6706cfb65f1f2026290b80db4ce792668d87de40cb4220f885`

```dockerfile
```

-	Layers:
	-	`sha256:0bc95c7adfc2cad97f9670d00fc417839d0a369b057b69e5ecd8f069c100b5c3`  
		Last Modified: Tue, 03 Jun 2025 04:16:39 GMT  
		Size: 2.5 MB (2488145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5246935068512df930cfaf2577a9c97665a2d6db9b6f49904bcb062a2fcbffb9`  
		Last Modified: Tue, 03 Jun 2025 04:16:39 GMT  
		Size: 7.0 KB (6958 bytes)  
		MIME: application/vnd.in-toto+json
