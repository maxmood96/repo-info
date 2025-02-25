## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:975954f095443eb0e3fe3cb26909d091bd5f2ec803669991ebb12d124cdc796f
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
$ docker pull buildpack-deps@sha256:085faf4852d3a06b005f51862bbd9f0c30b0bba6db8429b8b47d9003e77fd83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136977710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a9665295970c848b018fb73a3615b492f581cb058461f3df85dcf2728f404`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:5eb7a39b0019bff7c7c84e047f3e1f583a04358b1f598c468c944216bf4311bf`  
		Last Modified: Tue, 25 Feb 2025 08:39:03 GMT  
		Size: 65.1 MB (65143611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee3132e287f680c0b455c0a40a66a1253a39128d15155a7c77fab9ac1afaf0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7615111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad935290c9f2da35cfaa49a2f395f7dcc342590c06b0de2e950bdb8e7eacd12`

```dockerfile
```

-	Layers:
	-	`sha256:7bbdccbc69c5bccfc107e5b15cfd61852285cf2076eff9dae5ef15a755e1572d`  
		Last Modified: Tue, 25 Feb 2025 08:39:01 GMT  
		Size: 7.6 MB (7607737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e1db012da70020b96ad983e6517a8bfae69bf796657e3ad0e7c1b9b4020ed2`  
		Last Modified: Tue, 25 Feb 2025 08:39:00 GMT  
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
$ docker pull buildpack-deps@sha256:489cbcc42cbb74dd81fe59bdefc2602ab482ea86e21e5ee82863081dcc9cba7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152997745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeab6381330afc1eaa6f8cf0c2f305a358c9ecae237dea7eb733b928c4392ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:d0a7bb81cdfac8e52fedda82eb71511b491bce0161320904fa9a6cf3542f360d`  
		Last Modified: Tue, 25 Feb 2025 08:22:16 GMT  
		Size: 72.8 MB (72849870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a0c5ea61bf72445ad603e3f0a919815f04bbf1ec098b1f75a6eae3e7b070b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3410f9541cb3d4948c7c851214e8ed536aa73ea920d4dce4c3e2d20932da42c`

```dockerfile
```

-	Layers:
	-	`sha256:3e79957f795f20fea9bad86264e2f07607f6ac2084ef23e267a1a58f366487dc`  
		Last Modified: Tue, 25 Feb 2025 08:22:14 GMT  
		Size: 7.6 MB (7613978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0091e9531de0f98ba4de3037729168d47136afa5c1cfeffb876dfa25074b25e0`  
		Last Modified: Tue, 25 Feb 2025 08:22:13 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c61c3dc39c2e52c72daf8ccd6c69a419c348681f81fe4cb8db8060e021d253a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144614686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7896e9fabef8e8423d811aa137e1a24768d59f8329bd02dc2dd5d6de3075ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1740355200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:4971e21f8d766abab097575a50fb382c4f9461b5b1c49e9167693254a56cb32e`  
		Last Modified: Tue, 25 Feb 2025 07:19:01 GMT  
		Size: 68.5 MB (68498289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a46a938aa3e1e5c92281b102bed60eb977f596d1b1548f69b6e8fae05cab0e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7615201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd142dd896a56df52a2a52331c58cf7b48c3d93c4c81fbd783a8261578ef2e6b`

```dockerfile
```

-	Layers:
	-	`sha256:579c8c66ee9897cfabbeb5e9f0273feed6544126fbdffb981e284f684a5428a6`  
		Last Modified: Tue, 25 Feb 2025 07:18:59 GMT  
		Size: 7.6 MB (7607888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b6b2cbd496fc93fd247a1f9cfdeb05aa13c82157db1d5ccb3f19dfac78cc87`  
		Last Modified: Tue, 25 Feb 2025 07:18:58 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json
