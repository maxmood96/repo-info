## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:428cc397904a77b7b699eac0bf5bfbd73707570170743fcb6fa1d89cff45cbe0
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

### `buildpack-deps:testing-curl` - linux; amd64

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8f229be78533695f2b01838c909094820a711d4a9b6da18c9c01d8bb85d7e041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71834099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c34124109b78cf2b6e174aec34114f77e2300c1bbbc37ee87e50c5a79c4e789`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:131ae520a4eaed5ef3f8bfb62695032fc5b0cf09159cb958245abf1bbddef3b8`  
		Last Modified: Tue, 25 Feb 2025 01:33:17 GMT  
		Size: 45.7 MB (45706841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cfbb99d11f866136a1de25d46d555105f60a1f7b061aaf7d89155339ee129`  
		Last Modified: Tue, 25 Feb 2025 05:17:32 GMT  
		Size: 26.1 MB (26127258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:771b1bc7da51b672b9e4b8fb5ff74caf4775ef963f5d20a317dd579cf51f2cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfbc7363dea40509fbd47c84726da57f51935453b4c4fb70e1fab2a885d69be`

```dockerfile
```

-	Layers:
	-	`sha256:c3c7bec1128a438c70d24a30d1717cb462a04c85c8c1466f900c6d4297dc825d`  
		Last Modified: Tue, 25 Feb 2025 05:17:31 GMT  
		Size: 4.0 MB (3990809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c0ed172c31310db2c3124d65aad5ba829d4da5234e93f3d4001644ab0f46e3`  
		Last Modified: Tue, 25 Feb 2025 05:17:30 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8c844b9f3d0cf203e944fa57031c8232be27515e6339cac98bec7134e0b1ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69181570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cc20f04a9f28d645fdbd4a9aeb3f85307e752144294469b6b653040a08462c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1268bec7b6bf92bd5fc4d4120fd51b9bde5a9c50d4b8a8decb59fbe4a53da6fb`  
		Last Modified: Tue, 25 Feb 2025 01:33:55 GMT  
		Size: 43.9 MB (43903193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe307003fac8d59260832b7e5476d782c0d94c51fc746df3d40b574a8cd73406`  
		Last Modified: Tue, 25 Feb 2025 07:18:31 GMT  
		Size: 25.3 MB (25278377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d44c218c94a00152a9a98f11e6561b7a9956ba15903b65df09cc676bfdd9cba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2853be4af73e3581e434f66ef64aadc11fc936331bd025d9ee2968b0dbe29449`

```dockerfile
```

-	Layers:
	-	`sha256:f1788d96e00421b0ceb3ae4c75db7ba3ee286b669e4089847c374a1e35d8a87b`  
		Last Modified: Tue, 25 Feb 2025 07:18:30 GMT  
		Size: 4.0 MB (3983399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420eb896b5f05bf72bb258c5219094d71dc763131f00d66d741d3c906235da4b`  
		Last Modified: Tue, 25 Feb 2025 07:18:30 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:302310fcb56e2ef2e166721c0b1709c36fbd66f6bd03430681d79b0eab01f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74740734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9ccb614d37086a3252f07b50d52f4011406bf9eeffdaf1082d4895dfffab68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4febb367456c7cd84b8043b3b3b3c93073aa9439fb54961fd46a9370758fe523`  
		Last Modified: Tue, 25 Feb 2025 01:33:49 GMT  
		Size: 47.9 MB (47858532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f249b42e8ca4f2ab0a926162c24ad19731e17ebec889633ecab6f0a37257460`  
		Last Modified: Tue, 25 Feb 2025 05:43:15 GMT  
		Size: 26.9 MB (26882202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:01f1ec51610eb6b9c7db1c5d37d823354745c7c3f06ef0db9ef50970679c735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3990978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f495175603d95bc0144f0801a04627c2e831fb811c03474d5abcdf5b3e716ba2`

```dockerfile
```

-	Layers:
	-	`sha256:8169d87f65c15a10837c0e0316d8c54b4d04d20864d1a9939d67e50b5465e4e6`  
		Last Modified: Tue, 25 Feb 2025 05:43:15 GMT  
		Size: 4.0 MB (3984077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535cfbc57e7fa30dc4ae5333fc7fcef55f5ba2f3e55d118903d5a2041dc932ed`  
		Last Modified: Tue, 25 Feb 2025 05:43:14 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; mips64le

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; ppc64le

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; riscv64

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; s390x

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

### `buildpack-deps:testing-curl` - unknown; unknown

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
