<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20231003`](#ubuntufocal-20231003)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20231004`](#ubuntujammy-20231004)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20231004`](#ubuntulunar-20231004)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20231011`](#ubuntumantic-20231011)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:59f5f8b43ebcd48f0cad95b16570b17e67bcedf8455394011d0922fd4db668ad
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
$ docker pull ubuntu@sha256:218bb51abbd1864df8be26166f847547b3851a89999ca7bfceb85ca9b5d2e95d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27505999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf40b7bc7a11b43785755d3c5f23dee03b08e988b327a2f10b22d01d5dc5259d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:96d54c3075c9eeaed5561fd620828fd6bb5d80ecae7cb25f9ba5f7d88ea6e15c`  
		Last Modified: Tue, 03 Oct 2023 11:16:43 GMT  
		Size: 27.5 MB (27505999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06e174da2c1a4cd683a888d933a235407a02f2d98fedb49c34601b293fc5e36e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eba8b8e77a0ca1c3d8315507ef4e67d817fb199a4cdbc603a0e06fb1b9f78ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a50255c0017d09ab86514148fe36d006a4ad9a46633b82efd4b0233a9c9082e8`  
		Last Modified: Tue, 03 Oct 2023 11:16:56 GMT  
		Size: 23.6 MB (23612914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a80d11b67ef30474bcccab048020ee25aee659c4caaca70794867deba5d392b6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0341906bdafc976cd73b05ea0e3df2e4884c6b6816197a2ffbd2367061c19acf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:915eebb74587f0e5d3919cb77720c143be9a85a8d2d5cd44675d84c8c3a2b74a`  
		Last Modified: Tue, 03 Oct 2023 11:16:49 GMT  
		Size: 26.0 MB (25973940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d85c88c0c9d7d331683e7f9d96db67946ecd217b57e5e477d1f4e527578ac026
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673ae00b2a1a4c999ed047c4a07731716987185e46132b80a58bb9cdb1f7305d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:03:52 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:03:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:03:56 GMT
ADD file:ba2394102af0c0584d39af9ec5dd4fa13286293b4607ac7cb9e16d7a2781eef2 in / 
# Tue, 03 Oct 2023 11:03:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1c4ab65f666dae98ad8e32b78770e1c705b2a66bd87bd84de1371ecc6e45b22`  
		Last Modified: Tue, 03 Oct 2023 11:17:02 GMT  
		Size: 32.1 MB (32070731 bytes)  
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
$ docker pull ubuntu@sha256:e4e00f1b61658b116ea6f9c787e16b4aa7e833352d17dcacb02c884729377ac1
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
$ docker pull ubuntu@sha256:c9cf959fd83770dfdefd8fb42cfef0761432af36a764c077aed54bbc5bb25368
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c58958181a5925816faa528ce959e487632f4cfd192f8132f71b32df2744b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aece8493d3972efa43bfd4ee3cdba659c0f787f8f59c82fb3e48c87cbb22a12e`  
		Last Modified: Thu, 05 Oct 2023 07:43:26 GMT  
		Size: 29.5 MB (29537387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:02410fbfad7f2842cce3cf7655828424f4f7f6b5105b0016e24f1676f3bd15f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e343402cadef796b4f12c2ee20b7346978a42a8d95516619c36c6397c4b0c766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bfbe77e41a78ee38147c5761aa8bc896d9f6e1e648b23468f294065ffe03c107`  
		Last Modified: Thu, 05 Oct 2023 07:43:33 GMT  
		Size: 27.4 MB (27351048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b5759015a02040b956d02fb5cd8150ae0fdc3db0fd15af76dd006f6833bc9ab4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34555968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a609d38c5a2e47b65cf2a2ff61e6d2d5db4be6eb7578f40c4a672efc1f0cd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90496cba4a92b0bf6a8307bab5dd30100905ac891d478aa27771408328244c33`  
		Last Modified: Thu, 05 Oct 2023 07:43:45 GMT  
		Size: 34.6 MB (34555968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:7c789f181465e5474aa9093b939a9992e2e67637c827a1b81e7890c3f04f6bf6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28024260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04042eae942dd0a766b4d45f17617014c8c3e464113d08a245ee7b43ddfb1f6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:26 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:28 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Mon, 25 Sep 2023 10:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:594ea103c983265390944410c6ac8624359909261a656484e971d00ca0ff8b20`  
		Last Modified: Mon, 25 Sep 2023 10:31:02 GMT  
		Size: 28.0 MB (28024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:9bb767f58e265334f623c972d4234a1b12df34eaeed7631ee02e676dc26b3cb1
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
$ docker pull ubuntu@sha256:04714a1bfbb2d8b5390b5cc0c055e48ebfabd4aa395821b860730ff3277ed74a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26877033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639282825872ec6978281e00795f8f02e3b752112dfa01a5f55a19a0f6cf47dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:18:17 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:18:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:18:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:18:18 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:18:19 GMT
ADD file:d4fca0b2b53fa4e2c3e0d721bf983f4095061c5df5fb084d2daf5efad5ee663d in / 
# Wed, 04 Oct 2023 12:18:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f93f952dad401041cbf7200ea1438a832b72273179a2d36e029ccfda15d49507`  
		Last Modified: Wed, 04 Oct 2023 12:33:09 GMT  
		Size: 26.9 MB (26877033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4dc1dd258d16171c6cd696ed5420402319d7cabe638b176b471495e94373f2a9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83502f31cce9655561356390e34e8d506e888f6ce4743a8400bfa765f6eedb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:25:21 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:25:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:25:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:25:24 GMT
ADD file:b92305119eab5dd3dfb00f4d83cd84e00c8ae57143739329da5a19aeda55be4e in / 
# Wed, 04 Oct 2023 12:25:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:725335f54d3eb8903e713867d9f04db29fbc8835da3539fd3898faa22eaf016e`  
		Last Modified: Wed, 04 Oct 2023 12:33:24 GMT  
		Size: 24.6 MB (24629439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:aa2be6baa498ab5862770bbc08cf00a058154cb257e41dca6ef8b7f7aebe22f8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4783be26912a96818aa1c9468ea8acb5eff2608697f62deff67048595a613145`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:23:52 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:23:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:23:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:23:52 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:23:53 GMT
ADD file:c9b1098bc90ac9b887c3bffdffbcff0c32f32e48df9a673041e3aa796296e69b in / 
# Wed, 04 Oct 2023 12:23:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:89e6336dd9e04a0993754adca328bf88d988540bb95cff284667037dd50f79eb`  
		Last Modified: Wed, 04 Oct 2023 12:33:17 GMT  
		Size: 26.1 MB (26065969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2d697e1fc26340ae1a77a08397f53f978a6966d3c8a3cf195ee0870ca6e7dc2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6651a10a7ea6479a915882811fa23c286c9baabb6ea68a11e48c3235246b574e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:08:54 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:08:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:08:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:08:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:08:57 GMT
ADD file:24bc2f22a395e93a2ebbcfc45da8e5fc7f08e7c03cdc985c997300643d0310ec in / 
# Wed, 04 Oct 2023 12:08:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fafd77e1a2b2b77f4b648372d147a2d31af161695aa89bed56883733707bd39f`  
		Last Modified: Wed, 04 Oct 2023 12:33:31 GMT  
		Size: 30.9 MB (30905941 bytes)  
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
$ docker pull ubuntu@sha256:79bcf74b7ee64b05d8ad7f7451e8ef6865531bae01f5dc9e42ae89acf20a78bd
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
$ docker pull ubuntu@sha256:13f233a16be210b57907b98b0d927ceff7571df390701e14fe1f3901b2c4a4d7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27271091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7a3960a97ee41f84c8045700d2e5bd671a42f02a64ee33dde10627dee1a7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:04:48 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:04:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:04:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:04:49 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:04:50 GMT
ADD file:492ae1940ef5a9a4d7af92b9120b5b7c7d3bfd8107ce94d28eab844ace024981 in / 
# Wed, 11 Oct 2023 18:04:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1cf823cf1f0c938d15f343c52a2110dffb08010fe39e69aba493326b5629709`  
		Last Modified: Wed, 11 Oct 2023 18:17:47 GMT  
		Size: 27.3 MB (27271091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7708743264cbb7f6cf7fc13e915faece45a6cdda455748bc55e58e8de3d27b63
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26379954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9cf3a31fbf871322b774402c7c25b800d0e93c222d5a44339f2d3a99dede82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:03:02 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:03:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:03:10 GMT
ADD file:9e750ebbbf7e47a121d153e6699006776ea61b04b6c8e31556600483a020f617 in / 
# Wed, 11 Oct 2023 18:03:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f906b88252effff97383eeb7dd4d265f3f31a54aa3833dd349cf8c4a35fbdbe9`  
		Last Modified: Wed, 11 Oct 2023 18:17:54 GMT  
		Size: 26.4 MB (26379954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:347a278b913b988b85442a3e187001edfe854da3ed499f45782d4a714f08632f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31340704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fb712785eb8f8fe4cdc47a6bb3bd8014c2b376c684dd430b32f81e786cdd5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:06:00 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:06:03 GMT
ADD file:a18be8add7eb60493b13d2aac8d624230297bd15be033756795582dc07cb04bb in / 
# Wed, 11 Oct 2023 18:06:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e4ddce09953092c8c6052d38bc7c2044237f1337f42f1f86edab6718af804ea`  
		Last Modified: Wed, 11 Oct 2023 18:18:11 GMT  
		Size: 31.3 MB (31340704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:a353c527eb5233fdfc2ad112c7897cce7da6ac28b24d3aaa8f441f27ddf613c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27072390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eca28f81d0bd51084742dc133e32c215a83739fc5603306f1ad774311dc6ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 04:58:19 GMT
ARG RELEASE
# Tue, 26 Sep 2023 04:58:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 04:58:21 GMT
ADD file:e86e9b7546a97fa45e9c726cc317a624a7f94b0bd6dd413d89946ff778b18c77 in / 
# Tue, 26 Sep 2023 04:58:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56312385d597227d0c1232049609586ed3412b04e6ec96c5f6626f5f50f438fe`  
		Last Modified: Tue, 26 Sep 2023 05:34:22 GMT  
		Size: 27.1 MB (27072390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:59f5f8b43ebcd48f0cad95b16570b17e67bcedf8455394011d0922fd4db668ad
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
$ docker pull ubuntu@sha256:218bb51abbd1864df8be26166f847547b3851a89999ca7bfceb85ca9b5d2e95d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27505999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf40b7bc7a11b43785755d3c5f23dee03b08e988b327a2f10b22d01d5dc5259d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:96d54c3075c9eeaed5561fd620828fd6bb5d80ecae7cb25f9ba5f7d88ea6e15c`  
		Last Modified: Tue, 03 Oct 2023 11:16:43 GMT  
		Size: 27.5 MB (27505999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06e174da2c1a4cd683a888d933a235407a02f2d98fedb49c34601b293fc5e36e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eba8b8e77a0ca1c3d8315507ef4e67d817fb199a4cdbc603a0e06fb1b9f78ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a50255c0017d09ab86514148fe36d006a4ad9a46633b82efd4b0233a9c9082e8`  
		Last Modified: Tue, 03 Oct 2023 11:16:56 GMT  
		Size: 23.6 MB (23612914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a80d11b67ef30474bcccab048020ee25aee659c4caaca70794867deba5d392b6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0341906bdafc976cd73b05ea0e3df2e4884c6b6816197a2ffbd2367061c19acf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:915eebb74587f0e5d3919cb77720c143be9a85a8d2d5cd44675d84c8c3a2b74a`  
		Last Modified: Tue, 03 Oct 2023 11:16:49 GMT  
		Size: 26.0 MB (25973940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d85c88c0c9d7d331683e7f9d96db67946ecd217b57e5e477d1f4e527578ac026
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673ae00b2a1a4c999ed047c4a07731716987185e46132b80a58bb9cdb1f7305d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:03:52 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:03:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:03:56 GMT
ADD file:ba2394102af0c0584d39af9ec5dd4fa13286293b4607ac7cb9e16d7a2781eef2 in / 
# Tue, 03 Oct 2023 11:03:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1c4ab65f666dae98ad8e32b78770e1c705b2a66bd87bd84de1371ecc6e45b22`  
		Last Modified: Tue, 03 Oct 2023 11:17:02 GMT  
		Size: 32.1 MB (32070731 bytes)  
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

## `ubuntu:focal-20231003`

```console
$ docker pull ubuntu@sha256:f1e98bf76dada0b7b6acfc1321f2cbe083894b8461d97b8490b3a63741149386
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:focal-20231003` - linux; amd64

```console
$ docker pull ubuntu@sha256:218bb51abbd1864df8be26166f847547b3851a89999ca7bfceb85ca9b5d2e95d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27505999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf40b7bc7a11b43785755d3c5f23dee03b08e988b327a2f10b22d01d5dc5259d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:96d54c3075c9eeaed5561fd620828fd6bb5d80ecae7cb25f9ba5f7d88ea6e15c`  
		Last Modified: Tue, 03 Oct 2023 11:16:43 GMT  
		Size: 27.5 MB (27505999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20231003` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:06e174da2c1a4cd683a888d933a235407a02f2d98fedb49c34601b293fc5e36e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23612914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eba8b8e77a0ca1c3d8315507ef4e67d817fb199a4cdbc603a0e06fb1b9f78ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a50255c0017d09ab86514148fe36d006a4ad9a46633b82efd4b0233a9c9082e8`  
		Last Modified: Tue, 03 Oct 2023 11:16:56 GMT  
		Size: 23.6 MB (23612914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20231003` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a80d11b67ef30474bcccab048020ee25aee659c4caaca70794867deba5d392b6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25973940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0341906bdafc976cd73b05ea0e3df2e4884c6b6816197a2ffbd2367061c19acf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:915eebb74587f0e5d3919cb77720c143be9a85a8d2d5cd44675d84c8c3a2b74a`  
		Last Modified: Tue, 03 Oct 2023 11:16:49 GMT  
		Size: 26.0 MB (25973940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20231003` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d85c88c0c9d7d331683e7f9d96db67946ecd217b57e5e477d1f4e527578ac026
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673ae00b2a1a4c999ed047c4a07731716987185e46132b80a58bb9cdb1f7305d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:03:52 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:03:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:03:53 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:03:56 GMT
ADD file:ba2394102af0c0584d39af9ec5dd4fa13286293b4607ac7cb9e16d7a2781eef2 in / 
# Tue, 03 Oct 2023 11:03:56 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1c4ab65f666dae98ad8e32b78770e1c705b2a66bd87bd84de1371ecc6e45b22`  
		Last Modified: Tue, 03 Oct 2023 11:17:02 GMT  
		Size: 32.1 MB (32070731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:e4e00f1b61658b116ea6f9c787e16b4aa7e833352d17dcacb02c884729377ac1
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
$ docker pull ubuntu@sha256:c9cf959fd83770dfdefd8fb42cfef0761432af36a764c077aed54bbc5bb25368
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c58958181a5925816faa528ce959e487632f4cfd192f8132f71b32df2744b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aece8493d3972efa43bfd4ee3cdba659c0f787f8f59c82fb3e48c87cbb22a12e`  
		Last Modified: Thu, 05 Oct 2023 07:43:26 GMT  
		Size: 29.5 MB (29537387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:02410fbfad7f2842cce3cf7655828424f4f7f6b5105b0016e24f1676f3bd15f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e343402cadef796b4f12c2ee20b7346978a42a8d95516619c36c6397c4b0c766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bfbe77e41a78ee38147c5761aa8bc896d9f6e1e648b23468f294065ffe03c107`  
		Last Modified: Thu, 05 Oct 2023 07:43:33 GMT  
		Size: 27.4 MB (27351048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b5759015a02040b956d02fb5cd8150ae0fdc3db0fd15af76dd006f6833bc9ab4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34555968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a609d38c5a2e47b65cf2a2ff61e6d2d5db4be6eb7578f40c4a672efc1f0cd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90496cba4a92b0bf6a8307bab5dd30100905ac891d478aa27771408328244c33`  
		Last Modified: Thu, 05 Oct 2023 07:43:45 GMT  
		Size: 34.6 MB (34555968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:7c789f181465e5474aa9093b939a9992e2e67637c827a1b81e7890c3f04f6bf6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28024260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04042eae942dd0a766b4d45f17617014c8c3e464113d08a245ee7b43ddfb1f6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:26 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:28 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Mon, 25 Sep 2023 10:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:594ea103c983265390944410c6ac8624359909261a656484e971d00ca0ff8b20`  
		Last Modified: Mon, 25 Sep 2023 10:31:02 GMT  
		Size: 28.0 MB (28024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20231004`

```console
$ docker pull ubuntu@sha256:bcc71729ff023690d265462eb16cd6f88b5aa62af0dd25dd126053b9f995509a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:jammy-20231004` - linux; amd64

```console
$ docker pull ubuntu@sha256:c9cf959fd83770dfdefd8fb42cfef0761432af36a764c077aed54bbc5bb25368
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c58958181a5925816faa528ce959e487632f4cfd192f8132f71b32df2744b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aece8493d3972efa43bfd4ee3cdba659c0f787f8f59c82fb3e48c87cbb22a12e`  
		Last Modified: Thu, 05 Oct 2023 07:43:26 GMT  
		Size: 29.5 MB (29537387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20231004` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20231004` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:02410fbfad7f2842cce3cf7655828424f4f7f6b5105b0016e24f1676f3bd15f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e343402cadef796b4f12c2ee20b7346978a42a8d95516619c36c6397c4b0c766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bfbe77e41a78ee38147c5761aa8bc896d9f6e1e648b23468f294065ffe03c107`  
		Last Modified: Thu, 05 Oct 2023 07:43:33 GMT  
		Size: 27.4 MB (27351048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20231004` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b5759015a02040b956d02fb5cd8150ae0fdc3db0fd15af76dd006f6833bc9ab4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34555968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a609d38c5a2e47b65cf2a2ff61e6d2d5db4be6eb7578f40c4a672efc1f0cd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90496cba4a92b0bf6a8307bab5dd30100905ac891d478aa27771408328244c33`  
		Last Modified: Thu, 05 Oct 2023 07:43:45 GMT  
		Size: 34.6 MB (34555968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:e4e00f1b61658b116ea6f9c787e16b4aa7e833352d17dcacb02c884729377ac1
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
$ docker pull ubuntu@sha256:c9cf959fd83770dfdefd8fb42cfef0761432af36a764c077aed54bbc5bb25368
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29537387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c58958181a5925816faa528ce959e487632f4cfd192f8132f71b32df2744b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aece8493d3972efa43bfd4ee3cdba659c0f787f8f59c82fb3e48c87cbb22a12e`  
		Last Modified: Thu, 05 Oct 2023 07:43:26 GMT  
		Size: 29.5 MB (29537387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:212b9f426e7be12bf9a80b65e1a14fc39e319cff3a7857772b21c02f1eaff610
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26629612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3f9d425ffe4e459ab4cfc7b6f32c504d3f86b0fcb2a1b58d7646ab045ca4c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:56 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:56 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:35:01 GMT
ADD file:4b9d52f97ed5796b14772a84c1e7213402430d32312d15ae04a2dcc9fc485a52 in / 
# Thu, 05 Oct 2023 07:35:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4091a3a7d6aa711dc0e0bbacfd3546df44ca257c300de1ad00fbdc95e218f7bd`  
		Last Modified: Thu, 05 Oct 2023 07:43:39 GMT  
		Size: 26.6 MB (26629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:02410fbfad7f2842cce3cf7655828424f4f7f6b5105b0016e24f1676f3bd15f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27351048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e343402cadef796b4f12c2ee20b7346978a42a8d95516619c36c6397c4b0c766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bfbe77e41a78ee38147c5761aa8bc896d9f6e1e648b23468f294065ffe03c107`  
		Last Modified: Thu, 05 Oct 2023 07:43:33 GMT  
		Size: 27.4 MB (27351048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b5759015a02040b956d02fb5cd8150ae0fdc3db0fd15af76dd006f6833bc9ab4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34555968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a609d38c5a2e47b65cf2a2ff61e6d2d5db4be6eb7578f40c4a672efc1f0cd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90496cba4a92b0bf6a8307bab5dd30100905ac891d478aa27771408328244c33`  
		Last Modified: Thu, 05 Oct 2023 07:43:45 GMT  
		Size: 34.6 MB (34555968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:7c789f181465e5474aa9093b939a9992e2e67637c827a1b81e7890c3f04f6bf6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28024260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04042eae942dd0a766b4d45f17617014c8c3e464113d08a245ee7b43ddfb1f6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:26 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:28 GMT
ADD file:78683f2464233172a7cd0d6adc4c7d9fb3ef05fa67ca22e6fbaca0325496a536 in / 
# Mon, 25 Sep 2023 10:17:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:594ea103c983265390944410c6ac8624359909261a656484e971d00ca0ff8b20`  
		Last Modified: Mon, 25 Sep 2023 10:31:02 GMT  
		Size: 28.0 MB (28024260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:9bb767f58e265334f623c972d4234a1b12df34eaeed7631ee02e676dc26b3cb1
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
$ docker pull ubuntu@sha256:04714a1bfbb2d8b5390b5cc0c055e48ebfabd4aa395821b860730ff3277ed74a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26877033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639282825872ec6978281e00795f8f02e3b752112dfa01a5f55a19a0f6cf47dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:18:17 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:18:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:18:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:18:18 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:18:19 GMT
ADD file:d4fca0b2b53fa4e2c3e0d721bf983f4095061c5df5fb084d2daf5efad5ee663d in / 
# Wed, 04 Oct 2023 12:18:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f93f952dad401041cbf7200ea1438a832b72273179a2d36e029ccfda15d49507`  
		Last Modified: Wed, 04 Oct 2023 12:33:09 GMT  
		Size: 26.9 MB (26877033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4dc1dd258d16171c6cd696ed5420402319d7cabe638b176b471495e94373f2a9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83502f31cce9655561356390e34e8d506e888f6ce4743a8400bfa765f6eedb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:25:21 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:25:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:25:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:25:24 GMT
ADD file:b92305119eab5dd3dfb00f4d83cd84e00c8ae57143739329da5a19aeda55be4e in / 
# Wed, 04 Oct 2023 12:25:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:725335f54d3eb8903e713867d9f04db29fbc8835da3539fd3898faa22eaf016e`  
		Last Modified: Wed, 04 Oct 2023 12:33:24 GMT  
		Size: 24.6 MB (24629439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:aa2be6baa498ab5862770bbc08cf00a058154cb257e41dca6ef8b7f7aebe22f8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4783be26912a96818aa1c9468ea8acb5eff2608697f62deff67048595a613145`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:23:52 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:23:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:23:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:23:52 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:23:53 GMT
ADD file:c9b1098bc90ac9b887c3bffdffbcff0c32f32e48df9a673041e3aa796296e69b in / 
# Wed, 04 Oct 2023 12:23:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:89e6336dd9e04a0993754adca328bf88d988540bb95cff284667037dd50f79eb`  
		Last Modified: Wed, 04 Oct 2023 12:33:17 GMT  
		Size: 26.1 MB (26065969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2d697e1fc26340ae1a77a08397f53f978a6966d3c8a3cf195ee0870ca6e7dc2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6651a10a7ea6479a915882811fa23c286c9baabb6ea68a11e48c3235246b574e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:08:54 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:08:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:08:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:08:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:08:57 GMT
ADD file:24bc2f22a395e93a2ebbcfc45da8e5fc7f08e7c03cdc985c997300643d0310ec in / 
# Wed, 04 Oct 2023 12:08:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fafd77e1a2b2b77f4b648372d147a2d31af161695aa89bed56883733707bd39f`  
		Last Modified: Wed, 04 Oct 2023 12:33:31 GMT  
		Size: 30.9 MB (30905941 bytes)  
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

## `ubuntu:lunar-20231004`

```console
$ docker pull ubuntu@sha256:60035245fd2cfdfecac0fd5eab5cefde5407624a75bebcf803b355174b460311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:lunar-20231004` - linux; amd64

```console
$ docker pull ubuntu@sha256:04714a1bfbb2d8b5390b5cc0c055e48ebfabd4aa395821b860730ff3277ed74a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26877033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639282825872ec6978281e00795f8f02e3b752112dfa01a5f55a19a0f6cf47dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:18:17 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:18:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:18:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:18:18 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:18:19 GMT
ADD file:d4fca0b2b53fa4e2c3e0d721bf983f4095061c5df5fb084d2daf5efad5ee663d in / 
# Wed, 04 Oct 2023 12:18:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f93f952dad401041cbf7200ea1438a832b72273179a2d36e029ccfda15d49507`  
		Last Modified: Wed, 04 Oct 2023 12:33:09 GMT  
		Size: 26.9 MB (26877033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20231004` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4dc1dd258d16171c6cd696ed5420402319d7cabe638b176b471495e94373f2a9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24629439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83502f31cce9655561356390e34e8d506e888f6ce4743a8400bfa765f6eedb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:25:21 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:25:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:25:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:25:24 GMT
ADD file:b92305119eab5dd3dfb00f4d83cd84e00c8ae57143739329da5a19aeda55be4e in / 
# Wed, 04 Oct 2023 12:25:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:725335f54d3eb8903e713867d9f04db29fbc8835da3539fd3898faa22eaf016e`  
		Last Modified: Wed, 04 Oct 2023 12:33:24 GMT  
		Size: 24.6 MB (24629439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20231004` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:aa2be6baa498ab5862770bbc08cf00a058154cb257e41dca6ef8b7f7aebe22f8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4783be26912a96818aa1c9468ea8acb5eff2608697f62deff67048595a613145`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:23:52 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:23:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:23:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:23:52 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:23:53 GMT
ADD file:c9b1098bc90ac9b887c3bffdffbcff0c32f32e48df9a673041e3aa796296e69b in / 
# Wed, 04 Oct 2023 12:23:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:89e6336dd9e04a0993754adca328bf88d988540bb95cff284667037dd50f79eb`  
		Last Modified: Wed, 04 Oct 2023 12:33:17 GMT  
		Size: 26.1 MB (26065969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20231004` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:2d697e1fc26340ae1a77a08397f53f978a6966d3c8a3cf195ee0870ca6e7dc2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6651a10a7ea6479a915882811fa23c286c9baabb6ea68a11e48c3235246b574e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Oct 2023 12:08:54 GMT
ARG RELEASE
# Wed, 04 Oct 2023 12:08:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 12:08:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 12:08:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 04 Oct 2023 12:08:57 GMT
ADD file:24bc2f22a395e93a2ebbcfc45da8e5fc7f08e7c03cdc985c997300643d0310ec in / 
# Wed, 04 Oct 2023 12:08:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fafd77e1a2b2b77f4b648372d147a2d31af161695aa89bed56883733707bd39f`  
		Last Modified: Wed, 04 Oct 2023 12:33:31 GMT  
		Size: 30.9 MB (30905941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:79bcf74b7ee64b05d8ad7f7451e8ef6865531bae01f5dc9e42ae89acf20a78bd
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
$ docker pull ubuntu@sha256:13f233a16be210b57907b98b0d927ceff7571df390701e14fe1f3901b2c4a4d7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27271091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7a3960a97ee41f84c8045700d2e5bd671a42f02a64ee33dde10627dee1a7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:04:48 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:04:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:04:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:04:49 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:04:50 GMT
ADD file:492ae1940ef5a9a4d7af92b9120b5b7c7d3bfd8107ce94d28eab844ace024981 in / 
# Wed, 11 Oct 2023 18:04:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1cf823cf1f0c938d15f343c52a2110dffb08010fe39e69aba493326b5629709`  
		Last Modified: Wed, 11 Oct 2023 18:17:47 GMT  
		Size: 27.3 MB (27271091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7708743264cbb7f6cf7fc13e915faece45a6cdda455748bc55e58e8de3d27b63
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26379954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9cf3a31fbf871322b774402c7c25b800d0e93c222d5a44339f2d3a99dede82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:03:02 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:03:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:03:10 GMT
ADD file:9e750ebbbf7e47a121d153e6699006776ea61b04b6c8e31556600483a020f617 in / 
# Wed, 11 Oct 2023 18:03:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f906b88252effff97383eeb7dd4d265f3f31a54aa3833dd349cf8c4a35fbdbe9`  
		Last Modified: Wed, 11 Oct 2023 18:17:54 GMT  
		Size: 26.4 MB (26379954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:347a278b913b988b85442a3e187001edfe854da3ed499f45782d4a714f08632f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31340704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fb712785eb8f8fe4cdc47a6bb3bd8014c2b376c684dd430b32f81e786cdd5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:06:00 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:06:03 GMT
ADD file:a18be8add7eb60493b13d2aac8d624230297bd15be033756795582dc07cb04bb in / 
# Wed, 11 Oct 2023 18:06:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e4ddce09953092c8c6052d38bc7c2044237f1337f42f1f86edab6718af804ea`  
		Last Modified: Wed, 11 Oct 2023 18:18:11 GMT  
		Size: 31.3 MB (31340704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:a353c527eb5233fdfc2ad112c7897cce7da6ac28b24d3aaa8f441f27ddf613c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27072390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eca28f81d0bd51084742dc133e32c215a83739fc5603306f1ad774311dc6ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 26 Sep 2023 04:58:19 GMT
ARG RELEASE
# Tue, 26 Sep 2023 04:58:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Sep 2023 04:58:19 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 26 Sep 2023 04:58:21 GMT
ADD file:e86e9b7546a97fa45e9c726cc317a624a7f94b0bd6dd413d89946ff778b18c77 in / 
# Tue, 26 Sep 2023 04:58:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56312385d597227d0c1232049609586ed3412b04e6ec96c5f6626f5f50f438fe`  
		Last Modified: Tue, 26 Sep 2023 05:34:22 GMT  
		Size: 27.1 MB (27072390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20231011`

```console
$ docker pull ubuntu@sha256:132ce742d38acf2372bfef3c1ae7b1f020d0da61406c5216e3389ad7f9bb995b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:mantic-20231011` - linux; amd64

```console
$ docker pull ubuntu@sha256:13f233a16be210b57907b98b0d927ceff7571df390701e14fe1f3901b2c4a4d7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27271091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7a3960a97ee41f84c8045700d2e5bd671a42f02a64ee33dde10627dee1a7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:04:48 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:04:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:04:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:04:49 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:04:50 GMT
ADD file:492ae1940ef5a9a4d7af92b9120b5b7c7d3bfd8107ce94d28eab844ace024981 in / 
# Wed, 11 Oct 2023 18:04:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1cf823cf1f0c938d15f343c52a2110dffb08010fe39e69aba493326b5629709`  
		Last Modified: Wed, 11 Oct 2023 18:17:47 GMT  
		Size: 27.3 MB (27271091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20231011` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20231011` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7708743264cbb7f6cf7fc13e915faece45a6cdda455748bc55e58e8de3d27b63
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26379954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9cf3a31fbf871322b774402c7c25b800d0e93c222d5a44339f2d3a99dede82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:03:02 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:03:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:03:10 GMT
ADD file:9e750ebbbf7e47a121d153e6699006776ea61b04b6c8e31556600483a020f617 in / 
# Wed, 11 Oct 2023 18:03:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f906b88252effff97383eeb7dd4d265f3f31a54aa3833dd349cf8c4a35fbdbe9`  
		Last Modified: Wed, 11 Oct 2023 18:17:54 GMT  
		Size: 26.4 MB (26379954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20231011` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:347a278b913b988b85442a3e187001edfe854da3ed499f45782d4a714f08632f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31340704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fb712785eb8f8fe4cdc47a6bb3bd8014c2b376c684dd430b32f81e786cdd5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:06:00 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:06:03 GMT
ADD file:a18be8add7eb60493b13d2aac8d624230297bd15be033756795582dc07cb04bb in / 
# Wed, 11 Oct 2023 18:06:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e4ddce09953092c8c6052d38bc7c2044237f1337f42f1f86edab6718af804ea`  
		Last Modified: Wed, 11 Oct 2023 18:18:11 GMT  
		Size: 31.3 MB (31340704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:064f544c977450f09da254e3512b9d28f0399a11ab6006cffef9d141b87856f6
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
$ docker pull ubuntu@sha256:13f233a16be210b57907b98b0d927ceff7571df390701e14fe1f3901b2c4a4d7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27271091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7a3960a97ee41f84c8045700d2e5bd671a42f02a64ee33dde10627dee1a7d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:04:48 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:04:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:04:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:04:49 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:04:50 GMT
ADD file:492ae1940ef5a9a4d7af92b9120b5b7c7d3bfd8107ce94d28eab844ace024981 in / 
# Wed, 11 Oct 2023 18:04:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1cf823cf1f0c938d15f343c52a2110dffb08010fe39e69aba493326b5629709`  
		Last Modified: Wed, 11 Oct 2023 18:17:47 GMT  
		Size: 27.3 MB (27271091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:2a465a4c4831c57977b6646e481f504061294f1bf1ae1b99fb5d93c67b8a471a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25201383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc753c284b47a7a5ff3ec2e926551ba95dc6c9072415649cb13a9cdff503dc04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:02:33 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:02:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:02:34 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:02:39 GMT
ADD file:1be1311acbd557f7769fb5c1913ef56305431e7547f96c20ac36284fdd926223 in / 
# Wed, 11 Oct 2023 18:02:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8761b0d436cd2e1ff47496b7cc353cf0b49347ffc92b070c31a5cf5431041614`  
		Last Modified: Wed, 11 Oct 2023 18:18:00 GMT  
		Size: 25.2 MB (25201383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:7708743264cbb7f6cf7fc13e915faece45a6cdda455748bc55e58e8de3d27b63
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26379954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9cf3a31fbf871322b774402c7c25b800d0e93c222d5a44339f2d3a99dede82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:03:02 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:03:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:03:02 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:03:10 GMT
ADD file:9e750ebbbf7e47a121d153e6699006776ea61b04b6c8e31556600483a020f617 in / 
# Wed, 11 Oct 2023 18:03:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f906b88252effff97383eeb7dd4d265f3f31a54aa3833dd349cf8c4a35fbdbe9`  
		Last Modified: Wed, 11 Oct 2023 18:17:54 GMT  
		Size: 26.4 MB (26379954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:347a278b913b988b85442a3e187001edfe854da3ed499f45782d4a714f08632f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31340704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fb712785eb8f8fe4cdc47a6bb3bd8014c2b376c684dd430b32f81e786cdd5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:06:00 GMT
ARG RELEASE
# Wed, 11 Oct 2023 18:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Oct 2023 18:06:00 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 11 Oct 2023 18:06:03 GMT
ADD file:a18be8add7eb60493b13d2aac8d624230297bd15be033756795582dc07cb04bb in / 
# Wed, 11 Oct 2023 18:06:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6e4ddce09953092c8c6052d38bc7c2044237f1337f42f1f86edab6718af804ea`  
		Last Modified: Wed, 11 Oct 2023 18:18:11 GMT  
		Size: 31.3 MB (31340704 bytes)  
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
