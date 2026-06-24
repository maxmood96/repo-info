## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:1fe83bd23a7b07700675614ddab4679e106f9d07b57b22b85f15ce3a8ec8b174
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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ba4d5a4e2160345b211ae5aa10dd16b0827ec0310743a9d31bc87c11aa56d230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71859333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725e028f73933c26e77eee2748d0d13db11aa629b5fb774ea81115b6f363cd09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0904cce1afe0c8a47ab4491cfda145d253ca2ea73dc133ce8c90a1475215fe54`  
		Last Modified: Wed, 24 Jun 2026 00:28:15 GMT  
		Size: 47.5 MB (47494964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eaea8159712ba25c96ef93db0fc4f7d8dc3d1df2aeb2cfbb90861e303446027`  
		Last Modified: Wed, 24 Jun 2026 02:19:32 GMT  
		Size: 24.4 MB (24364369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec7071a8a5b7c30204707ef654e8907d52c65eab9066cd63a6bf5a6ee03de2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c64856888c92dac5f803e6d03ce31c2245067a641bee1ea9a0c999b221339f`

```dockerfile
```

-	Layers:
	-	`sha256:0f4ce58556a01c271053df1b4c329866776c287393e10474654cf19b60db73ab`  
		Last Modified: Wed, 24 Jun 2026 02:19:32 GMT  
		Size: 4.1 MB (4123127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c53bc3653d86ea3096ee4c994fd8bb6a520ee7b0ed4435702c0664df4381d09`  
		Last Modified: Wed, 24 Jun 2026 02:19:32 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:716e7999e82deca537ef5c24ad02d65e2afbf91bf827158a46f9e262ec5c4146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69384589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5ddf2fbe301815782d27bd9ebfcdc4dde6e42747b9d19691b90e06c0655bdc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9464e40e694b52e0301b7a2cd7e049fd292bf0826158ee4ca357cc01b05764c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da900e9dd381c962fcd0404fed327d87172d8c00e9d6fc8078c8a8e46da8b023`

```dockerfile
```

-	Layers:
	-	`sha256:054306fa85f4bfed94c791c58c32574f9149cac0744a21a9ed9577b09da6180e`  
		Last Modified: Wed, 24 Jun 2026 02:25:20 GMT  
		Size: 4.1 MB (4121638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1be8f6bf675c463844264b851239b92ee568dccd471a94359c2e33aadfe586d`  
		Last Modified: Wed, 24 Jun 2026 02:25:19 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce1c5994300b708ab1704d11b4a16505d0d38ae034290baa1e8a449faa54c294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74705258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3418489b3b1bb78ffbff67964352c327d230d2fabab5d866692900f9ecfa0fc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c5db37e38a17339e815947e2c667196d88fa0b9756fa4c4b5b0af6b4d776de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5823ebe368905880ae52aeebc02b580e4628cead96c454c517d686b29da4b8`

```dockerfile
```

-	Layers:
	-	`sha256:5f84623c76f14b406675a0d140176e3d58ad2cebf9531e9602a4f400be667f67`  
		Last Modified: Wed, 24 Jun 2026 01:45:25 GMT  
		Size: 4.1 MB (4121042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b1389da88e4d374548e0a44ff9c328b02e57eccbc21a5820623e7f37db559e`  
		Last Modified: Wed, 24 Jun 2026 01:45:25 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; ppc64le

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; riscv64

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; s390x

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

### `buildpack-deps:stable-curl` - unknown; unknown

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
