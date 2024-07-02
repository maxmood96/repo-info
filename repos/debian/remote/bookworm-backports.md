## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:18da0419fb0c996b2134d098f2ce8b86bb4a0a66210b0226e04eccb4b9eb9f44
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
$ docker pull debian@sha256:821912045518ade005f651decd3945f94baff3fdc85268740405cd8c38c373c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49554287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3b2201f1d743ff4edca973c3b488d9f348973691adb4219408342cafb1db3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:24:54 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162b741114de36b892baca799c63e64f7a7550ce719077dc651c79b9861a74fd`  
		Last Modified: Tue, 02 Jul 2024 01:28:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:bf239576d67058afaea317a9fcd37e11d4fa71540c8aa87ee9faef0277bc48d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47320585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f34e30ead8a165ea292616a24f5d122e6facd385c2766790ed5ad6a902f433`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:18 GMT
ADD file:e0c33927a1af62d353710ab02fe9345a8805475ab99685993742946d38302465 in / 
# Tue, 02 Jul 2024 00:48:19 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:48:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f1ff7b6851f56d19040d12cd1d8757075037a3e51cd0d20ddfedfe600e399be6`  
		Last Modified: Tue, 02 Jul 2024 00:51:07 GMT  
		Size: 47.3 MB (47320358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c349182d4eea863be7d6bb14ddc9cf5b33742c9fb5875613a21f1fc7eba9b5`  
		Last Modified: Tue, 02 Jul 2024 00:51:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8d107a32f99d4442cb1880e2bfc045a73f1b6bd078ba29a7c395bc8c2607ce1d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b6c3ebf2f45419127a324f62a0fab6d952e610f337974febf374ec3012be17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:59:52 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Tue, 02 Jul 2024 00:59:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:59:56 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa91bd5b4d0e6bfc7620273c9717fd3875ad8d79b62b6ce419a38c6d57387755`  
		Last Modified: Tue, 02 Jul 2024 01:03:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a2e705a425703159fcc5424a5c9d2197c2fa581d776a95fe639d7dd0618b5f4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49588671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2444b810650035d3180ed8468c2675b71a2c4b6df52c4dbfd0815173af0a20`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:39:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae6234505f14ba25137658a61633e7f4cc9582aa8628cb15f7426f6e34de9b1`  
		Last Modified: Tue, 02 Jul 2024 00:42:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:7679eeb613047fd143ff6bde2a634c62f5e5b6679c4ee72a3f26ab20de7bf349
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50579530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907ea57b6f3cd8a0d9f76806ad240a8a7209fe2a89ebb1219fbe418ff1e56eb3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:40 GMT
ADD file:262529672396993121e97bbbdda3d91ce43c7548adf11a263b7ec53bb7cda4d2 in / 
# Tue, 02 Jul 2024 00:38:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:38:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:04a42c358dbd9e835f8ae412589572f1bb5a19d9428a4854e4e845c88e34cb31`  
		Last Modified: Tue, 02 Jul 2024 00:42:16 GMT  
		Size: 50.6 MB (50579307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8588304ab54c57e32f87059f34f3a277ee15bee29ebae296b0911691e7973d87`  
		Last Modified: Tue, 02 Jul 2024 00:42:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:01b3b5ea6372d2631fde902a47e4b8b789c589b59ffd3439fb4718f47f723207
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49563344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd5ad0ff5ac1a13ad453619265378af5fbfec768ef88da5ea3d4d0f40d859b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:40 GMT
ADD file:7398b3272eb97d7c196f6072f2a25952abf995169e82ecb85361b7659b2fb005 in / 
# Tue, 02 Jul 2024 01:17:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:18:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:827f475650f14eab4a6679f0e49d9155db82de1d5209a3817922c689f46adf08`  
		Last Modified: Tue, 02 Jul 2024 01:28:47 GMT  
		Size: 49.6 MB (49563118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706b221dbdef31e123a7ff8a1390d5f6c62f058342af19ca7cea1ea20dfa67f5`  
		Last Modified: Tue, 02 Jul 2024 01:29:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b442b822041bf5c2f298c0a81326d3311f1349fd49f80b2f9c97bf9fac50558d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ad4037bfa63bdb9c9787178ffd1f2ccf4d26092dffa79aaa7c6ec10d81937f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:20 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Tue, 02 Jul 2024 01:17:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:17:28 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36598989c3c6b8b5ac19e2d966ef35bc6de7cb554c0f4982e9b65c735d1309`  
		Last Modified: Tue, 02 Jul 2024 01:21:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:310a82b5a178db2c87391845299f569d756f418f6358bd084d2c85e663966522
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47931734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb95e578fb2ea19c87be0b243f3b16cbc03053c85c2efecc1f0462ee1569241b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:28 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Tue, 02 Jul 2024 00:43:30 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:43:37 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ab807c2d8b2d344c0bb26e5308d8905d7440639f3f527dca66f5c42cb93fb9`  
		Last Modified: Tue, 02 Jul 2024 00:48:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
