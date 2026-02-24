## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:9337b96777a9604e559a439e32dd42ef7bb6b36ef8796ec7c9afaf91028a5ac5
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
$ docker pull buildpack-deps@sha256:c5c55cd655a8fae099ebc471570380ac70dbc6071eb1a8c4eb4a33c25576ecdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137127956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bb7166728deba532b567265b8bedabc44a23154e7c348ce01ef0afca04d66f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:17:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba31dc65cf53cae37b5517f251f4d408e91109de491cbd8816a9f21c33a05203`  
		Last Modified: Tue, 03 Feb 2026 01:14:09 GMT  
		Size: 47.5 MB (47453997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91afe525ee94a6eec8f0285b6d37bd019b53a0d3e972edf130127870dbcc171e`  
		Last Modified: Tue, 03 Feb 2026 03:26:40 GMT  
		Size: 24.4 MB (24355517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648cbf60fd3bc74c2c5bd50ba637a7b59518c4e57992aeed5e381e96d894fe6e`  
		Last Modified: Tue, 03 Feb 2026 05:17:31 GMT  
		Size: 65.3 MB (65318442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5f026523b38dd8d8d67271d8307b92251767a0ae84b532c212b0be280fed5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f99a263c302837df177a91994283d7c72f5c7d31e295609a21bf63c7d3f01db`

```dockerfile
```

-	Layers:
	-	`sha256:cdf538eed5337c25982de0eebf6745ffdf2de024c80562e4f000ff17dd3aaf54`  
		Last Modified: Tue, 03 Feb 2026 05:17:30 GMT  
		Size: 7.8 MB (7769175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8eda677236205e1833c35968fc08f61c33b7b78fc7981596dc0ae70d7e72a32`  
		Last Modified: Tue, 03 Feb 2026 05:17:29 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8549daf1a1e941fa81a5a86b661a6eb23bacc0dc5adae38ff2b801a868f7c85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132066852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c6db34e411fe8655f5031eb77bc2b5f21a417de771eba6b430e1869fdb3c29`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:01:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e712004ad7e72ac7b512e7e067d08c1f627b7b81a230302cbad4864b08acbdff`  
		Last Modified: Tue, 03 Feb 2026 01:14:45 GMT  
		Size: 45.7 MB (45724966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db74387350d2cb71494f8cd51684a1223fa4d67c2770958430649aa3d99f0d84`  
		Last Modified: Tue, 03 Feb 2026 03:32:37 GMT  
		Size: 23.6 MB (23628323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eaf2b8f43157ee85fb0c9ace18005d09181f51842f1543a4a0e4d1072f633e`  
		Last Modified: Tue, 03 Feb 2026 05:01:35 GMT  
		Size: 62.7 MB (62713563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5c1ae6bfa1d528ec9579008b9b2adeb11df279da6a20561e52e90e47c190243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ac56f766b0b65a62659351e266163cbcc89bd8172917d4f4dc60c28c877685`

```dockerfile
```

-	Layers:
	-	`sha256:927305f03fc29e5ea0a2a8bc8ef5f3ee31b07084d978501dfd64388d637370f6`  
		Last Modified: Tue, 03 Feb 2026 05:01:33 GMT  
		Size: 7.8 MB (7768644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995c8fa5731296690898d55a372fedef03e40518a75135b8459d130ec29a45b3`  
		Last Modified: Tue, 03 Feb 2026 05:01:33 GMT  
		Size: 7.6 KB (7649 bytes)  
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
$ docker pull buildpack-deps@sha256:37236ae03f3a328f47c3ae3f91fc8e64c8a573aabb490ece17dbe25bf067a52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153142473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ccdbe3b593172ba3d997d4b2fa2e801b1cc2bf698cfaab4a9bfaf999ca39f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 10:37:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bdc2ae5f94587ddf291ce56c3dd3c244bdeaf3ba39bf6598fe7a02816ade7e`  
		Last Modified: Tue, 03 Feb 2026 05:24:24 GMT  
		Size: 27.0 MB (26998144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee79ae595ce83805d9060f1c610385dfe6280391251ea73a1f48c7cf8bcb3f09`  
		Last Modified: Tue, 03 Feb 2026 10:38:14 GMT  
		Size: 73.0 MB (73032214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9c88914ec18b09b5c09cc4f5fabf135adad764928d06bb879c2876d1d48bb11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fd8df58da35ad447dcd2624b2862abad08f6e578fd050bf4bb31496c621c9f`

```dockerfile
```

-	Layers:
	-	`sha256:b1fc0f46a74f56f309d54d710e9b626b7c3154afdbc9a17dc187d4375d94dc9e`  
		Last Modified: Tue, 03 Feb 2026 10:38:12 GMT  
		Size: 7.8 MB (7775262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f933f77fc364f36086e1fccfc319f16b8ac91638a7a40a471ffa0063d114aaac`  
		Last Modified: Tue, 03 Feb 2026 10:38:12 GMT  
		Size: 7.6 KB (7614 bytes)  
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
$ docker pull buildpack-deps@sha256:1273ac48e517d3e53cdb6672baf95adb567d8733ae867cc73e84852f71c12db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144772210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588717059e6f395a752b2375a1cb6d5752511b5d5189348b05fbdb1420b89d6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 05:29:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24c0cb82fa1ab6f1887f140586ec94ae060d22e6053b5747ce4acc96547b39`  
		Last Modified: Tue, 03 Feb 2026 03:45:31 GMT  
		Size: 26.8 MB (26794717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec3c6a3ae754d274216ffbec3754da469ace4e7c5b6e8e123969f0516b4a968`  
		Last Modified: Tue, 03 Feb 2026 05:29:44 GMT  
		Size: 68.6 MB (68623115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e1560589c3986e63d5cb16738fe663a91dcadc5c60127bcde34d5d045c9bbdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bb9facd52c9bfddc170fbbeca2cf0899e728de2a767ddd677bcab56e8efa15`

```dockerfile
```

-	Layers:
	-	`sha256:296cf597549da352641e169c8052352ec5eaacd53a4dba74b4269c6e7272b631`  
		Last Modified: Tue, 03 Feb 2026 05:29:42 GMT  
		Size: 7.8 MB (7769050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6903e7b5d9f04544ae90e406c6085e66d899da93f1017ebf0dab9db72f5b5566`  
		Last Modified: Tue, 03 Feb 2026 05:29:42 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json
