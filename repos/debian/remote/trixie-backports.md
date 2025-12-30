## `debian:trixie-backports`

```console
$ docker pull debian@sha256:39d458a7683476c576e47ea5c9287e71a89535513dd522d6532f4dbca44c7ece
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
$ docker pull debian@sha256:85246919009f6f053a46c35583ebf5c7b449172b8f9ddcd43d556c863996ce08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ec093706d36ae925715abe1c51323fbb1af3c8417e2a0d148b0bad6406a222`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:16:03 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08500c4beaf60fb864d57d5bc896b600ed5f3c23dd424bdb70e7b2a2767bd80`  
		Last Modified: Mon, 29 Dec 2025 23:16:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d1b4b907fc1b6c9e28ce510039a39a74d33fbad6cd5e300866f8f8f4a97ebf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfc4120f0655c4123e5a57b6c1a64e2a8ded3c74470067c5ccd9e0c3cda50e0`

```dockerfile
```

-	Layers:
	-	`sha256:6825f360f4962d88bcb5b0a5d0b39064be150da0cce9ec4ca2e04be943a0b9b9`  
		Last Modified: Tue, 30 Dec 2025 04:28:24 GMT  
		Size: 3.2 MB (3170018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02fc1167ebbf5155683bd11812e12980ecb5824dc24cfd8c09bdbc58e79af621`  
		Last Modified: Tue, 30 Dec 2025 04:28:25 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dd0412afd22880df37138d09cb010afbdb6f90e3ee4aa554f42c46723f1e7235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbf1e9eb9727b6b325aacc7ea035996b351fa2540f1b3ffc5f4b15db35b0192`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:34295e8c92d32055cf38cee5aec380c4d26fb9f87d9d69deffe81403a9d5a203`  
		Last Modified: Mon, 29 Dec 2025 22:26:50 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcde60ca24bfa04ddba01741724ce7fdebc06a0139d17f2170f1df88424446d`  
		Last Modified: Mon, 29 Dec 2025 23:15:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3d1bc5b2bbffb5dc39e4289823a1ffb4cdd7353962b5789017d62288c2c16e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d995e2da2885827ad2178205f91af4dc8c6a52edfb4cdc4a2d9c603c6c36d553`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a15e03e59a5fa59b24b4dd1d4bf69694bf232e644157bc3ee8cb40d78f9b8`  
		Last Modified: Tue, 30 Dec 2025 01:30:53 GMT  
		Size: 3.2 MB (3172955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae86f09e87b2189145d81768126434623ff0ddb6ff086babe44c50aa7418c68`  
		Last Modified: Tue, 30 Dec 2025 01:30:54 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8c2be0ae6941a7f2c675b69a17a472e0c81e3278e697fd859de70680d80b46ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45718540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08aedb1f43421b8e2ec8e27c7cd85956dabc8f8697422b771e7ff6ac4f05de2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74178e82b48751146a91b0f7390384ddea8b02ffff73e6be0922be3fda1ca15e`  
		Last Modified: Mon, 29 Dec 2025 23:15:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bafd9a2db72ee4f686d7ebb7531cc72da34854b9d5baf729536ed04d2d45bfa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b940d67163c672ff4ebee0413f2d832a9e483594e4ca763a8ade98839f224c4`

```dockerfile
```

-	Layers:
	-	`sha256:164a2bb3207cdf203f27cb596dc15428cb04785b4e7a8dc60d6e5516e6994e46`  
		Last Modified: Tue, 30 Dec 2025 04:28:32 GMT  
		Size: 3.2 MB (3171392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29894f0563fe654754294c02304f9ed0d4332985feded1e8fa9fc5a63d8903e4`  
		Last Modified: Tue, 30 Dec 2025 04:28:33 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:dfd3a3e0b23418f36742316e65a8bf896c74a7fdebe978e57becbf69339c444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49650415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fa73197d8bd57bbb0334befd7313de666252d004a4fe7fd95e61dc674e6d16`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:16 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c74822f311cfaf3809cda83d4f47dadcd43961b2c0d5fc7ad2cd2664702c81c`  
		Last Modified: Mon, 29 Dec 2025 23:15:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aacfa55c97d13cadac40d88c1baf0c8423da66852264fe37cbdd9904c8e9ea00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b2ca97aa105eb5afe1260e2efa5cf46954e17082c19d2a279d7b6be0001683`

```dockerfile
```

-	Layers:
	-	`sha256:72e6d2009c1a162fbf80a913ba796f8b6f7b5f2fe39ba8e62ced353d683fda1b`  
		Last Modified: Tue, 30 Dec 2025 04:28:37 GMT  
		Size: 3.2 MB (3171499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0416ab576072b58e4b343c67d8b0088873e1861bcbbc6651fc6cda669113ba6a`  
		Last Modified: Tue, 30 Dec 2025 04:28:37 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:13a810542edf9639c75d080029c02d499d59bee7922df882eadff6f2b512587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50801906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa6d27db95fa5470c44256d48f4494fc4dc3006028c3bf372a66a2daefb4a28`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36700950ecc0fcc7d1a40324a1c20162fb1aef24dec055e0f4039bd6f99f99ee`  
		Last Modified: Mon, 29 Dec 2025 23:15:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c009e5214926e2b07e478996c2579085e9314e918db4adfec271cf1d10d86ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538c3efbe889b2bd8f2f4ff9910967ba88f6ada0a77c8845a8aaad00cd11d58b`

```dockerfile
```

-	Layers:
	-	`sha256:a36556a894a559c216724774235af527468c7adb37ee1d9d7258ae085089d5e0`  
		Last Modified: Tue, 30 Dec 2025 04:28:41 GMT  
		Size: 3.2 MB (3167221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9686abf06c8dbb2fe5649e22d35f4f5e4c40dccb46f1abfde38f826b6e6c02ad`  
		Last Modified: Tue, 30 Dec 2025 04:28:42 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d647ddb5ad4b23fe5747be95b933b5a181033d6ff792bf838b7e86a665330c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53108709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4bc09b13cc09e9bc85b3f609bbebad9faec04f3a391131809fabac87d64f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:14:49 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827d173800c8c264006d9576428bf57718e0719c9d0e01636e5b8f3e49cf0f18`  
		Last Modified: Tue, 30 Dec 2025 02:15:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4dc4aa8e4c72bfe1c74fc8df6617c85b9f8cf149340587b2e11d7791e9173cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17c2881d82cfc4c8fc1c0f49e3b8b2a5ea54a3c7fd289e4c4ac036c2ee42008`

```dockerfile
```

-	Layers:
	-	`sha256:8afc71580f10e87d966840019821c5965203320cdbf5eb7440d3d47fdb05298a`  
		Last Modified: Tue, 30 Dec 2025 04:28:45 GMT  
		Size: 3.2 MB (3173529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3769948495ba16e8c539dfce8756ab1634d0d1c744df98161d271f854bb4ab2`  
		Last Modified: Tue, 30 Dec 2025 04:28:46 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:f8c8ae7f3ed1092856f2016de7d2297f23c331848f79c249d29089536d9b67c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47771379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f633aa4a93060c4a451b79cce657fa2c60ae0b242e6b2d054b4cebdfc259fa3e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:23:46 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6463951be79437202347bcba9b75ba48b1532d07cdae78e10f2d30dd9be7f4`  
		Last Modified: Tue, 30 Dec 2025 01:24:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:634f52b3a92fc01c9a9918d410eb820fcc215aa4a74f8790524343b1f64f95da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f014f8b5b5bd73f083c60ae12e792c96c228d358e1888f8fe4de4783568a80`

```dockerfile
```

-	Layers:
	-	`sha256:bc6ff9ea566692cdaa71a6a47b71a4964190eb57f8aa917dec23d7f38c8e55ed`  
		Last Modified: Tue, 30 Dec 2025 04:28:50 GMT  
		Size: 3.2 MB (3162341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035abc96ab41853180feecf51ad7c0a3eee610a27c6b5fe87b70868e3aa5a9bb`  
		Last Modified: Tue, 30 Dec 2025 04:28:50 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:9232aced68beb2e13adab8fe934d04f0e0ec47457d532973f82de61f2801d4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640bfb75f2558c7adb01aa06c6a85e81b3561f5c9acd61d2dc9094201436554`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 04:13:21 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc00d75bc522835f91d0e75f2b13b72002003ebe21f6d3274821c20e149aef`  
		Last Modified: Tue, 30 Dec 2025 04:13:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5e0619ad8cfdfa7a25d2eb75e6364c7e522f99165cbe0f5057b0a12b664c9ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61aa741f63e3bb80276f9b300e02d562b55d293ffcedbe03aa0297eec4f1a91`

```dockerfile
```

-	Layers:
	-	`sha256:0730e8a36e015b5bd6056130931fe04b7d08b106e841ffe2e5d0ad6a59d7110b`  
		Last Modified: Tue, 30 Dec 2025 07:25:05 GMT  
		Size: 3.2 MB (3171465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b223e409d097ee5246983312b1f7b7ad1b4ea869d677db723c90d7504792a8`  
		Last Modified: Tue, 30 Dec 2025 07:25:06 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
