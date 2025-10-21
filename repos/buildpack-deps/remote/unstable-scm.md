## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:218d03fbb7d03edad9a4bbf47744db9a01ceedbb0fe4176394209362b93b9bd3
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
$ docker pull buildpack-deps@sha256:8d9e7adb0d6da11b21f4a45b666d435d7f19ff0542343d4969bfecacd68367a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142849847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772c5739057062d7135b49fe5c7a0e04b2a2657ea60b1428be0c40833b2f623b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4775def833a620dde4f1cc169ae067301bfe3a34dcf5509c22eb227d3468f1ec`  
		Last Modified: Mon, 29 Sep 2025 23:36:30 GMT  
		Size: 48.5 MB (48517068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9e4d8c8e300db469e918627e177662d2c9145c896127a833eae485613de801`  
		Last Modified: Tue, 30 Sep 2025 14:02:31 GMT  
		Size: 26.9 MB (26941858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355dcb4e6f8d4305f466d18918201a1d1987966e7ad83941fc93d52a3f5818a5`  
		Last Modified: Tue, 30 Sep 2025 20:30:18 GMT  
		Size: 67.4 MB (67390921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:626b16bf388cd353586efcab02aebed2307e1b3e4d14b38058014404f65c8343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0831a24731a90b23610f617e00478b0a17c81c0eb6e4af78a46de064a606ce`

```dockerfile
```

-	Layers:
	-	`sha256:ed9d6b344ebfcfa31f7a655119adbf9751002d021a6fb3dc4607d371d5231f5c`  
		Last Modified: Wed, 01 Oct 2025 19:20:58 GMT  
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
$ docker pull buildpack-deps@sha256:36ea4018e87900f2c2f46b4a4f43e075c07a731f95892c9565651e5949f8cd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145651201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ba05169c62993c8a27b5e389c11b27851197e3c20c9d91a2ad8a719f0d4d0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d997811a60a9b9144b07fdb085fc1feb6f43f5adf62ec1daf292a386279413a0`  
		Last Modified: Mon, 29 Sep 2025 23:37:26 GMT  
		Size: 48.2 MB (48234517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263fee109e376d69cd8ab45eebe497b85f6bb9dab4d00421e46048f3b05dbc2`  
		Last Modified: Tue, 30 Sep 2025 03:10:36 GMT  
		Size: 28.2 MB (28155087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1c052f36ed7138d27ebb7e300cd8fe66223f9064d8cb89d721192113efa6f0`  
		Last Modified: Sat, 04 Oct 2025 09:22:53 GMT  
		Size: 69.3 MB (69261597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51dace851ea579899ae87626a7f07b318216c47b8a063a387534dc74d137d8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7745343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409df6aa9bb2e21bff6515efeb74cbedafc53773453e5c9798def71f16b5acfc`

```dockerfile
```

-	Layers:
	-	`sha256:d6c39508545d3b4725f80d4150ae87587cbcb2bf2f9d3de52f8b537def3a9802`  
		Last Modified: Wed, 01 Oct 2025 01:30:31 GMT  
		Size: 7.7 MB (7738047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b035baa73b68a360a1cb183da33e8163402c9857155b3e26e40a39a1f50c4ad`  
		Last Modified: Wed, 01 Oct 2025 01:30:31 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
