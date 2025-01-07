## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:a35e10076b4b541856d385f0c319b51b6ba59a8a06e9e4c843b0300b81baae75
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

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7a6e14b21f336650edc3e71d7f25b0b3395c5ccec0b4a161b81c3994a1a69e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72362883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf141798fb0864e026d7947b50d512c71245cbf8234cf56900ea091bf59979c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:78e10cbf9a671667bf7b3d8335e47d06fd1c1ec245b783404cbd6cc55134592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa776e513d8b8d2a8ed6400b0bca15f8574d26db4e717bb1bd25a638b610d582`

```dockerfile
```

-	Layers:
	-	`sha256:58854f5729553ed11b4b4acdcb9e1d4974197f6848542b0ec0095851f527aae0`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 4.4 MB (4359309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a17346ad6f402d6b78f1873712cfbd4e4f3c11982f6d58aadb843ee325276480`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:43c3fe3599693f430f453258da6dfb4563e08ab662f2108a00db62c2ca8b3145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68564708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd72ca462ca719def774c70d2bcba1024af644dc7a5cdf09046aba65ea945d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dacfc4ff8ced481a75baead434c95cce638efbbbf7b92a050c071321bc92c163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4370057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560e22381c6c0c1b31ad0d748210750d1d91bc8473339d0506fe97616aea784b`

```dockerfile
```

-	Layers:
	-	`sha256:8814efa3479cf77453560000df9410c14567d804d1a3a461b16cc68a9639e3d2`  
		Last Modified: Wed, 25 Dec 2024 01:30:38 GMT  
		Size: 4.4 MB (4362825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a324b8ab44626d90be7697e1f13539f06a57658d76836d0d86d5ec2653ed0651`  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0d1125fa1c95fd7fe9121816bda73f7c6bb898dc057fb4e67d347345203fea2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (65967184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6510bf854749e66b7cee14558d88a8b6da3f779cdc465a6ecafb6ef364f706`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d67a17d5a36c000b2191f82e7edae2c6a75b33c8e65471bd2105bb6b28646ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4368838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ab8a5e65f51fa6172b7052d6d5396f6f817d3bcce53bf91846e262957b1ab7`

```dockerfile
```

-	Layers:
	-	`sha256:711af75a51e215dbac7d45c5f18276c8d952d0e5c6e601e565c0ee2dcaf672df`  
		Last Modified: Wed, 25 Dec 2024 03:43:43 GMT  
		Size: 4.4 MB (4361606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f048ee02e32945f1c18564d37520dcc996a12d72b93ece94bc1d02f279b2a3`  
		Last Modified: Wed, 25 Dec 2024 03:43:43 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ca4db2209ddd603e8cebf77bc6506314d5ac7369512119009f41a1380515d9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71731252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404852d15cd1270907bf4352e0334f4339b1ebf671a1093001cd65beee9290b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b238c9cd2f14226485469825b8a3cfa1731f7453f3823d597ac12557aa2656d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9734be0c45caa8cc623aee10ecfe437f263091757e9ae23b920a51576de3704`

```dockerfile
```

-	Layers:
	-	`sha256:a4874f311d120362736c534666909ee974089cd772be5cefff8c1248b23dc6fd`  
		Last Modified: Wed, 25 Dec 2024 01:49:18 GMT  
		Size: 4.4 MB (4359582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5468e18d32057a0d0df379bdfe3d55df236e0d986efbfa384c639f747c5fc091`  
		Last Modified: Wed, 25 Dec 2024 01:49:18 GMT  
		Size: 7.3 KB (7256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b7260ce3f86c4ec2d0521239620c027ec97856b83b32f677f9f58d96d3cffe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74182820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b2de402edc3ccf155210cb8d59c3d471fd5b58e3bf14804915511f6216aca2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ca5ddc166b3a9080f2d317f24aed8b3f9e6d270e829006b0b020ccd094fdcfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4363502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a2de3b1eaff7c31e027084caa49d0a2769a48d2dea4e519a56777dae92aaa3`

```dockerfile
```

-	Layers:
	-	`sha256:c1177544b515ad946b5993d76f99f87518868cb930ec617deb4c7f333ac01bbd`  
		Size: 4.4 MB (4356366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081c0e46ba5dd437f4f05afde3518463673e1fd42af7910cfce86ed4f4afdcbb`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 7.1 KB (7136 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e3f9b9dacad3628747aa99140b12c0d0992105aa4e9fe1fd3e456b85181f3e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72229726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b6eae4818a2a1e2542b4595d96e402a9ca832cd699815be4fc43f9e7a2074`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd8c1e729dacb91e16c49a56e98da090bce02ce17dab8dd89a1c394782c88c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 KB (7006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c242ef0e0fcd3fe5a9949283f243ac4a411329ea195a681d2d335aba196172a`

```dockerfile
```

-	Layers:
	-	`sha256:cddae7c01e0599dd8afd114ce526c5dcaa255b678e983b14114dbbd43aa81fca`  
		Last Modified: Wed, 25 Dec 2024 11:45:54 GMT  
		Size: 7.0 KB (7006 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fb696f71ec0f7fd63dfc7b62c73dc1b9e880e9a07e3becc80659f600bef3c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77851756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb8d58f840661e84a33ba7e0a37302aa9f5a32d3d1af17ea91754de3a89bbcd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee671725fe2eaeae8338c22d56d2be8c639dca084792869aa5ec9dc91ac7b55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4371005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8cfe57f383d4756fe8a9b9bb6c5071270401489bc2422e8492a5750b0f1530`

```dockerfile
```

-	Layers:
	-	`sha256:06b51dd9ca395ea9f7641de19b8f1c18e098cc323dcddec4bf5491352dd711f4`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 4.4 MB (4363803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84cd721456527ca3c47587daeb5fd20f32149ad0c985d1a99784b192a70f350d`  
		Last Modified: Wed, 25 Dec 2024 12:51:21 GMT  
		Size: 7.2 KB (7202 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8f278b562316f2bc7b55f3e08079c81ff017ad09e946a81d5dd6d9f8598230cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71014356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728a0d92d147b0daa2076dbce85d54f7beaa33953499bee0ebce2c99940864d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0bc318236cf578da569ea59b23d5bce3688a76c0f3233eb7456f15f421d327de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4366167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f6b13095d9d2482dc2351c2bbc06549b8407463580d0f007cbe0a36b5425b9`

```dockerfile
```

-	Layers:
	-	`sha256:55b7a088a088661f207e5acf4c7faec66966dd53a109373e4f51a224876fea37`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 4.4 MB (4359005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37810c3e790c3dc0a9f90a1f9803c4946d0d752009844b0baf18aab082363bd5`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 7.2 KB (7162 bytes)  
		MIME: application/vnd.in-toto+json
