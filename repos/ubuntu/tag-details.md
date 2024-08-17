<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:24.10`](#ubuntu2410)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240530`](#ubuntufocal-20240530)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240808`](#ubuntujammy-20240808)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240801`](#ubuntunoble-20240801)
-	[`ubuntu:oracular`](#ubuntuoracular)
-	[`ubuntu:oracular-20240811.1`](#ubuntuoracular-202408111)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:6b74c1a5996659717ade273c4dae317b58790479b46ce8c7d4e635e7262e8cac
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
$ docker pull ubuntu@sha256:d86db849e59626d94f768c679aba441163c996caf7a3426f44924d0239ffe03f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5250218d28ad6612bf653eced407165dd6475a4daf9210b299fed991e172e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:717a8dabf82777782587740c79fd8704d3ec06583be6eacc67242cd00b9a0fd1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b0680c06e6c394ed258bc7929b97e1bdf910e0b7f128b98d5e332363e570e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6edb9576e2a2080a42e4e0e9a6bc0bd91a2bf06375f9832d400bf33841d35ece
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583f1722e16e377baf906fee1ec6a9fda85ff7f3d13f536f912998601fd85ed8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b1d0786a9e95b462ff37e855dd76b6e0f31be52efd33e8c12b53e14c4291816d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfa8b239ff8a37b60ae553fa44a77dd68c130936e5dd66a23f91f96ec61cae0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:c0e96f609e5f128bdb6d24d21d3bf0a9af6f17234976fa574dad7146a0f97fb2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24245212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2ff3eb6191a7eeebc6ff2a4f23d0124d7ec1544dfbd3cd89f2eaf05d9b32f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:10:28 GMT
ADD file:50c1d21a50d57d99470bd427f2ee427504ad0602a5046dbc6a04680574d27f39 in / 
# Fri, 09 Dec 2022 01:10:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1bf57572b326faac5012873a6b3ea48eee0fe2649c47d425e34e149459c96c29`  
		Last Modified: Fri, 09 Dec 2022 01:32:24 GMT  
		Size: 24.2 MB (24245212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:bec8a96229e24d6a9b3c333071b645c7aa7d864596ac609fbbbc89d990312394
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9374e168016e3656c0194d188dfb164fb07c23e9386799c0aec38196d359c357`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:94618b2ce8a064c6e3b88ef11e7030a6ad6f3e2bcb62b5afba2f63feb01a8f32
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
$ docker pull ubuntu@sha256:0eb0f877e1c869a300c442c41120e778db7161419244ee5cbc6fa5f134e74736
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3cdc4d1ad3e314a91f76b7b99eed443f2152e3a9bf33e46669b31d094be443`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e215e52905ebb967da009a009b681f219e456122d4382a370b0c7d56c21c7bb8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0de33827595e70e002da57b43f06ee3bbef7f7418dd4edcd8e402aba2011dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f6d2cceb710e897ef3b81e28ea21268aa6d28deae90ac1ab9602ff738c88a650`  
		Last Modified: Thu, 27 Jun 2024 20:18:40 GMT  
		Size: 26.6 MB (26638444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d19c776e76cdb32dcc72cbd44a689c9be9518b9c4ed7f9a92b38f46176b931b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27360025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04dcc2ab57b0d5d6e9d3d9c65f899d400d14114dace7a30acc84f36bb609cdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:58148fb210e3d70c972b5e72bdfcd68be667dec91e8a2ed6376b9e9c980cd573
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34464178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ca497369fa4f71884a0e797df02b607d17d11d79197872cba3edadc77b8a1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f31546bc71659c643837d57f09a161f04e866b59da4f418e064082a756c4c23a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27749556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55084b9c02c8c6d013ed4b10f3e0c9306a50be9526ee8bf5870c8175554a72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:12:29 GMT
ADD file:f46f460af5409f8fff839ed52d7332dff314cffbb59ee3f40e898ecb6bfa21f9 in / 
# Fri, 09 Dec 2022 01:12:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7548465e3aa5fee0518ca5aefe07a54411b419ec670a320e18c9b8892b0afc0f`  
		Last Modified: Fri, 09 Dec 2022 01:34:47 GMT  
		Size: 27.7 MB (27749556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:01c176682053467414f35141cdc9da3c40a340eba1f0d3a928e4e52d021fa5f9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611e60cc7007d67350be72fec6adb06b36ffa3f04bac4400b7ca37107acf9cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:c2072afab1848810176ac88daea6d9c714af8de454d8a574dafc6c41f355eb39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:24.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:fc72c25cdd14ec36b46f27172dc7fd590d6a2d9759f587c6df579168de86dfcc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34507572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fd182940b2c665f969ccc688c43fdee74537cd7d8146daa6890bb9461c4848`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.10`

```console
$ docker pull ubuntu@sha256:ec705e3704caa11dbe38b62469eee39fc7d2af812bb2ea2ba931790d8d972fed
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
$ docker pull ubuntu@sha256:2a1e42397521001f21178a06e37ba1024481d3e8b6a754902ac5fb6a0861c7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29784075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94351b6d67ec74ba3dbc8816e783fd62253ef818a920616c0e6142348af486c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:32 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:34 GMT
ADD file:7de44056586ca78e2d663ff6f13ed78bd93df3759032c25b398020b7f7a508e9 in / 
# Tue, 18 Jun 2024 11:55:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:044e986ad11c8558c1ced47a645123223d7169e0603217f6b5810ae6d5ed8990`  
		Last Modified: Tue, 18 Jun 2024 12:05:48 GMT  
		Size: 29.8 MB (29784075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:454de8793a5d34b0dee0dbd13719a2c6eeadd7944bacdcace19263cbe9b3a94e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c89d5967405dc83e44998f274cee92367c1a5535fedf5b28786b266541ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:40 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:46 GMT
ADD file:c13178f5cbf3534e02829f373860ffe37af2e84d45812bd7eabc39b4e79bf01a in / 
# Tue, 18 Jun 2024 11:55:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26cb78abf3e6e59cb1ecc37a2ce7bfa44b6eea15ae8bd75ae12a67b744fb8a14`  
		Last Modified: Tue, 18 Jun 2024 12:06:00 GMT  
		Size: 26.9 MB (26906015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0f58dd64e1e2b1f2c96e2b2cab30402540724a399061b035051534808114144a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28910084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a556a9a5dea3e4f745912c1182f1a25e8814ed8f855b4221bd99bb15e0d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:34 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:40 GMT
ADD file:34ce123f3395299e473794d0c46e368375bf7c9630a67258382f114f83a82c40 in / 
# Tue, 18 Jun 2024 11:55:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8fecd43832f92adee10b7b226a92bb3186239d955e0f1d97d8239791a46784fe`  
		Last Modified: Tue, 18 Jun 2024 12:05:54 GMT  
		Size: 28.9 MB (28910084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5968260bcb13d88a91955cb0f3b3717e81cf63d3f5564fd0d485956a7f06d37e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34985755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58bda9aa9d22428684e273a82adb85de1f555adb4bd580bbffcac6e78bc3c0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd625c7f091deeffe9e3c544a32cb5fbee7a7134b96c2fb01a588adb4acdc03d`  
		Last Modified: Sun, 11 Aug 2024 16:47:13 GMT  
		Size: 35.0 MB (34985755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; riscv64

```console
$ docker pull ubuntu@sha256:5d9a58fb2a15e7b1a7d42e7fc95aa405be562aefd06d677af4edbf11c7c10a3e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30977999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04623951616be2049aa17400c6a153be8a070113b976dc9c156c824ceeda23af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 10:56:58 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:56:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:56:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:56:59 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 10:57:28 GMT
ADD file:92289105b8f29d547ee9730040ad9dddd1ca3b8da52ac32705bba4ed479b0ac3 in / 
# Tue, 18 Jun 2024 10:57:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49d2944d02efd91d628db839a7dfe895a3e7a39ab1e09740a05b84ef1cc98acd`  
		Last Modified: Tue, 18 Jun 2024 12:06:13 GMT  
		Size: 31.0 MB (30977999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:579f926bf5b5737bb4a6e7a96a26b972ff53efd0e897ca6ad60a5177f646fc23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acda71050f1c0d987f22287e80bf0f8d8053b3603156d7110c4c8ac85ce1d13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:36 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:39 GMT
ADD file:4bdbaa8c03466d03a76656bbdf683d02b08207350051e5d5d8d46f60ae2ebffd in / 
# Tue, 18 Jun 2024 11:55:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92821b1303c5ddcb3e722c91af39dfee67d938dade7d06501348340be1bafc4b`  
		Last Modified: Tue, 18 Jun 2024 12:06:20 GMT  
		Size: 30.0 MB (30020524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:ec705e3704caa11dbe38b62469eee39fc7d2af812bb2ea2ba931790d8d972fed
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
$ docker pull ubuntu@sha256:2a1e42397521001f21178a06e37ba1024481d3e8b6a754902ac5fb6a0861c7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29784075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94351b6d67ec74ba3dbc8816e783fd62253ef818a920616c0e6142348af486c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:32 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:34 GMT
ADD file:7de44056586ca78e2d663ff6f13ed78bd93df3759032c25b398020b7f7a508e9 in / 
# Tue, 18 Jun 2024 11:55:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:044e986ad11c8558c1ced47a645123223d7169e0603217f6b5810ae6d5ed8990`  
		Last Modified: Tue, 18 Jun 2024 12:05:48 GMT  
		Size: 29.8 MB (29784075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:454de8793a5d34b0dee0dbd13719a2c6eeadd7944bacdcace19263cbe9b3a94e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c89d5967405dc83e44998f274cee92367c1a5535fedf5b28786b266541ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:40 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:46 GMT
ADD file:c13178f5cbf3534e02829f373860ffe37af2e84d45812bd7eabc39b4e79bf01a in / 
# Tue, 18 Jun 2024 11:55:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26cb78abf3e6e59cb1ecc37a2ce7bfa44b6eea15ae8bd75ae12a67b744fb8a14`  
		Last Modified: Tue, 18 Jun 2024 12:06:00 GMT  
		Size: 26.9 MB (26906015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0f58dd64e1e2b1f2c96e2b2cab30402540724a399061b035051534808114144a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28910084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a556a9a5dea3e4f745912c1182f1a25e8814ed8f855b4221bd99bb15e0d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:34 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:40 GMT
ADD file:34ce123f3395299e473794d0c46e368375bf7c9630a67258382f114f83a82c40 in / 
# Tue, 18 Jun 2024 11:55:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8fecd43832f92adee10b7b226a92bb3186239d955e0f1d97d8239791a46784fe`  
		Last Modified: Tue, 18 Jun 2024 12:05:54 GMT  
		Size: 28.9 MB (28910084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5968260bcb13d88a91955cb0f3b3717e81cf63d3f5564fd0d485956a7f06d37e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34985755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58bda9aa9d22428684e273a82adb85de1f555adb4bd580bbffcac6e78bc3c0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd625c7f091deeffe9e3c544a32cb5fbee7a7134b96c2fb01a588adb4acdc03d`  
		Last Modified: Sun, 11 Aug 2024 16:47:13 GMT  
		Size: 35.0 MB (34985755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; riscv64

```console
$ docker pull ubuntu@sha256:5d9a58fb2a15e7b1a7d42e7fc95aa405be562aefd06d677af4edbf11c7c10a3e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30977999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04623951616be2049aa17400c6a153be8a070113b976dc9c156c824ceeda23af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 10:56:58 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:56:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:56:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:56:59 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 10:57:28 GMT
ADD file:92289105b8f29d547ee9730040ad9dddd1ca3b8da52ac32705bba4ed479b0ac3 in / 
# Tue, 18 Jun 2024 10:57:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49d2944d02efd91d628db839a7dfe895a3e7a39ab1e09740a05b84ef1cc98acd`  
		Last Modified: Tue, 18 Jun 2024 12:06:13 GMT  
		Size: 31.0 MB (30977999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:579f926bf5b5737bb4a6e7a96a26b972ff53efd0e897ca6ad60a5177f646fc23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acda71050f1c0d987f22287e80bf0f8d8053b3603156d7110c4c8ac85ce1d13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:36 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:39 GMT
ADD file:4bdbaa8c03466d03a76656bbdf683d02b08207350051e5d5d8d46f60ae2ebffd in / 
# Tue, 18 Jun 2024 11:55:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92821b1303c5ddcb3e722c91af39dfee67d938dade7d06501348340be1bafc4b`  
		Last Modified: Tue, 18 Jun 2024 12:06:20 GMT  
		Size: 30.0 MB (30020524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:6b74c1a5996659717ade273c4dae317b58790479b46ce8c7d4e635e7262e8cac
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
$ docker pull ubuntu@sha256:d86db849e59626d94f768c679aba441163c996caf7a3426f44924d0239ffe03f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5250218d28ad6612bf653eced407165dd6475a4daf9210b299fed991e172e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:717a8dabf82777782587740c79fd8704d3ec06583be6eacc67242cd00b9a0fd1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b0680c06e6c394ed258bc7929b97e1bdf910e0b7f128b98d5e332363e570e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6edb9576e2a2080a42e4e0e9a6bc0bd91a2bf06375f9832d400bf33841d35ece
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583f1722e16e377baf906fee1ec6a9fda85ff7f3d13f536f912998601fd85ed8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b1d0786a9e95b462ff37e855dd76b6e0f31be52efd33e8c12b53e14c4291816d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfa8b239ff8a37b60ae553fa44a77dd68c130936e5dd66a23f91f96ec61cae0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; riscv64

```console
$ docker pull ubuntu@sha256:c0e96f609e5f128bdb6d24d21d3bf0a9af6f17234976fa574dad7146a0f97fb2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24245212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2ff3eb6191a7eeebc6ff2a4f23d0124d7ec1544dfbd3cd89f2eaf05d9b32f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:10:28 GMT
ADD file:50c1d21a50d57d99470bd427f2ee427504ad0602a5046dbc6a04680574d27f39 in / 
# Fri, 09 Dec 2022 01:10:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1bf57572b326faac5012873a6b3ea48eee0fe2649c47d425e34e149459c96c29`  
		Last Modified: Fri, 09 Dec 2022 01:32:24 GMT  
		Size: 24.2 MB (24245212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:bec8a96229e24d6a9b3c333071b645c7aa7d864596ac609fbbbc89d990312394
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9374e168016e3656c0194d188dfb164fb07c23e9386799c0aec38196d359c357`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240530`

```console
$ docker pull ubuntu@sha256:aa2ab9d4e8c496925a70b6d08b11d6305bcfdb5a0af068d8c29150460c71d502
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20240530` - linux; amd64

```console
$ docker pull ubuntu@sha256:d86db849e59626d94f768c679aba441163c996caf7a3426f44924d0239ffe03f
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5250218d28ad6612bf653eced407165dd6475a4daf9210b299fed991e172e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240530` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:717a8dabf82777782587740c79fd8704d3ec06583be6eacc67242cd00b9a0fd1
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b0680c06e6c394ed258bc7929b97e1bdf910e0b7f128b98d5e332363e570e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7fbbd3a0a9f6bdbc27b1387d026c5e6212aea61a60bdc85455992d7d72d65a50`  
		Last Modified: Mon, 03 Jun 2024 17:19:55 GMT  
		Size: 23.6 MB (23623382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240530` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:6edb9576e2a2080a42e4e0e9a6bc0bd91a2bf06375f9832d400bf33841d35ece
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583f1722e16e377baf906fee1ec6a9fda85ff7f3d13f536f912998601fd85ed8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240530` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b1d0786a9e95b462ff37e855dd76b6e0f31be52efd33e8c12b53e14c4291816d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32077140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfa8b239ff8a37b60ae553fa44a77dd68c130936e5dd66a23f91f96ec61cae0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240530` - linux; s390x

```console
$ docker pull ubuntu@sha256:bec8a96229e24d6a9b3c333071b645c7aa7d864596ac609fbbbc89d990312394
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26367194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9374e168016e3656c0194d188dfb164fb07c23e9386799c0aec38196d359c357`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 17:11:27 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:11:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:11:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:11:29 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Mon, 03 Jun 2024 17:11:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f1664199ed409e4e98c964539b5e8b7c7b2e71d591963ef8cebbd5b1f0fec40c`  
		Last Modified: Mon, 03 Jun 2024 17:20:08 GMT  
		Size: 26.4 MB (26367194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:94618b2ce8a064c6e3b88ef11e7030a6ad6f3e2bcb62b5afba2f63feb01a8f32
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
$ docker pull ubuntu@sha256:0eb0f877e1c869a300c442c41120e778db7161419244ee5cbc6fa5f134e74736
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3cdc4d1ad3e314a91f76b7b99eed443f2152e3a9bf33e46669b31d094be443`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:e215e52905ebb967da009a009b681f219e456122d4382a370b0c7d56c21c7bb8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0de33827595e70e002da57b43f06ee3bbef7f7418dd4edcd8e402aba2011dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:33:13 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:33:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:33:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:33:16 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 19:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f6d2cceb710e897ef3b81e28ea21268aa6d28deae90ac1ab9602ff738c88a650`  
		Last Modified: Thu, 27 Jun 2024 20:18:40 GMT  
		Size: 26.6 MB (26638444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1d19c776e76cdb32dcc72cbd44a689c9be9518b9c4ed7f9a92b38f46176b931b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27360025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04dcc2ab57b0d5d6e9d3d9c65f899d400d14114dace7a30acc84f36bb609cdd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:58148fb210e3d70c972b5e72bdfcd68be667dec91e8a2ed6376b9e9c980cd573
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34464178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ca497369fa4f71884a0e797df02b607d17d11d79197872cba3edadc77b8a1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f31546bc71659c643837d57f09a161f04e866b59da4f418e064082a756c4c23a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27749556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55084b9c02c8c6d013ed4b10f3e0c9306a50be9526ee8bf5870c8175554a72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:12:29 GMT
ADD file:f46f460af5409f8fff839ed52d7332dff314cffbb59ee3f40e898ecb6bfa21f9 in / 
# Fri, 09 Dec 2022 01:12:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7548465e3aa5fee0518ca5aefe07a54411b419ec670a320e18c9b8892b0afc0f`  
		Last Modified: Fri, 09 Dec 2022 01:34:47 GMT  
		Size: 27.7 MB (27749556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:01c176682053467414f35141cdc9da3c40a340eba1f0d3a928e4e52d021fa5f9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611e60cc7007d67350be72fec6adb06b36ffa3f04bac4400b7ca37107acf9cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240808`

```console
$ docker pull ubuntu@sha256:1fd9d804f59db5db201ce17ad1561fb36c4d0738392d97d8fbcacf7bbc9f9d3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; ppc64le

### `ubuntu:jammy-20240808` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:58148fb210e3d70c972b5e72bdfcd68be667dec91e8a2ed6376b9e9c980cd573
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34464178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ca497369fa4f71884a0e797df02b607d17d11d79197872cba3edadc77b8a1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:90bfd34c04da0652bc2137f8c72cf0be8374db294cc140975053c6af62c7f982
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
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:fc72c25cdd14ec36b46f27172dc7fd590d6a2d9759f587c6df579168de86dfcc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34507572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fd182940b2c665f969ccc688c43fdee74537cd7d8146daa6890bb9461c4848`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; riscv64

```console
$ docker pull ubuntu@sha256:f31546bc71659c643837d57f09a161f04e866b59da4f418e064082a756c4c23a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27749556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55084b9c02c8c6d013ed4b10f3e0c9306a50be9526ee8bf5870c8175554a72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:12:29 GMT
ADD file:f46f460af5409f8fff839ed52d7332dff314cffbb59ee3f40e898ecb6bfa21f9 in / 
# Fri, 09 Dec 2022 01:12:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7548465e3aa5fee0518ca5aefe07a54411b419ec670a320e18c9b8892b0afc0f`  
		Last Modified: Fri, 09 Dec 2022 01:34:47 GMT  
		Size: 27.7 MB (27749556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:c2072afab1848810176ac88daea6d9c714af8de454d8a574dafc6c41f355eb39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble` - linux; amd64

```console
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:fc72c25cdd14ec36b46f27172dc7fd590d6a2d9759f587c6df579168de86dfcc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34507572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fd182940b2c665f969ccc688c43fdee74537cd7d8146daa6890bb9461c4848`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240801`

```console
$ docker pull ubuntu@sha256:0e76c1f0a076ce85e9a1f875980aaee8eae763204eab22f3ece87147f16339b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; ppc64le

### `ubuntu:noble-20240801` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:fc72c25cdd14ec36b46f27172dc7fd590d6a2d9759f587c6df579168de86dfcc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34507572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fd182940b2c665f969ccc688c43fdee74537cd7d8146daa6890bb9461c4848`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular`

```console
$ docker pull ubuntu@sha256:ec705e3704caa11dbe38b62469eee39fc7d2af812bb2ea2ba931790d8d972fed
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
$ docker pull ubuntu@sha256:2a1e42397521001f21178a06e37ba1024481d3e8b6a754902ac5fb6a0861c7ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29784075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94351b6d67ec74ba3dbc8816e783fd62253ef818a920616c0e6142348af486c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:32 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:32 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:34 GMT
ADD file:7de44056586ca78e2d663ff6f13ed78bd93df3759032c25b398020b7f7a508e9 in / 
# Tue, 18 Jun 2024 11:55:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:044e986ad11c8558c1ced47a645123223d7169e0603217f6b5810ae6d5ed8990`  
		Last Modified: Tue, 18 Jun 2024 12:05:48 GMT  
		Size: 29.8 MB (29784075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:454de8793a5d34b0dee0dbd13719a2c6eeadd7944bacdcace19263cbe9b3a94e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26906015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c89d5967405dc83e44998f274cee92367c1a5535fedf5b28786b266541ed4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:40 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:41 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:46 GMT
ADD file:c13178f5cbf3534e02829f373860ffe37af2e84d45812bd7eabc39b4e79bf01a in / 
# Tue, 18 Jun 2024 11:55:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:26cb78abf3e6e59cb1ecc37a2ce7bfa44b6eea15ae8bd75ae12a67b744fb8a14`  
		Last Modified: Tue, 18 Jun 2024 12:06:00 GMT  
		Size: 26.9 MB (26906015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0f58dd64e1e2b1f2c96e2b2cab30402540724a399061b035051534808114144a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28910084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a556a9a5dea3e4f745912c1182f1a25e8814ed8f855b4221bd99bb15e0d61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:34 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:34 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:40 GMT
ADD file:34ce123f3395299e473794d0c46e368375bf7c9630a67258382f114f83a82c40 in / 
# Tue, 18 Jun 2024 11:55:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8fecd43832f92adee10b7b226a92bb3186239d955e0f1d97d8239791a46784fe`  
		Last Modified: Tue, 18 Jun 2024 12:05:54 GMT  
		Size: 28.9 MB (28910084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5968260bcb13d88a91955cb0f3b3717e81cf63d3f5564fd0d485956a7f06d37e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34985755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58bda9aa9d22428684e273a82adb85de1f555adb4bd580bbffcac6e78bc3c0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd625c7f091deeffe9e3c544a32cb5fbee7a7134b96c2fb01a588adb4acdc03d`  
		Last Modified: Sun, 11 Aug 2024 16:47:13 GMT  
		Size: 35.0 MB (34985755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; riscv64

```console
$ docker pull ubuntu@sha256:5d9a58fb2a15e7b1a7d42e7fc95aa405be562aefd06d677af4edbf11c7c10a3e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30977999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04623951616be2049aa17400c6a153be8a070113b976dc9c156c824ceeda23af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 10:56:58 GMT
ARG RELEASE
# Tue, 18 Jun 2024 10:56:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 10:56:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 10:56:59 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 10:57:28 GMT
ADD file:92289105b8f29d547ee9730040ad9dddd1ca3b8da52ac32705bba4ed479b0ac3 in / 
# Tue, 18 Jun 2024 10:57:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49d2944d02efd91d628db839a7dfe895a3e7a39ab1e09740a05b84ef1cc98acd`  
		Last Modified: Tue, 18 Jun 2024 12:06:13 GMT  
		Size: 31.0 MB (30977999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:oracular` - linux; s390x

```console
$ docker pull ubuntu@sha256:579f926bf5b5737bb4a6e7a96a26b972ff53efd0e897ca6ad60a5177f646fc23
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30020524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acda71050f1c0d987f22287e80bf0f8d8053b3603156d7110c4c8ac85ce1d13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 18 Jun 2024 11:55:36 GMT
ARG RELEASE
# Tue, 18 Jun 2024 11:55:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 11:55:36 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 18 Jun 2024 11:55:39 GMT
ADD file:4bdbaa8c03466d03a76656bbdf683d02b08207350051e5d5d8d46f60ae2ebffd in / 
# Tue, 18 Jun 2024 11:55:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:92821b1303c5ddcb3e722c91af39dfee67d938dade7d06501348340be1bafc4b`  
		Last Modified: Tue, 18 Jun 2024 12:06:20 GMT  
		Size: 30.0 MB (30020524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:oracular-20240811.1`

```console
$ docker pull ubuntu@sha256:0c57aa7d6de53179fee49dd525c99f55452cb73a269cf902a2a94b13b5f4ea27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 1
	-	linux; ppc64le

### `ubuntu:oracular-20240811.1` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:5968260bcb13d88a91955cb0f3b3717e81cf63d3f5564fd0d485956a7f06d37e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (34985755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58bda9aa9d22428684e273a82adb85de1f555adb4bd580bbffcac6e78bc3c0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 11 Aug 2024 15:39:31 GMT
ARG RELEASE
# Sun, 11 Aug 2024 15:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 11 Aug 2024 15:39:31 GMT
LABEL org.opencontainers.image.version=24.10
# Sun, 11 Aug 2024 15:39:34 GMT
ADD file:c995bac66bc8ed18a9e5e7591143905810e18f366ac82dd51470210c97712108 in / 
# Sun, 11 Aug 2024 15:39:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bd625c7f091deeffe9e3c544a32cb5fbee7a7134b96c2fb01a588adb4acdc03d`  
		Last Modified: Sun, 11 Aug 2024 16:47:13 GMT  
		Size: 35.0 MB (34985755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:7981ed1a44acbdd6f3653ed5644e1ef3ba4f635789db5fee6b2c03312a2ac451
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
$ docker pull ubuntu@sha256:c920ba4cfca05503764b785c16b76d43c83a6df8d1ab107e7e6610000d94315c
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29705153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a88802559dd2077e584394471ddaa1a2c5bfd16893b829ea57619301eb3908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8550f6af59aad999f559457c57eaea97078b9b17ac98f794e2f5dde953857798
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26820356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4061e67449f319a37fa3f57e590401f1ea99a5494ed5ea494bdbce2f481a0681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aa9f84d6e529483956a3454f02193e9a0f758a08b5191f2199c928065d307720`  
		Last Modified: Fri, 07 Jun 2024 12:11:39 GMT  
		Size: 26.8 MB (26820356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:010f94447a26deb0dcdbbeb08d7dfcd87b64c40b4f25d0cf4d582949b735039d
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 MB (28843043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb64c9b7e8b9f1891f7a72609d4e691c4671dc4aa83084fc7b5774958d827de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:fc72c25cdd14ec36b46f27172dc7fd590d6a2d9759f587c6df579168de86dfcc
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34507572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fd182940b2c665f969ccc688c43fdee74537cd7d8146daa6890bb9461c4848`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; riscv64

```console
$ docker pull ubuntu@sha256:d708589f4214d8612f0fdf9ba3e8488e16f9a665f7fd9e0ba24edcdfc326f0f7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 MB (25640259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4819792eac8ee5fc12e4dd0eb179280d6e3dcae69b77905d52a750f15b2cd6e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:14:46 GMT
ADD file:7e2bfb25c400fe48fedbb3adb245a3bc6b40ec07dae2feeb339c704b967ce658 in / 
# Fri, 09 Dec 2022 01:14:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:080423a9398e3d16c0feb2851e7596ddc2d8d33fdfb3bf0b4a881619b9b86c9f`  
		Last Modified: Fri, 09 Dec 2022 01:37:40 GMT  
		Size: 25.6 MB (25640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:3963c438d67a34318a3672faa6debd1dfff48e5d52de54305988b932c61514ca
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30045689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32e15d262a4ff29bf2db8a69e8d2be0c7cd93e2277dec366be684c4a777c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
