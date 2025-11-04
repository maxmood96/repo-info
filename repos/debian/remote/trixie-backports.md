## `debian:trixie-backports`

```console
$ docker pull debian@sha256:9428bf5d4a86ba7f8de621ac924c05d015ed9149a05f7064e8820eeda5fd1da6
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:2fa40b88a264a8b641a6c3fd412a5afc63189435e72d7bcfe13e3fa5b16afd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49285193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0d9645cd575fa08549eaef7f912ec05b93d1fcf7af909a59e7c7aeb0671bc6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a25ba7a779411b04b1fb3889ab8ab6b9094a5abfc7c8f9d1170d661d2c5abc`  
		Last Modified: Tue, 21 Oct 2025 01:16:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c9fca72f05cf70a924f89ca43e051aad380f0881d1db616c908ae9cf2b5d9194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8122c24eb86598c3ba0afd8b776fba42bf5f35cad23129694c8ab9727ae401`

```dockerfile
```

-	Layers:
	-	`sha256:2d8cfbe23c42de41d75b6c4d225c904196be3a4e556bad48495be33e3d87f60e`  
		Last Modified: Tue, 21 Oct 2025 09:25:52 GMT  
		Size: 3.2 MB (3170024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429248c5d31fbe3f6e36606d3d6cb4d49dc4e5fe40aa6c412d02c3175a39b16c`  
		Last Modified: Tue, 21 Oct 2025 09:25:52 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:60d55888d8e12b04ddf4572daeda16b90183c2c7b50f21d22461be2c5a9c4f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47449649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16aa47ff32e218cdfe9530ef2bc6e373c1c34ba34b14c0b0d9878da7a9d70c7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:20:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ece3d43cc91380b968e97ebcb749d1c0cc4d780ea6ab83e3cb6fd3762b28d8b8`  
		Last Modified: Tue, 04 Nov 2025 00:13:14 GMT  
		Size: 47.4 MB (47449426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60968a27b1b9f44b1d699bad6f44ffb91627fdbfbc1929a5b4026723606508c`  
		Last Modified: Tue, 04 Nov 2025 00:20:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bf6f7426b4935102c0333046db77a1178d57aa1d4c0b2196b4a6f06f8f03e0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63063bb5a16e1c4465559c569cdd7d9376a0dbb5de78c77a093efcb04b4f3d36`

```dockerfile
```

-	Layers:
	-	`sha256:e976efd6c04020ef3127d38f85ac55dad20ebe2fe36473b0302ffaa4f311e4bb`  
		Last Modified: Tue, 04 Nov 2025 07:30:03 GMT  
		Size: 3.2 MB (3172961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb7c1b5afa67defd5fa1bf96698b4d4f745d4fbed2b338fd71feef1a163c3e35`  
		Last Modified: Tue, 04 Nov 2025 07:30:04 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6a0eb536fc3bdaa193ddfeabe15d9edeebc283e467f22ebffae94db7da04e50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45716715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940959a16d98976a01745b774e57cd3ffa09f41f9b894d80c902e4e8c4ecff0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827db731198ab7d1b942b2833a22e577589f5802210b7917b4b913b19386ea`  
		Last Modified: Tue, 21 Oct 2025 01:17:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2c231d36857d96f7ae2dc3069531bdb12c9dff444d2b4014ad1de03859a106be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a785aa05287fa6a904ed9038f9c18393126b597c57c64044f0e28a142ced975`

```dockerfile
```

