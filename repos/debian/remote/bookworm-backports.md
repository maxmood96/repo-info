## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:bc3199cae73a84628d527e940b113690e8a254e48c77a1f004e6bf3073b77136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:3d939224597b4c47eb6cff65b903a62aca9c785c707e613d1524e7edafba8065
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ceae9aa460dac446caf0f75fa70b14d39877db7dba4f2229287784f315c983`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:29:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1a18641a4b26fbe5aa7dc972bb5ff4066757d95777e5b88b4fe78e10cf0ecc`  
		Last Modified: Fri, 27 Sep 2024 04:33:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:bb8e3ee7ce8175ec1d2b56e1785c70f2df7970de126c79962129f9f117af0941
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d826ad06cd83f8893c2d2c7d4d5c47f76d1301c602bb72255d16d672228f41d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:19:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fa60900c3d22ae1a350b5928f87aa91b8221bd8d4869e01a9243d33238b98a`  
		Last Modified: Fri, 27 Sep 2024 03:21:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:db8d75c02c09de8ee477d6d681133b397852a26ce64e52e01597d66f1127885f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9508c8d895190f31db686a2086ff018e6a2b99accbcb6469b62799f577cc6f1f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:13:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314341ba16cceaf03e054c1313be372f299edb91133608e4604968a606a9d348`  
		Last Modified: Fri, 27 Sep 2024 05:17:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6d2711a1af93028b88d912b30d39fd2a84c6f1bcc7242d48897c0ef9e5ba80ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49585109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d5f55823ea9c16e25ebea9f8050b6f73de74add89d46633fe92bd43a74be71`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:38:12 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f6bb2b2f3cf599ef84191b6a8fc2165839f7ce263313c38b42a3584d2e0597`  
		Last Modified: Fri, 27 Sep 2024 04:40:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:2367c085d0779b03b9781297aa74acb431374cba30a332ed8d47c577da073d59
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50576864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0479de11dfca729018c84a9115bbd0599114332d438ef4abe1458b4e61005ff`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:22:52 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146407935c94e6419601a39c0dd626bd7040dd439546a5e3352e61d574f7a9ed`  
		Last Modified: Fri, 27 Sep 2024 07:26:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e796470cae3b188ada600d919088bc9be7dcbd128d53fb6309b9a5f5a2aa58f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a77b73ec7beff45aa1c2fbb71fdc7dfa3b1fd21e660cdb03cd8dd8c5ed1ab8d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 09:02:42 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d478a32b2e5955959f103b1e58909ef6f46ceb86fab81d837015aa09e0cf9d`  
		Last Modified: Fri, 27 Sep 2024 09:11:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8cee285b34d79ce9e803bcb45d938de9599a263d84fdc1196310414d7a0fefdf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dc968f44a8a6060d905aa7419a41954652dbdad4ee11c63646d4cb77606622`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:32:59 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee4502b5c35a59e453e359f9ecac4c6919790e3ce47194a7cec285056a61f61`  
		Last Modified: Fri, 27 Sep 2024 05:36:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:79db3460bf9bf1f01b87b4ea6ae3cb091fdcb913ce9865b95944b99ba492a34d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47938895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e2ba7e77f5081a432fcd8f4cf13bc4eaa505bd26096b81e69611cd31d9bdd1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:43:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ad6788b50baf006cecb6bc0fc96aeef7c6f670c3773e53551257fde36785ac`  
		Last Modified: Fri, 27 Sep 2024 02:47:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
