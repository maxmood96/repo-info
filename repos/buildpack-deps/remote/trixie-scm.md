## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:4593950a51df5a72713e76dd1ad4d4250e27e97c7a9279cb91cf212714251567
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4c9687cfeecdd688448a8e045f7e58ca8e17d20671b79c5ff3321b44b02ed6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142686657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba530825b50eab47ad77d05e79278ee6709f176e82e004fe545e82e0c4856a39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b50f0455ac706e59be1a6ff3b4904595e2dcde0743ca3473c879026f0eb62b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e527fdaa48d7661fd8e77066f8ce80690a9c6ad7d4766020f4fb21468c11ef`

```dockerfile
```

-	Layers:
	-	`sha256:2dd4c7354953cdae57b867c3856ed88ed5cb35bdf9ede4f6e41ba79a16ef4e60`  
		Last Modified: Tue, 24 Feb 2026 20:04:26 GMT  
		Size: 7.8 MB (7768137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c414b02dbfc56e2c3d74e85f44a166f1f6e548ef19b9e508904be20cabf06cb8`  
		Last Modified: Tue, 24 Feb 2026 20:04:25 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:744570a979d06b9f77ae71f7f6e2420b3a8cb5fea6807c38b0afb01a7346c3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137133992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcb026b5692b33e0f41c9b695b71ecba68380af02f5c491fabbd34c38124c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:56:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:15:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6c0530a0840df8a05679f77d095cbed0674c87160dab8f0e65ed5257ed4b0ca9`  
		Last Modified: Tue, 24 Feb 2026 18:42:14 GMT  
		Size: 47.5 MB (47454162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc237884c34f3f7758c4fcaea06d5eb8bbc53d28e124d2e90e646c55a9ccd0`  
		Last Modified: Tue, 24 Feb 2026 19:56:25 GMT  
		Size: 24.4 MB (24361479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667af045e313c4df4ebab8d75985bcd9590a6b8f2ba5798c2335e4044f0dd348`  
		Last Modified: Tue, 24 Feb 2026 21:15:38 GMT  
		Size: 65.3 MB (65318351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:31194dfcd5fb47ece4e2164358053162ffd20ef5a64e4119ee188f9e93ed1ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b1c5a120a11a5a6d564bad3675587519d55846960a375cf0b4d76a0688f4e9`

```dockerfile
```

-	Layers:
	-	`sha256:fed719fe191e893c3c7ae597d621a9e79a65a4ffbd5420f2acbf84228f6f51bd`  
		Last Modified: Tue, 24 Feb 2026 21:15:36 GMT  
		Size: 7.8 MB (7769175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d780c251dd6c610e5e519272a522f84c1daadcdbcc11033d39828a53cbb607`  
		Last Modified: Tue, 24 Feb 2026 21:15:36 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:813f86de3244193339097384713be71b807f2b8b25cfc73fbd21aaef23683098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132072332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9dde28078454df3240600507577a47966fa9950cb7a1dbefaab5e948ea3e8f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77120a84626d4a7f2d6bdca75bb942d16ac419ff1bc25fc6e9d95035fe35f65e`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 23.6 MB (23633662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27016c2923c40df4d7f8b1909d8aac2050fedaaac6d29c1a4942dcab0ae038b`  
		Last Modified: Tue, 24 Feb 2026 21:35:13 GMT  
		Size: 62.7 MB (62713584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8694f6ea48a3a14bf630c8f8c222854ce2837043112f09cda10c84bb05d5615d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5896fa3c918c76860caba45c8a86af9aae08fbfcffc343658a3130423f2d81`

```dockerfile
```

-	Layers:
	-	`sha256:1a9014e315d1d45295f3a64f82465ca48f6d514a944478b9c445ee2e09241750`  
		Last Modified: Tue, 24 Feb 2026 21:35:12 GMT  
		Size: 7.8 MB (7768644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f61f228e2a2bf29b1e2bc072586dc83a1799b057467ac18529473418bad788`  
		Last Modified: Tue, 24 Feb 2026 21:35:11 GMT  
		Size: 7.6 KB (7647 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:89146e3ee596f560967da8351731ef50383f6e7f51a5ae6f8812890fbb374cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142261212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb966b926fb6de98e7723288135505f7a1ed819be5633098e67573dcf0fb090`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b85579d70a2385ff3e0faa3a2d33cf45ad03b098e369f2fd05ef738c67dcb2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07413d01b6ed2d787a0668111f562d728698a643bd13b31437c8aeb90da6b914`

```dockerfile
```

-	Layers:
	-	`sha256:8ca0add12aabde4eb46cd2abfeb5f2f2cd44683d6018b60efd2a0e3237c4ceff`  
		Last Modified: Tue, 24 Feb 2026 20:15:07 GMT  
		Size: 7.8 MB (7775812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9a5f5a149869ac1bbd950f96b0df662373169e4c9f0a8bfd846d92a4eb184b`  
		Last Modified: Tue, 24 Feb 2026 20:15:07 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3586f7d0dbac402184bc70c0200d1143bd5ab6b2e8bb6ad07f98be99bc00243f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147379779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ad01f6b1e62985a2415f55265872c3e8cad91468c772343c7922e74f0c6806`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c73fe9d5e539e615e830926d2ddb692fd4ffb36bb2ea42d3131dcab6528d49`  
		Last Modified: Tue, 24 Feb 2026 19:57:28 GMT  
		Size: 69.8 MB (69794855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5d258a4e45d8674d0ddb9127eb672b3ca17750ca031ea6c8363a75b5f5b26eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060264a014dad1de8bfdcf18f077e4e240dd3206a8d7f47e685f9c7e81c03f83`

```dockerfile
```

-	Layers:
	-	`sha256:72684e0bbe8af809e8d478936a99e213d9af014e77652a23c021519d85278fdd`  
		Last Modified: Tue, 24 Feb 2026 19:57:26 GMT  
		Size: 7.8 MB (7764271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b87308dbd17db94f95f1c8f55719569c015681f040535e7fb4990a7468578e`  
		Last Modified: Tue, 24 Feb 2026 19:57:25 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5c46fb39891cc25749b8ce456a659ac36b3d16043188db369ce60f4ce73a26c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153138761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791ef6cc3ffb872227c8014aebcca6d5ab1ea3751805b7deda2980278f33253a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078b8ed13f55a8d2e3bc098e87fe680e2a4289c11315d3e460db7bcd51cc93f`  
		Last Modified: Wed, 25 Feb 2026 02:59:03 GMT  
		Size: 73.0 MB (73022125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d9c25312ca3ed45ed92c060683c69cf3e1c4d8ab7630fa7f1cf9b71309706d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4debd16e8b28830ece4e96dbaf091844dace361447d90d3f7ec0d598b0e2e4`

```dockerfile
```

-	Layers:
	-	`sha256:0c369ba15e705bf80af245fc99671305cf0da65c3b6276aaa5d8bbcf48886499`  
		Last Modified: Wed, 25 Feb 2026 02:59:01 GMT  
		Size: 7.8 MB (7775262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e112c00bb236ea8d5e2c9db37b6d10e66c06c608161d780e63cdce518fc68b62`  
		Last Modified: Wed, 25 Feb 2026 02:59:00 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1e758672c0a2a5eb687219e1f90579a2a0aaa98e799acebf82f2a63573344b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139390353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c97ab799c6c00a2c2a20504e94a90f8e15a65480d2c646ee67233494558233d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 03:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 06 Feb 2026 07:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e689506e8938c3b552c90ad33fbba57defdbbcda283a92391186d21213ea281`  
		Last Modified: Thu, 05 Feb 2026 03:20:07 GMT  
		Size: 25.0 MB (24953161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518328709aef2ec161ee90f4be9eea82346936a41f7fadae6c748b8ca89b81be`  
		Last Modified: Fri, 06 Feb 2026 08:00:06 GMT  
		Size: 66.7 MB (66660429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28ec1592820c3222376324edc164b7d4b0135bc729809ee425dd90aa8870aa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420f8217cf75080fdcfe3df1a8fca9698e90fa13b8b4443d114e694061b28b4e`

```dockerfile
```

-	Layers:
	-	`sha256:a9286b63930e3de7fea1e35aced90f1855d76785a92ba7e32a68a4807c4bfcb5`  
		Last Modified: Fri, 06 Feb 2026 07:59:56 GMT  
		Size: 7.8 MB (7757975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d820ac61a190123eafea5d476ff950b199cfad79ff23f8a7278602d28a6db8cc`  
		Last Modified: Fri, 06 Feb 2026 07:59:53 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c3be472e295245f9ca701442a89d716ddee53f6a6276692f1f419992ebdea2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144780131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a99621fba2d7d3b2e4585d90ed1668fb34d234736c77c6d5bcc62dd3794ce2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:53:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9712b896509afe6ce616cc91aa36b272afd379950384122674a69ff7d6929`  
		Last Modified: Tue, 24 Feb 2026 20:59:42 GMT  
		Size: 26.8 MB (26801071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62d9ba5f66f052b2790c9aa6ddd7ff161b24db86972e603be616bc922281de`  
		Last Modified: Tue, 24 Feb 2026 23:54:27 GMT  
		Size: 68.6 MB (68624526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6ae7a023481b7b8f0858052efc2b15756e0c233fb673f3e387d05b930e8ea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e496a8b656d1c848f708a56f33226ced3e8cf77e8eed44df33b7a10c63e1c5ea`

```dockerfile
```

-	Layers:
	-	`sha256:ffbbb43fa35e1c94095ddaf6c32e70825f3f510b9b04e4aa828b5bf8d8748719`  
		Last Modified: Tue, 24 Feb 2026 23:54:25 GMT  
		Size: 7.8 MB (7769050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5db77ea50ebcb2b38fb725d013062a26239ac43d36a941b3bf12f030197a96b`  
		Last Modified: Tue, 24 Feb 2026 23:54:25 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
