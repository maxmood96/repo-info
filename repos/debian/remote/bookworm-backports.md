## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:55ff8e6eab4423bc596bf74994b43ac76af0eb72f81a0532b0984f2451311a4c
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
$ docker pull debian@sha256:b3b77b2cbf5b64d02f92d9ceb7e9e846d033d3f91dd3d942177212688e7467ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2629de5247de053ddd7e512cff7c8d5714c7ae77ae151435fcb7d81491b680d9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:17 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 17 Oct 2024 00:20:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:20:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cbd7ed1971391b93f5289b75626f89d81cbf61f97f87a62e924f693d9d5fa4`  
		Last Modified: Thu, 17 Oct 2024 00:23:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:005eb6def7a0877b6769797ea3f1949f561bfaddf21e43cf1a221567597f84a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936a0e17c3cdcbf02c9b987c3b4772547b8b66347b791e4f3609bd032f628d84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:12 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Thu, 17 Oct 2024 00:54:13 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:54:19 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf2bca8acd294df1dc44dc5c47a5a85038d1be3207686d1ddb7c18b1364e69`  
		Last Modified: Thu, 17 Oct 2024 00:57:19 GMT  
		Size: 226.0 B  
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
$ docker pull debian@sha256:d486bb56ea436bc26e19cfb917026d86cb55eba8ba9a5d5225951fde6c0c7345
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50577056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ee78b0de9892376ee72f566555b1798e81315849303cb5d4bb542c918767a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:42 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Thu, 17 Oct 2024 00:38:45 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:38:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51bd45ec812fbe99b0b9ac227201b5bb38e4d4bfdfe6ef5d8e780d62ae9590a`  
		Last Modified: Thu, 17 Oct 2024 00:42:23 GMT  
		Size: 222.0 B  
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
