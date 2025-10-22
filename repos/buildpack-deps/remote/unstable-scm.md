## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:716d50e3e6fbb04f85eab23f8e23d4725d5b6685b599c4d87a73f65b009518cf
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9e3e8988d960341975276d3a1e0370e199857f21bfe869d9dab24a3b5d1b784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144064466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5311a8d625935688122bc49ec76075439ac70b7948ef418b72580787293d36a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:767319f7ad72179f876946bf5b239f862d2d5ad761041b6e449acd3ce4c0bdde`  
		Last Modified: Tue, 21 Oct 2025 00:19:58 GMT  
		Size: 48.4 MB (48383307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0041865733f8eac4afbcf0e7351d1bf685e1d3b536723ebe09dcc7b7f34ad22f`  
		Last Modified: Tue, 21 Oct 2025 01:42:32 GMT  
		Size: 27.2 MB (27187028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd69ffbe16c127e7d3c7174dcb8501cef8b21f4527fd8e5e2b9c2d06b6a1611`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 68.5 MB (68494131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98519d108cf78dc551835f6746b71a0b0237b3e8d7298e6af0492ecff24878a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb524f2f48dd93db459cebe395078d4aea04e138c47ef279881f9fae86d3ab2`

```dockerfile
```

-	Layers:
	-	`sha256:8079f66968d314ba71fbacbfc5ec533f3cb0cf0845f9c139ff41053e8cae586f`  
		Last Modified: Tue, 21 Oct 2025 10:22:27 GMT  
		Size: 7.7 MB (7747083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7be9adaf279298e565524db918e1d244297ba7fcc704b486ed4a58184b9fb952`  
		Last Modified: Tue, 21 Oct 2025 10:22:27 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c223a66ffc590873d4c2bf64d9462b63fdc02febedffdb40e0e452c4f39d358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138318245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58489e8af514d871cd2ead66c3f2e47c1de72e631d749ef51ad0478b27b3ab4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:204bc56c72452e737a2bccff3f4208682016048e825d5ac2bc52dc2c4d4649de`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 46.6 MB (46593513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3882f8d4f2701b8365480052f7e556ff8fd1101d8f1b72e8141c4360f1d695`  
		Last Modified: Tue, 21 Oct 2025 02:32:18 GMT  
		Size: 25.8 MB (25784458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff346c12ee6ee902eef6ce2e57381cdb35b81a53850091071c07fa57c84dbf1`  
		Last Modified: Tue, 21 Oct 2025 03:57:08 GMT  
		Size: 65.9 MB (65940274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aed025f08383477e19bb13b1616d8e380b4f8008e6e2a48258c271c8c9db74ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7755491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18925bbd133c4aa947aa81fa4a42d3e6d55cb5cd5d5dad87c1d63955f6e8e3f6`

```dockerfile
```

-	Layers:
	-	`sha256:896f8033f2d33dc78216ee744bd43184b44ed315910bc776017412ac81d52d6e`  
		Last Modified: Tue, 21 Oct 2025 07:21:40 GMT  
		Size: 7.7 MB (7748130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95dfe831681bafbf943c96341b0477d83e9912e5d29d3d1e389b86ae4489fdb4`  
		Last Modified: Tue, 21 Oct 2025 07:21:41 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:027c29889b9b50812dee3b113d570b0de3df4bcafecacc5f3a15920c81ed5914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133128737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40454afb32c885390447fcf9cf68460a577da9ddf659d80713c1569ad605a4e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d46bd548fc78deefe00dfcd2b559377066496f2d6beb8d1543970d5a2164151e`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 44.9 MB (44911556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ca5d6a8872c7e1682c82eee718887aef134a416249261516f2ddbf348e5bb1`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 24.9 MB (24922039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa63c9ab104c5969f04bb0672948fcd7f46b1680b5c36ee57bb532b455b361`  
		Last Modified: Tue, 21 Oct 2025 04:11:34 GMT  
		Size: 63.3 MB (63295142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72136c9115a0570232c01a21fbb937ae3591a63b8a970685b0a3b461ebecac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e45379e0f1eaab3dbebbd3f2251031dd4acf6f8862615e33b423da0703d7973`

```dockerfile
```

-	Layers:
	-	`sha256:79d3aa1436ea63574a966c1b9d313a57c5aa02d3777220e1bcf9696bf1692e6a`  
		Last Modified: Tue, 21 Oct 2025 07:21:47 GMT  
		Size: 7.7 MB (7747582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a175056fdde3a74733e4a9063b107c3ed50b8dccb84a41ae44b4dbd51a74e17c`  
		Last Modified: Tue, 21 Oct 2025 07:21:48 GMT  
		Size: 7.4 KB (7360 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:41afe5044e15d71c60ee076e61a72670b9babd4d9a21977ef123ce98e966ad0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143148778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6b19d92971504928f3fd4e44a034edadab97d71343aecafac815d1d773eb31`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e43e2837b589215836966b2f88d71f57e2c4d5e8f8cb435d19f6ca010856531d`  
		Last Modified: Tue, 21 Oct 2025 00:21:19 GMT  
		Size: 48.5 MB (48506031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d1d3885aec81341d6c3f13d004d1c421d5225a47b5dd56191da09737f82f78`  
		Last Modified: Tue, 21 Oct 2025 01:46:53 GMT  
		Size: 26.5 MB (26496461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88e1c8c165dfa86647e2df68d9d0101605400d05b4a3fee9701c9bdbcf2caa`  
		Last Modified: Tue, 21 Oct 2025 02:35:29 GMT  
		Size: 68.1 MB (68146286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74aece5f1449379629263c10eb82fe772bbdca5ca384b20dd878887b3d165fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc29f4e6cd8cd053d464352e00e82770b008b6d2ab8b6852eb4d47b83cc1b14`

```dockerfile
```

-	Layers:
	-	`sha256:5f8cdfaf45357952ffb94824e6e05644565eb670c9f83b0639e74aa323850aac`  
		Last Modified: Tue, 21 Oct 2025 10:22:41 GMT  
		Size: 7.8 MB (7754108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e658bd379a909a4a1adf4f498f28b03858946a556b6fb3b31a5a0f1e27c3fa9`  
		Last Modified: Tue, 21 Oct 2025 10:22:42 GMT  
		Size: 7.4 KB (7376 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:de8260a48c7727815c74bc47046c1f872f009b18abd8543ee50b0495b7365e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148502238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f31fcae46e86a44882b9c0cbf4557c16ab22b855b8d9cb7881379e5ee97627`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c10cb3338a430a2ff28907bb8e87eec0d18b9eda310d3dbee0b9f6e1108bcaaa`  
		Last Modified: Tue, 21 Oct 2025 00:21:24 GMT  
		Size: 49.7 MB (49718167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda6499db2a9a6f591335665b50167bb19c3bb91ebb991c34e464fc868a2cca0`  
		Last Modified: Tue, 21 Oct 2025 01:53:31 GMT  
		Size: 28.4 MB (28427634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a7d07fbe9a973112bda41167c09a4493891f62e438b759d8affbcdc6011e39`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 70.4 MB (70356437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59f88588b77f09637eb79c7b26cfe4bcf4ae6e58d49bc81dd3ad7bd96e8cf61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7750508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e9774c35a121f6b8ff7ab4843859ad7d25bdf20af5d53c7244e310530f39fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa8be7af80719f3f0ed7d5f5e44ac1c9dc66013aca47739388a1eeb55895b6a8`  
		Last Modified: Tue, 21 Oct 2025 10:22:47 GMT  
		Size: 7.7 MB (7743233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bacf2fd4f62ccdd0b0171d109d9b53ce7e0f9110255bd417e7719da5bb04fc`  
		Last Modified: Tue, 21 Oct 2025 10:22:49 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f4d4b8efa4d4b7dbd7c4420d03be3b1be7d44f97e4dac84631c42dbf3b7e5ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143100185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2338eb536c70aa05189c527b9df1366ce9175a840efe775da8a001baf2f7a64b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6dd82e8f3bb693d3ab0a24c9bfd56d40d1be2ec87a80a565bb29ebde51d7a8a9`  
		Last Modified: Tue, 21 Oct 2025 00:21:36 GMT  
		Size: 48.6 MB (48586528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ece089fc78cd5e3356fd704455c8030636434bdf37dbc15a1b8e5f08d992f0`  
		Last Modified: Tue, 21 Oct 2025 17:28:53 GMT  
		Size: 27.1 MB (27137104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dac4a728c1c024723307311b4d3c1931b919b823de1d71a9e5a1adf855f73a`  
		Last Modified: Tue, 21 Oct 2025 23:46:40 GMT  
		Size: 67.4 MB (67376553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fafeb8054fc3069cc55e1abd177747640a35a1de7422911b733203557eb6b041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2840010d56154a41d304f6dd1aedd8fa1a390c4d8b9ec4ff931027552bbfd7`

```dockerfile
```

-	Layers:
	-	`sha256:6728e1a30c11a32a867326ac816980c0ba6f9ee23394e6d345099ebdbff40a07`  
		Last Modified: Wed, 22 Oct 2025 01:21:22 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4def7e48853458603f5369a2a26235cc5fd767cdc152c9c3ebb06dc8d103da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155773795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed17b602107891d4a5382e566619c8ae6f8c0624c99efac1ee2d3e0d395efa1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:573dcf794048f7c1a04d7e5caace5a2fd1f7290004272bc4f3dfd960a096f8a9`  
		Last Modified: Tue, 21 Oct 2025 00:23:18 GMT  
		Size: 53.2 MB (53217563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d66ae6d7a7d4ee86e6e6ff963fcaf8df404ad10cfa1d1fd6e312e128f220b4`  
		Last Modified: Tue, 21 Oct 2025 07:45:26 GMT  
		Size: 28.7 MB (28740070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ce499c900f022c6bd64723f2ec0116e5a84c4bbd95c63b9450125c67c0d19d`  
		Last Modified: Tue, 21 Oct 2025 17:34:21 GMT  
		Size: 73.8 MB (73816162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:afa2f0d41dde98874c8d470238f49c95a3ea581cb240b635bc93e400e493cb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c008d05993acbcf791533e742e3d6947682711e7b5ecad7716eb28d9c8d67b9`

```dockerfile
```

-	Layers:
	-	`sha256:7c0514c4f10be6d66100b862442972d340b2146fb67e118559392752392be3ee`  
		Last Modified: Tue, 21 Oct 2025 19:20:58 GMT  
		Size: 7.8 MB (7754180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f12a1361dc05ffc9a19ba219def6c16df3267100094df12430bb46bb3308960`  
		Last Modified: Tue, 21 Oct 2025 19:20:59 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:23f17cd327db62b22a1444b64dc6673d230f782876076f5e031270be4f6fa140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144148398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9667e18ac20a3f26ea4ad13acbcdfa8593f06d7c0fb8942285b3bc9e3a0e5c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5296fd171b043d9adeac427b668a2c333e09261704a2befe2a2593421c6da9fd`  
		Last Modified: Tue, 30 Sep 2025 00:53:09 GMT  
		Size: 46.7 MB (46680971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d995bc0710c59defc3b6e948b5fec04402ad900b4af1204d7420bb8e2736886a`  
		Last Modified: Wed, 01 Oct 2025 18:09:27 GMT  
		Size: 29.3 MB (29334857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5342a4415df6cfdfa16b453bdb12523178508b905f6d7a7425c52c9dbe807e2`  
		Last Modified: Sat, 04 Oct 2025 09:26:31 GMT  
		Size: 68.1 MB (68132570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:deb1f03bfdbed59713bb74f6ea096156ade980096f6ab8264e7d367663621811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7743459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09e357dcac8d89cf8fd1b2c1f9aff86ab444ad6d03c98a2465f046dce42c8f5`

```dockerfile
```

-	Layers:
	-	`sha256:6de0dcec7d3bea8635e2794cf8803d2180fc98608aa87810fe3a7ea4c50ecb60`  
		Last Modified: Sat, 04 Oct 2025 04:20:44 GMT  
		Size: 7.7 MB (7736131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f794f21f54111e248d9c50528f28477c22291c90a0856e240272a5e684b0039`  
		Last Modified: Sat, 04 Oct 2025 04:20:45 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2a932e9d899ba2b008a82a3aff4e57fe1a115faac3a8c6eb51c1ae86307e83fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145818372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1db98cee0a112e6389ca6157c7370c292e13ed345a6d5de5971059c3dc4fff9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bfcdf3c01297eb06b59232529bb37e83cf5e8225551f7278d0bbddf997984733`  
		Last Modified: Tue, 21 Oct 2025 00:24:47 GMT  
		Size: 48.3 MB (48267195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93e1c83200c153fd9fe1cb55ab94175e48e69920e85393ca3619fdc448ac729`  
		Last Modified: Tue, 21 Oct 2025 12:40:44 GMT  
		Size: 28.3 MB (28338908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6410c1ffbf6eee212a1300994f21b930c4c72129d51c06fad2416ce3f8de042`  
		Last Modified: Tue, 21 Oct 2025 23:23:59 GMT  
		Size: 69.2 MB (69212269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7bc7763aa08ffe875c11104253ccc6cd031dce14b4e45343e3594eeb2827fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7755293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d8a0fb228c1115497d867dca6891ac0bc6d2a8e2d5538ba4c346d11219733f`

```dockerfile
```

-	Layers:
	-	`sha256:6d29e2d5dbb05d02273e3a9b02e97efd410c3bf1b4aef3d2c3db187e98d9d99e`  
		Last Modified: Wed, 22 Oct 2025 01:21:36 GMT  
		Size: 7.7 MB (7747996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b850ee6d6076832c0aed7f9f0db8969439ba28b51476df041884956e76a22190`  
		Last Modified: Wed, 22 Oct 2025 01:21:36 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
