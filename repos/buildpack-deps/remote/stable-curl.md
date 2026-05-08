## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:4dbed5908764ba81ce3b989f5de67b16f1bcb88741019dff78646495bd492c7e
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f5cf1317dfc446088fd8398addabc67da10dc42f8d25ece6aae6f83ac11b6868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74924545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dd4df12de63984ffd801a8f28bf0c4734a03eaa11a41ee729f08ead389a511`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30be87dd2f96c581cc094e9cf292a574dc11b38db02e2528fc7e38fd3fc1af8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d8e2b6acf03b37620dc90066d461f250fd68f4592199d7c9a9158e5b74c1a1`

```dockerfile
```

-	Layers:
	-	`sha256:3d2b18939cfc39533ea779a8141778424275852a11da46db0d90068159c3b16c`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 4.1 MB (4119951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6929ffc5b64823fc28c4e35cb3b0479abddca247838ca0291c963955754f4cfb`  
		Last Modified: Wed, 22 Apr 2026 01:39:49 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:02a42356cad83656e3a3689dd27f6b7beeeaf556132285d490b7c80f2702d513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71829707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50943218f0d38441eb6f456c32f7f5aad383b0dc2f2a2cfae25de8115d4b564a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2a20d1d425bc7f9412bd28183d8c6af38f835b7563f035cf6476381816d73dd3`  
		Last Modified: Wed, 22 Apr 2026 00:16:22 GMT  
		Size: 47.5 MB (47466106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bd1c760e36c64cea860128e609cb23ecd251d01c38d67fa6179d5cca0da73`  
		Last Modified: Wed, 22 Apr 2026 02:17:34 GMT  
		Size: 24.4 MB (24363601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dfb1c0c896c243354aba227a91751a82d0d48c3a67aff65e9acdbac01608ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c9ab6274dd515e6061eab323cfbf1cacbe032b97c7a7a0f8d55bfaec80fa74`

```dockerfile
```

-	Layers:
	-	`sha256:432fdf6633c197db15439da56f04926f3275cba807c492c5d2375f3282ea8eab`  
		Last Modified: Wed, 22 Apr 2026 02:17:33 GMT  
		Size: 4.1 MB (4122941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5656198f8a4b8a2ab298b046edb5d41995a81ebc6216fd509649c47ef5422f`  
		Last Modified: Wed, 22 Apr 2026 02:17:33 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:776bd60a73a94349ec7680d47b7c9109b17899a9e793c81646bb3da29dc9681e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69374809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eec7299c7f704ef1a788c391ce87983aef059bb672154150ca689b37120d322`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fac7c594bdd032deaa673e94487ba17b8b7fc8297285daafab1d169724391c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79109c0c83452fd6be3efd7d11f7d1542b44925d3db9fdcc387b7e2510b739d9`

```dockerfile
```

-	Layers:
	-	`sha256:f522efff2c7db1fa35a114c75e48928e16d27605384a676ab90e21f0ce6fc593`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 4.1 MB (4121452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b1fd1b206dc62682f9073f3f36cb134dbd4169d59854ad0e2c7d7975238fb4`  
		Last Modified: Wed, 22 Apr 2026 02:19:58 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d7036c90a342109bf3add851e050ef41bcb9e1becb818eaf29c0b3c14de86b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74692921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd7a7604864dc81c1b2a47b98c87e8a1eaf8002668d0169ef06f7e21d175367`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c082919fe4a5042e65713a7cc29c769140673e486308fb73a8330b0a8a379a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa04ab33ee0bc22d2a28d22b9331fac32d0e3c19299a5cdd77e2332974a00013`

```dockerfile
```

-	Layers:
	-	`sha256:d7ff2775a2a14dc8c2a6680dc560ff8101a4c0134b01cf327be6e6e220010db8`  
		Last Modified: Fri, 08 May 2026 19:42:45 GMT  
		Size: 4.1 MB (4121493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5bf9f3cb2a8e4d3ab52bd7348eb26e124298e2149e193c4fd406fd5a965a79`  
		Last Modified: Fri, 08 May 2026 19:42:45 GMT  
		Size: 7.2 KB (7177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:25b49114c429aca32f0481c4c014ec51405899467d683fcdb00645672de0f204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77610192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671195603169df72579a85f5d391dc1c8ad35c71d78bbf36feb52295d8ace885`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321bfd0f3573fe94aa2216d1519cf604989d7a9e912196633f5d9b7a4e8097c`  
		Last Modified: Wed, 22 Apr 2026 01:43:12 GMT  
		Size: 26.8 MB (26784835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b6782dc9a6018c97b99aaf5fd56e2c84f52e5c2feca6da8f9af97cb77e38a757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cce858c7830f576ebffa3d2d534536ad5370f80d4fdb4c0ab7cd72062a631a9`

```dockerfile
```

-	Layers:
	-	`sha256:f2063ffb7cd7f168a83af2cdd34a89a3f0456e69781ca2ddfd845fb1cde16f0b`  
		Last Modified: Wed, 22 Apr 2026 01:43:11 GMT  
		Size: 4.1 MB (4117058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65ed9ee04b9f05d3785f6d54a7d8fc3d543e408e10f7ac78215706ca0792bf0`  
		Last Modified: Wed, 22 Apr 2026 01:43:11 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8b7823741ad9d735cb4cc8db0fcc09ac464a172c171d39153b33e84b016df40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80137600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef48ee29c92ae1cbd7f354101816ee85d731f98d35ada7fc9bcec01cf4997b2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5cfbff82f4b1d183f7002d9a7babd31de37ea7b56514bbb1ddb88df9e84c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5949133b84162d433348e45c8866ece4822e58331c3ac763996a874fac13f1c`

```dockerfile
```

-	Layers:
	-	`sha256:a1907fa5ba009334c683aa2e247eb8322f83af70744dc26201d62259add50f39`  
		Last Modified: Wed, 22 Apr 2026 03:40:50 GMT  
		Size: 4.1 MB (4123799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e0464d419b632e3ad1ea99c02ae1783f598e84807574e8d1f60deee41d315`  
		Last Modified: Wed, 22 Apr 2026 03:40:50 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d7ad0f772b2af14f334f325c107c2b7fde0c27dae27eea33ff48e611dca23034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72754022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5727fdbb39b026f3c82ebf5896bb1327d5a24b2dca9b152e36905a4804af5b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c8811ed40a86b0ccfbafb2d5f038ce8aca3784988dc8b8eb0fcaf79c94c5ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867c042731785db2c25e9c932323c5f01d5d7c16e380d22cc1647fd3e6cfbd5b`

```dockerfile
```

-	Layers:
	-	`sha256:b61ff389cdda027e658bd62ab9de5d621afda176e75670225902e315676b5c65`  
		Last Modified: Sun, 26 Apr 2026 15:22:55 GMT  
		Size: 4.1 MB (4112463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e51a19ed3c9a791ecbd503256d0a8da80ce52b933b317d2881000f26d3b2660`  
		Last Modified: Sun, 26 Apr 2026 15:22:54 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f5d55ce766d35870f9e4300e7cfda7f2396e8a60bfc80b67b53a039f9bdb3f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76174531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18020ae2aeafe6a736eebdb8f016c1241c41846776806a8e2d8104dee2b8b93e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5ac32d9401ac5d551752ea5160b6b5c2c2c552e6c4f397c27bbe383d517d4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128661342c1578bc5a97ba303300975c876f77a7ed3fdb27e05e93b79e2abc4d`

```dockerfile
```

-	Layers:
	-	`sha256:7c7fb1b57c203b82952299cfb36d3ea77d8f8de1e712fbb0670c09aac0bd4f3b`  
		Last Modified: Wed, 22 Apr 2026 02:32:50 GMT  
		Size: 4.1 MB (4121361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460b73a43c64bc4cdf7ab5361c934dc56bdd8e1e50659e7f83034482165085ab`  
		Last Modified: Wed, 22 Apr 2026 02:32:50 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
