<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:24.10`](#ubuntu2410)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240918`](#ubuntufocal-20240918)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240911.1`](#ubuntujammy-202409111)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240904.1`](#ubuntunoble-202409041)
-	[`ubuntu:oracular`](#ubuntuoracular)
-	[`ubuntu:oracular-20240918`](#ubuntuoracular-20240918)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:6d8d9799fe6ab3221965efac00b4c34a2bcc102c086a58dff9e19a08b913c7ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:4334ab5016f708cf4a15794e48ebea4c5666fd2bad49679badc4930bf42d9ccb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9522b5ff29b80fb026c27040cc14b743d714a57f3ca4cff1c76c9e59ca244163`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8e1fcaeb011b78519a2d06ec8a4bd4c84e2b584aa49ad6c82fe4f5ca200162fd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23619920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307068409b77ae136b2a4929ea2fef3dd46d105a464f26c0bccfdfb426d591f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:11eda96b18d1f3db85ac2aa91b88e0f8afbb12b21c50d6dfa06eec4ced4c76dd`  
		Last Modified: Wed, 18 Sep 2024 05:32:52 GMT  
		Size: 23.6 MB (23619920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d3075bef3a8dea9174be5d6c537b9828396fcb516851b8418c84cc770c94bbf2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecfa68232396b9e2dbbdf15d9eb41c6304666dab1fe76a4f1cdf6ae60f0e403`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a89e9a4e6e75a6c9b1f3898744edf74093d1d40f70bb71666c9f9c082f428fe3
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339c75c16d775305f761d67f788e7267b9e43436a416eab6c7ad3ba1bfb2593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:aa23e326daa7a1f4bcd13c414efebde3ce33ebbeafd5ccdcc383e8cd4cdf24da
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23470151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8bd0733c6a214da3d6288349edb04028e786377a8d34feabc6ba1929b4e120`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:44:06 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:44:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:44:35 GMT
ADD file:2b79df939efa8d17a9cd9432bbfe34fed1d540f46c23529b1cdab31b56362460 in / 
# Wed, 18 Sep 2024 04:44:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0efaa43698cbf8c0e0a6b9e91349afc67eaa948267787cd9ac74cffc25bbe0a`  
		Last Modified: Wed, 18 Sep 2024 05:33:04 GMT  
		Size: 23.5 MB (23470151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:0f8ff9783a36e5326836da25ab66d3a3457fb9edb3292f92fe8d548d464c7b68
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26365746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed33c211787a7025976a0dc02a989e86ef988b792ce7eb8cae18fa6b56e409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e84e73c86cd80310316bdb1d20baeccb3a0d4ffc98a27283aa05f904ec53469`  
		Last Modified: Wed, 18 Sep 2024 05:33:10 GMT  
		Size: 26.4 MB (26365746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:58b87898e82351c6cf9cf5b9f3c20257bb9e2dcf33af051e12ce532d7f94e3fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:3d1556a8a18cf5307b121e0a98e93f1ddf1f3f8e092f1fddfd941254785b95d7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29535688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97271d29cb7956f0908cfb1449610a2cd9cb46b004ac8af25f0255663eb364ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:17d75c44d078810c2264962f31c2c3c8a5889ec05edd4e2a00e273a5e1219ebf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961b5577e6c5b1fdd517169f74499d1838c10e4f3718cecce954f693e47f36a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7c75ab2b0567edbb9d4834a2c51e462ebd709740d1f2c40bcd23c56e974fe2a8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981912c48e9a89e903c89b228be977e23eeba83d42e2c8e0593a781a2b251cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:15abdf6cd20e250f2cd5796047ca8370c45c70a2a1279fe0c37c061116d9a525
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34448242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff7ea5b4e8ca182006855f3fca8147b1e0089f2e2d583daa5427ab9e105c226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:e04b34e48954230514d2d2178f4eb0f9629caa21700c263680fc8cc1e0b87b71
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27038996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e091d008a3a95d995fcb7c609f2ba781d4de1ebaa917c98ab01b95bd0c5b551b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:af903bc2047b8dd70bb96aaf5a35df3b722966b7c6659cb37001535f0d643d9c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b0d4008b4e81651b2cf6e89af8946d4d616c267fe863f9a43100a72b585038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:c838b564c4f32429d13b6c7727b95a778d8584ef11ca32a0d9faed2554c7a285
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:24.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:74f92a6b3589aa5cac6028719aaac83de4037bad4371ae79ba362834389035aa
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2756d6fa9d6242fafd5b29f674404779be561db2d0bd932aa3640ae67b9e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4192b2c3b4311ccb41d838a0e33bd1e403afe72d77d424432259dd81fba88edb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26865322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c776a8a25a70e419c94461a02211bf3ba15ee69efd73e1066a416747f715dbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ab09dcd0b4be1b4898671e294ebca9f99c6f189fd24b185e1d6ec8d0fe3a0414`  
		Last Modified: Mon, 16 Sep 2024 07:36:38 GMT  
		Size: 26.9 MB (26865322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d392dca9b7043b31d8214bb8c42e4371df17a6304597c0fb4fe5d2060186b19
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28885430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22ec0081bf1bc159b97b27b55812319e99b710df960a16c2f2495dc7fc61c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:294858195461fe9a982d4c046e6d59ed65032087d32a2aafa734d0e230f06470
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34392021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d041664d09c959aca4ad59f950abc24c7d9b51eec29e7c16aa19f49cae6cd413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f950b6051974e54649098d6026f910465c379ebe8599449cc28a3128b5ad095c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30949308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59070ee36cb209e4ea49d1fc1bee870b1ba13088133e9da9be676abf3434f904`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Aug 2024 16:13:45 GMT
ARG RELEASE
# Tue, 27 Aug 2024 16:13:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 16:13:46 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 16:14:17 GMT
ADD file:93d9ee7cf8a421a6d4ab56202ff743dbe7e87beb3d3c9bc1cebb49cf8e1ae4a7 in / 
# Tue, 27 Aug 2024 16:14:20 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:651d7149a766bf9e12f26204ac9f977fa21fa3adbb24c0d2746c0b1cb99c8924`  
		Last Modified: Tue, 27 Aug 2024 17:08:30 GMT  
		Size: 30.9 MB (30949308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:48459f9f4d0b5444d5a43078d844fd5caf05b31b7553ae79e26d7a18200b9460
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30024612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dceaddeb2575ed72aa25a94acbe027620f89097623fc3756aed0162504bc7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6eecd880048ce8df29a37255a220602697090d0bcdcd331dc292de4df5aa5680`  
		Last Modified: Mon, 16 Sep 2024 07:36:56 GMT  
		Size: 30.0 MB (30024612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.10`

```console
$ docker pull ubuntu@sha256:1e88ea62c606fbe97b8ce78827cf738e5e176308480d23ed691c8dbf950f9eaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:24.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:164c01664783caf799e9026babceea81bfa6341686f7296da93769ceab803583
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34157024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add12d7b778609844adc9ba32b26ed4b9728813cd4429e427a7c1f2e4fa61864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6ed718898f896f4c4be21c3a3b756d67ad875c912218b75ed680b9bde8724054`  
		Last Modified: Wed, 18 Sep 2024 05:12:55 GMT  
		Size: 34.2 MB (34157024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1c274f6fa5acd46af265b71438c44eaee8f8db6a5d901e972920e311cfc69326
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33319358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4905a7ca40462061da37733c75c8f204058ded8d89dbe558b4fbfff957e47e13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6462a9c7bec4ee02c6cb999394470c548578984f9e6a46bac0373a89eb633020`  
		Last Modified: Wed, 18 Sep 2024 05:13:07 GMT  
		Size: 33.3 MB (33319358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f64ecfbbd782f5b1827c225e9ffbb211d5c1898cc21278aa654bc05621943611
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33752693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e967f2622b3aa7937b6a93721d099c89507203b9fe015a8166826c3bdf0f8ad8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f29bcb9f3dcd50ce2c38f06e79cc1abe6a86636c54e28cbb98477500bd529de7`  
		Last Modified: Wed, 18 Sep 2024 05:13:01 GMT  
		Size: 33.8 MB (33752693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cce4f13e55e73c568d263542667529c3a4f86ce95a0c7356f272bc8f03506b7d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38594353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b06b4a13971534bc9438bb6920b151d748b366f6f896ae3c6c00fa6dda5ebf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b757bb330fe281460c337e6ae780d03d402d3fa352293150531f7b0591f1d87`  
		Last Modified: Wed, 18 Sep 2024 05:13:14 GMT  
		Size: 38.6 MB (38594353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; riscv64

```console
$ docker pull ubuntu@sha256:38cc6624fc5e7074e0c7ccccb3edb5164b2776c6c09fc99e213ae07e30496d0c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37492206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826cd41ee39a6a31f4953d251cc635d0a54462e52f4259562aabf23e1f8cf53f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3882895786a68e515e4d5b8476cd78c75ffffdc84986272e09896ba2c6aa36da`  
		Last Modified: Fri, 13 Sep 2024 04:52:32 GMT  
		Size: 37.5 MB (37492206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:891d888358d9f17b68429662b28d0e0db1bc019bf183abac1109ff8c0de24df7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33947344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0563f7b016b2957dce269f79a994ec0d0e047445969ef480e0d0cc6b9e36fc71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6cbf574dc20eda221af72fd72bc11c1735a5a0faaf03911b95d0794647e6dc58`  
		Last Modified: Wed, 18 Sep 2024 05:13:26 GMT  
		Size: 33.9 MB (33947344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:1e88ea62c606fbe97b8ce78827cf738e5e176308480d23ed691c8dbf950f9eaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:164c01664783caf799e9026babceea81bfa6341686f7296da93769ceab803583
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34157024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add12d7b778609844adc9ba32b26ed4b9728813cd4429e427a7c1f2e4fa61864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6ed718898f896f4c4be21c3a3b756d67ad875c912218b75ed680b9bde8724054`  
		Last Modified: Wed, 18 Sep 2024 05:12:55 GMT  
		Size: 34.2 MB (34157024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1c274f6fa5acd46af265b71438c44eaee8f8db6a5d901e972920e311cfc69326
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33319358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4905a7ca40462061da37733c75c8f204058ded8d89dbe558b4fbfff957e47e13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6462a9c7bec4ee02c6cb999394470c548578984f9e6a46bac0373a89eb633020`  
		Last Modified: Wed, 18 Sep 2024 05:13:07 GMT  
		Size: 33.3 MB (33319358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f64ecfbbd782f5b1827c225e9ffbb211d5c1898cc21278aa654bc05621943611
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33752693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e967f2622b3aa7937b6a93721d099c89507203b9fe015a8166826c3bdf0f8ad8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f29bcb9f3dcd50ce2c38f06e79cc1abe6a86636c54e28cbb98477500bd529de7`  
		Last Modified: Wed, 18 Sep 2024 05:13:01 GMT  
		Size: 33.8 MB (33752693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cce4f13e55e73c568d263542667529c3a4f86ce95a0c7356f272bc8f03506b7d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38594353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b06b4a13971534bc9438bb6920b151d748b366f6f896ae3c6c00fa6dda5ebf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b757bb330fe281460c337e6ae780d03d402d3fa352293150531f7b0591f1d87`  
		Last Modified: Wed, 18 Sep 2024 05:13:14 GMT  
		Size: 38.6 MB (38594353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; riscv64

```console
$ docker pull ubuntu@sha256:38cc6624fc5e7074e0c7ccccb3edb5164b2776c6c09fc99e213ae07e30496d0c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37492206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826cd41ee39a6a31f4953d251cc635d0a54462e52f4259562aabf23e1f8cf53f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3882895786a68e515e4d5b8476cd78c75ffffdc84986272e09896ba2c6aa36da`  
		Last Modified: Fri, 13 Sep 2024 04:52:32 GMT  
		Size: 37.5 MB (37492206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:891d888358d9f17b68429662b28d0e0db1bc019bf183abac1109ff8c0de24df7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33947344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0563f7b016b2957dce269f79a994ec0d0e047445969ef480e0d0cc6b9e36fc71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6cbf574dc20eda221af72fd72bc11c1735a5a0faaf03911b95d0794647e6dc58`  
		Last Modified: Wed, 18 Sep 2024 05:13:26 GMT  
		Size: 33.9 MB (33947344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:6d8d9799fe6ab3221965efac00b4c34a2bcc102c086a58dff9e19a08b913c7ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:4334ab5016f708cf4a15794e48ebea4c5666fd2bad49679badc4930bf42d9ccb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9522b5ff29b80fb026c27040cc14b743d714a57f3ca4cff1c76c9e59ca244163`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8e1fcaeb011b78519a2d06ec8a4bd4c84e2b584aa49ad6c82fe4f5ca200162fd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23619920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307068409b77ae136b2a4929ea2fef3dd46d105a464f26c0bccfdfb426d591f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:11eda96b18d1f3db85ac2aa91b88e0f8afbb12b21c50d6dfa06eec4ced4c76dd`  
		Last Modified: Wed, 18 Sep 2024 05:32:52 GMT  
		Size: 23.6 MB (23619920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d3075bef3a8dea9174be5d6c537b9828396fcb516851b8418c84cc770c94bbf2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecfa68232396b9e2dbbdf15d9eb41c6304666dab1fe76a4f1cdf6ae60f0e403`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a89e9a4e6e75a6c9b1f3898744edf74093d1d40f70bb71666c9f9c082f428fe3
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339c75c16d775305f761d67f788e7267b9e43436a416eab6c7ad3ba1bfb2593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; riscv64

```console
$ docker pull ubuntu@sha256:aa23e326daa7a1f4bcd13c414efebde3ce33ebbeafd5ccdcc383e8cd4cdf24da
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23470151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8bd0733c6a214da3d6288349edb04028e786377a8d34feabc6ba1929b4e120`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:44:06 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:44:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:44:35 GMT
ADD file:2b79df939efa8d17a9cd9432bbfe34fed1d540f46c23529b1cdab31b56362460 in / 
# Wed, 18 Sep 2024 04:44:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0efaa43698cbf8c0e0a6b9e91349afc67eaa948267787cd9ac74cffc25bbe0a`  
		Last Modified: Wed, 18 Sep 2024 05:33:04 GMT  
		Size: 23.5 MB (23470151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:0f8ff9783a36e5326836da25ab66d3a3457fb9edb3292f92fe8d548d464c7b68
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26365746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed33c211787a7025976a0dc02a989e86ef988b792ce7eb8cae18fa6b56e409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e84e73c86cd80310316bdb1d20baeccb3a0d4ffc98a27283aa05f904ec53469`  
		Last Modified: Wed, 18 Sep 2024 05:33:10 GMT  
		Size: 26.4 MB (26365746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240918`

```console
$ docker pull ubuntu@sha256:6d8d9799fe6ab3221965efac00b4c34a2bcc102c086a58dff9e19a08b913c7ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:focal-20240918` - linux; amd64

```console
$ docker pull ubuntu@sha256:4334ab5016f708cf4a15794e48ebea4c5666fd2bad49679badc4930bf42d9ccb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9522b5ff29b80fb026c27040cc14b743d714a57f3ca4cff1c76c9e59ca244163`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240918` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8e1fcaeb011b78519a2d06ec8a4bd4c84e2b584aa49ad6c82fe4f5ca200162fd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23619920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307068409b77ae136b2a4929ea2fef3dd46d105a464f26c0bccfdfb426d591f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:49 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:49 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:52 GMT
ADD file:b45f16aef7261ad85f3d12973e7c45554ae8daa512a016d6898c6c1c37fe383f in / 
# Wed, 18 Sep 2024 04:18:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:11eda96b18d1f3db85ac2aa91b88e0f8afbb12b21c50d6dfa06eec4ced4c76dd`  
		Last Modified: Wed, 18 Sep 2024 05:32:52 GMT  
		Size: 23.6 MB (23619920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240918` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d3075bef3a8dea9174be5d6c537b9828396fcb516851b8418c84cc770c94bbf2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecfa68232396b9e2dbbdf15d9eb41c6304666dab1fe76a4f1cdf6ae60f0e403`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240918` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:a89e9a4e6e75a6c9b1f3898744edf74093d1d40f70bb71666c9f9c082f428fe3
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339c75c16d775305f761d67f788e7267b9e43436a416eab6c7ad3ba1bfb2593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240918` - linux; riscv64

```console
$ docker pull ubuntu@sha256:aa23e326daa7a1f4bcd13c414efebde3ce33ebbeafd5ccdcc383e8cd4cdf24da
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23470151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8bd0733c6a214da3d6288349edb04028e786377a8d34feabc6ba1929b4e120`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:44:06 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:44:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:44:07 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:44:35 GMT
ADD file:2b79df939efa8d17a9cd9432bbfe34fed1d540f46c23529b1cdab31b56362460 in / 
# Wed, 18 Sep 2024 04:44:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0efaa43698cbf8c0e0a6b9e91349afc67eaa948267787cd9ac74cffc25bbe0a`  
		Last Modified: Wed, 18 Sep 2024 05:33:04 GMT  
		Size: 23.5 MB (23470151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240918` - linux; s390x

```console
$ docker pull ubuntu@sha256:0f8ff9783a36e5326836da25ab66d3a3457fb9edb3292f92fe8d548d464c7b68
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26365746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed33c211787a7025976a0dc02a989e86ef988b792ce7eb8cae18fa6b56e409`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:29 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:29 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:31 GMT
ADD file:df7e2b5c8c623d387fbe67b0b2d9c79bf4738453942e9b3f983b876e6e1ec871 in / 
# Wed, 18 Sep 2024 04:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e84e73c86cd80310316bdb1d20baeccb3a0d4ffc98a27283aa05f904ec53469`  
		Last Modified: Wed, 18 Sep 2024 05:33:10 GMT  
		Size: 26.4 MB (26365746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:58b87898e82351c6cf9cf5b9f3c20257bb9e2dcf33af051e12ce532d7f94e3fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:3d1556a8a18cf5307b121e0a98e93f1ddf1f3f8e092f1fddfd941254785b95d7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29535688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97271d29cb7956f0908cfb1449610a2cd9cb46b004ac8af25f0255663eb364ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:17d75c44d078810c2264962f31c2c3c8a5889ec05edd4e2a00e273a5e1219ebf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961b5577e6c5b1fdd517169f74499d1838c10e4f3718cecce954f693e47f36a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7c75ab2b0567edbb9d4834a2c51e462ebd709740d1f2c40bcd23c56e974fe2a8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981912c48e9a89e903c89b228be977e23eeba83d42e2c8e0593a781a2b251cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:15abdf6cd20e250f2cd5796047ca8370c45c70a2a1279fe0c37c061116d9a525
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34448242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff7ea5b4e8ca182006855f3fca8147b1e0089f2e2d583daa5427ab9e105c226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; riscv64

```console
$ docker pull ubuntu@sha256:e04b34e48954230514d2d2178f4eb0f9629caa21700c263680fc8cc1e0b87b71
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27038996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e091d008a3a95d995fcb7c609f2ba781d4de1ebaa917c98ab01b95bd0c5b551b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:af903bc2047b8dd70bb96aaf5a35df3b722966b7c6659cb37001535f0d643d9c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b0d4008b4e81651b2cf6e89af8946d4d616c267fe863f9a43100a72b585038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240911.1`

```console
$ docker pull ubuntu@sha256:58b87898e82351c6cf9cf5b9f3c20257bb9e2dcf33af051e12ce532d7f94e3fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:jammy-20240911.1` - linux; amd64

```console
$ docker pull ubuntu@sha256:3d1556a8a18cf5307b121e0a98e93f1ddf1f3f8e092f1fddfd941254785b95d7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29535688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97271d29cb7956f0908cfb1449610a2cd9cb46b004ac8af25f0255663eb364ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240911.1` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:17d75c44d078810c2264962f31c2c3c8a5889ec05edd4e2a00e273a5e1219ebf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26639293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961b5577e6c5b1fdd517169f74499d1838c10e4f3718cecce954f693e47f36a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:56 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:59 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Wed, 11 Sep 2024 16:25:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b477f0f37762a62f631ac4fbaed78c3b23c47db7ac1eaefe95bda0e85ce052a0`  
		Last Modified: Wed, 11 Sep 2024 17:24:53 GMT  
		Size: 26.6 MB (26639293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240911.1` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7c75ab2b0567edbb9d4834a2c51e462ebd709740d1f2c40bcd23c56e974fe2a8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27358329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981912c48e9a89e903c89b228be977e23eeba83d42e2c8e0593a781a2b251cba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240911.1` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:15abdf6cd20e250f2cd5796047ca8370c45c70a2a1279fe0c37c061116d9a525
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34448242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff7ea5b4e8ca182006855f3fca8147b1e0089f2e2d583daa5427ab9e105c226`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240911.1` - linux; riscv64

```console
$ docker pull ubuntu@sha256:e04b34e48954230514d2d2178f4eb0f9629caa21700c263680fc8cc1e0b87b71
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27038996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e091d008a3a95d995fcb7c609f2ba781d4de1ebaa917c98ab01b95bd0c5b551b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:40:02 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:40:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:40:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:40:33 GMT
ADD file:d73c592fd8b1cf53b1e79e60cc01a9371bf9156f299ddf5a8482ea43525aaa9a in / 
# Wed, 11 Sep 2024 16:40:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6579073ec343e2eff1822992b7ff52b06a067be5c14999033789394aadca585d`  
		Last Modified: Wed, 11 Sep 2024 17:25:05 GMT  
		Size: 27.0 MB (27038996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240911.1` - linux; s390x

```console
$ docker pull ubuntu@sha256:af903bc2047b8dd70bb96aaf5a35df3b722966b7c6659cb37001535f0d643d9c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28001475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b0d4008b4e81651b2cf6e89af8946d4d616c267fe863f9a43100a72b585038`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:b359f1067efa76f37863778f7b6d0e8d911e3ee8efa807ad01fbf5dc1ef9006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:74f92a6b3589aa5cac6028719aaac83de4037bad4371ae79ba362834389035aa
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2756d6fa9d6242fafd5b29f674404779be561db2d0bd932aa3640ae67b9e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4192b2c3b4311ccb41d838a0e33bd1e403afe72d77d424432259dd81fba88edb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26865322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c776a8a25a70e419c94461a02211bf3ba15ee69efd73e1066a416747f715dbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ab09dcd0b4be1b4898671e294ebca9f99c6f189fd24b185e1d6ec8d0fe3a0414`  
		Last Modified: Mon, 16 Sep 2024 07:36:38 GMT  
		Size: 26.9 MB (26865322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d392dca9b7043b31d8214bb8c42e4371df17a6304597c0fb4fe5d2060186b19
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28885430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22ec0081bf1bc159b97b27b55812319e99b710df960a16c2f2495dc7fc61c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:294858195461fe9a982d4c046e6d59ed65032087d32a2aafa734d0e230f06470
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34392021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d041664d09c959aca4ad59f950abc24c7d9b51eec29e7c16aa19f49cae6cd413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; riscv64

```console
$ docker pull ubuntu@sha256:08d0f41b17da54c7c5bc30c9275b9cfad79e59915138325ba846f8d7b254c0e2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30949550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c91726a64f8152872b78353cc403464ee89890d2fc6483833de774c5107ac5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:072c212ebb6b7710c5a2278c572459079136713a45c588184d91ca6cdbfcca3c`  
		Last Modified: Mon, 16 Sep 2024 07:36:50 GMT  
		Size: 30.9 MB (30949550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:48459f9f4d0b5444d5a43078d844fd5caf05b31b7553ae79e26d7a18200b9460
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30024612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dceaddeb2575ed72aa25a94acbe027620f89097623fc3756aed0162504bc7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6eecd880048ce8df29a37255a220602697090d0bcdcd331dc292de4df5aa5680`  
		Last Modified: Mon, 16 Sep 2024 07:36:56 GMT  
		Size: 30.0 MB (30024612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:b359f1067efa76f37863778f7b6d0e8d911e3ee8efa807ad01fbf5dc1ef9006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:noble` - linux; amd64

```console
$ docker pull ubuntu@sha256:74f92a6b3589aa5cac6028719aaac83de4037bad4371ae79ba362834389035aa
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2756d6fa9d6242fafd5b29f674404779be561db2d0bd932aa3640ae67b9e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4192b2c3b4311ccb41d838a0e33bd1e403afe72d77d424432259dd81fba88edb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26865322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c776a8a25a70e419c94461a02211bf3ba15ee69efd73e1066a416747f715dbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ab09dcd0b4be1b4898671e294ebca9f99c6f189fd24b185e1d6ec8d0fe3a0414`  
		Last Modified: Mon, 16 Sep 2024 07:36:38 GMT  
		Size: 26.9 MB (26865322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d392dca9b7043b31d8214bb8c42e4371df17a6304597c0fb4fe5d2060186b19
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28885430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22ec0081bf1bc159b97b27b55812319e99b710df960a16c2f2495dc7fc61c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:294858195461fe9a982d4c046e6d59ed65032087d32a2aafa734d0e230f06470
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34392021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d041664d09c959aca4ad59f950abc24c7d9b51eec29e7c16aa19f49cae6cd413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; riscv64

```console
$ docker pull ubuntu@sha256:08d0f41b17da54c7c5bc30c9275b9cfad79e59915138325ba846f8d7b254c0e2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30949550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c91726a64f8152872b78353cc403464ee89890d2fc6483833de774c5107ac5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:072c212ebb6b7710c5a2278c572459079136713a45c588184d91ca6cdbfcca3c`  
		Last Modified: Mon, 16 Sep 2024 07:36:50 GMT  
		Size: 30.9 MB (30949550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:48459f9f4d0b5444d5a43078d844fd5caf05b31b7553ae79e26d7a18200b9460
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30024612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dceaddeb2575ed72aa25a94acbe027620f89097623fc3756aed0162504bc7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6eecd880048ce8df29a37255a220602697090d0bcdcd331dc292de4df5aa5680`  
		Last Modified: Mon, 16 Sep 2024 07:36:56 GMT  
		Size: 30.0 MB (30024612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240904.1`

```console
$ docker pull ubuntu@sha256:b359f1067efa76f37863778f7b6d0e8d911e3ee8efa807ad01fbf5dc1ef9006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:noble-20240904.1` - linux; amd64

```console
$ docker pull ubuntu@sha256:74f92a6b3589aa5cac6028719aaac83de4037bad4371ae79ba362834389035aa
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2756d6fa9d6242fafd5b29f674404779be561db2d0bd932aa3640ae67b9e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240904.1` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4192b2c3b4311ccb41d838a0e33bd1e403afe72d77d424432259dd81fba88edb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26865322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c776a8a25a70e419c94461a02211bf3ba15ee69efd73e1066a416747f715dbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ab09dcd0b4be1b4898671e294ebca9f99c6f189fd24b185e1d6ec8d0fe3a0414`  
		Last Modified: Mon, 16 Sep 2024 07:36:38 GMT  
		Size: 26.9 MB (26865322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240904.1` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d392dca9b7043b31d8214bb8c42e4371df17a6304597c0fb4fe5d2060186b19
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28885430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22ec0081bf1bc159b97b27b55812319e99b710df960a16c2f2495dc7fc61c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240904.1` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:294858195461fe9a982d4c046e6d59ed65032087d32a2aafa734d0e230f06470
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34392021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d041664d09c959aca4ad59f950abc24c7d9b51eec29e7c16aa19f49cae6cd413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240904.1` - linux; riscv64

```console
$ docker pull ubuntu@sha256:08d0f41b17da54c7c5bc30c9275b9cfad79e59915138325ba846f8d7b254c0e2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30949550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c91726a64f8152872b78353cc403464ee89890d2fc6483833de774c5107ac5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:072c212ebb6b7710c5a2278c572459079136713a45c588184d91ca6cdbfcca3c`  
		Last Modified: Mon, 16 Sep 2024 07:36:50 GMT  
		Size: 30.9 MB (30949550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240904.1` - linux; s390x

```console
$ docker pull ubuntu@sha256:48459f9f4d0b5444d5a43078d844fd5caf05b31b7553ae79e26d7a18200b9460
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30024612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dceaddeb2575ed72aa25a94acbe027620f89097623fc3756aed0162504bc7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6eecd880048ce8df29a37255a220602697090d0bcdcd331dc292de4df5aa5680`  
		Last Modified: Mon, 16 Sep 2024 07:36:56 GMT  
		Size: 30.0 MB (30024612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular`

```console
$ docker pull ubuntu@sha256:c62f1babc85f8756f395e6aabda682acd7c58a1b0c3bea250713cd0184a93efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:oracular` - linux; amd64

```console
$ docker pull ubuntu@sha256:164c01664783caf799e9026babceea81bfa6341686f7296da93769ceab803583
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34157024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add12d7b778609844adc9ba32b26ed4b9728813cd4429e427a7c1f2e4fa61864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6ed718898f896f4c4be21c3a3b756d67ad875c912218b75ed680b9bde8724054`  
		Last Modified: Wed, 18 Sep 2024 05:12:55 GMT  
		Size: 34.2 MB (34157024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1c274f6fa5acd46af265b71438c44eaee8f8db6a5d901e972920e311cfc69326
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33319358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4905a7ca40462061da37733c75c8f204058ded8d89dbe558b4fbfff957e47e13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6462a9c7bec4ee02c6cb999394470c548578984f9e6a46bac0373a89eb633020`  
		Last Modified: Wed, 18 Sep 2024 05:13:07 GMT  
		Size: 33.3 MB (33319358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f64ecfbbd782f5b1827c225e9ffbb211d5c1898cc21278aa654bc05621943611
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33752693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e967f2622b3aa7937b6a93721d099c89507203b9fe015a8166826c3bdf0f8ad8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f29bcb9f3dcd50ce2c38f06e79cc1abe6a86636c54e28cbb98477500bd529de7`  
		Last Modified: Wed, 18 Sep 2024 05:13:01 GMT  
		Size: 33.8 MB (33752693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cce4f13e55e73c568d263542667529c3a4f86ce95a0c7356f272bc8f03506b7d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38594353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b06b4a13971534bc9438bb6920b151d748b366f6f896ae3c6c00fa6dda5ebf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b757bb330fe281460c337e6ae780d03d402d3fa352293150531f7b0591f1d87`  
		Last Modified: Wed, 18 Sep 2024 05:13:14 GMT  
		Size: 38.6 MB (38594353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; riscv64

```console
$ docker pull ubuntu@sha256:15b1b51fd69ef84b63e5e6fa7182fa414edd4d245a0a921f383a6bb6724d7425
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37487731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5324e0cb95a436a317ad3777a5584f9c70f6e5decef80bb6181122721ec6dd2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:04591114bd13d93275353d817ee6001e80c82f44ceff99120d8f777ccc92274b`  
		Last Modified: Wed, 18 Sep 2024 05:13:20 GMT  
		Size: 37.5 MB (37487731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; s390x

```console
$ docker pull ubuntu@sha256:891d888358d9f17b68429662b28d0e0db1bc019bf183abac1109ff8c0de24df7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33947344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0563f7b016b2957dce269f79a994ec0d0e047445969ef480e0d0cc6b9e36fc71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6cbf574dc20eda221af72fd72bc11c1735a5a0faaf03911b95d0794647e6dc58`  
		Last Modified: Wed, 18 Sep 2024 05:13:26 GMT  
		Size: 33.9 MB (33947344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular-20240918`

```console
$ docker pull ubuntu@sha256:c62f1babc85f8756f395e6aabda682acd7c58a1b0c3bea250713cd0184a93efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:oracular-20240918` - linux; amd64

```console
$ docker pull ubuntu@sha256:164c01664783caf799e9026babceea81bfa6341686f7296da93769ceab803583
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34157024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add12d7b778609844adc9ba32b26ed4b9728813cd4429e427a7c1f2e4fa61864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:56:52 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:56:52 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:56:54 GMT
ADD file:34960976e9fa0e0fb13074c6911c3f1ec7b0f3060a3e974a7990f112b21dfd8e in / 
# Wed, 18 Sep 2024 03:56:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6ed718898f896f4c4be21c3a3b756d67ad875c912218b75ed680b9bde8724054`  
		Last Modified: Wed, 18 Sep 2024 05:12:55 GMT  
		Size: 34.2 MB (34157024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240918` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:1c274f6fa5acd46af265b71438c44eaee8f8db6a5d901e972920e311cfc69326
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33319358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4905a7ca40462061da37733c75c8f204058ded8d89dbe558b4fbfff957e47e13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:56 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:56 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:59 GMT
ADD file:b20509e33aca34c58565d5c38befc8f0446b34a5cbb409d03147aab392e5bb95 in / 
# Wed, 18 Sep 2024 03:58:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6462a9c7bec4ee02c6cb999394470c548578984f9e6a46bac0373a89eb633020`  
		Last Modified: Wed, 18 Sep 2024 05:13:07 GMT  
		Size: 33.3 MB (33319358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240918` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f64ecfbbd782f5b1827c225e9ffbb211d5c1898cc21278aa654bc05621943611
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33752693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e967f2622b3aa7937b6a93721d099c89507203b9fe015a8166826c3bdf0f8ad8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:05 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:05 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:07 GMT
ADD file:cd1dbd2cf0195cc6d4674a585350e1a69fa96a310f6fcb1779824f40d9dad7bc in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f29bcb9f3dcd50ce2c38f06e79cc1abe6a86636c54e28cbb98477500bd529de7`  
		Last Modified: Wed, 18 Sep 2024 05:13:01 GMT  
		Size: 33.8 MB (33752693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240918` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cce4f13e55e73c568d263542667529c3a4f86ce95a0c7356f272bc8f03506b7d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38594353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b06b4a13971534bc9438bb6920b151d748b366f6f896ae3c6c00fa6dda5ebf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:58:02 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:58:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:58:02 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:58:06 GMT
ADD file:06706071c1ca331eeb46804ea489d12de04ca8396c988aa1af4d825df23c914f in / 
# Wed, 18 Sep 2024 03:58:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2b757bb330fe281460c337e6ae780d03d402d3fa352293150531f7b0591f1d87`  
		Last Modified: Wed, 18 Sep 2024 05:13:14 GMT  
		Size: 38.6 MB (38594353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240918` - linux; riscv64

```console
$ docker pull ubuntu@sha256:15b1b51fd69ef84b63e5e6fa7182fa414edd4d245a0a921f383a6bb6724d7425
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37487731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5324e0cb95a436a317ad3777a5584f9c70f6e5decef80bb6181122721ec6dd2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 04:12:38 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:12:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:12:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:12:39 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 04:13:12 GMT
ADD file:845e21eb0f8f24ff79deb49f33bb09a928b70e6af9d901303a950a5614468b9a in / 
# Wed, 18 Sep 2024 04:13:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:04591114bd13d93275353d817ee6001e80c82f44ceff99120d8f777ccc92274b`  
		Last Modified: Wed, 18 Sep 2024 05:13:20 GMT  
		Size: 37.5 MB (37487731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular-20240918` - linux; s390x

```console
$ docker pull ubuntu@sha256:891d888358d9f17b68429662b28d0e0db1bc019bf183abac1109ff8c0de24df7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33947344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0563f7b016b2957dce269f79a994ec0d0e047445969ef480e0d0cc6b9e36fc71`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Sep 2024 03:57:27 GMT
ARG RELEASE
# Wed, 18 Sep 2024 03:57:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 03:57:27 GMT
LABEL org.opencontainers.image.version=24.10
# Wed, 18 Sep 2024 03:57:28 GMT
ADD file:e41c6d9ae5268de87153f5edfcf09d55f5acd46b261a676b5cdd694b2af56a03 in / 
# Wed, 18 Sep 2024 03:57:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6cbf574dc20eda221af72fd72bc11c1735a5a0faaf03911b95d0794647e6dc58`  
		Last Modified: Wed, 18 Sep 2024 05:13:26 GMT  
		Size: 33.9 MB (33947344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:b359f1067efa76f37863778f7b6d0e8d911e3ee8efa807ad01fbf5dc1ef9006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:74f92a6b3589aa5cac6028719aaac83de4037bad4371ae79ba362834389035aa
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b2756d6fa9d6242fafd5b29f674404779be561db2d0bd932aa3640ae67b9e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4192b2c3b4311ccb41d838a0e33bd1e403afe72d77d424432259dd81fba88edb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26865322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c776a8a25a70e419c94461a02211bf3ba15ee69efd73e1066a416747f715dbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:20 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:20 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:23 GMT
ADD file:e936767f044e9a1b6b2475ee575c7d052960fd234a0ce2b100a12bc3713dfe95 in / 
# Mon, 16 Sep 2024 06:23:23 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ab09dcd0b4be1b4898671e294ebca9f99c6f189fd24b185e1d6ec8d0fe3a0414`  
		Last Modified: Mon, 16 Sep 2024 07:36:38 GMT  
		Size: 26.9 MB (26865322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d392dca9b7043b31d8214bb8c42e4371df17a6304597c0fb4fe5d2060186b19
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28885430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22ec0081bf1bc159b97b27b55812319e99b710df960a16c2f2495dc7fc61c00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:294858195461fe9a982d4c046e6d59ed65032087d32a2aafa734d0e230f06470
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34392021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d041664d09c959aca4ad59f950abc24c7d9b51eec29e7c16aa19f49cae6cd413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; riscv64

```console
$ docker pull ubuntu@sha256:08d0f41b17da54c7c5bc30c9275b9cfad79e59915138325ba846f8d7b254c0e2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30949550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c91726a64f8152872b78353cc403464ee89890d2fc6483833de774c5107ac5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:39:54 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:39:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:39:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:40:26 GMT
ADD file:eb024225b66c42c2c00cd16c5d9c4512c68d4b5212da677d150921eefaa6606e in / 
# Mon, 16 Sep 2024 06:40:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:072c212ebb6b7710c5a2278c572459079136713a45c588184d91ca6cdbfcca3c`  
		Last Modified: Mon, 16 Sep 2024 07:36:50 GMT  
		Size: 30.9 MB (30949550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:48459f9f4d0b5444d5a43078d844fd5caf05b31b7553ae79e26d7a18200b9460
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30024612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dceaddeb2575ed72aa25a94acbe027620f89097623fc3756aed0162504bc7cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 06:24:19 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:24:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:24:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:24:21 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Mon, 16 Sep 2024 06:24:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6eecd880048ce8df29a37255a220602697090d0bcdcd331dc292de4df5aa5680`  
		Last Modified: Mon, 16 Sep 2024 07:36:56 GMT  
		Size: 30.0 MB (30024612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
