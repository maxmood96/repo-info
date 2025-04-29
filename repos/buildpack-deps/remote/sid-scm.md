## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:3da59f886b76e252ad55f429f228ad7237a71e9498b79b825023c78b37bd9f3b
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
		Last Modified: Mon, 28 Apr 2025 21:08:16 GMT  
		Size: 49.2 MB (49246057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d1ecbaf1bddaf2bd9cbc9debb88e4614fb6c0dfb32a08b3f3e0e22fd2a9b7e`  
		Last Modified: Mon, 28 Apr 2025 21:55:21 GMT  
		Size: 25.6 MB (25573234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26542a7c9e9d2a5ec56f7af776fecf60cd09723335c9c3b49c5dc5bdc77a4f0`  
		Last Modified: Mon, 28 Apr 2025 22:15:49 GMT  
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
$ docker pull buildpack-deps@sha256:51a83913a3d1fb28eea1e17a8aac3a1d26fce1cd70d468e24c8a89359b859b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136406047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0199a72a714d847bc58b7145c181c598d2b394e04c3ec25bdf18f8b1c137b71f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7a67f90f752f0b4c3cbc55e5cc36457c9464d60f34b4c1a8cb2a06c06cfda363`  
		Last Modified: Tue, 08 Apr 2025 00:23:29 GMT  
		Size: 47.2 MB (47203396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a07c09d53242d965ab755e1358498dc94eabdef8c99be65a21d5b9eea16d2`  
		Last Modified: Tue, 08 Apr 2025 05:12:45 GMT  
		Size: 24.0 MB (24031511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b89d4498cb31b4e330ac0bf8f8366b90ab05c82f7ed154f09e19faaaf575be5`  
		Last Modified: Tue, 08 Apr 2025 08:38:45 GMT  
		Size: 65.2 MB (65171140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bf2334b66690915e97da36328409dbf6861ab69b3c7fd4018b14917c718ac91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7619120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6c0481967776346d3241c3e9a4e5747d4492437f9630264214bf5f8163aa6`

```dockerfile
```

-	Layers:
	-	`sha256:0b0607048247000dc44f0e6a99aad6b058a648ab663600701ecb5cba57ff25f7`  
		Last Modified: Tue, 08 Apr 2025 08:38:43 GMT  
		Size: 7.6 MB (7611763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf38d62528c6518b4d12d781b51c59e21da77d285c0bc7708805be123175af35`  
		Last Modified: Tue, 08 Apr 2025 08:38:42 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c866d0af4edc016dabe48806c6290c893dcbde67aa39dee6ec05c25d5820801e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131448967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6452b92055810c27ee4d1bdc3543c1974a0bbc8e928f54ad88c12b4dfbdd97ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9e1d1d502e5470a18b1778621dae87bc08126015f4514c8d42f4923e5bbe3526`  
		Last Modified: Tue, 08 Apr 2025 00:24:51 GMT  
		Size: 45.5 MB (45459990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aef4244a5aaa0829da0ede8fd328ccc49be5178ede43a05010a5169a12ac0dc`  
		Last Modified: Tue, 08 Apr 2025 07:39:15 GMT  
		Size: 23.3 MB (23303278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f877aab82202905af0b48ebd21bac544815a1b4a8d0acbea3e524330c43db1`  
		Last Modified: Tue, 08 Apr 2025 17:31:40 GMT  
		Size: 62.7 MB (62685699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf000902a4f0d9e28dde200a8cda562464f4fdbfaa7517517fdb1ca0daf4845b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e2ac1899251c7ba82e90ea872dd4c174dee62bcc284c7aec57f17c9897a93f`

```dockerfile
```

-	Layers:
	-	`sha256:a9fbbc95120cee49b6a6901ef927432a913f1ef856ba3ee28d27bcac0698ef9d`  
		Last Modified: Tue, 08 Apr 2025 17:31:38 GMT  
		Size: 7.6 MB (7605309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad2ba1fbc0d47dadc84f2285a014929eb92004da895c7c442ed1b4d3452b631`  
		Last Modified: Tue, 08 Apr 2025 17:31:39 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e2fc2c3e226bfeb325b19fe6f060327c06241ae782d4907b3e0c6df5d962855b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141481557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811f47d93db9c7678056fa9009352ad6ca9be480bc9062d4c07319cf6429c26f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:09d775ffe2e3a261e25d75c66999fe50b8109b656ae312ea92d80a3277b69b88`  
		Last Modified: Tue, 08 Apr 2025 00:24:23 GMT  
		Size: 49.4 MB (49356840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd26d5bca0f15f13ec1e165536514cafcf57ff3d2c87ab2850f356915ddeb3aa`  
		Last Modified: Tue, 08 Apr 2025 06:04:11 GMT  
		Size: 24.7 MB (24668055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435258a53ca79e7f70aa94751fa20a91cc1653438c309c299182c4de6da3bdd2`  
		Last Modified: Tue, 08 Apr 2025 12:19:28 GMT  
		Size: 67.5 MB (67456662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ee4c2725d5c2194ee9117784767ed0885e13a7d0cce89da56b6e380ebafc8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7619850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb898fee0aaba28e2e38dcbe7c8400549be386e57d2983d82edac912c97d8cba`

```dockerfile
```

-	Layers:
	-	`sha256:b0f3b3738874b491d2a28c3b7cc528215748cca26e71a91f72f26bd5b0788d1f`  
		Last Modified: Tue, 08 Apr 2025 12:19:27 GMT  
		Size: 7.6 MB (7612473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f3611f10a23bf2532d7ac3392efb92ab25334c2b1e72be3fd1f1cc691b2c9f`  
		Last Modified: Tue, 08 Apr 2025 12:19:26 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:08:12 GMT  
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
$ docker pull buildpack-deps@sha256:d4b3d66c79f85686a9e4a05025e4cb356f977ce75d3289b93526c8eea24e4e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141270385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276aa63bb44e0a6ee46f6a335a61fe30c7d7049f76df02bdac43e75a79b19870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e47ff6f8c72dd6db533d94619301df4fe359af27c4bdf16e11f5c32ee9c26e9`  
		Last Modified: Tue, 08 Apr 2025 00:23:50 GMT  
		Size: 49.3 MB (49276857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e51d673a637240b96d7c17ea9519652624afebf48f4c69f85cde5bf9564505c`  
		Last Modified: Tue, 08 Apr 2025 16:33:23 GMT  
		Size: 25.3 MB (25333380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6496631413be1b4af7658f44458c20e2e7b199a13d97fee3752f289b6ea176`  
		Last Modified: Wed, 09 Apr 2025 00:41:38 GMT  
		Size: 66.7 MB (66660148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:961968fa2e02b47c2b251907ef1698069df7b182a8ffd6e9a4879f42839d4004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ae736cc2f0a902ab012909dd1dba84a36efb12c69233842bb922f87796004`

```dockerfile
```

-	Layers:
	-	`sha256:300420acad9d8d5219747b5dfbc3795015e6c18c1bda4c6932c2cd273603e365`  
		Last Modified: Wed, 09 Apr 2025 00:41:31 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:367f939991027b42a5009f021c517b683d364e771a4c1aab89bf38ab5a75ba89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152246469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686cc5d2862d37e1a77c3618b0cb468575540ecbb4ea2940c2aa06cd9d099abb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:24038d07494a40a6e0f9bb4cfa800b5c396d2199d38fdbd9a4d93a09f5534ac0`  
		Last Modified: Tue, 08 Apr 2025 00:24:22 GMT  
		Size: 52.8 MB (52784300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db81c823da47f6b320f39ca946071003941c644715aa03b5cfb4494f3617d2b`  
		Last Modified: Tue, 08 Apr 2025 04:31:07 GMT  
		Size: 26.6 MB (26637683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40825775c0fc5d49e80018df1342d3a42c3a0c76661dcf0b4bcd002c52dbd16`  
		Last Modified: Tue, 08 Apr 2025 08:39:20 GMT  
		Size: 72.8 MB (72824486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a8a7de7a25dc7bb0a2ad6581f286978f18dc52bde33d8952700ef8841b3b7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7625275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823fbf76b8bee27b33a47bcfaf954905198b2e94ccfb8719816112d5861755c8`

```dockerfile
```

-	Layers:
	-	`sha256:6e8beef348bec3a12fc55014baf3c4d760c06ada146675263a259b57df7d9642`  
		Last Modified: Tue, 08 Apr 2025 08:39:18 GMT  
		Size: 7.6 MB (7617946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443d4e27d56cf92a980c1bf665f91a6fefa405201d862e884d506ec08ef0412d`  
		Last Modified: Tue, 08 Apr 2025 08:39:17 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:09:48 GMT  
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
$ docker pull buildpack-deps@sha256:a9ed0c43fa50349539ba692b68311e7612d1acb7d9f5a90e6e68aa407d327ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143721920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0820c7ef4f895df8a8dfe7aac1cbbfdb874941c10a8a684d76e8551238a09370`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4724dabe4aa05329c356a033beb752bf4d3d8e15762c4c9025e18f8b74f6a65`  
		Last Modified: Tue, 08 Apr 2025 00:24:40 GMT  
		Size: 49.0 MB (49047465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70d32a5e527bdaaef0ef8d058290901aa64df97cc259e7f2fd2e845c51227b`  
		Last Modified: Tue, 08 Apr 2025 03:45:05 GMT  
		Size: 26.5 MB (26460166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d56a7d1628e664d6ddfb9ea04b13051b1461c586b96d98f706033c1d083c89e`  
		Last Modified: Tue, 08 Apr 2025 06:53:42 GMT  
		Size: 68.2 MB (68214289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb80040911f979319ae8e4fe549675726f9e6375ebe31d322bd759f03d9ca132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7599543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27289725925469a872c1a4faecc190035613796bf915d35d54eb64c891130bdc`

```dockerfile
```

-	Layers:
	-	`sha256:f1ca06c151fc095028cbf0fe841b3eb7e1010402b147220bf8a103e721dd897e`  
		Last Modified: Tue, 08 Apr 2025 06:53:40 GMT  
		Size: 7.6 MB (7592246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24cbf7ad1a8a6714fb130c76dda5b087840fa92ef62a1ecbc747e87d5f457f7f`  
		Last Modified: Tue, 08 Apr 2025 06:53:40 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
