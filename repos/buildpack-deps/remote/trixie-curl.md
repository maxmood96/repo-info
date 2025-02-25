## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:7b3930a96806ff2de5393dbd5ff5d9042788602a9d0ed9d79a83d3a66d1b4ea1
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:adae7a92b7ed99b7fe59447b481cda378b86113c71bab227cfd80334998f75f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74902436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add2948489a8673b6769c3d838f75ae98ed1b8368735d0b4376b8efd75c58805`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:692a22a94aa33126be6870a35a1980ffe9de71c0099f51ae704bd57260a9fc1b`  
		Last Modified: Tue, 25 Feb 2025 01:29:54 GMT  
		Size: 47.5 MB (47471280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119cdb265769f912819a0900d5eb7385b02b7a4a1f5220c788c3497c9f3670b0`  
		Last Modified: Tue, 25 Feb 2025 02:12:43 GMT  
		Size: 27.4 MB (27431156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a327c73120a4e726d22b8427227261c75f8d786e078f3044caa8185ac80ecd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ad91001a44920be4e09becec8b90e7c14c0c80d8eddbb486d117161b2a91b5`

```dockerfile
```

-	Layers:
	-	`sha256:1d3f9d41ed657bfafdb1841f8415f09ce335f072cd2a91121fa8f86940e829c6`  
		Last Modified: Tue, 25 Feb 2025 02:12:43 GMT  
		Size: 4.0 MB (3983184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea74f84f57cf47dfcc47f538eacdeffe4bee55a75162b4f5aafba2c49c4d958`  
		Last Modified: Tue, 25 Feb 2025 02:12:43 GMT  
		Size: 6.8 KB (6820 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c8b72309a00c55121660036dc53fc7a55227dd584a370f77d25f8d06e544c915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71245572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c5897d4a1b1f8a5acad55b61b1aac3c28340525f575546f22605ce71a4b008`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3c37ea07ec604ed597239c3e420144e4445ac99f8ebe34ec8d721c622caa657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95d254ad2a5dead6eb395b06930bd6dd081a28e79a3adf074ed155d8dc59799`

```dockerfile
```

-	Layers:
	-	`sha256:008cc661fa77c12a00af319e8adc81a6ad24da66847717769b4f90b93b6dc8e8`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 4.0 MB (4048918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438f772e281905bb522f01575f7ec1286452b5b73198927e065d129b4448a0b9`  
		Last Modified: Tue, 04 Feb 2025 08:04:28 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17ce56187dd8b5bd14eb7c413f6bc63b31f85a987ed03de91f8c44f8f8f4244c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68525856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad6dd9272c626efbc13786e9d52c18d1ea6af09a6ea304e613c00980e7bdb0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e33ebdd9205b4932e0915a58ae82fa3919bb7ba65980ba80c0f55146637007ef`  
		Last Modified: Tue, 04 Feb 2025 01:41:14 GMT  
		Size: 44.6 MB (44632834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b579f9683272f3a08c4aea06231a8e2c1bb0d003cd712e88bfd308809a74d5`  
		Last Modified: Tue, 04 Feb 2025 22:18:45 GMT  
		Size: 23.9 MB (23893022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d895484555f88bfbe6868c65a3b8722a26f16f50b03ebb8bf95e112a52130c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4048393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb28a48d69df1a402726ad788fa4ea4658f7e9ed9a370353466ebe85fe13e8`

```dockerfile
```

-	Layers:
	-	`sha256:b52032a92ac270b2d9c500993ae54800682187997a4344bff92629e9e3c71bc0`  
		Last Modified: Tue, 04 Feb 2025 22:18:44 GMT  
		Size: 4.0 MB (4041512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf59eae7bff5f72e387a4ef57402a8ca24040a76fc27433ee7e3c8efca89134`  
		Last Modified: Tue, 04 Feb 2025 22:18:44 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7680b91d4d72d5fa6e01ad7110a7be2a65c2c1255c7186a6bac50da12d15c650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74239100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410311625c1c975966a96b8c08c37737161d80e4792f19eee2142b7660a3528a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5e40a2b9fe32b2158c946023b700f61f57f567701b6be2e04192bbcc68fb32d`  
		Last Modified: Tue, 04 Feb 2025 01:40:49 GMT  
		Size: 48.7 MB (48735381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7a097e6822ff46406de4794f79cc58a671b1cf4aca2e12e0e5d75f3e88af8`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 25.5 MB (25503719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:303d7512961423b549ecbc3135fa423ffc439df03b4168223325681753f21177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338e85b070ec19c90c8f570a3d068cfe50e05677cc95e41bb216dbc2aca9fcd1`

```dockerfile
```

-	Layers:
	-	`sha256:8da040da9e8301aa2cc9fab27ddedef51e88742ead9e384fd037dccfeeff1449`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 4.0 MB (4042186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad182928bef2359b12df2205d712273972389550d13ce80f836942225a82f170`  
		Last Modified: Tue, 04 Feb 2025 09:01:33 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c2ef78a8a776cf2037d8f3ada92118aad6c2ea2edd5681ddd64a9aaa63cea975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77337979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bb7f10eade60adeeb727d827b9bc92070c50d1b02c823b2f489259f2b0a09c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dcb935698360f1bab29ac55f866f04fa900325b5fd7cc453717787a10e4c3537`  
		Last Modified: Tue, 25 Feb 2025 01:29:53 GMT  
		Size: 48.8 MB (48768687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d32c316fc3ccb64f40c6d0195841a31fb8d71e5cc812824cf157a401090b0a3`  
		Last Modified: Tue, 25 Feb 2025 02:24:52 GMT  
		Size: 28.6 MB (28569292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:110e738d6f4e9896cfbcb88738c1b112c978e347187789f47ff8f7e5c31e0f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5e833023a41d0f181baed5a1f35732bef5047aa5c819b77c58d7658157273c`

```dockerfile
```

-	Layers:
	-	`sha256:3dc2b7ba0db4c7152ff7ce7221e87586e116c2cc8b1b560fb78a2b5914df43ca`  
		Last Modified: Tue, 25 Feb 2025 02:24:52 GMT  
		Size: 4.0 MB (3978947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314e9850ef9a1357236fe47e37b8bcaac5ca51f99f92df334b668ce716f8bc1b`  
		Last Modified: Tue, 25 Feb 2025 02:24:52 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:86412e93445910f1ed1074312e25572705d586496cb7f088b1392e36107ebf2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74577983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a331b214c2c756a4c2af343495e0e4f68416c368b983d1bbd906472fcdefc25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7826127ebc82b4ee7746953f0d6a69270e61dcbbf770239c14d7990a9a75f3f7`  
		Last Modified: Tue, 04 Feb 2025 01:41:04 GMT  
		Size: 48.5 MB (48512402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1db1bb102af1e1e6cc9344b3dc0fe8a2eacb41e418cb6879c409441345ea5e`  
		Last Modified: Tue, 04 Feb 2025 19:29:29 GMT  
		Size: 26.1 MB (26065581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e38a36244521f22a44637e5e6de406bb111f7888062bf17485e8b93821f66683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b04128000a2994fec0c3792d9199ebb1d6edfb0b7810ca105754efe943abb28`

```dockerfile
```

-	Layers:
	-	`sha256:ad5c6179ea903265d77a106dd51ba2c4baaa83660a3702c0df0311e586c1ba20`  
		Last Modified: Tue, 04 Feb 2025 19:29:26 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b1158a1ec6a61db1d9370c72173b789c3416211360bd5679a1b9866a29c8e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80147875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2891972b26f3d78e67d74b03fc14ea53c2f1b650602db0698cfe0251e023a229`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ea3e230c71f31965fdc8d0bdc4e71749c73ddb97789439e708ba01bec0516b7`  
		Last Modified: Tue, 25 Feb 2025 01:34:02 GMT  
		Size: 51.1 MB (51131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136b138a9fbadd117790fd6473b3c1516b6ff1b1b1e5e321ff71f2a2c4c08c6`  
		Last Modified: Tue, 25 Feb 2025 04:34:33 GMT  
		Size: 29.0 MB (29016584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59ab33c6d69ca74e8bada3143400b82227893657d0eac5d97c493f45738d89a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c56668a96d1a0780c777b1d8a2785f652f3f95f8de436baa2d7f5c8b02b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:64800b663f1c764868477f33b530157d92e817dff12f93a144e393fbd6ef29ef`  
		Last Modified: Tue, 25 Feb 2025 04:34:32 GMT  
		Size: 4.0 MB (3991833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4287831e1e8e54dfa2124acebf7438381b568bab05c1f486a703bd4ec377a45`  
		Last Modified: Tue, 25 Feb 2025 04:34:32 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b4bd62d90720ca812632dcbe9dde74a4e0031d715b513f9b7607047cc0276211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72789303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4268f17865cd3790fcf5506b07978e69aa6ac152fa073d81107852bb7bab0ec8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1862047c5c2e3bc8bf387c45c8ffcc794d0fd200d932ca96fa8d4a70b351837e`  
		Last Modified: Tue, 25 Feb 2025 01:39:42 GMT  
		Size: 46.0 MB (46022471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d365975c2dbb4757e9eadc31d85f233c999d8929db74432f77d4f828b44e0bb5`  
		Last Modified: Tue, 25 Feb 2025 02:41:04 GMT  
		Size: 26.8 MB (26766832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7f0e328a775da09940ca894b0e56a9357ab32dab2fb737c07e73e109597121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3981419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb13866a5fdb0a9d1837595169ed337d2c8700636f316c9a0f6dd756bde9ce6`

```dockerfile
```

-	Layers:
	-	`sha256:768f3842113cee1166415fc36319d8b8443bc4155705a7a3af28a6565859fb1a`  
		Last Modified: Tue, 25 Feb 2025 02:41:01 GMT  
		Size: 4.0 MB (3974566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca74a2bb398be2ad0f60c1b7937d35808b5a777407130c50cd076ee21e2434b7`  
		Last Modified: Tue, 25 Feb 2025 02:41:00 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8ed01bc7a03531098cd6f408377c7336a7534f981a488d48a9269483f6f4438e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76116397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82df6e34dc335d3f4a50c408dcc7f52060d439944fa03ca167995d033dcc7212`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab0460cfb129d20515573ff27552b94c41a5822739be2d7bf548df5315225ee2`  
		Last Modified: Tue, 25 Feb 2025 01:34:35 GMT  
		Size: 47.5 MB (47508261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec199ac309750ebc4bdf20cce23eb64ef847d0a7c63d2075c1e80b9a8017dc`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 28.6 MB (28608136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:407eb3c7c939808f061754255cdf557aa1630839f83fd3e8fabc0bc8cb616217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a357f9cc36eb6cde6b9bb8358bd17a1be209a6a36723290add6b2da240775d67`

```dockerfile
```

-	Layers:
	-	`sha256:e1578435a5544e8d5dad9fe4381e1ea273ee66e7c43084d0dee991aaba9d7e41`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 4.0 MB (3989519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46822171c85a53f4d4d3365568c0dcb182a9f73f44777ce529288d81e69faa4f`  
		Last Modified: Tue, 25 Feb 2025 04:05:59 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
