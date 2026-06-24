## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:2d7d7a8420590b9dd5b388c1abf447aec6589ef4e8631ccf3e4b625315fd1c3a
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ceb2d76b9fcbd9258f676552f502fca5c2881676a6a8eac3335d3684499ae5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74952193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832f40bf47d41fe2a4de398aa8175737c221b1557ccd8fba64cfe68b4897469d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c834518a49045cad5b3e493572abed2a8604ab45cc9cb25688e8cb9531f84bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59ce6de8a81e9e25971476047b74827c233cc3d52c61bb63456d566fb79990`

```dockerfile
```

-	Layers:
	-	`sha256:17c4ba7d3317689b932692d233be8a8395cbdc5e8c54192c06199d9edeeb08ae`  
		Last Modified: Wed, 24 Jun 2026 01:41:49 GMT  
		Size: 4.1 MB (4120137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699836a8109e7f8be93b800d6f8c95f8ce0ec9234500f020c164d3496cca197f`  
		Last Modified: Wed, 24 Jun 2026 01:41:49 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7efa231bcaca9fdbc9537ab3888ad9441c0cba0c538d1d049417f8c028894d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71859124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6e1e3abe649f8151fb37a83759e457c357f475097bba1d8f9767d7987c66b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2fe4398658f2e778be1d833b246f06d1ca3a02ebfb12b603474f9f0a15716ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330e92b80a32aaca8bb1c523678ed49ef55db1cb066c602a7e221c450232562b`

```dockerfile
```

-	Layers:
	-	`sha256:6c3504de416a934c2dfb9610974fd6541ab10a0b5357a9a3451858df395f9a07`  
		Last Modified: Thu, 11 Jun 2026 01:21:44 GMT  
		Size: 4.1 MB (4123127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3735fdc37ac8656f04914e812fdde2dbfc26afee6d68b89b4d49cecd7dfbec21`  
		Last Modified: Thu, 11 Jun 2026 01:21:43 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1d7b349391a66bbd5eeb87f8bde6c1eb4a811c8bbc5625ae91db4a13beda64ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69384636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad9a0e9142b73500d0df012a9cb89e8182fb2784bec37d9be8f937fca282236`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:27:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04879054973f6f0ae366a776f1ee6e23a5ae9b6072a5861ec514fdf29f7dbd68`  
		Last Modified: Thu, 11 Jun 2026 01:27:20 GMT  
		Size: 23.6 MB (23635995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38cdc49139e4eb1648f12647f0f2d041ac8208b6bb75a83add7929b8a1a4014f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572efc31822c0327bf7acedec31d122b5b425229acbc90d6deb8c1a11d8fde0d`

```dockerfile
```

-	Layers:
	-	`sha256:51965b94b80afa140c54a2cb13693f6efdc414390e33e286c8e906f594c1bd0c`  
		Last Modified: Thu, 11 Jun 2026 01:27:19 GMT  
		Size: 4.1 MB (4121638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c9a444d032e76a1001a012a961ca052834354d684a3b7d9bbfe2aeed7a9cc0`  
		Last Modified: Thu, 11 Jun 2026 01:27:19 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f0ee60f09b21b397638b844a7e6245842dea632eb64636843bd702abb3a9a266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74705080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a4ce75baa15c0ffea163be8b7c8522ccf09c18f6b5f4aa9d20b7f764c5a4c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f62fb37f3b0346e0b6656f3c22afbda5030fcfa605a2963ab50c12543758ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bca7c103f9effa81136769e3a7585aadce2c8384d002e895f2a14f40f9b018`

```dockerfile
```

-	Layers:
	-	`sha256:e6611d88af4c264de0e7834868d003b5cf284994c5c5876a6634a49cdc035901`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 4.1 MB (4121042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196e58fc654d64241cb8edb9a03d43d09535f276dea9c5cbd1b53a47c6095a5a`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2b5874b11c8cc76eaf8894deff697389de54c5c66270baac995748777e056d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77633059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962dfd1c988258c43606ba6005dd0ec5a16df29dd09b2260b681b7ae1e100373`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ae12c2ff3fb5df23b854f2a97ab858f54bb2f71491a9276fddf8be7e76d3182a`  
		Last Modified: Wed, 24 Jun 2026 00:28:34 GMT  
		Size: 50.8 MB (50835655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429f3d50e84943497f0eadc90e14107210f6f5e2fba29257d54a1c7858400bdf`  
		Last Modified: Wed, 24 Jun 2026 01:44:16 GMT  
		Size: 26.8 MB (26797404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f220d6807ad67c642890266da8975f1fc401b17a884e6bc969a61d703d281ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f584064f44d68ddd3c05698e06fa0ec56c6d30056d3022ba9131afbdec991f`

```dockerfile
```

-	Layers:
	-	`sha256:e44d43909d0b65bb6062b829a08fa71379011f239e9961be692005b3a7eacd7e`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 4.1 MB (4117244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c354c21414166eba7b44e24da885fb46a33d353d01989d0d439796286e15496`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d2f3599516d4b886a99d20fc80764d268624e4735accecbf8e00f7b1f0ed577a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80159916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8103d5309e4c3cf27956ccd018228f925bee7d8c94b3a11055911873cbbb4e71`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c448374e27406af619bc6cafcb8b3bd01537deefacb97de462e65b4f2162938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272bc752da9ed2024e03caf1e54861730b7a4e0de7ca7bc2df46079f0393ebee`

```dockerfile
```

-	Layers:
	-	`sha256:ab76aa9d0e7a43c45d5a94dd96c4a292d66d39b828978facdb3ee98a62390b97`  
		Last Modified: Thu, 11 Jun 2026 04:45:57 GMT  
		Size: 4.1 MB (4123985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d10806b088f1f5c51056503fccbe891e13eb6bdd937dbefd89004e658b04e2f`  
		Last Modified: Thu, 11 Jun 2026 04:45:57 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:365b969027575f776ff9db0696ff4270eea90fdc605ad1ddf1864d4d7f6d9a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72770958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f728dbb92ec5c37e30efd8877ffa257f4f53fb0766a3e2fdd07fc0dc1bd4a75e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 04:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2670e50f22a310111d5d3f90773e6abb3ff490ca41b39d2937a6caa4dbc2b022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc621949f38e2d05945c7c5f44c31277129b7db50596d1db5e09cf2d5a49b17`

```dockerfile
```

-	Layers:
	-	`sha256:9255e92ce4073b47e3683ba5d4972470f3abd2477969ff570d22e71428daf2d4`  
		Last Modified: Sat, 13 Jun 2026 04:46:34 GMT  
		Size: 4.1 MB (4112649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9968ab43651e8ea439af00aa4bbfbbb14df4927cf205f5da3516bc596c56eb7e`  
		Last Modified: Sat, 13 Jun 2026 04:46:33 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:de4d16b3a9f3ee7ca01deb2e3230f1e5bc339257f7f3c06f8d91c0524eb2ce6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76190005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bca96160c6f746f66e3eacac06c4c64ae36313ac4165664b781b4ccfc09056`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26ad8b668881e5b88baa7f13010c93f1bce4021cd7e873db608fc3d64c83f78`  
		Last Modified: Wed, 24 Jun 2026 02:46:45 GMT  
		Size: 26.8 MB (26803945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f514ae6e70e898d094db15f81c9948fc7e4ae7354d79db2ba146aff12393d631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffc84893c41d8bcf2e10089a871de5bde9c3caa5c442ffc9b5d8b4a925ec2e2`

```dockerfile
```

-	Layers:
	-	`sha256:7ca84fa567e81e33a6da09913cb83500c1cc1c44ea229b334852e74c9832a7c6`  
		Last Modified: Wed, 24 Jun 2026 02:46:45 GMT  
		Size: 4.1 MB (4121547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cac083c66bdc7a624a16e62d3ec52b1cabffdc8b2130801c0d2c160ca8bf84`  
		Last Modified: Wed, 24 Jun 2026 02:46:44 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
