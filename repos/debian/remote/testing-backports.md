## `debian:testing-backports`

```console
$ docker pull debian@sha256:867bc65262e653456aa8caecc55ad179b585c2e9c98f2bac1c7bc8446fb8e88d
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e24f4205978e6c0f98697e2075439825f86df56457d2d1ea9e0f8593cf5b5236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52361049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c193dc6cda36b169fad30dfd9b93c507b25adde6e92c92c8425296339dc572f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:23:19 GMT
ADD file:522a6d12a8a3032c984d93fd141274f1cb7cc1e9a6942e3b36cbf803bbe36a12 in / 
# Tue, 12 Mar 2024 01:23:20 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:23:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6f920f542b4ac4c8439263aaa577872294912b5aaa038e252993d921098eff73`  
		Last Modified: Tue, 12 Mar 2024 01:29:24 GMT  
		Size: 52.4 MB (52360825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a82ffce816b92bc90262e1a3761c38fb35300d08817a24ddfbebf417bdf05e8`  
		Last Modified: Tue, 12 Mar 2024 01:29:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b8185f097555e5a45bc0e20d28893a7a123249d0f0cb3b9df78592adf38c5f6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49418261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e90278d3ac7dcfbe670b43c5a7ee721ff753041b5757658b8f26f0ba343ced`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:49:40 GMT
ADD file:c77e9732e138f32878ee1d185f6556aa70f368f3a7b348b99ca39e7934b060b7 in / 
# Tue, 12 Mar 2024 00:49:40 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:49:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7bc5c917a93801411f7e87cf724c98a04503d7ce7065edc28d64120df24306ed`  
		Last Modified: Tue, 12 Mar 2024 00:54:50 GMT  
		Size: 49.4 MB (49418038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a5cc84bbaf722a2ba3c31517ae56cf2b688ed69a3ba674637579f526aa4b98`  
		Last Modified: Tue, 12 Mar 2024 00:55:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:43c879b9b8632f89691f4a097aca24beb26bea2f0756ce7c3a53538f8ec91ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46919347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca110d5ce1b19d20608e881746eb0c7febc812d95f34fe429e712fdaf8c4c0a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:01:23 GMT
ADD file:908e973d9d8333dc3caff8775e4f6b94048f473bf1f68e4c571be34da3cf20a3 in / 
# Tue, 12 Mar 2024 01:01:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:01:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:12d3ac6dffbce35a512571e251b96129cf86a1a0fbcd2a1dadb5f7133ce5243a`  
		Last Modified: Tue, 12 Mar 2024 01:07:45 GMT  
		Size: 46.9 MB (46919125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3471897630cfe50754fe33a33a08bb8e02a75b5bb38ea61448f79ed968ab405`  
		Last Modified: Tue, 12 Mar 2024 01:07:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bb496232a5c28a01a8337cac688b05d038a3d4e854aeaa7bea21d886a4736649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52191555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bba30c78ae53ed4936e912f1ba78ed522c1628a77ad7bdb4df301001d90f974`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:47:08 GMT
ADD file:aa95db2c8e57643981efcdec0f1d6b86b507e56fdab54a8247748679a6433c70 in / 
# Tue, 12 Mar 2024 00:47:09 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:47:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9753ceab8e9b6188a30d0d3bb81834420e64806a562e2bf8fe628f8f5abe3bd1`  
		Last Modified: Tue, 12 Mar 2024 00:52:29 GMT  
		Size: 52.2 MB (52191334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acd35c7cf8b98826416be472de62bb8b2f2c24fcd8c007ea1c43421bb5e8a6d`  
		Last Modified: Tue, 12 Mar 2024 00:52:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:1bc322450c48ece5fed2ba3c22af104d8be2bf9c01c203b4ec2d8abab899cb74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53172887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc290d7a846563967c7dab593d71861a6b1819e99404f74f1d761c2564fd02e1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:00:22 GMT
ADD file:6cc20e9ccdb1df7ce1d4990f715e8a5ae01c948db3848423737d3390e1a04784 in / 
# Tue, 12 Mar 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:00:26 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:29fb00bb05ec2c993d0e42509cdab8523940310bf816bf82b5587313e85baac8`  
		Last Modified: Tue, 12 Mar 2024 01:07:05 GMT  
		Size: 53.2 MB (53172662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ad4d4151c8370070c256311662152348538c32ff8c0a826cedfa93780635d2`  
		Last Modified: Tue, 12 Mar 2024 01:07:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ffae555602631f25466d2df6703f1a43a82e59e192f16bd0f694831cf233f7b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51407967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad21d3c4f80963c781eddd2201391c17f7a6f02cde33937e5acd3a6a5e61ab2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:11:37 GMT
ADD file:cd74238aa52b27336660b14ea6608ca519ab0e138a701c67bfcbb64231501327 in / 
# Tue, 12 Mar 2024 01:11:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:11:57 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6b1a3f8e5e804154381a1854a500242f8a7822a20b40b5865898d0b7e1f52827`  
		Last Modified: Tue, 12 Mar 2024 01:23:42 GMT  
		Size: 51.4 MB (51407743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edf297d1b78e950abd33fdbaa21edfb9fb133341c21a97ae19393375634eeb6`  
		Last Modified: Tue, 12 Mar 2024 01:23:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a5d2cf74fafdf34d764f8ba753dce0f061a03a8070fcf62664ea1999527b64b4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56241055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade65ec286e6722bb0c9f84faba371acbf97bef4870f21d6e1cd282a6a1185f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:33:43 GMT
ADD file:28eae816397952c51c49be5b893eefaf784b74fcc86be5f7530f348f3bd79748 in / 
# Tue, 12 Mar 2024 00:33:54 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:34:04 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a330bc7a744677f7e934fa2e18de7eb61220cadc075ee5145cd435289dd3d817`  
		Last Modified: Tue, 12 Mar 2024 00:41:14 GMT  
		Size: 56.2 MB (56240830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0421d65a5d17acba48593345926af628035721f0739732cb142695fac630d8b`  
		Last Modified: Tue, 12 Mar 2024 00:41:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:438677999606bc67da361e47e08d1440019a3545861aa13ba7396d6958bdb7a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51738720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0af31e361cf4f714cd60b8d2ae5a33f31ac0cd89f65c493e87138d6973e4f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:50 GMT
ADD file:283bc28845dbc58b098cbb254944cfae0c1d6f16ae79ae7362fad52560500387 in / 
# Tue, 12 Mar 2024 01:08:55 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:09:58 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:073f53dd9806858358fdd1059a56d049af47a20cad92d4f3e90dc7bcff46e1b1`  
		Last Modified: Tue, 12 Mar 2024 01:23:21 GMT  
		Size: 51.7 MB (51738496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2419e9e07296ae99b712332074cc02f8d7ddef66c841cbda1724cec10d22a4bb`  
		Last Modified: Tue, 12 Mar 2024 01:23:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
