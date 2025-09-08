## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:7918998154b9a9305764567478284498bbf87169e00b4fcc3b6c80351c6fde3f
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:499f9636127525ffe27f320a8b60c0908363552019e7da336828e6dab2c499cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48494737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818c6b2340b7a589d80cc44f3e65d144911fd1361aa0fe60ebbe67f191f6d2c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:15e1075366401815a427be6be6b115a78b149e22b7946582c5f0a7294e269390`  
		Last Modified: Tue, 12 Aug 2025 20:44:44 GMT  
		Size: 48.5 MB (48494514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c586e0cd5fb9ad2909165296693a4d6ada6a53fc2e5690aea53cb2e077678b`  
		Last Modified: Tue, 12 Aug 2025 21:10:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0fc69ddfb7d6d9f3db9e0fcc5c7954decf55f2e6a7a182fc3c49b8b00f9ff9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb011744371a396db8fd9d8e106552e2cf4c9200cdaa68c3562729dd8a69f0c4`

```dockerfile
```

-	Layers:
	-	`sha256:314a81701f72f5f9c234b8591f41d46a4636201da7b679867013e494d6d6e96e`  
		Last Modified: Tue, 12 Aug 2025 21:27:01 GMT  
		Size: 3.7 MB (3726840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269404b30605192161ad41a2b06a43ef9880b470f8c3b9de291ff79e3c6909bf`  
		Last Modified: Tue, 12 Aug 2025 21:27:02 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:cbca1ca79f0b2672a3bb909c09a606b60a8da2a5557b82b6cc07deaa024a7122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8087ab35dbbc585de264198d6e8b6502de285e6522d7004dc8a0914de938cd64`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d909cf146b0af6dd17f747fac78ebb1b8630dde04a3c60a9097a59afa9432a42`  
		Last Modified: Mon, 08 Sep 2025 21:14:27 GMT  
		Size: 46.0 MB (46015693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df200dc09d184ae39564dc9838da5212214bd0ed9a9d2b8bd03ff32207de5ec`  
		Last Modified: Mon, 08 Sep 2025 21:30:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7d2128aaef86579fa0690eaa7753d7624625ec951e49b96a2a16682ea86477b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf72ec2ed21ea06a2d0b8d2ef7fd261be02712a0e5cc09e8a3b69a2ecbd3c3c`

```dockerfile
```

-	Layers:
	-	`sha256:539f1890f5692cbfb0f6ed9efec2234a6012c4246cc5e3b32548676d370251f2`  
		Last Modified: Mon, 08 Sep 2025 21:27:33 GMT  
		Size: 3.7 MB (3733634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45cae403be59527d82066e5b0464371d41f1e9df5e7bac619397ed5a33dd5b2f`  
		Last Modified: Mon, 08 Sep 2025 21:27:34 GMT  
		Size: 5.9 KB (5909 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ad7c74db51a83fec81cf56a646fe3ce36fd4a7525a3c1b477b571763c4a02cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e27dd8b7be28bf8241499dbe8006bc82cca387469542209d70a3232ba758aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2a9928d0cc54fc9e24e414daacf4076225fb49ca0a69985946d30a8b9b667e91`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 44.2 MB (44196001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc934b3fc7975dfe11c3fc1f9d2a51de1774e462c03270f93ac86c33f174a760`  
		Last Modified: Mon, 08 Sep 2025 21:28:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cf797023233f11ef071e782b2a2a808536911ce4b991258fcf0bfee3b85e2e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bef905aeef0fceac564b11e4e439085f56b604fc494ea97f0764cf9916a5bf1`

```dockerfile
```

-	Layers:
	-	`sha256:9bae2de71f4c4b1ccaa0c35ff5567e625a554561c6ced4e560a481e706b484b3`  
		Last Modified: Mon, 08 Sep 2025 21:27:39 GMT  
		Size: 3.7 MB (3735612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cf7dc0778efdb082bc97beb7c0b2dc620ba034051f3bf83f252fe853f27c27b`  
		Last Modified: Mon, 08 Sep 2025 21:27:40 GMT  
		Size: 5.9 KB (5908 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:73acd54e9d8781d398c510b89ec01d5227f95d3cda63f3d84d28e45cf9ef8265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48342679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0738b5c104f3d9268898dafe967ac264253d85dae75a3f79650803738c577c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:46528f99331830eb2ca1964fb6d95040b4852af004209ae79084d829595dbee4`  
		Last Modified: Tue, 12 Aug 2025 22:10:02 GMT  
		Size: 48.3 MB (48342454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cb2c954ed97faceb13774788a9ca0a87b0ec09b690b7988fa125d6bebb091c`  
		Last Modified: Wed, 13 Aug 2025 01:49:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3f04d692095de3199ffcd7529440963f6fd3d91d155af84fff9dc4f9cf928036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031ca67156685f610c9f7e69bf370d8e49de1ac0be00f4471f05669b5268d9c7`

```dockerfile
```

-	Layers:
	-	`sha256:3c291f5aa8929cc74beb98180d874f24e5bc4851a1684784f5365fe7abf99fb8`  
		Last Modified: Wed, 13 Aug 2025 03:24:39 GMT  
		Size: 3.7 MB (3727055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d452374ebe3799d6226c89eefc8ed06d96bc849b5569e86b09114964d3172d`  
		Last Modified: Wed, 13 Aug 2025 03:24:39 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:9060d038f2a725e0e2200a4e3fc98e7623554e58c853851acde21995452db11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7638b5e1d1d602ef556d01a1f3e67812350e792c2a79d9893f59bbfcf18e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4eaf9ccee430fafbda7687771994aa99740695510b84578f373620b602e41fcf`  
		Last Modified: Tue, 12 Aug 2025 20:45:04 GMT  
		Size: 49.5 MB (49478124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f629a992fdc5b1ebe9a19b54c41a8b0db10d21ef7296081865b2f55cd2ef587`  
		Last Modified: Tue, 12 Aug 2025 21:10:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7fc24e9f9d207b26faacf9ce676a4fe29c055f5c982781778a8e87b834ff2184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fce5bf5794e6e5144f9e856bf96f88f0723f9573f095755dde772f06e3133e`

```dockerfile
```

-	Layers:
	-	`sha256:3ad313b0273ff7b5c4e4e1a1a126b9fc8a8a1f79c36008c5b5cf9738c69bc58f`  
		Last Modified: Tue, 12 Aug 2025 21:27:24 GMT  
		Size: 3.7 MB (3724042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ebdb6a0638cfb131b24a9318a307c74d4822484f94f8ace88bc4df5cb1bd9d`  
		Last Modified: Tue, 12 Aug 2025 21:27:25 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:4f15a42e2726ccd827cae0454ba1d1836f15dbf75b3e02dbd323409b4667394a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc77bc28b3d776d3375ffa7ae5d959880c2bfa319a3c04215bf6f4cbd31c9047`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:81f02cb4e160fc5084d601458247b571dfaec69d1b71a4cc834d01a34240a7f3`  
		Last Modified: Mon, 08 Sep 2025 21:15:53 GMT  
		Size: 48.8 MB (48760786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e6b37c461307a89959ef4cec716a9be2a779df62c2e15c615318997a633fc7`  
		Last Modified: Mon, 08 Sep 2025 21:28:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:80ad7276e8da8fd8e793144d3cb01eb1cb5d722d21d495257410a099dbd6e89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9b3f549a356bd592fcb166fda947e14bcc2ca8fc2b9879f7f64eefa5945d6a`

```dockerfile
```

-	Layers:
	-	`sha256:dafe196759615598e94e85664d78f920209bfefd69f176dd6d3a3cead2cb78a6`  
		Last Modified: Mon, 08 Sep 2025 21:27:52 GMT  
		Size: 5.7 KB (5676 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2a1501ab91f669fcae4b1315d7920b4678ac35a5ff115db503a3e62560b61190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff38824bca3d28379ea21e40f61f8e239a56db3b95e03e43ca3cfea746527a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f54dcb7e47208f057aa81cf2174295022370015b155688521b2f676c8352333`  
		Last Modified: Mon, 08 Sep 2025 20:36:39 GMT  
		Size: 52.3 MB (52326826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44baf3c7b9e5651e25c281cbe974782cf0148dfc4d6c4b1195921f6295f1d405`  
		Last Modified: Mon, 08 Sep 2025 21:16:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9f3b340d42a18828bd9aa48d1132088fb1eadc91866fa0a0aa4479d830f740e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ae7b4644295c3ec1012ef73bd7fbb755de218f7f4fdc3d8444f19dd55814b3`

```dockerfile
```

-	Layers:
	-	`sha256:4cfbe41513403e8e12c7887f29a1cda601623a3cea446c919f81e300f84a7f06`  
		Last Modified: Mon, 08 Sep 2025 21:27:57 GMT  
		Size: 3.7 MB (3737789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579005768530388868c2a6cd6c559d97597d9577e24bb884e151c43cea01dfc9`  
		Last Modified: Mon, 08 Sep 2025 21:27:59 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:dcadfdd242bc59ad2e12c6f24697e573efcdb3935bed82bae261531db1bd1801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b4a5487584694614f6ad0cf5e9131cd5fdfd31056dd72d0866c6e83d0a02d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b68d43703d2d9af0a719d0682250c51f9ac27e5f246b85caabc56601e893eb90`  
		Last Modified: Mon, 08 Sep 2025 20:36:58 GMT  
		Size: 47.1 MB (47137541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8b8ad2bb38ab5732834fd1345ef6d14adbe12bb8765063d0034c4f476956b`  
		Last Modified: Mon, 08 Sep 2025 21:14:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f1fbbf858d0152647f765179be6e4361251827bd705a636d293b60653c761204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221abbe38b6cfcfb1e40451d82b988bf74fe3074e906b4c188916080b4d0c532`

```dockerfile
```

-	Layers:
	-	`sha256:525247f2edba16f8eeec5f82da21e9a27e268617a945fb6c4d2f3f8ad143c3bc`  
		Last Modified: Mon, 08 Sep 2025 21:28:04 GMT  
		Size: 3.7 MB (3730271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2e106cf47860605e438a081e55fadcfa49f8ea799ac3bae342906d0ca0a436`  
		Last Modified: Mon, 08 Sep 2025 21:28:05 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json
