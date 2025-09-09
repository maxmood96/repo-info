## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:fc5f8cca7fd8a7573ad085b97ccaed241fae9ff572f612652507cdf583a36760
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
$ docker pull debian@sha256:f33efa2956641cf4a5adc22ed87da1a7b083baa1a8e0a078f1ec4bbe91a59d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03462e65817ac0a0df79e50f72c051e221e4483acc8fd545cbcecb557e71dd8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1ab3b6075b3ed9647a8bfcc838e8f6e3470bae9af09a1e28ad4758aa16d24ad5`  
		Last Modified: Mon, 08 Sep 2025 21:12:40 GMT  
		Size: 48.5 MB (48480609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4377b3e0d39014489c0a5625b068a19cc9a34737bd488de66b1a64ea9e856a`  
		Last Modified: Mon, 08 Sep 2025 22:00:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b8190c2bd0c7904aedc814455a6322a7a58d98933dff973216627bee37d9560d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a008bfe3999ee2ce4dc4c72b6678c8b15e865231eaa36690a696975a23e7e7`

```dockerfile
```

-	Layers:
	-	`sha256:60555522cab3c158d080ff7f2f76f325c4fba18129e4312867d50afcf014470b`  
		Last Modified: Tue, 09 Sep 2025 00:25:26 GMT  
		Size: 3.7 MB (3733433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0612c1bc62317d0b89d71fe5a7324ed436948090b746eb8e3ada06376a946680`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
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
$ docker pull debian@sha256:3349d552d3f10ecb5c0103b659e135b3d57558220913448bcef18144ada7ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16dc425e700fb02b4c1ea1fbd89dbe6f93e0efc106d6127de78f86eab258f315`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f06894cd95e9c473a95f7e79f2c785d9c69285dd7c76790a6f22ce27aab014b6`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 48.4 MB (48359023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6efb03c6f945565b0b038c2d6dca8178c19bf547ccd05319a1495cf6334683`  
		Last Modified: Mon, 08 Sep 2025 21:57:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e19013c288b04821879e5c0b001ef1e4c448aa0787e9c59f9ee94804489ee31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a3fdc391730545fd5f924ffc0366d05ffcdd4576fb96a403ebd45297349f88`

```dockerfile
```

-	Layers:
	-	`sha256:52ea6cdf286f696ebb65c7a87c33362a0deda255755f2398247fe12faa96f434`  
		Last Modified: Tue, 09 Sep 2025 00:25:37 GMT  
		Size: 3.7 MB (3733648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c853553f6068e69caa8fd571a639a4156bda70a9b9a1f7db706a5299d657d28a`  
		Last Modified: Tue, 09 Sep 2025 00:25:38 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:c1b5ca8486fc1f36ce264172a8b55d660b6d6d512f3fde9f89d474ebd0e60e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49466908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d85b7cff8dad00adea92a7242afa92a6e6f37928f624e26bbd935f99fcbdc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:04329fafda35186a3dbe4fb6c5cbeb6fcb4b57f1957e138189f9220815197dfa`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 49.5 MB (49466685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02f76f1ff225d5709740e8e2ddaf302268c5f7841f48a16c6bd17f67a7c1750`  
		Last Modified: Mon, 08 Sep 2025 21:52:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:82c169f1fba05337dcfa3c3c60a2593b2a0e04811c997edb00776cf5ab4c6424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6b2ee932dbb2313120c8b5e46b48e88a3381f284e3b745f6e12382531bccf5`

```dockerfile
```

-	Layers:
	-	`sha256:e687f0ffefb9d49fb1116aca9c43d06681993b8739aa80ebec3510daff33f496`  
		Last Modified: Tue, 09 Sep 2025 00:25:43 GMT  
		Size: 3.7 MB (3730630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb42c2db081009deb5dd104c97bb04420a0754a346b6a46c96c1ef708271c7e`  
		Last Modified: Tue, 09 Sep 2025 00:25:44 GMT  
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
		Last Modified: Mon, 08 Sep 2025 22:09:56 GMT  
		Size: 52.3 MB (52326826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44baf3c7b9e5651e25c281cbe974782cf0148dfc4d6c4b1195921f6295f1d405`  
		Last Modified: Mon, 08 Sep 2025 21:56:08 GMT  
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
		Last Modified: Mon, 08 Sep 2025 22:09:57 GMT  
		Size: 47.1 MB (47137541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8b8ad2bb38ab5732834fd1345ef6d14adbe12bb8765063d0034c4f476956b`  
		Last Modified: Mon, 08 Sep 2025 21:54:40 GMT  
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