-	Layers:
	-	`sha256:a5a25e48fe25085fa02dc5657f73ba096b85d3562be3e8e88f710747ba9c5acc`  
		Last Modified: Tue, 21 Oct 2025 09:25:59 GMT  
		Size: 3.2 MB (3171398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba840e2ca86d037e1fb926483cb7e295e41d966fee7a58d4a9d37597c768e80b`  
		Last Modified: Tue, 21 Oct 2025 09:26:00 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f3e3ba70851549feb6a60fb181d2b2bde13c69a8362644259f64d37dbdb9e07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49649964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43be5f5633abb875823486313899614ce9f3e2dfba9707ae27157638597fbe5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75e0353c685136614933b10716f79bc4ac8d86af9bb583dc1049b61d58599fb`  
		Last Modified: Tue, 21 Oct 2025 01:16:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0cf11bacdebfc590bd580cf806568fdcd663db500b14ff6519000b5aecb136ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492374775aff86907037dd832c2b08018b86801b207fd49df1f071c6b8e8fb89`

```dockerfile
```

-	Layers:
	-	`sha256:4963da145f9cbe25e8032a4089133667f56bf9b805d139239fe54a96997723ee`  
		Last Modified: Tue, 21 Oct 2025 09:26:04 GMT  
		Size: 3.2 MB (3171505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cbeac2b804cdf7a3d0d998b078de86bf40004ff20433b37ec3485a65581b0df`  
		Last Modified: Tue, 21 Oct 2025 09:26:05 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:aaa0e6f22307928e1399319c82d54aa9f227ce1715762c2f43213cf2ce734f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50800796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d925caf19a39f4c0d6b64d7e79b39baf7b84cbb764bea8e750d8b74365433943`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b279888b1f9d908ea6429ff41746045b023cd1171a3407e61ca980b0409d413`  
		Last Modified: Tue, 21 Oct 2025 01:17:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b21c9cd4ca33db7d3115fe0a6eddbdfed210053a750c746d2ac4e45259b76638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f6e71194f83d73907e95e5b3f572d01c52b54e2f1d39350915cde265a5aca6`

```dockerfile
```

-	Layers:
	-	`sha256:6f6d18408f7df4348a713f82691962957e52a42aa741d70b678ee1204b25709f`  
		Last Modified: Tue, 21 Oct 2025 09:26:09 GMT  
		Size: 3.2 MB (3167227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff698c057228713ad1955a8b6363ca4dc4fe7ec0b431707fd25d231022297fde`  
		Last Modified: Tue, 21 Oct 2025 09:26:10 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f0749b9f09767fe9962e65248a300b291e18a85bece06816328bb92a1854946c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53109698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb77df218c9a280a27d0ddd89bdec90039b51e262a19bb26f413f430b8ff9b7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a97a59d13c31064f55f9380726bb3a16a87007ea2fe0993370dad2f3ae0ab9`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7e5be3ed000229503f8846d66ba09187f973db619b9baa216a213b2ad7683455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f384a4979e92f5cca2f7818f6ee5fd33a2fea710089bd5d02863000f424b0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:59b4902670d95a480ce3ac63437c00e3d61fb10afabfaaf264a0cb0c16f87978`  
		Last Modified: Tue, 21 Oct 2025 03:30:58 GMT  
		Size: 3.2 MB (3173535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060e198a91ec29ca1dd5d57eeb13dd2b4aee7b0b7ff4c27172223f34598faf63`  
		Last Modified: Tue, 21 Oct 2025 03:30:59 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:8840665111a068825beff33e2b3ac106b128afb57db43739e4486897aeee8c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515b77f759a38cd4a7b813413da363f6a1aec5c55771fc811de601815e76dea1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:23:27 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4e1c32ed7d0367c2a3b90b2f374f3f260880d0511aac6a128e163c0850b8bd`  
		Last Modified: Tue, 04 Nov 2025 01:24:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0504c1bcd73f65a037eeea3c611e9b7ce08d061d1584f8328151d7ac54db9d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06087deb4d5c98ec7d4c0463f0cad8aa15ea96e9490fddee320f48470aefd484`

```dockerfile
```

-	Layers:
	-	`sha256:bf622b29889812c52dc7e79b4ddf3214b15148c87bb525874123599c39cb579e`  
		Last Modified: Tue, 04 Nov 2025 07:30:21 GMT  
		Size: 3.2 MB (3162347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1994dc0ac4bb6fded33e3679a6f07dcd674e7933aa02322baacad497959b6b39`  
		Last Modified: Tue, 04 Nov 2025 07:30:22 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:8f12f2bf4552c81969b7b9683b34d4cd08cded335ec473b8eb3e338fcef5bcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49351921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e6f09e6aa520c0657d3abff62092c3c11b979622f97c096425f9319f5b0557`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a7d49607018ddffbdba473375a205197327a8f9b34ee9200e14e47e212f41f`  
		Last Modified: Tue, 21 Oct 2025 01:21:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5a0d3ba22aae96ca737a8db90879881c158cb151a896d03a0a1f2dc897704f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdcd099a9f63bcc44066d543d920574bb0609696649e8b7a17beb4b2cede444`

```dockerfile
```

-	Layers:
	-	`sha256:733aba472fa9c21d2695cf417119f4cc057f53a9066074d7e6dda41989f47105`  
		Last Modified: Tue, 21 Oct 2025 06:25:33 GMT  
		Size: 3.2 MB (3171471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c7b54a453761cc54b032b4af920e02ff6ae1113831c7049efda6425e3e8d31`  
		Last Modified: Tue, 21 Oct 2025 06:25:34 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
