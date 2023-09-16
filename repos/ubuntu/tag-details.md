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
-	[`ubuntu:jammy-20230816`](#ubuntujammy-20230816)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230816`](#ubuntulunar-20230816)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20230912`](#ubuntumantic-20230912)
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
$ docker pull ubuntu@sha256:aabed3296a3d45cede1dc866a24476c4d7e093aa806263c27ddaadbdce3c1054
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
$ docker pull ubuntu@sha256:b492494d8e0113c4ad3fe4528a4b5ff89faa5331f7d52c5c138196f69ce176a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b84b685f35f1a5d63661f5d4aa662ad9b7ee4f4b8c394c022f25023c907b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:445a6a12be2be54b4da18d7c77d4a41bc4746bc422f1f4325a60ff4fc7ea2e5d`  
		Last Modified: Wed, 16 Aug 2023 06:32:47 GMT  
		Size: 29.5 MB (29537716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2589fe6bcf90466564741ae0d8309d1323f33b6ec8a5d401a62d0b256bcc3c37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edd8b11048dd1910bbeeae6325888a34a64e8a0d2576b6d843063825b339cd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:08:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:08:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:08:32 GMT
ADD file:e61c6bbfc8728cb119b4cfd4a35d1e5aad76e84c0ac8f2ff9850a7ceec9f3dc5 in / 
# Wed, 16 Aug 2023 06:08:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d79cf5fbd02b4f64ddfb1ba3ae0178a904f012bc2ff0e5603ffdb4668a8f529c`  
		Last Modified: Wed, 16 Aug 2023 06:32:59 GMT  
		Size: 26.1 MB (26142545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:94d12db896d07af18a04319f1023edd091629f558dcc29f84208a7cf5ca040ec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a47e077731f534f14de4df8639e35a1792a555b74e46920200ec05cb4af3d12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20274425734a05472f3772bae7ce7124a9832f5eb168456d6cb53e92d6e718a8`  
		Last Modified: Wed, 16 Aug 2023 06:32:53 GMT  
		Size: 27.4 MB (27351105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1fcbe2d7e928d0be9476e3079df8e69072dfb140be94f5d34091f09f6917dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34567229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67aa2427a930674989cafcaf3fa7d1d16b2c47ed37003fe712bcbf5bc07a6fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c76fbfef684586d44d4a79c1a2c093ecf60b0f6c5deb0742082a5152ecd9a1fa`  
		Last Modified: Wed, 16 Aug 2023 06:33:06 GMT  
		Size: 34.6 MB (34567229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:ed1a67bb47f3c35d782293229127ac1f8d64873a131186c49fe079dada0fa7e0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34a6de6626fe032cc2ff34b644898f997ccd85378e081b63c95246ad6b11e3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e1b6153f78cbd4f98e7250bc413a393734736138dcb57f1e41f45c3e43c5a120`  
		Last Modified: Wed, 16 Aug 2023 06:33:12 GMT  
		Size: 28.0 MB (28016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:f1090cfa89ab321a6d670e79652f61593502591f2fc7452fb0b7c6da575729c4
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
$ docker pull ubuntu@sha256:24898c8e1ac370d2d309d6d9df56af52bebdad86925c623b5e87e12404453518
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26873617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21098a29e034a8f6f1952d1d8a49b5732b70e532c31f0e88e1ff499c6540c57c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:28:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:28:32 GMT
ADD file:7392bed4dbab9fb7c9ad5bde6f3bfcde3bcbf1885c336af9c231af6defaa31e1 in / 
# Wed, 16 Aug 2023 04:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10fb01f4f619bc954ba611cebca23f2b96d255c7ead4040b449f063e530df1a4`  
		Last Modified: Wed, 16 Aug 2023 04:34:32 GMT  
		Size: 26.9 MB (26873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1e9568cacc4bd0a59a44d8e68ae8fc5f4287c132d455492881f7a1106b722beb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24627247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f21739314ec025a0ce92c7a657ddb65785a29870d74435a08554207fb3688`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:11 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:16 GMT
ADD file:1f1c9502544acdbb6a7450226ced78cfe982a6305f2aea77ab7d1f73b50fc7f0 in / 
# Wed, 16 Aug 2023 04:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e05ef4abc6c76087042349392d272a7eeb590834dc45d1247295302c212fda9d`  
		Last Modified: Wed, 16 Aug 2023 04:34:45 GMT  
		Size: 24.6 MB (24627247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d68d8bcae123a839bc72b91fa9df55956be3fcb2dbfc247acb7f65908eaa6c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8e9335de75964dd320b20b4290408432be2962faf7ad36d3a47d48f3131cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:15:57 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:15:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:01 GMT
ADD file:adea2962926b29b76eb8da76ae9e830c5ad7050ae9b19f5427191b338c8a2c56 in / 
# Wed, 16 Aug 2023 04:16:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b2d15932a31f0857b9499cc218b8777708cb1d73ae6ef680f624ca7d4342763`  
		Last Modified: Wed, 16 Aug 2023 04:34:39 GMT  
		Size: 26.1 MB (26064545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1306e75f505a2305f2c46f51f33be8b8599923bd5a652c3b5dc37333db4f44ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91733a8763fe80d6e620ec400c2721ee45c0f80398506088d1278d6531299a90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:34 GMT
ADD file:a9d35b320d969ee1ae8a7bc83aba49da30d93724befb5948c680066ad4f1acdf in / 
# Wed, 16 Aug 2023 04:16:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f51cbff870f31d4c4397c2f21529046998f8d6e7748fd6f059b325a0759c7dd4`  
		Last Modified: Wed, 16 Aug 2023 04:34:51 GMT  
		Size: 30.9 MB (30905042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec9620bbf89d1a3b1171f961340a890166607be3423d96e740f6d56f36ccb125
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289eb3132a14bc161676d7f928d557bf63eb8561718e9d5247e16e88ebee8ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:29:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:29:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:29:29 GMT
ADD file:14fcf0756fb29b609af54412c31e2ff9acbf4634984ce95bf204c67668706cb5 in / 
# Wed, 16 Aug 2023 04:29:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1e434384d3d3b546e155df0cf143c8c0a92bf766c6808bf2e3e1d2f22010839`  
		Last Modified: Wed, 16 Aug 2023 04:34:57 GMT  
		Size: 25.7 MB (25691524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:ed5b80e7117fe03f4197adc76c64a86a290d31898a5d491e32f66c7eb7558fe3
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
$ docker pull ubuntu@sha256:8c890bff8be02ca8851438c5bc3aa6926b239b6d7ecc1b88bab1786791b4be4a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27105424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f19d7ce16de2c46864cbad83431ca20523d56b3d8b2ec73f622537f9c2988b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:04:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:04:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:04:55 GMT
ADD file:87bbd4b1a17b5a9990befc7d85a50c9b813d3cea95c9f28e0001a40d6b7deaf4 in / 
# Sat, 19 Aug 2023 05:04:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d9082f03f929cae81e2745d2a1f84039f043bd9b3a4540578db92416ae0f93b9`  
		Last Modified: Sat, 19 Aug 2023 05:24:16 GMT  
		Size: 27.1 MB (27105424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:fdf900365429ac02f12cb6095990dbf32f3852988aea55a16a4c71fab29a9e30
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24654282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce7c7b00c3aeccc3ff3f30998f4fd966db8e6bb9a5d44f7c2e3cb9b5705cb07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:05:42 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:05:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:05:47 GMT
ADD file:b2556a8208f666e3c07a759d0acbc23841ac60abc72026ca23e8a2d2c96a3c9e in / 
# Sat, 19 Aug 2023 05:05:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72b4b38e5bfce833af02b676c68b5f082fd586fe6a99eaa6efea0f934e56ccc8`  
		Last Modified: Sat, 19 Aug 2023 05:24:28 GMT  
		Size: 24.7 MB (24654282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:8626f9672aaa735f2daa2593cc7311e9a1d6a8c31d7248927d515daf9cdd1b09
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26303684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b9a14b6fea1edc32255a74ee2d1ec7208f511c6e3b04e12ef5ea5a0ed4606c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:09:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:09:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:10:02 GMT
ADD file:cc6a3e0225d3c4171348881d7482651292156aeaaee88bc0ed81e8a850fe21f7 in / 
# Sat, 19 Aug 2023 05:10:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e1a7676413a2a5845d40b76cb97caffadaf7e87244e6c283b4e4a8c339837a8`  
		Last Modified: Sat, 19 Aug 2023 05:24:22 GMT  
		Size: 26.3 MB (26303684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:47562423fe5f9c1e2d652389970daa881246aff9d041f6a3ba0c6075e2e8127c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31242759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2819f0362dd8edc6597790ab1a94a19c6522742701be2a2754df563c0a08f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:08:05 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:08:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:08:08 GMT
ADD file:e4a36c75d3f498442e29bc6100bb11ebebbc8ba67e315acb43bc0ad4a1d1421a in / 
# Sat, 19 Aug 2023 05:08:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f384095696b2736f3120375c4f04235ec254057830767ec72b5adf85ebfddb8`  
		Last Modified: Sat, 19 Aug 2023 05:24:35 GMT  
		Size: 31.2 MB (31242759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:89c018c5ddbc7656b0af4b7afe4f0d531acca40e79138905853191b6cdc75d1d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26407096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94161fa8d33b8ff4133c502abc2c434f7d1f5b21c437d5ea6521820d6ee22136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:07:37 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:07:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:07:39 GMT
ADD file:681bda53818a2c0f492a5b6c8f35eb4ecba1d81c3c51e02310824c03db9146e6 in / 
# Sat, 19 Aug 2023 05:07:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fd9cf1abf5e584207948c92e06b060305d0e1e0babd02387c55d8b25ad7ae623`  
		Last Modified: Sat, 19 Aug 2023 05:24:41 GMT  
		Size: 26.4 MB (26407096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:ed5b80e7117fe03f4197adc76c64a86a290d31898a5d491e32f66c7eb7558fe3
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
$ docker pull ubuntu@sha256:8c890bff8be02ca8851438c5bc3aa6926b239b6d7ecc1b88bab1786791b4be4a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27105424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f19d7ce16de2c46864cbad83431ca20523d56b3d8b2ec73f622537f9c2988b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:04:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:04:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:04:55 GMT
ADD file:87bbd4b1a17b5a9990befc7d85a50c9b813d3cea95c9f28e0001a40d6b7deaf4 in / 
# Sat, 19 Aug 2023 05:04:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d9082f03f929cae81e2745d2a1f84039f043bd9b3a4540578db92416ae0f93b9`  
		Last Modified: Sat, 19 Aug 2023 05:24:16 GMT  
		Size: 27.1 MB (27105424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:fdf900365429ac02f12cb6095990dbf32f3852988aea55a16a4c71fab29a9e30
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24654282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce7c7b00c3aeccc3ff3f30998f4fd966db8e6bb9a5d44f7c2e3cb9b5705cb07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:05:42 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:05:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:05:47 GMT
ADD file:b2556a8208f666e3c07a759d0acbc23841ac60abc72026ca23e8a2d2c96a3c9e in / 
# Sat, 19 Aug 2023 05:05:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72b4b38e5bfce833af02b676c68b5f082fd586fe6a99eaa6efea0f934e56ccc8`  
		Last Modified: Sat, 19 Aug 2023 05:24:28 GMT  
		Size: 24.7 MB (24654282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:8626f9672aaa735f2daa2593cc7311e9a1d6a8c31d7248927d515daf9cdd1b09
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26303684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b9a14b6fea1edc32255a74ee2d1ec7208f511c6e3b04e12ef5ea5a0ed4606c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:09:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:09:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:10:02 GMT
ADD file:cc6a3e0225d3c4171348881d7482651292156aeaaee88bc0ed81e8a850fe21f7 in / 
# Sat, 19 Aug 2023 05:10:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e1a7676413a2a5845d40b76cb97caffadaf7e87244e6c283b4e4a8c339837a8`  
		Last Modified: Sat, 19 Aug 2023 05:24:22 GMT  
		Size: 26.3 MB (26303684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:47562423fe5f9c1e2d652389970daa881246aff9d041f6a3ba0c6075e2e8127c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31242759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2819f0362dd8edc6597790ab1a94a19c6522742701be2a2754df563c0a08f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:08:05 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:08:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:08:08 GMT
ADD file:e4a36c75d3f498442e29bc6100bb11ebebbc8ba67e315acb43bc0ad4a1d1421a in / 
# Sat, 19 Aug 2023 05:08:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f384095696b2736f3120375c4f04235ec254057830767ec72b5adf85ebfddb8`  
		Last Modified: Sat, 19 Aug 2023 05:24:35 GMT  
		Size: 31.2 MB (31242759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:89c018c5ddbc7656b0af4b7afe4f0d531acca40e79138905853191b6cdc75d1d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26407096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94161fa8d33b8ff4133c502abc2c434f7d1f5b21c437d5ea6521820d6ee22136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:07:37 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:07:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:07:39 GMT
ADD file:681bda53818a2c0f492a5b6c8f35eb4ecba1d81c3c51e02310824c03db9146e6 in / 
# Sat, 19 Aug 2023 05:07:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fd9cf1abf5e584207948c92e06b060305d0e1e0babd02387c55d8b25ad7ae623`  
		Last Modified: Sat, 19 Aug 2023 05:24:41 GMT  
		Size: 26.4 MB (26407096 bytes)  
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
$ docker pull ubuntu@sha256:aabed3296a3d45cede1dc866a24476c4d7e093aa806263c27ddaadbdce3c1054
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
$ docker pull ubuntu@sha256:b492494d8e0113c4ad3fe4528a4b5ff89faa5331f7d52c5c138196f69ce176a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b84b685f35f1a5d63661f5d4aa662ad9b7ee4f4b8c394c022f25023c907b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:445a6a12be2be54b4da18d7c77d4a41bc4746bc422f1f4325a60ff4fc7ea2e5d`  
		Last Modified: Wed, 16 Aug 2023 06:32:47 GMT  
		Size: 29.5 MB (29537716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2589fe6bcf90466564741ae0d8309d1323f33b6ec8a5d401a62d0b256bcc3c37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edd8b11048dd1910bbeeae6325888a34a64e8a0d2576b6d843063825b339cd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:08:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:08:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:08:32 GMT
ADD file:e61c6bbfc8728cb119b4cfd4a35d1e5aad76e84c0ac8f2ff9850a7ceec9f3dc5 in / 
# Wed, 16 Aug 2023 06:08:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d79cf5fbd02b4f64ddfb1ba3ae0178a904f012bc2ff0e5603ffdb4668a8f529c`  
		Last Modified: Wed, 16 Aug 2023 06:32:59 GMT  
		Size: 26.1 MB (26142545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:94d12db896d07af18a04319f1023edd091629f558dcc29f84208a7cf5ca040ec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a47e077731f534f14de4df8639e35a1792a555b74e46920200ec05cb4af3d12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20274425734a05472f3772bae7ce7124a9832f5eb168456d6cb53e92d6e718a8`  
		Last Modified: Wed, 16 Aug 2023 06:32:53 GMT  
		Size: 27.4 MB (27351105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1fcbe2d7e928d0be9476e3079df8e69072dfb140be94f5d34091f09f6917dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34567229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67aa2427a930674989cafcaf3fa7d1d16b2c47ed37003fe712bcbf5bc07a6fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c76fbfef684586d44d4a79c1a2c093ecf60b0f6c5deb0742082a5152ecd9a1fa`  
		Last Modified: Wed, 16 Aug 2023 06:33:06 GMT  
		Size: 34.6 MB (34567229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:ed1a67bb47f3c35d782293229127ac1f8d64873a131186c49fe079dada0fa7e0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34a6de6626fe032cc2ff34b644898f997ccd85378e081b63c95246ad6b11e3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e1b6153f78cbd4f98e7250bc413a393734736138dcb57f1e41f45c3e43c5a120`  
		Last Modified: Wed, 16 Aug 2023 06:33:12 GMT  
		Size: 28.0 MB (28016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230816`

```console
$ docker pull ubuntu@sha256:aabed3296a3d45cede1dc866a24476c4d7e093aa806263c27ddaadbdce3c1054
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230816` - linux; amd64

```console
$ docker pull ubuntu@sha256:b492494d8e0113c4ad3fe4528a4b5ff89faa5331f7d52c5c138196f69ce176a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b84b685f35f1a5d63661f5d4aa662ad9b7ee4f4b8c394c022f25023c907b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:445a6a12be2be54b4da18d7c77d4a41bc4746bc422f1f4325a60ff4fc7ea2e5d`  
		Last Modified: Wed, 16 Aug 2023 06:32:47 GMT  
		Size: 29.5 MB (29537716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230816` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2589fe6bcf90466564741ae0d8309d1323f33b6ec8a5d401a62d0b256bcc3c37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edd8b11048dd1910bbeeae6325888a34a64e8a0d2576b6d843063825b339cd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:08:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:08:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:08:32 GMT
ADD file:e61c6bbfc8728cb119b4cfd4a35d1e5aad76e84c0ac8f2ff9850a7ceec9f3dc5 in / 
# Wed, 16 Aug 2023 06:08:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d79cf5fbd02b4f64ddfb1ba3ae0178a904f012bc2ff0e5603ffdb4668a8f529c`  
		Last Modified: Wed, 16 Aug 2023 06:32:59 GMT  
		Size: 26.1 MB (26142545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230816` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:94d12db896d07af18a04319f1023edd091629f558dcc29f84208a7cf5ca040ec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a47e077731f534f14de4df8639e35a1792a555b74e46920200ec05cb4af3d12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20274425734a05472f3772bae7ce7124a9832f5eb168456d6cb53e92d6e718a8`  
		Last Modified: Wed, 16 Aug 2023 06:32:53 GMT  
		Size: 27.4 MB (27351105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230816` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1fcbe2d7e928d0be9476e3079df8e69072dfb140be94f5d34091f09f6917dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34567229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67aa2427a930674989cafcaf3fa7d1d16b2c47ed37003fe712bcbf5bc07a6fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c76fbfef684586d44d4a79c1a2c093ecf60b0f6c5deb0742082a5152ecd9a1fa`  
		Last Modified: Wed, 16 Aug 2023 06:33:06 GMT  
		Size: 34.6 MB (34567229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230816` - linux; s390x

```console
$ docker pull ubuntu@sha256:ed1a67bb47f3c35d782293229127ac1f8d64873a131186c49fe079dada0fa7e0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34a6de6626fe032cc2ff34b644898f997ccd85378e081b63c95246ad6b11e3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e1b6153f78cbd4f98e7250bc413a393734736138dcb57f1e41f45c3e43c5a120`  
		Last Modified: Wed, 16 Aug 2023 06:33:12 GMT  
		Size: 28.0 MB (28016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:aabed3296a3d45cede1dc866a24476c4d7e093aa806263c27ddaadbdce3c1054
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
$ docker pull ubuntu@sha256:b492494d8e0113c4ad3fe4528a4b5ff89faa5331f7d52c5c138196f69ce176a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b84b685f35f1a5d63661f5d4aa662ad9b7ee4f4b8c394c022f25023c907b65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:445a6a12be2be54b4da18d7c77d4a41bc4746bc422f1f4325a60ff4fc7ea2e5d`  
		Last Modified: Wed, 16 Aug 2023 06:32:47 GMT  
		Size: 29.5 MB (29537716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2589fe6bcf90466564741ae0d8309d1323f33b6ec8a5d401a62d0b256bcc3c37
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26142545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5edd8b11048dd1910bbeeae6325888a34a64e8a0d2576b6d843063825b339cd1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:08:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:08:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:08:27 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:08:32 GMT
ADD file:e61c6bbfc8728cb119b4cfd4a35d1e5aad76e84c0ac8f2ff9850a7ceec9f3dc5 in / 
# Wed, 16 Aug 2023 06:08:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d79cf5fbd02b4f64ddfb1ba3ae0178a904f012bc2ff0e5603ffdb4668a8f529c`  
		Last Modified: Wed, 16 Aug 2023 06:32:59 GMT  
		Size: 26.1 MB (26142545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:94d12db896d07af18a04319f1023edd091629f558dcc29f84208a7cf5ca040ec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a47e077731f534f14de4df8639e35a1792a555b74e46920200ec05cb4af3d12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:20274425734a05472f3772bae7ce7124a9832f5eb168456d6cb53e92d6e718a8`  
		Last Modified: Wed, 16 Aug 2023 06:32:53 GMT  
		Size: 27.4 MB (27351105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:de1fcbe2d7e928d0be9476e3079df8e69072dfb140be94f5d34091f09f6917dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34567229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67aa2427a930674989cafcaf3fa7d1d16b2c47ed37003fe712bcbf5bc07a6fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c76fbfef684586d44d4a79c1a2c093ecf60b0f6c5deb0742082a5152ecd9a1fa`  
		Last Modified: Wed, 16 Aug 2023 06:33:06 GMT  
		Size: 34.6 MB (34567229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:ed1a67bb47f3c35d782293229127ac1f8d64873a131186c49fe079dada0fa7e0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28016004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34a6de6626fe032cc2ff34b644898f997ccd85378e081b63c95246ad6b11e3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e1b6153f78cbd4f98e7250bc413a393734736138dcb57f1e41f45c3e43c5a120`  
		Last Modified: Wed, 16 Aug 2023 06:33:12 GMT  
		Size: 28.0 MB (28016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:f1090cfa89ab321a6d670e79652f61593502591f2fc7452fb0b7c6da575729c4
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
$ docker pull ubuntu@sha256:24898c8e1ac370d2d309d6d9df56af52bebdad86925c623b5e87e12404453518
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26873617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21098a29e034a8f6f1952d1d8a49b5732b70e532c31f0e88e1ff499c6540c57c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:28:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:28:32 GMT
ADD file:7392bed4dbab9fb7c9ad5bde6f3bfcde3bcbf1885c336af9c231af6defaa31e1 in / 
# Wed, 16 Aug 2023 04:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10fb01f4f619bc954ba611cebca23f2b96d255c7ead4040b449f063e530df1a4`  
		Last Modified: Wed, 16 Aug 2023 04:34:32 GMT  
		Size: 26.9 MB (26873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1e9568cacc4bd0a59a44d8e68ae8fc5f4287c132d455492881f7a1106b722beb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24627247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f21739314ec025a0ce92c7a657ddb65785a29870d74435a08554207fb3688`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:11 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:16 GMT
ADD file:1f1c9502544acdbb6a7450226ced78cfe982a6305f2aea77ab7d1f73b50fc7f0 in / 
# Wed, 16 Aug 2023 04:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e05ef4abc6c76087042349392d272a7eeb590834dc45d1247295302c212fda9d`  
		Last Modified: Wed, 16 Aug 2023 04:34:45 GMT  
		Size: 24.6 MB (24627247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d68d8bcae123a839bc72b91fa9df55956be3fcb2dbfc247acb7f65908eaa6c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8e9335de75964dd320b20b4290408432be2962faf7ad36d3a47d48f3131cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:15:57 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:15:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:01 GMT
ADD file:adea2962926b29b76eb8da76ae9e830c5ad7050ae9b19f5427191b338c8a2c56 in / 
# Wed, 16 Aug 2023 04:16:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b2d15932a31f0857b9499cc218b8777708cb1d73ae6ef680f624ca7d4342763`  
		Last Modified: Wed, 16 Aug 2023 04:34:39 GMT  
		Size: 26.1 MB (26064545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1306e75f505a2305f2c46f51f33be8b8599923bd5a652c3b5dc37333db4f44ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91733a8763fe80d6e620ec400c2721ee45c0f80398506088d1278d6531299a90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:34 GMT
ADD file:a9d35b320d969ee1ae8a7bc83aba49da30d93724befb5948c680066ad4f1acdf in / 
# Wed, 16 Aug 2023 04:16:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f51cbff870f31d4c4397c2f21529046998f8d6e7748fd6f059b325a0759c7dd4`  
		Last Modified: Wed, 16 Aug 2023 04:34:51 GMT  
		Size: 30.9 MB (30905042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec9620bbf89d1a3b1171f961340a890166607be3423d96e740f6d56f36ccb125
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289eb3132a14bc161676d7f928d557bf63eb8561718e9d5247e16e88ebee8ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:29:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:29:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:29:29 GMT
ADD file:14fcf0756fb29b609af54412c31e2ff9acbf4634984ce95bf204c67668706cb5 in / 
# Wed, 16 Aug 2023 04:29:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1e434384d3d3b546e155df0cf143c8c0a92bf766c6808bf2e3e1d2f22010839`  
		Last Modified: Wed, 16 Aug 2023 04:34:57 GMT  
		Size: 25.7 MB (25691524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230816`

```console
$ docker pull ubuntu@sha256:f1090cfa89ab321a6d670e79652f61593502591f2fc7452fb0b7c6da575729c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20230816` - linux; amd64

```console
$ docker pull ubuntu@sha256:24898c8e1ac370d2d309d6d9df56af52bebdad86925c623b5e87e12404453518
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26873617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21098a29e034a8f6f1952d1d8a49b5732b70e532c31f0e88e1ff499c6540c57c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:28:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:28:32 GMT
ADD file:7392bed4dbab9fb7c9ad5bde6f3bfcde3bcbf1885c336af9c231af6defaa31e1 in / 
# Wed, 16 Aug 2023 04:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10fb01f4f619bc954ba611cebca23f2b96d255c7ead4040b449f063e530df1a4`  
		Last Modified: Wed, 16 Aug 2023 04:34:32 GMT  
		Size: 26.9 MB (26873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230816` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1e9568cacc4bd0a59a44d8e68ae8fc5f4287c132d455492881f7a1106b722beb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24627247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f21739314ec025a0ce92c7a657ddb65785a29870d74435a08554207fb3688`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:11 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:16 GMT
ADD file:1f1c9502544acdbb6a7450226ced78cfe982a6305f2aea77ab7d1f73b50fc7f0 in / 
# Wed, 16 Aug 2023 04:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e05ef4abc6c76087042349392d272a7eeb590834dc45d1247295302c212fda9d`  
		Last Modified: Wed, 16 Aug 2023 04:34:45 GMT  
		Size: 24.6 MB (24627247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230816` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d68d8bcae123a839bc72b91fa9df55956be3fcb2dbfc247acb7f65908eaa6c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8e9335de75964dd320b20b4290408432be2962faf7ad36d3a47d48f3131cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:15:57 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:15:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:01 GMT
ADD file:adea2962926b29b76eb8da76ae9e830c5ad7050ae9b19f5427191b338c8a2c56 in / 
# Wed, 16 Aug 2023 04:16:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b2d15932a31f0857b9499cc218b8777708cb1d73ae6ef680f624ca7d4342763`  
		Last Modified: Wed, 16 Aug 2023 04:34:39 GMT  
		Size: 26.1 MB (26064545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230816` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1306e75f505a2305f2c46f51f33be8b8599923bd5a652c3b5dc37333db4f44ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91733a8763fe80d6e620ec400c2721ee45c0f80398506088d1278d6531299a90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:34 GMT
ADD file:a9d35b320d969ee1ae8a7bc83aba49da30d93724befb5948c680066ad4f1acdf in / 
# Wed, 16 Aug 2023 04:16:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f51cbff870f31d4c4397c2f21529046998f8d6e7748fd6f059b325a0759c7dd4`  
		Last Modified: Wed, 16 Aug 2023 04:34:51 GMT  
		Size: 30.9 MB (30905042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230816` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec9620bbf89d1a3b1171f961340a890166607be3423d96e740f6d56f36ccb125
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289eb3132a14bc161676d7f928d557bf63eb8561718e9d5247e16e88ebee8ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:29:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:29:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:29:29 GMT
ADD file:14fcf0756fb29b609af54412c31e2ff9acbf4634984ce95bf204c67668706cb5 in / 
# Wed, 16 Aug 2023 04:29:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1e434384d3d3b546e155df0cf143c8c0a92bf766c6808bf2e3e1d2f22010839`  
		Last Modified: Wed, 16 Aug 2023 04:34:57 GMT  
		Size: 25.7 MB (25691524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:ed5b80e7117fe03f4197adc76c64a86a290d31898a5d491e32f66c7eb7558fe3
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
$ docker pull ubuntu@sha256:8c890bff8be02ca8851438c5bc3aa6926b239b6d7ecc1b88bab1786791b4be4a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27105424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f19d7ce16de2c46864cbad83431ca20523d56b3d8b2ec73f622537f9c2988b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:04:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:04:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:04:54 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:04:55 GMT
ADD file:87bbd4b1a17b5a9990befc7d85a50c9b813d3cea95c9f28e0001a40d6b7deaf4 in / 
# Sat, 19 Aug 2023 05:04:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d9082f03f929cae81e2745d2a1f84039f043bd9b3a4540578db92416ae0f93b9`  
		Last Modified: Sat, 19 Aug 2023 05:24:16 GMT  
		Size: 27.1 MB (27105424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:fdf900365429ac02f12cb6095990dbf32f3852988aea55a16a4c71fab29a9e30
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24654282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce7c7b00c3aeccc3ff3f30998f4fd966db8e6bb9a5d44f7c2e3cb9b5705cb07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:05:42 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:05:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:05:43 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:05:47 GMT
ADD file:b2556a8208f666e3c07a759d0acbc23841ac60abc72026ca23e8a2d2c96a3c9e in / 
# Sat, 19 Aug 2023 05:05:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72b4b38e5bfce833af02b676c68b5f082fd586fe6a99eaa6efea0f934e56ccc8`  
		Last Modified: Sat, 19 Aug 2023 05:24:28 GMT  
		Size: 24.7 MB (24654282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:8626f9672aaa735f2daa2593cc7311e9a1d6a8c31d7248927d515daf9cdd1b09
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26303684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b9a14b6fea1edc32255a74ee2d1ec7208f511c6e3b04e12ef5ea5a0ed4606c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:09:54 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:09:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:09:55 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:10:02 GMT
ADD file:cc6a3e0225d3c4171348881d7482651292156aeaaee88bc0ed81e8a850fe21f7 in / 
# Sat, 19 Aug 2023 05:10:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e1a7676413a2a5845d40b76cb97caffadaf7e87244e6c283b4e4a8c339837a8`  
		Last Modified: Sat, 19 Aug 2023 05:24:22 GMT  
		Size: 26.3 MB (26303684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:47562423fe5f9c1e2d652389970daa881246aff9d041f6a3ba0c6075e2e8127c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 MB (31242759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2819f0362dd8edc6597790ab1a94a19c6522742701be2a2754df563c0a08f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:08:05 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:08:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:08:05 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:08:08 GMT
ADD file:e4a36c75d3f498442e29bc6100bb11ebebbc8ba67e315acb43bc0ad4a1d1421a in / 
# Sat, 19 Aug 2023 05:08:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f384095696b2736f3120375c4f04235ec254057830767ec72b5adf85ebfddb8`  
		Last Modified: Sat, 19 Aug 2023 05:24:35 GMT  
		Size: 31.2 MB (31242759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:89c018c5ddbc7656b0af4b7afe4f0d531acca40e79138905853191b6cdc75d1d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26407096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94161fa8d33b8ff4133c502abc2c434f7d1f5b21c437d5ea6521820d6ee22136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Aug 2023 05:07:37 GMT
ARG RELEASE
# Sat, 19 Aug 2023 05:07:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 19 Aug 2023 05:07:37 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 19 Aug 2023 05:07:39 GMT
ADD file:681bda53818a2c0f492a5b6c8f35eb4ecba1d81c3c51e02310824c03db9146e6 in / 
# Sat, 19 Aug 2023 05:07:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fd9cf1abf5e584207948c92e06b060305d0e1e0babd02387c55d8b25ad7ae623`  
		Last Modified: Sat, 19 Aug 2023 05:24:41 GMT  
		Size: 26.4 MB (26407096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20230912`

```console
$ docker pull ubuntu@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:f1090cfa89ab321a6d670e79652f61593502591f2fc7452fb0b7c6da575729c4
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
$ docker pull ubuntu@sha256:24898c8e1ac370d2d309d6d9df56af52bebdad86925c623b5e87e12404453518
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26873617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21098a29e034a8f6f1952d1d8a49b5732b70e532c31f0e88e1ff499c6540c57c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:28:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:28:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:28:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:28:32 GMT
ADD file:7392bed4dbab9fb7c9ad5bde6f3bfcde3bcbf1885c336af9c231af6defaa31e1 in / 
# Wed, 16 Aug 2023 04:28:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:10fb01f4f619bc954ba611cebca23f2b96d255c7ead4040b449f063e530df1a4`  
		Last Modified: Wed, 16 Aug 2023 04:34:32 GMT  
		Size: 26.9 MB (26873617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1e9568cacc4bd0a59a44d8e68ae8fc5f4287c132d455492881f7a1106b722beb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24627247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46f21739314ec025a0ce92c7a657ddb65785a29870d74435a08554207fb3688`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:11 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:11 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:16 GMT
ADD file:1f1c9502544acdbb6a7450226ced78cfe982a6305f2aea77ab7d1f73b50fc7f0 in / 
# Wed, 16 Aug 2023 04:16:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e05ef4abc6c76087042349392d272a7eeb590834dc45d1247295302c212fda9d`  
		Last Modified: Wed, 16 Aug 2023 04:34:45 GMT  
		Size: 24.6 MB (24627247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d68d8bcae123a839bc72b91fa9df55956be3fcb2dbfc247acb7f65908eaa6c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26064545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c8e9335de75964dd320b20b4290408432be2962faf7ad36d3a47d48f3131cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:15:57 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:15:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:15:57 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:01 GMT
ADD file:adea2962926b29b76eb8da76ae9e830c5ad7050ae9b19f5427191b338c8a2c56 in / 
# Wed, 16 Aug 2023 04:16:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b2d15932a31f0857b9499cc218b8777708cb1d73ae6ef680f624ca7d4342763`  
		Last Modified: Wed, 16 Aug 2023 04:34:39 GMT  
		Size: 26.1 MB (26064545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1306e75f505a2305f2c46f51f33be8b8599923bd5a652c3b5dc37333db4f44ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91733a8763fe80d6e620ec400c2721ee45c0f80398506088d1278d6531299a90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:16:31 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:16:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:16:31 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:16:34 GMT
ADD file:a9d35b320d969ee1ae8a7bc83aba49da30d93724befb5948c680066ad4f1acdf in / 
# Wed, 16 Aug 2023 04:16:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f51cbff870f31d4c4397c2f21529046998f8d6e7748fd6f059b325a0759c7dd4`  
		Last Modified: Wed, 16 Aug 2023 04:34:51 GMT  
		Size: 30.9 MB (30905042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:ec9620bbf89d1a3b1171f961340a890166607be3423d96e740f6d56f36ccb125
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1289eb3132a14bc161676d7f928d557bf63eb8561718e9d5247e16e88ebee8ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Aug 2023 04:29:27 GMT
ARG RELEASE
# Wed, 16 Aug 2023 04:29:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 04:29:28 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 16 Aug 2023 04:29:29 GMT
ADD file:14fcf0756fb29b609af54412c31e2ff9acbf4634984ce95bf204c67668706cb5 in / 
# Wed, 16 Aug 2023 04:29:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b1e434384d3d3b546e155df0cf143c8c0a92bf766c6808bf2e3e1d2f22010839`  
		Last Modified: Wed, 16 Aug 2023 04:34:57 GMT  
		Size: 25.7 MB (25691524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
