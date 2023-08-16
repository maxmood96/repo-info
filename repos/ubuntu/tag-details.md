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
$ docker pull ubuntu@sha256:54071c3f40dfcbb302753d9dc2a5ef1377829310ea6183f8a5d8e4261ce71183
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
$ docker pull ubuntu@sha256:b060fffe8e1561c9c3e6dea6db487b900100fc26830b9ea2ec966c151ab4c020
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3153aa388d026c26a2235e1ed0163e350e451f41a8a313e1804d7e1afb857ab4`  
		Last Modified: Wed, 28 Jun 2023 08:58:40 GMT  
		Size: 29.5 MB (29533422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f01654f07625f4a1d40eecfc528693bd734f6c52d9b982da9a963abe3d9de6c8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2055d043d36664323c87d819decb339cfbe483a4ea379e6ba7a19b72dbad842`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:41:15 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:41:18 GMT
ADD file:c13f43a31510c7a4eaa7e4ca90e4f973b19895658b1f9993cab5f93979d4e2dc in / 
# Wed, 28 Jun 2023 08:41:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:579b5cf0e0f32d6ae38b8b84633c3075f3c12fbbadd8cef3ad028003eb456473`  
		Last Modified: Wed, 28 Jun 2023 08:58:53 GMT  
		Size: 26.1 MB (26141403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb4a67ec973b2995214edd101e37a83787b175a16750b372789c8f6314dc20ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27348699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f74891464b2067aacbde60d9e2888e002af047a0d5dfc0b06b701928e0b473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5af00eab97847634d0b3b8a5933f52ca8378f5f30a2949279d682de1e210d78b`  
		Last Modified: Wed, 28 Jun 2023 08:58:47 GMT  
		Size: 27.3 MB (27348699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a6020490a6bb2b83807200ffb93544553c308eb162fc97db2fd36557403d0d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275463239c0668c9671d378b78573d88a920da9973d267b412b0f83a6094f646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b3bf2b726f961315a137a10a9cd873883e14ee1093503fd84050c4b31345cb8`  
		Last Modified: Wed, 28 Jun 2023 08:58:59 GMT  
		Size: 34.6 MB (34591504 bytes)  
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
$ docker pull ubuntu@sha256:eba3af7359cb6aee0cb5418f7be8d2e945a384d15def5b57c56eb71fbe25d29d
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
$ docker pull ubuntu@sha256:56ccaa2998533e59772cfdf16677d7ab5139fdc774192a2b145df68b4d8c0d3a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27077045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e3c1117a258dc80827283ef70ac0b99733a20b91e65d0fc55255cc261cd38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:32:47 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:32:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:32:49 GMT
ADD file:7d5373d4ccc5f70f68afa885a495329e33f2bf9f97a437251cfc79e7b85a1a88 in / 
# Tue, 01 Aug 2023 05:32:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7a8b6c4b0b207f64cdc62856565316500dfab027acedf3d2be9df9c511c32c77`  
		Last Modified: Tue, 01 Aug 2023 05:42:33 GMT  
		Size: 27.1 MB (27077045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2c581d2179fa64461e164d9e54a62cf2bfcce59204fcae5de058e7ed51c2caa9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24586951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9232f7c121b42b5f19477664a32b8ee4e2154158c4b58036055aa141a965f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:25:35 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:25:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:25:40 GMT
ADD file:87326fc74610678eef05e8f4de7077af56538e06f1edcd35cdc95393dbe4a1fb in / 
# Tue, 01 Aug 2023 05:25:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37db25b9014fefaed2828418c6b1257a2c027222cb94a789d6d824ffcdc407fd`  
		Last Modified: Tue, 01 Aug 2023 05:42:45 GMT  
		Size: 24.6 MB (24586951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ea1b8a574050df536cf1ab2078badeae8236537ef46dd00e1b90486beed37f1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26261359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c421696d316d5ea9545b35e12e675f4733497c5b5d42533e55d1c14a55ba916c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:27 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:30 GMT
ADD file:17fe422cc794db64e2ba81827bc4b023be475037fbb2287e9a8f9b3188870856 in / 
# Tue, 01 Aug 2023 05:33:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c49df66f404e142a96161d558bdc6ce9be75a2c7b4aa5dc55daa6282d8c0882`  
		Last Modified: Tue, 01 Aug 2023 05:42:39 GMT  
		Size: 26.3 MB (26261359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:6ccd2ef68a1ee3b5458b3ca9a8bfbf9748c602e899db9ff7f3c0511996547a9e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31150442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4684c504a9c0c05d0210826cc4ee5f28a1e967a0e2ef58c49bcfba0af721415b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:10 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:13 GMT
ADD file:10d789d1b719d7a401c55c5b0aa22be71267e703ab44185d257d5615fb643c6f in / 
# Tue, 01 Aug 2023 05:33:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:30650f04d695028fc81d43c8a433b2760fc08e8bd71855912e36d8bb8b3b24d2`  
		Last Modified: Tue, 01 Aug 2023 05:42:52 GMT  
		Size: 31.2 MB (31150442 bytes)  
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
$ docker pull ubuntu@sha256:eba3af7359cb6aee0cb5418f7be8d2e945a384d15def5b57c56eb71fbe25d29d
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
$ docker pull ubuntu@sha256:56ccaa2998533e59772cfdf16677d7ab5139fdc774192a2b145df68b4d8c0d3a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27077045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e3c1117a258dc80827283ef70ac0b99733a20b91e65d0fc55255cc261cd38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:32:47 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:32:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:32:49 GMT
ADD file:7d5373d4ccc5f70f68afa885a495329e33f2bf9f97a437251cfc79e7b85a1a88 in / 
# Tue, 01 Aug 2023 05:32:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7a8b6c4b0b207f64cdc62856565316500dfab027acedf3d2be9df9c511c32c77`  
		Last Modified: Tue, 01 Aug 2023 05:42:33 GMT  
		Size: 27.1 MB (27077045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2c581d2179fa64461e164d9e54a62cf2bfcce59204fcae5de058e7ed51c2caa9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24586951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9232f7c121b42b5f19477664a32b8ee4e2154158c4b58036055aa141a965f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:25:35 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:25:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:25:40 GMT
ADD file:87326fc74610678eef05e8f4de7077af56538e06f1edcd35cdc95393dbe4a1fb in / 
# Tue, 01 Aug 2023 05:25:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37db25b9014fefaed2828418c6b1257a2c027222cb94a789d6d824ffcdc407fd`  
		Last Modified: Tue, 01 Aug 2023 05:42:45 GMT  
		Size: 24.6 MB (24586951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ea1b8a574050df536cf1ab2078badeae8236537ef46dd00e1b90486beed37f1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26261359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c421696d316d5ea9545b35e12e675f4733497c5b5d42533e55d1c14a55ba916c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:27 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:30 GMT
ADD file:17fe422cc794db64e2ba81827bc4b023be475037fbb2287e9a8f9b3188870856 in / 
# Tue, 01 Aug 2023 05:33:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c49df66f404e142a96161d558bdc6ce9be75a2c7b4aa5dc55daa6282d8c0882`  
		Last Modified: Tue, 01 Aug 2023 05:42:39 GMT  
		Size: 26.3 MB (26261359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:6ccd2ef68a1ee3b5458b3ca9a8bfbf9748c602e899db9ff7f3c0511996547a9e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31150442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4684c504a9c0c05d0210826cc4ee5f28a1e967a0e2ef58c49bcfba0af721415b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:10 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:13 GMT
ADD file:10d789d1b719d7a401c55c5b0aa22be71267e703ab44185d257d5615fb643c6f in / 
# Tue, 01 Aug 2023 05:33:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:30650f04d695028fc81d43c8a433b2760fc08e8bd71855912e36d8bb8b3b24d2`  
		Last Modified: Tue, 01 Aug 2023 05:42:52 GMT  
		Size: 31.2 MB (31150442 bytes)  
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
$ docker pull ubuntu@sha256:54071c3f40dfcbb302753d9dc2a5ef1377829310ea6183f8a5d8e4261ce71183
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
$ docker pull ubuntu@sha256:b060fffe8e1561c9c3e6dea6db487b900100fc26830b9ea2ec966c151ab4c020
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3153aa388d026c26a2235e1ed0163e350e451f41a8a313e1804d7e1afb857ab4`  
		Last Modified: Wed, 28 Jun 2023 08:58:40 GMT  
		Size: 29.5 MB (29533422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f01654f07625f4a1d40eecfc528693bd734f6c52d9b982da9a963abe3d9de6c8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2055d043d36664323c87d819decb339cfbe483a4ea379e6ba7a19b72dbad842`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:41:15 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:41:18 GMT
ADD file:c13f43a31510c7a4eaa7e4ca90e4f973b19895658b1f9993cab5f93979d4e2dc in / 
# Wed, 28 Jun 2023 08:41:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:579b5cf0e0f32d6ae38b8b84633c3075f3c12fbbadd8cef3ad028003eb456473`  
		Last Modified: Wed, 28 Jun 2023 08:58:53 GMT  
		Size: 26.1 MB (26141403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb4a67ec973b2995214edd101e37a83787b175a16750b372789c8f6314dc20ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27348699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f74891464b2067aacbde60d9e2888e002af047a0d5dfc0b06b701928e0b473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5af00eab97847634d0b3b8a5933f52ca8378f5f30a2949279d682de1e210d78b`  
		Last Modified: Wed, 28 Jun 2023 08:58:47 GMT  
		Size: 27.3 MB (27348699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a6020490a6bb2b83807200ffb93544553c308eb162fc97db2fd36557403d0d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275463239c0668c9671d378b78573d88a920da9973d267b412b0f83a6094f646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b3bf2b726f961315a137a10a9cd873883e14ee1093503fd84050c4b31345cb8`  
		Last Modified: Wed, 28 Jun 2023 08:58:59 GMT  
		Size: 34.6 MB (34591504 bytes)  
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
$ docker pull ubuntu@sha256:efdc4002fa69db852cbb0957464a1fc686c56c38cd38ef4c183e9e3e9009ad2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; s390x

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
$ docker pull ubuntu@sha256:54071c3f40dfcbb302753d9dc2a5ef1377829310ea6183f8a5d8e4261ce71183
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
$ docker pull ubuntu@sha256:b060fffe8e1561c9c3e6dea6db487b900100fc26830b9ea2ec966c151ab4c020
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a81c4b8502e4979e75bd8f91343b95b0d695ab67f241dbed0d1530a35bde1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3153aa388d026c26a2235e1ed0163e350e451f41a8a313e1804d7e1afb857ab4`  
		Last Modified: Wed, 28 Jun 2023 08:58:40 GMT  
		Size: 29.5 MB (29533422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f01654f07625f4a1d40eecfc528693bd734f6c52d9b982da9a963abe3d9de6c8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2055d043d36664323c87d819decb339cfbe483a4ea379e6ba7a19b72dbad842`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:41:15 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:41:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:41:18 GMT
ADD file:c13f43a31510c7a4eaa7e4ca90e4f973b19895658b1f9993cab5f93979d4e2dc in / 
# Wed, 28 Jun 2023 08:41:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:579b5cf0e0f32d6ae38b8b84633c3075f3c12fbbadd8cef3ad028003eb456473`  
		Last Modified: Wed, 28 Jun 2023 08:58:53 GMT  
		Size: 26.1 MB (26141403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb4a67ec973b2995214edd101e37a83787b175a16750b372789c8f6314dc20ca
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27348699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f74891464b2067aacbde60d9e2888e002af047a0d5dfc0b06b701928e0b473`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5af00eab97847634d0b3b8a5933f52ca8378f5f30a2949279d682de1e210d78b`  
		Last Modified: Wed, 28 Jun 2023 08:58:47 GMT  
		Size: 27.3 MB (27348699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5a6020490a6bb2b83807200ffb93544553c308eb162fc97db2fd36557403d0d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275463239c0668c9671d378b78573d88a920da9973d267b412b0f83a6094f646`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8b3bf2b726f961315a137a10a9cd873883e14ee1093503fd84050c4b31345cb8`  
		Last Modified: Wed, 28 Jun 2023 08:58:59 GMT  
		Size: 34.6 MB (34591504 bytes)  
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
$ docker pull ubuntu@sha256:eba3af7359cb6aee0cb5418f7be8d2e945a384d15def5b57c56eb71fbe25d29d
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
$ docker pull ubuntu@sha256:56ccaa2998533e59772cfdf16677d7ab5139fdc774192a2b145df68b4d8c0d3a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27077045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e3c1117a258dc80827283ef70ac0b99733a20b91e65d0fc55255cc261cd38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:32:47 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:32:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:32:47 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:32:49 GMT
ADD file:7d5373d4ccc5f70f68afa885a495329e33f2bf9f97a437251cfc79e7b85a1a88 in / 
# Tue, 01 Aug 2023 05:32:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7a8b6c4b0b207f64cdc62856565316500dfab027acedf3d2be9df9c511c32c77`  
		Last Modified: Tue, 01 Aug 2023 05:42:33 GMT  
		Size: 27.1 MB (27077045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2c581d2179fa64461e164d9e54a62cf2bfcce59204fcae5de058e7ed51c2caa9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24586951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9232f7c121b42b5f19477664a32b8ee4e2154158c4b58036055aa141a965f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:25:35 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:25:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:25:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:25:40 GMT
ADD file:87326fc74610678eef05e8f4de7077af56538e06f1edcd35cdc95393dbe4a1fb in / 
# Tue, 01 Aug 2023 05:25:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:37db25b9014fefaed2828418c6b1257a2c027222cb94a789d6d824ffcdc407fd`  
		Last Modified: Tue, 01 Aug 2023 05:42:45 GMT  
		Size: 24.6 MB (24586951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ea1b8a574050df536cf1ab2078badeae8236537ef46dd00e1b90486beed37f1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26261359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c421696d316d5ea9545b35e12e675f4733497c5b5d42533e55d1c14a55ba916c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:27 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:27 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:30 GMT
ADD file:17fe422cc794db64e2ba81827bc4b023be475037fbb2287e9a8f9b3188870856 in / 
# Tue, 01 Aug 2023 05:33:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c49df66f404e142a96161d558bdc6ce9be75a2c7b4aa5dc55daa6282d8c0882`  
		Last Modified: Tue, 01 Aug 2023 05:42:39 GMT  
		Size: 26.3 MB (26261359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:6ccd2ef68a1ee3b5458b3ca9a8bfbf9748c602e899db9ff7f3c0511996547a9e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31150442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4684c504a9c0c05d0210826cc4ee5f28a1e967a0e2ef58c49bcfba0af721415b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Aug 2023 05:33:10 GMT
ARG RELEASE
# Tue, 01 Aug 2023 05:33:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 05:33:10 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 01 Aug 2023 05:33:13 GMT
ADD file:10d789d1b719d7a401c55c5b0aa22be71267e703ab44185d257d5615fb643c6f in / 
# Tue, 01 Aug 2023 05:33:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:30650f04d695028fc81d43c8a433b2760fc08e8bd71855912e36d8bb8b3b24d2`  
		Last Modified: Tue, 01 Aug 2023 05:42:52 GMT  
		Size: 31.2 MB (31150442 bytes)  
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
$ docker pull ubuntu@sha256:5fbd289046eb316e4eea5900c1238354eeef2c8766011abca73b2a0432b23f98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; s390x

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
