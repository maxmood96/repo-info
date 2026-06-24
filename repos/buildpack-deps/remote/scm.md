## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:8deaefd58c22c4a7afeac2f0ac2055a658e9d4688f8f4dba33e1a9b76c4119b3
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d36aacabea446842b8e0ec061b99b2df639b293fe9eff958506abed5f292b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142730327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a8694fe85673c0f87851bc3724d25178c7c4302fe6a23ce1d2a3caec5ce8a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59c84a786323367a79d4959142649bb24b16c989bbaae7f273550b47325959`  
		Last Modified: Wed, 24 Jun 2026 01:41:50 GMT  
		Size: 25.6 MB (25634938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0db852850114cc79598cc8ab1ec19da54691d9e3267288bb3458d7488f125`  
		Last Modified: Wed, 24 Jun 2026 02:28:58 GMT  
		Size: 67.8 MB (67778134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9fcbb4d59ab7e770af677c214eab60561954cf09cc401bd1840fd7461671ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512c47e87411729ff9f086b1b7ea3d1cef60b20e945c2f3b3ec858816c9003e6`

```dockerfile
```

-	Layers:
	-	`sha256:20cdaa0cce67debd37b02a053619484be17470e8320669de20a64efb0f34168a`  
		Last Modified: Wed, 24 Jun 2026 02:28:57 GMT  
		Size: 7.8 MB (7768523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef04733a3b888e77666ec0533f13158f85f77ff7905914bde8fbb3797727fa8`  
		Last Modified: Wed, 24 Jun 2026 02:28:56 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d5c9ac0c2fd5a0421f714bc3adc4a1352e9267d11ee2e62c2f0103da731234df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137202459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1601c0404fe46aecc9efccc9a027725d09ffd705a7e13fb2570565fc40e4592`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:46:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f4fdc449648c31ec97234c27647662108b2d6bce3fe83032a1af88265bf2ff35`  
		Last Modified: Wed, 10 Jun 2026 23:40:32 GMT  
		Size: 47.5 MB (47494811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3be6b9d9888f84dbe643ff398f469da8712a1ac207b5975f98e812dad9062c`  
		Last Modified: Thu, 11 Jun 2026 01:21:44 GMT  
		Size: 24.4 MB (24364313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8792c8246eb40706682474cfe0f7440cebb3cc0986b9ca229c49e962ffcf1a6`  
		Last Modified: Thu, 11 Jun 2026 02:47:03 GMT  
		Size: 65.3 MB (65343335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:15ba2103e62024a2da4561c161e4da830639db37ed6bd1d18feb0b61c46b389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486bde47b748c981bf3e158214f16269fe4ba8cffc01961bf8866a7ccf33d8e`

```dockerfile
```

-	Layers:
	-	`sha256:5c17cfc0c06677efaa147c8ca47ce4744cbea4460ffafae03d73259b453f080d`  
		Last Modified: Thu, 11 Jun 2026 02:47:01 GMT  
		Size: 7.8 MB (7769561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d62ac269d23ada8f9e50cb7779625c4b32543e462c161381ff9569254cf596`  
		Last Modified: Thu, 11 Jun 2026 02:47:01 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a366e7f75977015507f2d6dbac4cd051bd724c2a9ea20d1a1f85cd4b136b7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132130963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dd211c36a2f49b6b2a10776fa50ed05244b69979a7c41cc515738bf6491b12`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ec13525e08787ad79558c5631e8f1a1fa24a87872974d31cec094e902b73822`  
		Last Modified: Wed, 24 Jun 2026 00:28:39 GMT  
		Size: 45.7 MB (45748717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5391dda58327007b323e3f3d892147e59e5e36215f08b370a235cf10aaf0a`  
		Last Modified: Wed, 24 Jun 2026 02:25:20 GMT  
		Size: 23.6 MB (23635872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0beb5aedec8fb711aa9d2285593f5263bc56957c577c835eda5256d1d6cc6`  
		Last Modified: Wed, 24 Jun 2026 03:55:30 GMT  
		Size: 62.7 MB (62746374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb3f33ebe257fbb7212c43fd06f65eaf815e4aff91933887366fc445dd68bd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dd5e4234ef1f80a69c36cd5d3f98341a0e57bba1b2121747ae745868b11c80`

```dockerfile
```

-	Layers:
	-	`sha256:b50f40026c16b104047fb10677a51ca1c0ef2cf401a28992a1dfaafab3934b97`  
		Last Modified: Wed, 24 Jun 2026 03:55:29 GMT  
		Size: 7.8 MB (7769030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ffda570a1fcaf9f6d65fa0be37156d6d1b86a2d02efe02ede398695da15865`  
		Last Modified: Wed, 24 Jun 2026 03:55:28 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9089ac9faf3f31e2d90c205a1483129a99e963dbb559beb8cea78e0e05c0827f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142297903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2ae9873c3d43a85cf07c9dafe8e2f99b2e40ccb2be2f1ddd8ae4deec8a7ff5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe059c57e3bc40ea8086d6be574927bed6c0a000b182f3354b758009265e197`  
		Last Modified: Wed, 24 Jun 2026 01:45:26 GMT  
		Size: 25.0 MB (25026863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf605f6b62a65326644e598c84134d29702579734c83dfca4cedf5dad7fb6d3`  
		Last Modified: Wed, 24 Jun 2026 02:35:43 GMT  
		Size: 67.6 MB (67592645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4771029b39809c93098699c42dcb614ec1ae06f56d9caee84ebbc67c507149cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcc61fc652aea2e6c86ca1f12f193e3f6cffa17ceca3d179481905bfcbd273c`

```dockerfile
```

-	Layers:
	-	`sha256:d6b23684c988af620b2dcf22ff46268246cc6ee897f7a97bdee2f40d99177756`  
		Last Modified: Wed, 24 Jun 2026 02:35:42 GMT  
		Size: 7.8 MB (7775561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c0940816d309b1393ee8983f6dbdb01abadc4a92517e3221ee53acafceebc6d`  
		Last Modified: Wed, 24 Jun 2026 02:35:41 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4422f366fd4a7c0d27bf02c4fea56bc01dc4d63712e314ca7d10ec432941acd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147456764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc14dc0f98eb6cbd85fbaaef34d31a175e51ce7fed047ba4d088e6198368634`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54ac1ec51d3293c1ade0065529ca23d5fc365d00997ff4e5a290cef3692dc04`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 26.8 MB (26797651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0028665ad759d9a734f0342c043d69fa3d024141c3329c900f163c639953f`  
		Last Modified: Thu, 11 Jun 2026 02:25:16 GMT  
		Size: 69.8 MB (69823550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28f691fbff76b49c2a1f5d7c889adc326ae6ddacc30cbbe3d2a39fa8b22f9800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c66da807796f3ca1f4fbb29f8d3ce50ac0a5e47f6d5494663d8a20c3b02f403`

```dockerfile
```

-	Layers:
	-	`sha256:14dad126a428a8686e85f88154c233a4cb7f1d8db69f25e8ca4892dc33fc7ace`  
		Last Modified: Thu, 11 Jun 2026 02:25:14 GMT  
		Size: 7.8 MB (7764657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa1fd6b16dfe312e5275842c5b380159362ea4fe0d5543f81cd8bb762e0d912`  
		Last Modified: Thu, 11 Jun 2026 02:25:14 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eb01477b3e53622179a49caa5c3b97620f1a094efceabf6a11b2409b5595d87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153210807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae50a2a7a88b48dfaf549cba038e98aa7c2d995271818137659b0a846cf318a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5ae5d968e23911f86d428bf6a67c0599a9449efc6170bd77e591b9eaf7c90d`  
		Last Modified: Thu, 11 Jun 2026 04:45:58 GMT  
		Size: 27.0 MB (27021977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a68ee36453f6ba3cb200c7dbe5182e1d61ba54c525dacec15d40f163304257`  
		Last Modified: Thu, 11 Jun 2026 10:28:58 GMT  
		Size: 73.1 MB (73050891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43b0fa76f8a8ad206ed1b3c062d1474f8d05c07fc2db5cd091ee844552e0eaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946deddb25ef01ea2e097c4fb00fbce8e2caca373143e39075ffffbd4f602855`

```dockerfile
```

-	Layers:
	-	`sha256:7b1de8761113f1a69772cfcd208de87dd0ce6ad68e0a070f19528d56d4e9ce5f`  
		Last Modified: Thu, 11 Jun 2026 10:28:56 GMT  
		Size: 7.8 MB (7775648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1046f4f18fb9ce0bdddb2a892a43ab48c70622d3ffa4861330a4ea0afb64cc0`  
		Last Modified: Thu, 11 Jun 2026 10:28:55 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4de12ed143520668077eafe96906f41abb9a7cae6f11d6b26287f38642da31b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139444371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77ccbd8797e9c19536ea66086ba5f7a5792132476191f73a935663bf97ee452`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 04:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 17:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d828555072267505fd8c01bd511aa2e85b57db4591d7af1c1c5df9ca568aac0`  
		Last Modified: Thu, 11 Jun 2026 02:59:31 GMT  
		Size: 47.8 MB (47802538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d2b568729c379fb90b9e1cebbb6d837dbce6619d04c8fefdbc963a4896afbc`  
		Last Modified: Sat, 13 Jun 2026 04:46:38 GMT  
		Size: 25.0 MB (24968420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa945f549d69516e9a84b82f6960a728d5cfcff0ade0170a3411238a96eb3a92`  
		Last Modified: Sun, 14 Jun 2026 17:09:04 GMT  
		Size: 66.7 MB (66673413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbb8bba7a5ad1eb14e012cf980f96063d539389e91f00ca3804fb9525f6197c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aada8d6c9694db2e7bb2ec72271cad074bc132436d4cf75b0e87214402c5a9e1`

```dockerfile
```

-	Layers:
	-	`sha256:08e0e7579476f0c900d5dfd4ad8f64e40d4a0523fac467e9262e196e0a93645f`  
		Last Modified: Sun, 14 Jun 2026 17:08:55 GMT  
		Size: 7.8 MB (7758361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3d7896796a3c36d4086709406951168b9a2db82f8ab030cdec5ae6952908de`  
		Last Modified: Sun, 14 Jun 2026 17:08:53 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7be60f9372bb12a2dda8515ff36646686f24a22d7f874415ddc9af420591703b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144843163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da4e2355435862ac8d1cf1aabced98cde1cbf607903f5cd0e1589e3e1f7815`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58925113278ed74d68122ff77b22976b064cb872b273063a3ab182209055ee`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 26.8 MB (26803918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c67e4e83aa860c5b719a4e0cc01db908ae525049821b3c459f866ed434f070e`  
		Last Modified: Thu, 11 Jun 2026 03:27:03 GMT  
		Size: 68.7 MB (68653348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9309cc2793723b52685ae0f66a4c08a6f1643f1246930618d09846354fb85af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fcf6cd1aa69354d725962b936960a7955e664978c2df7502f3425071159b5a`

```dockerfile
```

-	Layers:
	-	`sha256:5e156a9c1798d537f120a69f6e7edce33c05ab754ea2bf5f5363a66df08acaad`  
		Last Modified: Thu, 11 Jun 2026 03:27:01 GMT  
		Size: 7.8 MB (7769436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94461a9bf0d6c01685e5efb3905095506a4df1c41257f01f8008f9712fa681f1`  
		Last Modified: Thu, 11 Jun 2026 03:27:01 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
