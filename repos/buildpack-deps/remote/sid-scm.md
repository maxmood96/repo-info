## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:11eea093af04ed1742e0d2db983b4d2628bd254d3495929f8643c4ccef821ddb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a9580c6cfa9bff456e7ad82b0cb25a8c5b3f59d21a389fb69f224bd0011332f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142812158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813fcaf1518c60e2cb520498e02e731505f36c4c340958ddf3252d9be5f5e319`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6feaabef59d289e85af66797a02e340c4ef2c0b04736caed083c35478e55b244`  
		Last Modified: Thu, 08 May 2025 17:07:50 GMT  
		Size: 49.2 MB (49246057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d1ecbaf1bddaf2bd9cbc9debb88e4614fb6c0dfb32a08b3f3e0e22fd2a9b7e`  
		Last Modified: Thu, 08 May 2025 18:00:15 GMT  
		Size: 25.6 MB (25573234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26542a7c9e9d2a5ec56f7af776fecf60cd09723335c9c3b49c5dc5bdc77a4f0`  
		Last Modified: Fri, 09 May 2025 12:15:34 GMT  
		Size: 68.0 MB (67992867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4d74ad14c9f67ee8760ba46e0f48d2e8577849c0c91771f981854bc2e36a2063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7579257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55d936dc7a4ff7fb0c95033609aec045863f6d85aa1acf318f253a5219f8d61`

```dockerfile
```

-	Layers:
	-	`sha256:5a4b5c9f0e143b41e436ed5451618c085bd2fad7fa2ab79d84c0569db4c57a83`  
		Last Modified: Mon, 28 Apr 2025 22:15:48 GMT  
		Size: 7.6 MB (7571960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f208efcacdfc58d164c1b8f715bbc9c185e7d8cb5b0a21df079f5ea0fc55fd8d`  
		Last Modified: Mon, 28 Apr 2025 22:15:48 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bdca6a9c2832851dfa6b013e401dd4526dc01c91738569bf688d53f2d7efe134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137335211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe4186492e184d15376beb6fa5554d5a0365e3e63c249f860c126f9bd370455`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:404fd683a770153140d6973002a75f89d6a436af748f330e29e1c3f0ca67e300`  
		Last Modified: Thu, 08 May 2025 18:03:47 GMT  
		Size: 47.4 MB (47437736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e0a1e0dfa2983e94d5e01ac25e7f9b86f8206e92fe7aac9b2c5f9a123c36af`  
		Last Modified: Tue, 29 Apr 2025 00:47:07 GMT  
		Size: 24.3 MB (24301061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245945a0a2cee7723642bd65373a025bca132437cca15092326e78c91ef6b8b3`  
		Last Modified: Tue, 29 Apr 2025 03:55:21 GMT  
		Size: 65.6 MB (65596414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e4ee70f44dfe87e7c4daee2ef070eacf5e97c63f098ad87a75993cdf199d8533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7586270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0db16df1905ad27245da1d97668370eb3d39a46c6704b07d358e9d6d54f7bb`

```dockerfile
```

-	Layers:
	-	`sha256:fb272d0d7a90d290a43282cda8bccd326e07dfa6124371457bed722a6f4d4380`  
		Last Modified: Tue, 29 Apr 2025 03:55:19 GMT  
		Size: 7.6 MB (7578913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:218647cf408fb6f2adf8a7626099ac81fcb2dc4635c9d4dcb5f1fea77a16cb98`  
		Last Modified: Tue, 29 Apr 2025 03:55:18 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f5456a0fcb45a9648c921555206b412cb56a80431d9ff1015677ac6ceb894415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132275963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5088467c2efea6d3ca173ac41202c7757b9be133e37e0c640ce8a49dd07b5ad6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4f09954038071c4b7538cdbfd367f3552df4666eacc240bbf717397e0b9c060`  
		Last Modified: Thu, 08 May 2025 18:03:51 GMT  
		Size: 45.7 MB (45690318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea9aa9d3149432dc9bb5c2fe207c68224ef45d2d9f918a0e4d2c3d72b6f2c6`  
		Last Modified: Tue, 29 Apr 2025 03:38:23 GMT  
		Size: 23.6 MB (23574679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafdbfe38e24dca5b7ad9f38f6e93d3d1bc4e6bb311befa9c69d791b516b739e`  
		Last Modified: Tue, 29 Apr 2025 13:25:06 GMT  
		Size: 63.0 MB (63010966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0c7b3ac01f9b4297714bea8b926338aad96e7977ddd8bc8d324912d44da07576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7579816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d3d868db1b636848b372a80a54856701428b1946ddf91a3cb8b8fc4324216f`

```dockerfile
```

-	Layers:
	-	`sha256:0676561363eb5bee38c50f119a83f1f694b12f794c58b2d18d884cf472cfaf45`  
		Last Modified: Tue, 29 Apr 2025 13:25:04 GMT  
		Size: 7.6 MB (7572459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7800df02098af80eaf6b1f8d27ace7e5494d1810537627e79e0bce0548cb4e35`  
		Last Modified: Tue, 29 Apr 2025 13:25:04 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ce13f256c043d3b724525e6a5c0f894ce2d29a24b13a6131064023f90fcc672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142432458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8061076d3b30678895f4a27c86c401a90c40cfc6c6b98851d81ac3734b08`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2f619c4109fcbcc024465075840b71159fc76526814180d90bfff14b20db08c`  
		Last Modified: Thu, 08 May 2025 17:10:22 GMT  
		Size: 49.6 MB (49618408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ba9361c22f0e29208e6629c0b8872ae776c0157ff0e94dd78175d7d69661ee`  
		Last Modified: Tue, 29 Apr 2025 01:47:44 GMT  
		Size: 25.0 MB (24957999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908dfd8b0d455e2c1c6f55953fed71aa4cf1e842409ba85abe5575ec744af67e`  
		Last Modified: Tue, 29 Apr 2025 18:38:37 GMT  
		Size: 67.9 MB (67856051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98c3cdcdd49121830e2e79b4659d6f80eb25a41625726a07f748567e914ca097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7587000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2328975dcf39a17e1b83dd0d8002275cb1a91faf59319d9bf514e68086a3862c`

```dockerfile
```

-	Layers:
	-	`sha256:a6b4030aec2a37dea766d13899db0e4752e819a0f05a284cb5f1d641908404aa`  
		Last Modified: Tue, 29 Apr 2025 18:38:36 GMT  
		Size: 7.6 MB (7579623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a3af0aec7fad97d8638816cba806e028dad65bc23da7b7ee6b5063aa2401d5`  
		Last Modified: Tue, 29 Apr 2025 18:38:35 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2156dbe58c2220855ad79f93b52b307a6d1ef776f1e7d7b4307477bab37f9bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147406850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e12e1a9b708c73ec4f252958322abb1db5f35fc24427b284a50e7f01086c22`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f72acca1637ca2dd8a6d7b3e16eba9907e862c2052b181ab848453b963bf8836`  
		Last Modified: Thu, 08 May 2025 18:03:53 GMT  
		Size: 50.7 MB (50745529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c1f129fec1b0fb6b1af41a0589e5dacc9adddd0abb3826af4edb56b312c90b`  
		Last Modified: Mon, 28 Apr 2025 21:54:04 GMT  
		Size: 26.6 MB (26570218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bd94da87a016d305503e4abb4c5b3d2bb2be2305e1da2659a8df67b2645dc4`  
		Last Modified: Mon, 28 Apr 2025 22:15:03 GMT  
		Size: 70.1 MB (70091103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:121bfa70dd3708f7164eb18a1efd7bb4cf0d2bc0d30fc777c0ce6a2796729695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7575305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2346a6ab2d4cc1a3541e23c4d52d8cf96a7707fc3cbbb8c4e08aba83428746d`

```dockerfile
```

-	Layers:
	-	`sha256:8bff4b2cac45dfd61650ad7e38793b7133d41433e4d04509151e0645311e15ec`  
		Last Modified: Mon, 28 Apr 2025 22:15:01 GMT  
		Size: 7.6 MB (7568030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4f125d36312d44f80d12c360a2567234c75313a71544baf28b82f402ee52c2`  
		Last Modified: Mon, 28 Apr 2025 22:15:01 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:15784b120af8be38494d5d036dd67bca3916de7ac824ad4782fbeeb70bf4faca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142168851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468eff7ac7fb93a19075408cbf80855321980b70864f447c63825c2919b5d90b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d206785716d2e915433eb85845aaf9607094981ed3c32854f9401982e23a7af`  
		Last Modified: Mon, 28 Apr 2025 21:11:40 GMT  
		Size: 49.5 MB (49535121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46b0656b2eaf48d740fb0cc28ea93ea835c76c41dc63d12f18a3fd227d3d57`  
		Last Modified: Tue, 29 Apr 2025 12:45:17 GMT  
		Size: 25.6 MB (25618095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b53c377a8e6571103378ce926b4efdaa12bf0271ca14fa02f969e6c3d97192`  
		Last Modified: Tue, 29 Apr 2025 21:19:44 GMT  
		Size: 67.0 MB (67015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e1e9797789fcdfbd96147f620a6201ffb10e18f33910c3ed2ef4c3aa6a5db61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162f9565b699fb610e87177020e7803fca07a34a7056ac633b10af336c574084`

```dockerfile
```

-	Layers:
	-	`sha256:f02c450e6044cea86b9bebe4e9f26e8a4e334c25b0c98edc34562d3b7b639122`  
		Last Modified: Tue, 29 Apr 2025 21:19:37 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7a1c05d7d024f4aabf1d7240a7fe6d40ab6c6af8f573a553229a02be8d591d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153394481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e2a3d8bf04f2198819eb33a2393528efda841dd9e7a03975b7956b1544d3e8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d320c0b02fe20eeef6a5432aed2b294506f621139378d9f899d155d81d1080d`  
		Last Modified: Thu, 08 May 2025 18:03:47 GMT  
		Size: 53.1 MB (53078100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e713da9ea3255a6f791030cf59cd9bdead64cd96fffafbed2a4a6fe1aaeb2b4`  
		Last Modified: Tue, 29 Apr 2025 00:38:55 GMT  
		Size: 27.0 MB (26960240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cab10ca498aa4aa931178447c0fd221d2105fe390900e832573ae0d70bd2a58`  
		Last Modified: Tue, 29 Apr 2025 04:37:55 GMT  
		Size: 73.4 MB (73356141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d8ff24092f0fc99f0471391a9ec0e51f87f4ba20aa619f59cf4256a02bf70b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7592425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34aa634f4cb70db14ee079d08315bd66b5030f89954cd9732389da8c2a4e612`

```dockerfile
```

-	Layers:
	-	`sha256:c4bb6128ea5cdcf71980f914530a9cb8169402351132a78061e5e23d7a9e7ef3`  
		Last Modified: Tue, 29 Apr 2025 04:37:53 GMT  
		Size: 7.6 MB (7585096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749da50d0567240469de0c2241be5570724c5c5a85719e8fee27ce30c2dd4e63`  
		Last Modified: Tue, 29 Apr 2025 04:37:52 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:260bd2886258886eb84a15a34164b9dac1bc5059f839d21950a7b73de17ce20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139768329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b3ec584f30287860b134fd12cee1c42281f988aa47f455606da1c7e34c6e66`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:974932b0d4f6a2a6986aebb6971e9388758bb668ea9d86ad8d2fa557cb4fc4d8`  
		Last Modified: Thu, 08 May 2025 18:03:52 GMT  
		Size: 47.7 MB (47731445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66e85f6895b6c676e8788d49a505ba553dd35816b89660f34e2ff2455d80e6`  
		Last Modified: Mon, 28 Apr 2025 21:53:00 GMT  
		Size: 24.9 MB (24895784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54467a3d4fdf55370e452bcbbcea511942d0f832e606fb0d65962dd4ede4eeb2`  
		Last Modified: Mon, 28 Apr 2025 22:18:39 GMT  
		Size: 67.1 MB (67141100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ab757da4e1117ff5bed5d564da82b01b7a804efb86805c11bbfb56e1d634d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7614048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f5f6df60379c47b93564e3fea49153843ad8e24387c7d34e65dae29e33ef6f`

```dockerfile
```

-	Layers:
	-	`sha256:1f189e21c06a2d35e3f9eae03a8cd27e1bfb1856dc21c8110e3e910f9665d775`  
		Last Modified: Mon, 28 Apr 2025 22:18:29 GMT  
		Size: 7.6 MB (7606720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d6815878b95e031cb2b131979571d25cdba13421a164d07491d9c113b9ba8c`  
		Last Modified: Mon, 28 Apr 2025 22:18:28 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5dba32c43acda1b43436b1fbafe1f75433641d107f2ecd543356ea4dad95a0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144743783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b55f1b98a90f31947aa10329d3dd189457e66221e0ba2bd16ae8fadc2e86eb0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8157e1045a0b1a8c8f6ab28a26ace718f29668344110893144c8a16214d7a54c`  
		Last Modified: Thu, 08 May 2025 18:03:52 GMT  
		Size: 49.3 MB (49321224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ff5701e764e061146831a7cbe6697f1a1451a6db3d328a14bf9b0b7aedcd77`  
		Last Modified: Tue, 29 Apr 2025 00:01:55 GMT  
		Size: 26.8 MB (26765142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44ff1263d784021acfea0dd01784c46b994ae5ce4e21a5a296ca7feda4ed5e7`  
		Last Modified: Tue, 29 Apr 2025 02:59:42 GMT  
		Size: 68.7 MB (68657417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2342370dc87e667a3f646cf86cc9fe25f8b51107b4ed8d40b7586c4ad14bcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7566692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480dc6ff368c27ff21385c309085feef13ed8c98aa1fdd8d9fcfa7ff77ad270f`

```dockerfile
```

-	Layers:
	-	`sha256:79c46c36f00a862ad01fe7fcfcfcbf255d8196d3b49ccfb8f174746792a80232`  
		Last Modified: Tue, 29 Apr 2025 02:59:40 GMT  
		Size: 7.6 MB (7559396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff8aced42d44b3ba450efac252e1ce9f8ab9a4ece04487f3c2db5ab99484a37`  
		Last Modified: Tue, 29 Apr 2025 02:59:40 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
