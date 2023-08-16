<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230801`](#ubuntufocal-20230801)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230804`](#ubuntujammy-20230804)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230731`](#ubuntulunar-20230731)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20230807.1`](#ubuntumantic-202308071)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:33a5cc25d22c45900796a1aca487ad7a7cb09f09ea00b779e3b2026b4fc2faba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:3246518d9735254519e1b2ff35f95686e4a5011c90c85344c1f38df7bae9dd37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df89402372646d400cf092016c28066391a26f5d46c00b1153e75003465484d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaedc954fb53f42a7754a6e2d1b57f091bc9b11063bc445c2e325ea448f8f68`  
		Last Modified: Tue, 01 Aug 2023 06:54:06 GMT  
		Size: 27.5 MB (27506442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:993dc9215facb1278d78c1ac9aacaf0b10ce01a3319245477b526fb49bb3a85b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9647c2503ec334ee47dc65a547a14f79543680a640b31669e4e417949c03857b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:45 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:49 GMT
ADD file:60aa8465a6ba5538decc41365cc9b78ae86131e8c2cfc9177b4a336354ead988 in / 
# Tue, 01 Aug 2023 06:16:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d2b6ba5e7ade25cef0db07ca410b7d5e09085b9c442b62904956cd4d5a81ad10`  
		Last Modified: Tue, 01 Aug 2023 06:54:18 GMT  
		Size: 23.6 MB (23612645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:af43d52ea8f98c8ab92858a37b87be1805ce16f5300cb38b9958e63ac6b25902
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c9d636caddd81490d58a714937f112702f9239c98950221e9fd0dd9735df9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:82d728d38b98752cba7d2d7af8ee1cfe67ccdc5915814420650e78def5d1cebc`  
		Last Modified: Tue, 01 Aug 2023 06:54:12 GMT  
		Size: 26.0 MB (25974619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a305c3951a3741555d5019870f4827c4becdcc95df539ce7ed364ab5ab2db342
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92643ae09f6e607311cb05e4f0f7679c0873b7e4c235e1b57f5e409cfc47c50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fa78ce4014add322eddde3378405efe21c85e886c0195e18533d5991d5477833`  
		Last Modified: Tue, 01 Aug 2023 06:54:25 GMT  
		Size: 32.1 MB (32070704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:5ad386cefcdbd1248f73a3bbcfbf529f39864dddcf9497d9a705540afd23e6e9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26351280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5079141aa115a82eb5f952b45f4cf336075d4dc4bc3ea2cfdab4351497d2fc9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:773e1d05400f41114172ea2dbaa16f037c5812b7d1092cbf0df5d19e69586402`  
		Last Modified: Tue, 01 Aug 2023 06:54:31 GMT  
		Size: 26.4 MB (26351280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:ec050c32e4a6085b423d36ecd025c0d3ff00c38ab93a3d71a460ff1c44fa6d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:56887c5194fddd8db7e36ced1c16b3569d89f74c801dc8a5adbf48236fb34564
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f29b872827fa6f9aed0ea0b2ede53aea4ad9d66c7920e81a8db6d1fd9ab7f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b237fe92c4173e4dfb3ba82e76e5fed4b16186a6161e07af15814cb40eb9069d`  
		Last Modified: Fri, 04 Aug 2023 05:10:57 GMT  
		Size: 29.5 MB (29536501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c835a4f2a632bc91a2b494e871549f0dd83f2966c780e66435774e77e048ddf0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6030a449cb880d2fb07b1f96e5df80e5abf6240abed0917e1a0b949a02b76df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:19 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:24 GMT
ADD file:ca783750060711e8590ab362921bae8d7b02201c48fa3d2cb3fdf6aac045a793 in / 
# Fri, 04 Aug 2023 05:03:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:686ea46a78e6eee8c5e5d3ebd3869c61c6d6cfc8a08e1ebbefb0e08d03d0c7b2`  
		Last Modified: Fri, 04 Aug 2023 05:11:10 GMT  
		Size: 26.1 MB (26142375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cf3cc0848a5d6241b6218bdb51d42be7a9f9bd8c505f3abe1222b9c2ce2451ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f229f811bf715788cc7dae1fbe8f1d9146da54d3fbe2679ef6f230e38ea504`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db76c1f8aa176de7f2698c761088ac1e18cdbbafa6210e405f310221c7a9ea6a`  
		Last Modified: Fri, 04 Aug 2023 05:11:04 GMT  
		Size: 27.3 MB (27347607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da591ce0097593c4fc9934a6021317c39ec79272c49b05eb7f3f43cdc7885b87
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bf720957bcaf3e9dcc5ebf9bbccc2d60c661f0a45d0bf9d338094cc541b3e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6140760330bb52aa780087331e6207156dc1d36e412010f0de6faacee7817be`  
		Last Modified: Fri, 04 Aug 2023 05:11:17 GMT  
		Size: 34.6 MB (34590887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:2e71c457ff50fc8cf0ba846758e46dceca41b1f0776e1ac5a7b487de7ae60cde
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28013360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ff41546d1ecc2c5cfb5164f13df3dafe7cdb3e64da3f1f85c9b8bc2b8cec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bdf265a933ffdd52ec28f006765d35d4119c012d520b564de8ea1b8cdc6c269f`  
		Last Modified: Fri, 04 Aug 2023 05:11:24 GMT  
		Size: 28.0 MB (28013360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:7a520eeb6c18bc6d32a21bb7edcf673a7830813c169645d51c949cecb62387d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:3787e67b05ccc44d64b821470510a551eea6a2887c8e60379aca0e2fecaff599
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26840088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24881e92d6487bb77608e410fd9efa9aad6851112ab6500faa3a04bd72da5b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:16:11 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:16:12 GMT
ADD file:3ff011e7c817c9b010391c2b2f74a111d8c37165e6fdff18e18ccfa67ff7667b in / 
# Mon, 31 Jul 2023 17:16:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:03b3dca73f874f81f3e85e8b2df9f05c9f336bd15283a7d099040703fb204279`  
		Last Modified: Mon, 31 Jul 2023 17:39:26 GMT  
		Size: 26.8 MB (26840088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:02d4ef011cf12f8ee9addd2b6ab8fb7395f5e70b314fae9fc7cd55ef69bbdd9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24640558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fbdc2dd1107e4f9d06544ba6dc55d0b350113020b70f35852036991db7d5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:20:03 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:20:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:20:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:20:04 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:20:13 GMT
ADD file:3ec1cc20b36a86b78ff00125a182fab6d7ee8916dbdc6f52d40e182e2892dd06 in / 
# Mon, 31 Jul 2023 17:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b90fd1c5c84e67c72256cf32c741235e1afdc37bac915942134aaefb9364fec`  
		Last Modified: Mon, 31 Jul 2023 17:39:39 GMT  
		Size: 24.6 MB (24640558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:33a3158bf45e9e08d5fed2e6d93efb903156fcaba229f9923f151374bfbc6c94
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5956ca9d3275e20c813c20ddc5b86374d74bfc99bf0564dd6bd0a1e6a955ee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:24:02 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:24:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:24:11 GMT
ADD file:8af4f6767fc5b6665bedd4600c0601ee7d7f803de51e979a40bd3d6ebcd25f95 in / 
# Mon, 31 Jul 2023 17:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c0fc7a9f17ab38a3150f437abbf01140c32288aee7c84142c05295ecc002c85`  
		Last Modified: Mon, 31 Jul 2023 17:39:33 GMT  
		Size: 26.1 MB (26088468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9aebdde7682dbe06c885cf890f2e43a183c05803bff1f2b8464a187dc1b00b58
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31030701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad38d0665b88ca462694ffe4f53d6f572c4e77af16e64c111617df4668bbc75e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:18:51 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:18:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:18:54 GMT
ADD file:98fe279e3c3239702ac2eef51540228e24a3e15e923342cb3e7cd7dd3684a090 in / 
# Mon, 31 Jul 2023 17:18:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4e756d02ae4b4a4f9c9ebdc2ca11b9d859b96365868ba69442d2cb7158a5f827`  
		Last Modified: Mon, 31 Jul 2023 17:39:45 GMT  
		Size: 31.0 MB (31030701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:e6e00642db98617858caf8fc519710225eb0ae7099e6133c3d559a7cbbcdd2b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25717049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748eb92545cf245d6d5121803154031c63fbb4bf1dd8dee43cbc8847fd58ca35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:25:09 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:25:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:25:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:25:10 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:25:11 GMT
ADD file:02e6a6123ef99d36f86e3e53231b3ba93c90b4ac9fc0bdebe8f01f2a6c2efb4e in / 
# Mon, 31 Jul 2023 17:25:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:052de6ce81fd1abe2b7bd745faefd555b3e282e8fe2e611a52243f2179b7ea38`  
		Last Modified: Mon, 31 Jul 2023 17:39:51 GMT  
		Size: 25.7 MB (25717049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:4ece736cc64e12426819d31e82f17f81555148adc3093474908ca1df00222d62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:fe7c495a4f1d2e1d86a9644ea5963370674a9894e273e34e96896bcde63441ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27104601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1909bc6bc56b0a4ba4a50a33b4c27844fcab405b08eeb26b754ff4f1fcc36471`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:39:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:39:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:39:21 GMT
ADD file:c60b0770f6d1b35b4aba7ba0dceda2ee3453c09729d8640394a8fe388cb7932e in / 
# Mon, 07 Aug 2023 16:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd9cd860ef0ae602a40fdac6afd89d42f87a1a93dd70a90c07ae53f12f5fb022`  
		Last Modified: Mon, 07 Aug 2023 17:17:15 GMT  
		Size: 27.1 MB (27104601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d6d749318702da4223ac8deed60a4a9e9902f10aaba085486b67028eb237c0ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24654154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a48698bc6e604a3f75ab9bfc02a5b699bc5fdbb1bbf4e0aaa81a1d7fc0b439`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:43:12 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:43:20 GMT
ADD file:443a623a513d24fb17f92fecba92ab4b48c5cd58f4c71a4d1017f68cb28ed803 in / 
# Mon, 07 Aug 2023 16:43:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7384d9310f28ea2b7133f7446a72d62a93acda872b1e77361d3764cf8fe7b76`  
		Last Modified: Mon, 07 Aug 2023 17:17:29 GMT  
		Size: 24.7 MB (24654154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2a091f203ef368cd928dbd321be09448a30be52ddb17cb5b733e381206a9dec2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26304973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05b71631b7da894ff1926c05af25f1a6bb9d6054cd7ec150f031e6f62d953bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:59:38 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:59:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:59:47 GMT
ADD file:a621d5a90b1c5e05eb41dfa44616425f9e9c474acc76e148c36a525e99ff2bac in / 
# Mon, 07 Aug 2023 16:59:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f55d0f45237d17adcf4039963cc7ac0b6044348e89458f35c79d1a4a4aa62ad`  
		Last Modified: Mon, 07 Aug 2023 17:17:22 GMT  
		Size: 26.3 MB (26304973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:6c2eec01baef54b81a0a11aa340839d376aea2d2ec4f86d0529741533ef319a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cc3aafb4d9af81aeba0dd2bfeb9cb503b509c71f0278fb315af4f9903ff09f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:57:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:57:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:57:23 GMT
ADD file:4cb180718bb451f8c264f3c3ca17e21c2f353537e1350e7285186274e7c13aa1 in / 
# Mon, 07 Aug 2023 16:57:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e5976a7e300ece0ea0e1b134f66c311c8904a278eb1019c4997473190259ec8`  
		Last Modified: Mon, 07 Aug 2023 17:17:36 GMT  
		Size: 31.2 MB (31228462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:840aad7a3257d4ef41010f4580b5480a50ca322d56bf91405ef9c1bab8325e88
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26346739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8b4d20ddafc69b78425aa7c5c2cf679f9000364b92a086b46ff8e9cf59db3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:41:40 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:41:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:41:42 GMT
ADD file:7038e8b287279d65872808b33572bb449a981ceacdc4533e8e1047544044f524 in / 
# Mon, 07 Aug 2023 16:41:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e93f2054f5bc941ef3ea4037dce53f6fefca8d79721782c090dc34fb1c96569`  
		Last Modified: Mon, 07 Aug 2023 17:17:42 GMT  
		Size: 26.3 MB (26346739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:4ece736cc64e12426819d31e82f17f81555148adc3093474908ca1df00222d62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:fe7c495a4f1d2e1d86a9644ea5963370674a9894e273e34e96896bcde63441ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27104601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1909bc6bc56b0a4ba4a50a33b4c27844fcab405b08eeb26b754ff4f1fcc36471`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:39:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:39:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:39:21 GMT
ADD file:c60b0770f6d1b35b4aba7ba0dceda2ee3453c09729d8640394a8fe388cb7932e in / 
# Mon, 07 Aug 2023 16:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd9cd860ef0ae602a40fdac6afd89d42f87a1a93dd70a90c07ae53f12f5fb022`  
		Last Modified: Mon, 07 Aug 2023 17:17:15 GMT  
		Size: 27.1 MB (27104601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d6d749318702da4223ac8deed60a4a9e9902f10aaba085486b67028eb237c0ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24654154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a48698bc6e604a3f75ab9bfc02a5b699bc5fdbb1bbf4e0aaa81a1d7fc0b439`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:43:12 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:43:20 GMT
ADD file:443a623a513d24fb17f92fecba92ab4b48c5cd58f4c71a4d1017f68cb28ed803 in / 
# Mon, 07 Aug 2023 16:43:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7384d9310f28ea2b7133f7446a72d62a93acda872b1e77361d3764cf8fe7b76`  
		Last Modified: Mon, 07 Aug 2023 17:17:29 GMT  
		Size: 24.7 MB (24654154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2a091f203ef368cd928dbd321be09448a30be52ddb17cb5b733e381206a9dec2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26304973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05b71631b7da894ff1926c05af25f1a6bb9d6054cd7ec150f031e6f62d953bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:59:38 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:59:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:59:47 GMT
ADD file:a621d5a90b1c5e05eb41dfa44616425f9e9c474acc76e148c36a525e99ff2bac in / 
# Mon, 07 Aug 2023 16:59:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f55d0f45237d17adcf4039963cc7ac0b6044348e89458f35c79d1a4a4aa62ad`  
		Last Modified: Mon, 07 Aug 2023 17:17:22 GMT  
		Size: 26.3 MB (26304973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:6c2eec01baef54b81a0a11aa340839d376aea2d2ec4f86d0529741533ef319a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cc3aafb4d9af81aeba0dd2bfeb9cb503b509c71f0278fb315af4f9903ff09f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:57:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:57:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:57:23 GMT
ADD file:4cb180718bb451f8c264f3c3ca17e21c2f353537e1350e7285186274e7c13aa1 in / 
# Mon, 07 Aug 2023 16:57:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e5976a7e300ece0ea0e1b134f66c311c8904a278eb1019c4997473190259ec8`  
		Last Modified: Mon, 07 Aug 2023 17:17:36 GMT  
		Size: 31.2 MB (31228462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:840aad7a3257d4ef41010f4580b5480a50ca322d56bf91405ef9c1bab8325e88
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26346739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8b4d20ddafc69b78425aa7c5c2cf679f9000364b92a086b46ff8e9cf59db3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:41:40 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:41:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:41:42 GMT
ADD file:7038e8b287279d65872808b33572bb449a981ceacdc4533e8e1047544044f524 in / 
# Mon, 07 Aug 2023 16:41:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e93f2054f5bc941ef3ea4037dce53f6fefca8d79721782c090dc34fb1c96569`  
		Last Modified: Mon, 07 Aug 2023 17:17:42 GMT  
		Size: 26.3 MB (26346739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:33a5cc25d22c45900796a1aca487ad7a7cb09f09ea00b779e3b2026b4fc2faba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:3246518d9735254519e1b2ff35f95686e4a5011c90c85344c1f38df7bae9dd37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df89402372646d400cf092016c28066391a26f5d46c00b1153e75003465484d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaedc954fb53f42a7754a6e2d1b57f091bc9b11063bc445c2e325ea448f8f68`  
		Last Modified: Tue, 01 Aug 2023 06:54:06 GMT  
		Size: 27.5 MB (27506442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:993dc9215facb1278d78c1ac9aacaf0b10ce01a3319245477b526fb49bb3a85b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9647c2503ec334ee47dc65a547a14f79543680a640b31669e4e417949c03857b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:45 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:49 GMT
ADD file:60aa8465a6ba5538decc41365cc9b78ae86131e8c2cfc9177b4a336354ead988 in / 
# Tue, 01 Aug 2023 06:16:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d2b6ba5e7ade25cef0db07ca410b7d5e09085b9c442b62904956cd4d5a81ad10`  
		Last Modified: Tue, 01 Aug 2023 06:54:18 GMT  
		Size: 23.6 MB (23612645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:af43d52ea8f98c8ab92858a37b87be1805ce16f5300cb38b9958e63ac6b25902
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c9d636caddd81490d58a714937f112702f9239c98950221e9fd0dd9735df9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:82d728d38b98752cba7d2d7af8ee1cfe67ccdc5915814420650e78def5d1cebc`  
		Last Modified: Tue, 01 Aug 2023 06:54:12 GMT  
		Size: 26.0 MB (25974619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a305c3951a3741555d5019870f4827c4becdcc95df539ce7ed364ab5ab2db342
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92643ae09f6e607311cb05e4f0f7679c0873b7e4c235e1b57f5e409cfc47c50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fa78ce4014add322eddde3378405efe21c85e886c0195e18533d5991d5477833`  
		Last Modified: Tue, 01 Aug 2023 06:54:25 GMT  
		Size: 32.1 MB (32070704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:5ad386cefcdbd1248f73a3bbcfbf529f39864dddcf9497d9a705540afd23e6e9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26351280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5079141aa115a82eb5f952b45f4cf336075d4dc4bc3ea2cfdab4351497d2fc9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:773e1d05400f41114172ea2dbaa16f037c5812b7d1092cbf0df5d19e69586402`  
		Last Modified: Tue, 01 Aug 2023 06:54:31 GMT  
		Size: 26.4 MB (26351280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20230801`

```console
$ docker pull ubuntu@sha256:33a5cc25d22c45900796a1aca487ad7a7cb09f09ea00b779e3b2026b4fc2faba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20230801` - linux; amd64

```console
$ docker pull ubuntu@sha256:3246518d9735254519e1b2ff35f95686e4a5011c90c85344c1f38df7bae9dd37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df89402372646d400cf092016c28066391a26f5d46c00b1153e75003465484d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaedc954fb53f42a7754a6e2d1b57f091bc9b11063bc445c2e325ea448f8f68`  
		Last Modified: Tue, 01 Aug 2023 06:54:06 GMT  
		Size: 27.5 MB (27506442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230801` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:993dc9215facb1278d78c1ac9aacaf0b10ce01a3319245477b526fb49bb3a85b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9647c2503ec334ee47dc65a547a14f79543680a640b31669e4e417949c03857b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:45 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:49 GMT
ADD file:60aa8465a6ba5538decc41365cc9b78ae86131e8c2cfc9177b4a336354ead988 in / 
# Tue, 01 Aug 2023 06:16:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d2b6ba5e7ade25cef0db07ca410b7d5e09085b9c442b62904956cd4d5a81ad10`  
		Last Modified: Tue, 01 Aug 2023 06:54:18 GMT  
		Size: 23.6 MB (23612645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230801` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:af43d52ea8f98c8ab92858a37b87be1805ce16f5300cb38b9958e63ac6b25902
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c9d636caddd81490d58a714937f112702f9239c98950221e9fd0dd9735df9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:82d728d38b98752cba7d2d7af8ee1cfe67ccdc5915814420650e78def5d1cebc`  
		Last Modified: Tue, 01 Aug 2023 06:54:12 GMT  
		Size: 26.0 MB (25974619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230801` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a305c3951a3741555d5019870f4827c4becdcc95df539ce7ed364ab5ab2db342
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92643ae09f6e607311cb05e4f0f7679c0873b7e4c235e1b57f5e409cfc47c50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fa78ce4014add322eddde3378405efe21c85e886c0195e18533d5991d5477833`  
		Last Modified: Tue, 01 Aug 2023 06:54:25 GMT  
		Size: 32.1 MB (32070704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230801` - linux; s390x

```console
$ docker pull ubuntu@sha256:5ad386cefcdbd1248f73a3bbcfbf529f39864dddcf9497d9a705540afd23e6e9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26351280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5079141aa115a82eb5f952b45f4cf336075d4dc4bc3ea2cfdab4351497d2fc9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:773e1d05400f41114172ea2dbaa16f037c5812b7d1092cbf0df5d19e69586402`  
		Last Modified: Tue, 01 Aug 2023 06:54:31 GMT  
		Size: 26.4 MB (26351280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:ec050c32e4a6085b423d36ecd025c0d3ff00c38ab93a3d71a460ff1c44fa6d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:56887c5194fddd8db7e36ced1c16b3569d89f74c801dc8a5adbf48236fb34564
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f29b872827fa6f9aed0ea0b2ede53aea4ad9d66c7920e81a8db6d1fd9ab7f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b237fe92c4173e4dfb3ba82e76e5fed4b16186a6161e07af15814cb40eb9069d`  
		Last Modified: Fri, 04 Aug 2023 05:10:57 GMT  
		Size: 29.5 MB (29536501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c835a4f2a632bc91a2b494e871549f0dd83f2966c780e66435774e77e048ddf0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6030a449cb880d2fb07b1f96e5df80e5abf6240abed0917e1a0b949a02b76df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:19 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:24 GMT
ADD file:ca783750060711e8590ab362921bae8d7b02201c48fa3d2cb3fdf6aac045a793 in / 
# Fri, 04 Aug 2023 05:03:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:686ea46a78e6eee8c5e5d3ebd3869c61c6d6cfc8a08e1ebbefb0e08d03d0c7b2`  
		Last Modified: Fri, 04 Aug 2023 05:11:10 GMT  
		Size: 26.1 MB (26142375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cf3cc0848a5d6241b6218bdb51d42be7a9f9bd8c505f3abe1222b9c2ce2451ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f229f811bf715788cc7dae1fbe8f1d9146da54d3fbe2679ef6f230e38ea504`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db76c1f8aa176de7f2698c761088ac1e18cdbbafa6210e405f310221c7a9ea6a`  
		Last Modified: Fri, 04 Aug 2023 05:11:04 GMT  
		Size: 27.3 MB (27347607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da591ce0097593c4fc9934a6021317c39ec79272c49b05eb7f3f43cdc7885b87
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bf720957bcaf3e9dcc5ebf9bbccc2d60c661f0a45d0bf9d338094cc541b3e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6140760330bb52aa780087331e6207156dc1d36e412010f0de6faacee7817be`  
		Last Modified: Fri, 04 Aug 2023 05:11:17 GMT  
		Size: 34.6 MB (34590887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:2e71c457ff50fc8cf0ba846758e46dceca41b1f0776e1ac5a7b487de7ae60cde
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28013360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ff41546d1ecc2c5cfb5164f13df3dafe7cdb3e64da3f1f85c9b8bc2b8cec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bdf265a933ffdd52ec28f006765d35d4119c012d520b564de8ea1b8cdc6c269f`  
		Last Modified: Fri, 04 Aug 2023 05:11:24 GMT  
		Size: 28.0 MB (28013360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230804`

```console
$ docker pull ubuntu@sha256:ec050c32e4a6085b423d36ecd025c0d3ff00c38ab93a3d71a460ff1c44fa6d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230804` - linux; amd64

```console
$ docker pull ubuntu@sha256:56887c5194fddd8db7e36ced1c16b3569d89f74c801dc8a5adbf48236fb34564
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f29b872827fa6f9aed0ea0b2ede53aea4ad9d66c7920e81a8db6d1fd9ab7f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b237fe92c4173e4dfb3ba82e76e5fed4b16186a6161e07af15814cb40eb9069d`  
		Last Modified: Fri, 04 Aug 2023 05:10:57 GMT  
		Size: 29.5 MB (29536501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230804` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c835a4f2a632bc91a2b494e871549f0dd83f2966c780e66435774e77e048ddf0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6030a449cb880d2fb07b1f96e5df80e5abf6240abed0917e1a0b949a02b76df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:19 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:24 GMT
ADD file:ca783750060711e8590ab362921bae8d7b02201c48fa3d2cb3fdf6aac045a793 in / 
# Fri, 04 Aug 2023 05:03:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:686ea46a78e6eee8c5e5d3ebd3869c61c6d6cfc8a08e1ebbefb0e08d03d0c7b2`  
		Last Modified: Fri, 04 Aug 2023 05:11:10 GMT  
		Size: 26.1 MB (26142375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230804` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cf3cc0848a5d6241b6218bdb51d42be7a9f9bd8c505f3abe1222b9c2ce2451ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f229f811bf715788cc7dae1fbe8f1d9146da54d3fbe2679ef6f230e38ea504`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db76c1f8aa176de7f2698c761088ac1e18cdbbafa6210e405f310221c7a9ea6a`  
		Last Modified: Fri, 04 Aug 2023 05:11:04 GMT  
		Size: 27.3 MB (27347607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230804` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da591ce0097593c4fc9934a6021317c39ec79272c49b05eb7f3f43cdc7885b87
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bf720957bcaf3e9dcc5ebf9bbccc2d60c661f0a45d0bf9d338094cc541b3e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6140760330bb52aa780087331e6207156dc1d36e412010f0de6faacee7817be`  
		Last Modified: Fri, 04 Aug 2023 05:11:17 GMT  
		Size: 34.6 MB (34590887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230804` - linux; s390x

```console
$ docker pull ubuntu@sha256:2e71c457ff50fc8cf0ba846758e46dceca41b1f0776e1ac5a7b487de7ae60cde
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28013360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ff41546d1ecc2c5cfb5164f13df3dafe7cdb3e64da3f1f85c9b8bc2b8cec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bdf265a933ffdd52ec28f006765d35d4119c012d520b564de8ea1b8cdc6c269f`  
		Last Modified: Fri, 04 Aug 2023 05:11:24 GMT  
		Size: 28.0 MB (28013360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:ec050c32e4a6085b423d36ecd025c0d3ff00c38ab93a3d71a460ff1c44fa6d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:56887c5194fddd8db7e36ced1c16b3569d89f74c801dc8a5adbf48236fb34564
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29536501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f29b872827fa6f9aed0ea0b2ede53aea4ad9d66c7920e81a8db6d1fd9ab7f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b237fe92c4173e4dfb3ba82e76e5fed4b16186a6161e07af15814cb40eb9069d`  
		Last Modified: Fri, 04 Aug 2023 05:10:57 GMT  
		Size: 29.5 MB (29536501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c835a4f2a632bc91a2b494e871549f0dd83f2966c780e66435774e77e048ddf0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6030a449cb880d2fb07b1f96e5df80e5abf6240abed0917e1a0b949a02b76df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:19 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:24 GMT
ADD file:ca783750060711e8590ab362921bae8d7b02201c48fa3d2cb3fdf6aac045a793 in / 
# Fri, 04 Aug 2023 05:03:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:686ea46a78e6eee8c5e5d3ebd3869c61c6d6cfc8a08e1ebbefb0e08d03d0c7b2`  
		Last Modified: Fri, 04 Aug 2023 05:11:10 GMT  
		Size: 26.1 MB (26142375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cf3cc0848a5d6241b6218bdb51d42be7a9f9bd8c505f3abe1222b9c2ce2451ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f229f811bf715788cc7dae1fbe8f1d9146da54d3fbe2679ef6f230e38ea504`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db76c1f8aa176de7f2698c761088ac1e18cdbbafa6210e405f310221c7a9ea6a`  
		Last Modified: Fri, 04 Aug 2023 05:11:04 GMT  
		Size: 27.3 MB (27347607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da591ce0097593c4fc9934a6021317c39ec79272c49b05eb7f3f43cdc7885b87
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bf720957bcaf3e9dcc5ebf9bbccc2d60c661f0a45d0bf9d338094cc541b3e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6140760330bb52aa780087331e6207156dc1d36e412010f0de6faacee7817be`  
		Last Modified: Fri, 04 Aug 2023 05:11:17 GMT  
		Size: 34.6 MB (34590887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:2e71c457ff50fc8cf0ba846758e46dceca41b1f0776e1ac5a7b487de7ae60cde
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28013360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ff41546d1ecc2c5cfb5164f13df3dafe7cdb3e64da3f1f85c9b8bc2b8cec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:16 GMT
ADD file:d5b5687c046ca0689ccc4f42ddcc27543404ae2273aa12241e6636a2b3d675df in / 
# Fri, 04 Aug 2023 05:03:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bdf265a933ffdd52ec28f006765d35d4119c012d520b564de8ea1b8cdc6c269f`  
		Last Modified: Fri, 04 Aug 2023 05:11:24 GMT  
		Size: 28.0 MB (28013360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:7a520eeb6c18bc6d32a21bb7edcf673a7830813c169645d51c949cecb62387d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar` - linux; amd64

```console
$ docker pull ubuntu@sha256:3787e67b05ccc44d64b821470510a551eea6a2887c8e60379aca0e2fecaff599
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26840088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24881e92d6487bb77608e410fd9efa9aad6851112ab6500faa3a04bd72da5b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:16:11 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:16:12 GMT
ADD file:3ff011e7c817c9b010391c2b2f74a111d8c37165e6fdff18e18ccfa67ff7667b in / 
# Mon, 31 Jul 2023 17:16:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:03b3dca73f874f81f3e85e8b2df9f05c9f336bd15283a7d099040703fb204279`  
		Last Modified: Mon, 31 Jul 2023 17:39:26 GMT  
		Size: 26.8 MB (26840088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:02d4ef011cf12f8ee9addd2b6ab8fb7395f5e70b314fae9fc7cd55ef69bbdd9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24640558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fbdc2dd1107e4f9d06544ba6dc55d0b350113020b70f35852036991db7d5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:20:03 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:20:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:20:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:20:04 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:20:13 GMT
ADD file:3ec1cc20b36a86b78ff00125a182fab6d7ee8916dbdc6f52d40e182e2892dd06 in / 
# Mon, 31 Jul 2023 17:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b90fd1c5c84e67c72256cf32c741235e1afdc37bac915942134aaefb9364fec`  
		Last Modified: Mon, 31 Jul 2023 17:39:39 GMT  
		Size: 24.6 MB (24640558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:33a3158bf45e9e08d5fed2e6d93efb903156fcaba229f9923f151374bfbc6c94
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5956ca9d3275e20c813c20ddc5b86374d74bfc99bf0564dd6bd0a1e6a955ee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:24:02 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:24:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:24:11 GMT
ADD file:8af4f6767fc5b6665bedd4600c0601ee7d7f803de51e979a40bd3d6ebcd25f95 in / 
# Mon, 31 Jul 2023 17:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c0fc7a9f17ab38a3150f437abbf01140c32288aee7c84142c05295ecc002c85`  
		Last Modified: Mon, 31 Jul 2023 17:39:33 GMT  
		Size: 26.1 MB (26088468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9aebdde7682dbe06c885cf890f2e43a183c05803bff1f2b8464a187dc1b00b58
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31030701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad38d0665b88ca462694ffe4f53d6f572c4e77af16e64c111617df4668bbc75e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:18:51 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:18:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:18:54 GMT
ADD file:98fe279e3c3239702ac2eef51540228e24a3e15e923342cb3e7cd7dd3684a090 in / 
# Mon, 31 Jul 2023 17:18:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4e756d02ae4b4a4f9c9ebdc2ca11b9d859b96365868ba69442d2cb7158a5f827`  
		Last Modified: Mon, 31 Jul 2023 17:39:45 GMT  
		Size: 31.0 MB (31030701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:e6e00642db98617858caf8fc519710225eb0ae7099e6133c3d559a7cbbcdd2b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25717049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748eb92545cf245d6d5121803154031c63fbb4bf1dd8dee43cbc8847fd58ca35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:25:09 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:25:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:25:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:25:10 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:25:11 GMT
ADD file:02e6a6123ef99d36f86e3e53231b3ba93c90b4ac9fc0bdebe8f01f2a6c2efb4e in / 
# Mon, 31 Jul 2023 17:25:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:052de6ce81fd1abe2b7bd745faefd555b3e282e8fe2e611a52243f2179b7ea38`  
		Last Modified: Mon, 31 Jul 2023 17:39:51 GMT  
		Size: 25.7 MB (25717049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230731`

```console
$ docker pull ubuntu@sha256:7a520eeb6c18bc6d32a21bb7edcf673a7830813c169645d51c949cecb62387d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20230731` - linux; amd64

```console
$ docker pull ubuntu@sha256:3787e67b05ccc44d64b821470510a551eea6a2887c8e60379aca0e2fecaff599
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26840088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24881e92d6487bb77608e410fd9efa9aad6851112ab6500faa3a04bd72da5b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:16:11 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:16:12 GMT
ADD file:3ff011e7c817c9b010391c2b2f74a111d8c37165e6fdff18e18ccfa67ff7667b in / 
# Mon, 31 Jul 2023 17:16:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:03b3dca73f874f81f3e85e8b2df9f05c9f336bd15283a7d099040703fb204279`  
		Last Modified: Mon, 31 Jul 2023 17:39:26 GMT  
		Size: 26.8 MB (26840088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230731` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:02d4ef011cf12f8ee9addd2b6ab8fb7395f5e70b314fae9fc7cd55ef69bbdd9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24640558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fbdc2dd1107e4f9d06544ba6dc55d0b350113020b70f35852036991db7d5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:20:03 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:20:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:20:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:20:04 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:20:13 GMT
ADD file:3ec1cc20b36a86b78ff00125a182fab6d7ee8916dbdc6f52d40e182e2892dd06 in / 
# Mon, 31 Jul 2023 17:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b90fd1c5c84e67c72256cf32c741235e1afdc37bac915942134aaefb9364fec`  
		Last Modified: Mon, 31 Jul 2023 17:39:39 GMT  
		Size: 24.6 MB (24640558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230731` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:33a3158bf45e9e08d5fed2e6d93efb903156fcaba229f9923f151374bfbc6c94
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5956ca9d3275e20c813c20ddc5b86374d74bfc99bf0564dd6bd0a1e6a955ee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:24:02 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:24:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:24:11 GMT
ADD file:8af4f6767fc5b6665bedd4600c0601ee7d7f803de51e979a40bd3d6ebcd25f95 in / 
# Mon, 31 Jul 2023 17:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c0fc7a9f17ab38a3150f437abbf01140c32288aee7c84142c05295ecc002c85`  
		Last Modified: Mon, 31 Jul 2023 17:39:33 GMT  
		Size: 26.1 MB (26088468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230731` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9aebdde7682dbe06c885cf890f2e43a183c05803bff1f2b8464a187dc1b00b58
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31030701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad38d0665b88ca462694ffe4f53d6f572c4e77af16e64c111617df4668bbc75e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:18:51 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:18:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:18:54 GMT
ADD file:98fe279e3c3239702ac2eef51540228e24a3e15e923342cb3e7cd7dd3684a090 in / 
# Mon, 31 Jul 2023 17:18:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4e756d02ae4b4a4f9c9ebdc2ca11b9d859b96365868ba69442d2cb7158a5f827`  
		Last Modified: Mon, 31 Jul 2023 17:39:45 GMT  
		Size: 31.0 MB (31030701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230731` - linux; s390x

```console
$ docker pull ubuntu@sha256:e6e00642db98617858caf8fc519710225eb0ae7099e6133c3d559a7cbbcdd2b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25717049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748eb92545cf245d6d5121803154031c63fbb4bf1dd8dee43cbc8847fd58ca35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:25:09 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:25:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:25:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:25:10 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:25:11 GMT
ADD file:02e6a6123ef99d36f86e3e53231b3ba93c90b4ac9fc0bdebe8f01f2a6c2efb4e in / 
# Mon, 31 Jul 2023 17:25:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:052de6ce81fd1abe2b7bd745faefd555b3e282e8fe2e611a52243f2179b7ea38`  
		Last Modified: Mon, 31 Jul 2023 17:39:51 GMT  
		Size: 25.7 MB (25717049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:4ece736cc64e12426819d31e82f17f81555148adc3093474908ca1df00222d62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic` - linux; amd64

```console
$ docker pull ubuntu@sha256:fe7c495a4f1d2e1d86a9644ea5963370674a9894e273e34e96896bcde63441ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27104601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1909bc6bc56b0a4ba4a50a33b4c27844fcab405b08eeb26b754ff4f1fcc36471`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:39:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:39:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:39:21 GMT
ADD file:c60b0770f6d1b35b4aba7ba0dceda2ee3453c09729d8640394a8fe388cb7932e in / 
# Mon, 07 Aug 2023 16:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd9cd860ef0ae602a40fdac6afd89d42f87a1a93dd70a90c07ae53f12f5fb022`  
		Last Modified: Mon, 07 Aug 2023 17:17:15 GMT  
		Size: 27.1 MB (27104601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d6d749318702da4223ac8deed60a4a9e9902f10aaba085486b67028eb237c0ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24654154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a48698bc6e604a3f75ab9bfc02a5b699bc5fdbb1bbf4e0aaa81a1d7fc0b439`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:43:12 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:43:20 GMT
ADD file:443a623a513d24fb17f92fecba92ab4b48c5cd58f4c71a4d1017f68cb28ed803 in / 
# Mon, 07 Aug 2023 16:43:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7384d9310f28ea2b7133f7446a72d62a93acda872b1e77361d3764cf8fe7b76`  
		Last Modified: Mon, 07 Aug 2023 17:17:29 GMT  
		Size: 24.7 MB (24654154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2a091f203ef368cd928dbd321be09448a30be52ddb17cb5b733e381206a9dec2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26304973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05b71631b7da894ff1926c05af25f1a6bb9d6054cd7ec150f031e6f62d953bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:59:38 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:59:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:59:47 GMT
ADD file:a621d5a90b1c5e05eb41dfa44616425f9e9c474acc76e148c36a525e99ff2bac in / 
# Mon, 07 Aug 2023 16:59:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f55d0f45237d17adcf4039963cc7ac0b6044348e89458f35c79d1a4a4aa62ad`  
		Last Modified: Mon, 07 Aug 2023 17:17:22 GMT  
		Size: 26.3 MB (26304973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:6c2eec01baef54b81a0a11aa340839d376aea2d2ec4f86d0529741533ef319a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cc3aafb4d9af81aeba0dd2bfeb9cb503b509c71f0278fb315af4f9903ff09f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:57:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:57:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:57:23 GMT
ADD file:4cb180718bb451f8c264f3c3ca17e21c2f353537e1350e7285186274e7c13aa1 in / 
# Mon, 07 Aug 2023 16:57:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e5976a7e300ece0ea0e1b134f66c311c8904a278eb1019c4997473190259ec8`  
		Last Modified: Mon, 07 Aug 2023 17:17:36 GMT  
		Size: 31.2 MB (31228462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:840aad7a3257d4ef41010f4580b5480a50ca322d56bf91405ef9c1bab8325e88
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26346739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8b4d20ddafc69b78425aa7c5c2cf679f9000364b92a086b46ff8e9cf59db3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:41:40 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:41:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:41:42 GMT
ADD file:7038e8b287279d65872808b33572bb449a981ceacdc4533e8e1047544044f524 in / 
# Mon, 07 Aug 2023 16:41:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e93f2054f5bc941ef3ea4037dce53f6fefca8d79721782c090dc34fb1c96569`  
		Last Modified: Mon, 07 Aug 2023 17:17:42 GMT  
		Size: 26.3 MB (26346739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20230807.1`

```console
$ docker pull ubuntu@sha256:4ece736cc64e12426819d31e82f17f81555148adc3093474908ca1df00222d62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20230807.1` - linux; amd64

```console
$ docker pull ubuntu@sha256:fe7c495a4f1d2e1d86a9644ea5963370674a9894e273e34e96896bcde63441ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27104601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1909bc6bc56b0a4ba4a50a33b4c27844fcab405b08eeb26b754ff4f1fcc36471`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:39:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:39:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:39:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:39:21 GMT
ADD file:c60b0770f6d1b35b4aba7ba0dceda2ee3453c09729d8640394a8fe388cb7932e in / 
# Mon, 07 Aug 2023 16:39:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dd9cd860ef0ae602a40fdac6afd89d42f87a1a93dd70a90c07ae53f12f5fb022`  
		Last Modified: Mon, 07 Aug 2023 17:17:15 GMT  
		Size: 27.1 MB (27104601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230807.1` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d6d749318702da4223ac8deed60a4a9e9902f10aaba085486b67028eb237c0ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24654154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a48698bc6e604a3f75ab9bfc02a5b699bc5fdbb1bbf4e0aaa81a1d7fc0b439`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:43:12 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:43:12 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:43:20 GMT
ADD file:443a623a513d24fb17f92fecba92ab4b48c5cd58f4c71a4d1017f68cb28ed803 in / 
# Mon, 07 Aug 2023 16:43:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7384d9310f28ea2b7133f7446a72d62a93acda872b1e77361d3764cf8fe7b76`  
		Last Modified: Mon, 07 Aug 2023 17:17:29 GMT  
		Size: 24.7 MB (24654154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230807.1` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2a091f203ef368cd928dbd321be09448a30be52ddb17cb5b733e381206a9dec2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26304973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05b71631b7da894ff1926c05af25f1a6bb9d6054cd7ec150f031e6f62d953bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:59:38 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:59:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:59:39 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:59:47 GMT
ADD file:a621d5a90b1c5e05eb41dfa44616425f9e9c474acc76e148c36a525e99ff2bac in / 
# Mon, 07 Aug 2023 16:59:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f55d0f45237d17adcf4039963cc7ac0b6044348e89458f35c79d1a4a4aa62ad`  
		Last Modified: Mon, 07 Aug 2023 17:17:22 GMT  
		Size: 26.3 MB (26304973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230807.1` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:6c2eec01baef54b81a0a11aa340839d376aea2d2ec4f86d0529741533ef319a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31228462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cc3aafb4d9af81aeba0dd2bfeb9cb503b509c71f0278fb315af4f9903ff09f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:57:20 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:57:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:57:20 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:57:23 GMT
ADD file:4cb180718bb451f8c264f3c3ca17e21c2f353537e1350e7285186274e7c13aa1 in / 
# Mon, 07 Aug 2023 16:57:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e5976a7e300ece0ea0e1b134f66c311c8904a278eb1019c4997473190259ec8`  
		Last Modified: Mon, 07 Aug 2023 17:17:36 GMT  
		Size: 31.2 MB (31228462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230807.1` - linux; s390x

```console
$ docker pull ubuntu@sha256:840aad7a3257d4ef41010f4580b5480a50ca322d56bf91405ef9c1bab8325e88
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26346739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e8b4d20ddafc69b78425aa7c5c2cf679f9000364b92a086b46ff8e9cf59db3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 16:41:40 GMT
ARG RELEASE
# Mon, 07 Aug 2023 16:41:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Aug 2023 16:41:40 GMT
LABEL org.opencontainers.image.version=23.10
# Mon, 07 Aug 2023 16:41:42 GMT
ADD file:7038e8b287279d65872808b33572bb449a981ceacdc4533e8e1047544044f524 in / 
# Mon, 07 Aug 2023 16:41:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e93f2054f5bc941ef3ea4037dce53f6fefca8d79721782c090dc34fb1c96569`  
		Last Modified: Mon, 07 Aug 2023 17:17:42 GMT  
		Size: 26.3 MB (26346739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:7a520eeb6c18bc6d32a21bb7edcf673a7830813c169645d51c949cecb62387d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:3787e67b05ccc44d64b821470510a551eea6a2887c8e60379aca0e2fecaff599
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26840088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24881e92d6487bb77608e410fd9efa9aad6851112ab6500faa3a04bd72da5b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:16:11 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:16:12 GMT
ADD file:3ff011e7c817c9b010391c2b2f74a111d8c37165e6fdff18e18ccfa67ff7667b in / 
# Mon, 31 Jul 2023 17:16:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:03b3dca73f874f81f3e85e8b2df9f05c9f336bd15283a7d099040703fb204279`  
		Last Modified: Mon, 31 Jul 2023 17:39:26 GMT  
		Size: 26.8 MB (26840088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:02d4ef011cf12f8ee9addd2b6ab8fb7395f5e70b314fae9fc7cd55ef69bbdd9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24640558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fbdc2dd1107e4f9d06544ba6dc55d0b350113020b70f35852036991db7d5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:20:03 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:20:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:20:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:20:04 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:20:13 GMT
ADD file:3ec1cc20b36a86b78ff00125a182fab6d7ee8916dbdc6f52d40e182e2892dd06 in / 
# Mon, 31 Jul 2023 17:20:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b90fd1c5c84e67c72256cf32c741235e1afdc37bac915942134aaefb9364fec`  
		Last Modified: Mon, 31 Jul 2023 17:39:39 GMT  
		Size: 24.6 MB (24640558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:33a3158bf45e9e08d5fed2e6d93efb903156fcaba229f9923f151374bfbc6c94
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5956ca9d3275e20c813c20ddc5b86374d74bfc99bf0564dd6bd0a1e6a955ee2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:24:02 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:24:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:24:11 GMT
ADD file:8af4f6767fc5b6665bedd4600c0601ee7d7f803de51e979a40bd3d6ebcd25f95 in / 
# Mon, 31 Jul 2023 17:24:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c0fc7a9f17ab38a3150f437abbf01140c32288aee7c84142c05295ecc002c85`  
		Last Modified: Mon, 31 Jul 2023 17:39:33 GMT  
		Size: 26.1 MB (26088468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:9aebdde7682dbe06c885cf890f2e43a183c05803bff1f2b8464a187dc1b00b58
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31030701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad38d0665b88ca462694ffe4f53d6f572c4e77af16e64c111617df4668bbc75e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:18:51 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:18:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:18:51 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:18:54 GMT
ADD file:98fe279e3c3239702ac2eef51540228e24a3e15e923342cb3e7cd7dd3684a090 in / 
# Mon, 31 Jul 2023 17:18:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4e756d02ae4b4a4f9c9ebdc2ca11b9d859b96365868ba69442d2cb7158a5f827`  
		Last Modified: Mon, 31 Jul 2023 17:39:45 GMT  
		Size: 31.0 MB (31030701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:e6e00642db98617858caf8fc519710225eb0ae7099e6133c3d559a7cbbcdd2b3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25717049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748eb92545cf245d6d5121803154031c63fbb4bf1dd8dee43cbc8847fd58ca35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:25:09 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:25:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:25:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:25:10 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:25:11 GMT
ADD file:02e6a6123ef99d36f86e3e53231b3ba93c90b4ac9fc0bdebe8f01f2a6c2efb4e in / 
# Mon, 31 Jul 2023 17:25:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:052de6ce81fd1abe2b7bd745faefd555b3e282e8fe2e611a52243f2179b7ea38`  
		Last Modified: Mon, 31 Jul 2023 17:39:51 GMT  
		Size: 25.7 MB (25717049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
