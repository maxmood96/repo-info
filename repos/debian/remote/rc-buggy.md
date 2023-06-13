## `debian:rc-buggy`

```console
$ docker pull debian@sha256:eaf9ab3e86297768a3ad2d65f9c79e5ace1be5dd89a63039779c19fcba8a905d
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:3f7a8d150d6400a53198e6d4b890375771496b482188540f394c52cd5e201ea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49552191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9598b8eae75731d5616b6521473ce7a1620a95799ea808615ffee90da42a4140`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:22:34 GMT
ADD file:8ed2c72091b90575b320038c2ad715760d6382aeea5c416dd16f7ed04e955217 in / 
# Mon, 12 Jun 2023 23:22:35 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:24:31 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2e79cba44192968ca6ea42058e67723ae58bebd2ea54b31f432b1ffed9fea9d9`  
		Last Modified: Mon, 12 Jun 2023 23:28:29 GMT  
		Size: 49.6 MB (49551965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75902ec6fa24003aa6eafbb12464d5631a1b2c913f2a6d8c271ebb25209a56fd`  
		Last Modified: Mon, 12 Jun 2023 23:31:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:59b9fe2e5119353c69160279711ba0022e782ad88f7fbf86406f155286ca35fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47417546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffe9524648b99b5230e43581053c06e4dd14be27fec0a1c85216ff21aad0f00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:49:10 GMT
ADD file:b79d69fc6594f6ca5e9e76165017858724482b88aa3aa49e3db7b07a3dcabc0a in / 
# Mon, 12 Jun 2023 23:49:11 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:50:20 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:13ee4e7971510c95d7e625030699b854921da16f6d5ef29884b269a308a37afc`  
		Last Modified: Mon, 12 Jun 2023 23:52:56 GMT  
		Size: 47.4 MB (47417325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a9b929a100d7b1c6b6feb62ac37ba2b095bd807b314541341e1155cac46a12`  
		Last Modified: Mon, 12 Jun 2023 23:55:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:e8cdf3c8fbcada103c2033f2639db359d5bf848020f4c518119cc95eed5b8be4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45235064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6da251692a45662334256557bcc73d1e3d6a09ad18e06361ae011f2f1b7fb16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:00:33 GMT
ADD file:82567bde3caa9ad83c0c12c0525e6fd51cc833f0b29e733c2da572ed00150220 in / 
# Tue, 13 Jun 2023 00:00:39 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 00:02:35 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1d80e7ebc54969ad575378cf66dc58999cbf341e0d2a92c9ff0bfd5b3b9fb1c3`  
		Last Modified: Tue, 13 Jun 2023 00:06:30 GMT  
		Size: 45.2 MB (45234838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56229cab246f8f974dcd0de2ba87a05172c49db1b0a1e01d2013d8ed15eb6c4f`  
		Last Modified: Tue, 13 Jun 2023 00:09:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f2d64f9dfca60b88094943e852e16d2d59f1c58254e28dbd962df581d657cc02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49592320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6166bf04153622ceb081a6d7ad917e58e19deed2d74dadaf0d34d6afdff992b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:41:38 GMT
ADD file:94f1432513f9a03b38028af02b1d1720fb0558559faf3e7f9d7097cf6b962056 in / 
# Mon, 12 Jun 2023 23:41:39 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:43:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8ba9ab3e6f12b9702649c2e0c7d78e22ffb9183f68c288b9edef2387bd8d4efd`  
		Last Modified: Mon, 12 Jun 2023 23:46:36 GMT  
		Size: 49.6 MB (49592096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a26a4b55b505c1b8811d5ef643065d6a511757cd32a9e5903a600bbfdb41fa0`  
		Last Modified: Mon, 12 Jun 2023 23:48:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:f327ffb8e721124d17d34e11573771bd0bfe2f4cca46b564b50f46352d1bc39c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50562922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2917eca95e35bdc009a86c37d220a588cf15dc13bfeba7c3593f86304916cbf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:42:10 GMT
ADD file:209e3bb955801ad81eb18a280f9fbd5500a0e1f04565e6c94c9cd24dcba4c0af in / 
# Mon, 12 Jun 2023 23:42:10 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:45:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8bce10b6f772acc79b03d87add4bd359f98c767e3599f82d8e351cced14c1a11`  
		Last Modified: Mon, 12 Jun 2023 23:49:26 GMT  
		Size: 50.6 MB (50562699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dcb6086059e0e729dfeee6a8981c17e9a8ab6cd24b8230607a0442ec8cec23`  
		Last Modified: Mon, 12 Jun 2023 23:52:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:f24bee3f6a1cc054fa692448f6cfdf99c8545b1906c4f9410b824e0fb739f8a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e754dffde56ab9bc2aff2e0464f7f4edda58f0094d66a0a7efd273bd8b83b943`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:11:03 GMT
ADD file:4747b72418fe8be7c83a33927d22b74c9169c9f02959e41f61d71d739fd30ff8 in / 
# Tue, 23 May 2023 01:11:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:16:17 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0f1da758a33cea391a9b76cbdcea2cd41c87b5a2c179c4c1f3d65a456c65d8e1`  
		Last Modified: Tue, 23 May 2023 01:20:05 GMT  
		Size: 49.3 MB (49293333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacb7597e2e7c158018c057a11f3d14f20e3d19e914543dbd04950963c7c9695`  
		Last Modified: Tue, 23 May 2023 01:24:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:f444f0a3398423022d1d74efb121bf81d09bf32a510b56bb14bddc08672af7f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53558740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02da704596a01ec55697a318a9010f9d43c226519cee0226066b6cef34d88a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:19:31 GMT
ADD file:aded196ce7e0c005fe55d5a92492be8cc5d7934fac082b7ab95b8c946e71e0a2 in / 
# Mon, 12 Jun 2023 23:19:34 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:22:44 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6e3f8e732e00762188b5ba00db7db3f36c97d0fccdf3d6121db4ca1febc7d190`  
		Last Modified: Mon, 12 Jun 2023 23:26:13 GMT  
		Size: 53.6 MB (53558517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb443cafb17945962722ff343dcc88bc037e146dc7a95e4fbd9a82bcd7271a`  
		Last Modified: Mon, 12 Jun 2023 23:29:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:84e35182aabe24cb59a5664c253dcdaf2dfc5a34ec3abcc5b5318eed2f841ee5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47664842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ef5ea7483c30d687bee61eb1a2e0fd884462bdb7e86c9dfe6b118a849d3b4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:02 GMT
ADD file:7a71212c59dd3640d3ec2c6d4fd4df4a864f77e634571c1e200a6f7877a02cb2 in / 
# Tue, 23 May 2023 00:43:06 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:021a3707435b37ce556f1886fb9417a47cbfa836555f680d70cffb85f96a6eec`  
		Last Modified: Tue, 23 May 2023 00:45:58 GMT  
		Size: 47.7 MB (47664615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf18678c08e741e18d3e68d1e057a69c98ac089b51c0c6cec761803ddb321f`  
		Last Modified: Tue, 23 May 2023 00:47:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
