## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:6909e877423f189ff78d370ff7016ec10e0c8243357c1cb6d9b8671f281fa551
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:44e163a81bc6db041a7a2bbc59376757920670c16a9d2d833d3379165949d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142418608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839372cedbe40ef80f82daa569d959348e4c63cde36b5b627977bd9b92dea3f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:dba4fa7d8fdc56ce202984a19f0913c41ba64b96758e5cadfe4d2a5d6dd09f29`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 67.5 MB (67516172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89cdc565b8739f20b7638e683a1256d8804ae04fd89c7332f2313206ae7c47bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7609371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fce8b80b78d20ed3c97af649ad0f75a73f3957c529c9f4946fc9e9d2bfdcbc9`

```dockerfile
```

-	Layers:
	-	`sha256:54e4ecffd91b281fbc41d9d07cb24de9cdbd8a174f4639be0c0b8f26a122c7bb`  
		Last Modified: Tue, 25 Feb 2025 03:13:47 GMT  
		Size: 7.6 MB (7602057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:334c83770d86acd2b27953ff5a23186b399bca023fdc48a88ca283f4f6b9aa49`  
		Last Modified: Tue, 25 Feb 2025 03:13:46 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e880624c6dc241604b850a8cef96855202f8a48abc46d611cf70e79dfcc7e077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136349127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d34ac1c32b6ff9467ccf5a5594c9771fb9021215e7ffd7c7389b123a200000b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d17d90b594a7d89931d5de1b198b2dc07a97b965a1b004c4da3948056c117a8d`  
		Last Modified: Tue, 04 Feb 2025 10:23:00 GMT  
		Size: 65.1 MB (65103555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:164785459bb6b6d0f90da7e56eee4d7769da486e2f0fdf3d2526b87780cd6f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40000da731b6ab54e168ce98808313d9c4f419da4bfad48e01858f95acbe9d86`

```dockerfile
```

-	Layers:
	-	`sha256:7323964efa1407c77824afce3e74d3d93019898273512e6e067825cc358be661`  
		Last Modified: Tue, 04 Feb 2025 10:22:58 GMT  
		Size: 7.7 MB (7669362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b489edbda41a57517e3aa2211157756cd4a998ff40b48e2ae2b4ea4082aeeefe`  
		Last Modified: Tue, 04 Feb 2025 10:22:57 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e513acde7b84c4a7e9228b6ea90c139418d56aaa12d452c86cc6249d74221a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131086986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bf2a1a61965add02b229d9d5cc1307795f91c31b1fd315797576bb2bd19936`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:8433f727fdc7ab38c5833ce7296a33e709d29dfcce93ccb57257c21adc2e131d`  
		Last Modified: Wed, 05 Feb 2025 05:01:34 GMT  
		Size: 62.6 MB (62561130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a267e7c4b31372a558677218cc5a45243ba541eaf1e742c2781dd523485dcdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7670326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ab8610e6ae5914d4158922b651eb113a238f50f5b1dd5da0ba55c28565127a`

```dockerfile
```

-	Layers:
	-	`sha256:8c3fd3bc645d8a453df595b6a96a28fa411d55a5b407e6c8fa210c6771ccb811`  
		Last Modified: Wed, 05 Feb 2025 05:01:32 GMT  
		Size: 7.7 MB (7662952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ad9718b29b4cc270e5e6f8e0c7f53229eaca38196aabfcf86e78d7cd162776`  
		Last Modified: Wed, 05 Feb 2025 05:01:31 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ab45a975d43b9b4a09ce9ac0cf70d7564e3b72e31986960848263ca0ed4e3840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141748662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fec4a8cfbaba01c45c98027746f7c57868bcad2b614e4b22080d003a0f6631d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:6f2170d1913f7fa1e873c1ee369893d0954947e899c3a86eb221ad1345da5303`  
		Last Modified: Tue, 04 Feb 2025 19:04:01 GMT  
		Size: 67.5 MB (67509562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4784aed581d4ba642b53141f72e0bc5cdf450e1ac7a62977094c0af6c2326e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542a61bb8ec14d67d25658da6e8eb0d5ad2017ffa972da43c3d0c049810fa543`

```dockerfile
```

-	Layers:
	-	`sha256:6826450555636e9c09ee747de0b48cf260a8593988bddbf93770d4733f043aae`  
		Last Modified: Tue, 04 Feb 2025 19:04:00 GMT  
		Size: 7.7 MB (7670715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c3083b4a0b4e00b87a5408f5574acdd88758f7daa2ef281d12d2d004ae0d8e4`  
		Last Modified: Tue, 04 Feb 2025 19:03:59 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:497bf5ea5bba95da8e1a6824d8e9fe0381cfee2ca50437cd4b67b0ebdaf80949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146811450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee7df1720dc7153fce87bffd9ad4ebbf1e7523ef2c0ba711019229277c76893`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:bfa72fa9c3e348de2475feab504d12e1c7e8277a121ac1989fd7f7c0161b081d`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 69.5 MB (69473471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1289d66403fcd21f1789b22d564275118dc9b0837f627cc9e5f9a2818e760328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c905ea1edffcdea3dfc9fc3f9c0801ecc7c1b5df3446e1d364217ca8ddcc17e2`

```dockerfile
```

-	Layers:
	-	`sha256:49f93d203b27933f1c5e0dc7d94dccd81b2a9974f0d887883aa7bcb818f8ecf4`  
		Last Modified: Tue, 25 Feb 2025 03:13:39 GMT  
		Size: 7.6 MB (7596817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a5a53978b7909c82f4c4260a082cd59bf7f5dae907dfe6a49a45d30eb9ce5b`  
		Last Modified: Tue, 25 Feb 2025 03:13:38 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fcd97ce1b7c33d81268b91ad16e4b3d37035e1e01b976e82635ce4c931b8cf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141205712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fcc883695a9a52db2c54dd3d66eb788f538207e89c63201403d57288985b3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:696ddad714b4d53955dc18a1aeba118edf8c418c35d77183888fcf175b9f62c0`  
		Last Modified: Wed, 05 Feb 2025 03:00:07 GMT  
		Size: 66.6 MB (66627729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:300036d36c1c95da65430010dfe212712ae0df94844559e5c0dc4b77e1ff07d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a1ae45a3009e36fd6585c69b3c68bf64a6eea7b6f76ced28206352ca14cf53`

```dockerfile
```

-	Layers:
	-	`sha256:56f1639889a5a4d7152b1e177d47d9d85ed990ed95754a5db477ff8730af314c`  
		Last Modified: Wed, 05 Feb 2025 03:00:00 GMT  
		Size: 7.1 KB (7146 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:679b62951241ea2742a450ac8165fe34e76793db3e04aec66aaef2e3d5ba8c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152630984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc8305e1f97fa382b682cf34c99767fed202f6691a5d93f96754b1c69b381b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f8f4c2cf61c41cc250d2e87b5eba96ba3e64ef3a295453812dac1f66ba73216`  
		Last Modified: Tue, 04 Feb 2025 01:41:20 GMT  
		Size: 52.1 MB (52139243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7e1fce86863c28c734873936872848b6798972c915ef83ac0ef8757fcc152`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 27.6 MB (27596205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d5b75b14bc48f5cc9ed4250816b6c4c64a25a407024363029abe470236b5c7`  
		Last Modified: Tue, 04 Feb 2025 15:49:45 GMT  
		Size: 72.9 MB (72895536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83b6719e5b27f7dc614ef30d9f7bea83d114cf116d479e72d69850d5f2f456f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7682979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab624ba381a9105d5eea878f88a11cf43a5bf062864d870a6201a4f2aca1e2fc`

```dockerfile
```

-	Layers:
	-	`sha256:7c1d860b795dae0a068fd1a4f4a8765e6b572d07da8315aa1717914a6e9bd1d2`  
		Last Modified: Tue, 04 Feb 2025 15:49:43 GMT  
		Size: 7.7 MB (7675633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4be6b2e6a5745c74fef4344b5733e2a0ac56eb9a344c4d8a8da843615f7998`  
		Last Modified: Tue, 04 Feb 2025 15:49:42 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:841b670efa888fba12f3ca424d021bea46e276c2a406876d2805ebd30661cad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144183374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a538ed29c23de0033afa76c98443583277d7e4f244f6de7b22975a716779870`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371642bbb4f2496e43eaeaa75efac59f54344b0c0beee1184503290cbf7343a`  
		Last Modified: Tue, 04 Feb 2025 11:38:14 GMT  
		Size: 68.6 MB (68552428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b3506d5e6cc98bbe1f6132732531295f20e63be600a8132ce4f9e43c8b7f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099bc7a3a7b814638927fff3374f349bfee6919065f69fbd17ab7afe592ae384`

```dockerfile
```

-	Layers:
	-	`sha256:9c9e3a34680550da80f6d8ed94a748afe42e82068c2fd150cf281d40fa61cba8`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.7 MB (7669509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0d790adc26bb3f35199a82b70f773864a308950b877536a295c0a79358143f`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
