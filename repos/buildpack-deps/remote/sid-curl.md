## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:db0e4ebd0985e041b5c26f840972822a303e8847975ecf991befb58930b76a88
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:02445c6ac12eac8ab1c5a865ce37ccad682e53baaa75b90a7522d9c09d0d0b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74819291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99038f04dfff9aa3914f6c08299911f41ee99473f5a173cfc4b2964d8f89323e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bed06a94a08dd3ab57138defa88b970b3623c9fee2320decf9cee04925c4045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdd54599d7be8693550c8cf5ac233d7c3e4aa2cd284b347b32575594cb75c41`

```dockerfile
```

-	Layers:
	-	`sha256:849d57ab6a6dc88eabe0f4caba48896b35d533f5d500ea74a8643b5b4c52f995`  
		Last Modified: Mon, 28 Apr 2025 21:55:20 GMT  
		Size: 4.0 MB (3968849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a6adabf62cdce0173076b03710d3323b7e83a4d65705d674c99b7dd2324a33`  
		Last Modified: Mon, 28 Apr 2025 21:55:20 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6210bd50cd8e98d722dd3d3603b621a75f1182fad6a699f14b1a3a4a18390d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71738797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ebac556ae41833b2fe877065204a47479b3b7f815480e8f218fa694068d8de`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:404fd683a770153140d6973002a75f89d6a436af748f330e29e1c3f0ca67e300`  
		Last Modified: Mon, 28 Apr 2025 21:08:23 GMT  
		Size: 47.4 MB (47437736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e0a1e0dfa2983e94d5e01ac25e7f9b86f8206e92fe7aac9b2c5f9a123c36af`  
		Last Modified: Tue, 29 Apr 2025 00:47:07 GMT  
		Size: 24.3 MB (24301061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d14655d7589c8f5af45927cc749b070dc716e117ff53ee75b8437b9f6c9a759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3984618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8a4acb68d5e3b9d06c0597ce23d0ecb33d9c1867f260c8ed80915067c3eb7f`

```dockerfile
```

-	Layers:
	-	`sha256:4f7501c6dba2bf6cb444b0f3d5d8ad9668be814b5b4d7895267da572d4d8f8fe`  
		Last Modified: Tue, 29 Apr 2025 00:47:06 GMT  
		Size: 4.0 MB (3977754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1378a372051e701c5f88a66bb5a0055a03537269f7ed713270359d2becab4201`  
		Last Modified: Tue, 29 Apr 2025 00:47:06 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4557db05f712d0cf1540bc85259cb4a7329ecb2296530738a03977ece3b3d27d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69264997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e6a95fc28a304b497a3c5f17762d199881121ecea7e0e1a9a4d53a9f73506e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c4f09954038071c4b7538cdbfd367f3552df4666eacc240bbf717397e0b9c060`  
		Last Modified: Mon, 28 Apr 2025 21:17:18 GMT  
		Size: 45.7 MB (45690318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea9aa9d3149432dc9bb5c2fe207c68224ef45d2d9f918a0e4d2c3d72b6f2c6`  
		Last Modified: Tue, 29 Apr 2025 03:38:23 GMT  
		Size: 23.6 MB (23574679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2141a93fe55be97db0b32f1d36fc8340962a49f51bfb3c0ac4e6c93b8c51a7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a442ee23de4ca1c427dceac7ea31b1f689feaf9533ac639078e96789df6579f4`

```dockerfile
```

-	Layers:
	-	`sha256:61e72732e798d1b2c396e59f92a9a4848abc0292bd254d03a533136617c51ed7`  
		Last Modified: Tue, 29 Apr 2025 03:38:22 GMT  
		Size: 4.0 MB (3970342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08f666cb487a1ca2694575b601bcd09e8a274de27634476db40be673936ab357`  
		Last Modified: Tue, 29 Apr 2025 03:38:22 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:150b9ddd57715a9ca8af7d728dfb3ac288c553b122296eb52220364a5ab1bb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74576407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee3ca3ef0bd8d93eeb6823b5ac241899bccd82e312896dd8cfd6d6f55ac4ec9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2f619c4109fcbcc024465075840b71159fc76526814180d90bfff14b20db08c`  
		Last Modified: Mon, 28 Apr 2025 21:21:54 GMT  
		Size: 49.6 MB (49618408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ba9361c22f0e29208e6629c0b8872ae776c0157ff0e94dd78175d7d69661ee`  
		Last Modified: Tue, 29 Apr 2025 01:47:44 GMT  
		Size: 25.0 MB (24957999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:01a197efc016f12da2413309a0a0b35f55ea261bad43b422c62089873c560373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9703f8a97eb978932cd88971fe88709b006dedfc21365f150e42ae7d36ba6a`

```dockerfile
```

-	Layers:
	-	`sha256:c40fca45469f4e2106a004455b2eb7f591984208dc576dcfa75cb346485c4de9`  
		Last Modified: Tue, 29 Apr 2025 01:47:43 GMT  
		Size: 4.0 MB (3970379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b38f61ce288f634f6efb3054d1d48aef95d5610bd7875c48ac5e95dff528bf`  
		Last Modified: Tue, 29 Apr 2025 01:47:43 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f1de232033fe84f3e55e6accd8a15b5ad6e281162673dc3286bcdb085af03cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77315747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143bcfc3e9f9ca21ebcf55c4388bb0bcaaec0ca42dca8fc6cd6efbb5d4b68b89`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8893d266103debc8e91708397ee165b1fcb9598d054c081f193374cc8a5c6eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3972691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1963f0a0b73dca4a57d96b72b01af7e426a5d4830de0023e640c71be26b8b59e`

```dockerfile
```

-	Layers:
	-	`sha256:cb386e9cf134120b9e253e860d320afcd1067948b2ef485801997b2c63e093fc`  
		Last Modified: Mon, 28 Apr 2025 21:54:03 GMT  
		Size: 4.0 MB (3965909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e688426533b87a66176bb6049b1992e7e406f35ac0248d14345c156c5519728`  
		Last Modified: Mon, 28 Apr 2025 21:54:03 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4f63631b8122a3c491e666a920312be76cbc4a816fe371b0a14223ef1e010f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75153216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5252bc5c4e2e64ed4ac1b4c6208c215958b8bad10cad810ed68ae21f22e011b5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d206785716d2e915433eb85845aaf9607094981ed3c32854f9401982e23a7af`  
		Last Modified: Mon, 28 Apr 2025 21:11:40 GMT  
		Size: 49.5 MB (49535121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46b0656b2eaf48d740fb0cc28ea93ea835c76c41dc63d12f18a3fd227d3d57`  
		Last Modified: Tue, 29 Apr 2025 12:45:17 GMT  
		Size: 25.6 MB (25618095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1eb22788df5278714410643bcde5c5b8a8a33b2596944feed9a61121a5b12e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8e5ebb05edc6d9e8b9d4d6c47cace35c0362a0925204e3ef15a98d47a75bce`

```dockerfile
```

-	Layers:
	-	`sha256:56a384a3fa31022d2b3ee7cc45e0d48ccb71e0b3e093d0cac7cd2c94fc230ae5`  
		Last Modified: Tue, 29 Apr 2025 12:45:14 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d916505fd9629d53a5ba338e57ce1e055dc1310f11dc3d1ef85701b0465f9473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80038340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26813e88aae6e4da01a654c1721071112914a981436bf000496d3f48cf48e64c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d320c0b02fe20eeef6a5432aed2b294506f621139378d9f899d155d81d1080d`  
		Last Modified: Mon, 28 Apr 2025 21:22:39 GMT  
		Size: 53.1 MB (53078100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e713da9ea3255a6f791030cf59cd9bdead64cd96fffafbed2a4a6fe1aaeb2b4`  
		Last Modified: Tue, 29 Apr 2025 00:38:55 GMT  
		Size: 27.0 MB (26960240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0431bc5585e61cb1d616cf16e59e5c6fffa7fccc7f288e7dceae03311274214d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722c3b01fd5a7b5d42090f25c172ef052d954180666f8924ddaac8fbf4f9289c`

```dockerfile
```

-	Layers:
	-	`sha256:242bb3225b254c8fdf84a87808bbbfa902a63706f72753abdc42c0faa8bfe3f9`  
		Last Modified: Tue, 29 Apr 2025 00:38:55 GMT  
		Size: 4.0 MB (3978746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b2ec3b7d59cab72f07531f7e988a96cec555f4c2313880c70c572c566ee315`  
		Last Modified: Tue, 29 Apr 2025 00:38:54 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c1bcdc1e8a3f78cae50d6998c73334677ca33293c03e0dcf68946d213ac5774a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72627229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605972011265b42e8eee8e790bf098638a1d6ef758ba6ae09742448c33f2e26`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:464dfca8d6ff360a0917bf5abf554df6f43b11903ec16c6334100e345a03a9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8df1cd0fcc6090bf5ea7849115098d1410cddf34c63e1e08d2c3059e1204137`

```dockerfile
```

-	Layers:
	-	`sha256:5f6ad04569bad263598b87a8ac080fefc5b85d89e384c0deabd5de7b69044ffc`  
		Last Modified: Mon, 28 Apr 2025 21:52:57 GMT  
		Size: 4.0 MB (3961483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e2b4e00b3418b1a630b74d5e90ab97950375449e1909c238c33e987bd26e09`  
		Last Modified: Mon, 28 Apr 2025 21:52:56 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:434fd01db843714574c1ddd590bc428c5b90ed6706f1d3a1a5c477b48673bd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76086366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736d62db1c64e5e58ecc01a85c9c8273fd5cc71012e08a30fc723cf0a72da388`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8157e1045a0b1a8c8f6ab28a26ace718f29668344110893144c8a16214d7a54c`  
		Last Modified: Mon, 28 Apr 2025 21:08:48 GMT  
		Size: 49.3 MB (49321224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ff5701e764e061146831a7cbe6697f1a1451a6db3d328a14bf9b0b7aedcd77`  
		Last Modified: Tue, 29 Apr 2025 00:01:55 GMT  
		Size: 26.8 MB (26765142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51e3ffa142a334edfc431355124b766f0bf6c044c82a92c7b2e9210f2cdb8db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c5b4dc5304717fc0cea63e1a32dac034f2612e8da80ed8074d1f03a066188`

```dockerfile
```

-	Layers:
	-	`sha256:77dc4c93eb7b8ac69c0a6c1d32fcdcfccd0972c3fe9024b654fe0df2843631d1`  
		Last Modified: Tue, 29 Apr 2025 00:01:55 GMT  
		Size: 4.0 MB (3976466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59dc934b8186384579de2b8d3d138942425e5fa7ee2641b5818b37f752cb272d`  
		Last Modified: Tue, 29 Apr 2025 00:01:55 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
