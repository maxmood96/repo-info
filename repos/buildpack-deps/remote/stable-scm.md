## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:52d410958c40606e54a342db001264f4669422b9c493b7fc44091fe2cc5797e6
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

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dc535ab0f85a8bd7043d9b849e66693d57cb1716721b906b57903d74dc3df5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142714632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf692cfcd8fea7f0a09380af477f35e8c94f265eda803ec2be09748567065d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd9f7e0f16ee1c17d9a636ffa4f4a869c276dc1bb899deada64afaba45fb4a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393437fdf5608bc7987977dcfaf4dcc24da533a728abced638b7074c0a185adb`

```dockerfile
```

-	Layers:
	-	`sha256:563b17f107cf5ea37cda1f298603ab695c4c764bc85dc0bb983b062c4d806171`  
		Last Modified: Fri, 08 May 2026 20:27:00 GMT  
		Size: 7.8 MB (7768265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18143191ee4a21591882e3aa29e0b4abe0ef78c5b9ef13b28c47b877c66b40f`  
		Last Modified: Fri, 08 May 2026 20:27:00 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:99014823d2080a3af559d226479f373e584d4ba16adb229988f38d91df87dd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137148155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76d0bbbc84167b0a22f29723970c7fbad635b4a81b3642af2072489f5727897`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:57:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab1ea4901b2e5ef4c23bc85e77bccd29b5e37409a6599c547024038487caa48a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2782236aac3a37777665c4737690456903e8f45d5d8a06d88dfd8fdb29da5876`  
		Last Modified: Fri, 08 May 2026 20:57:34 GMT  
		Size: 24.4 MB (24363654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768a28224fae77f3965cdd69933693d2e36af26e730f0f75e576bd8b5e516d41`  
		Last Modified: Fri, 08 May 2026 21:56:37 GMT  
		Size: 65.3 MB (65318209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:02880f7291ebf15bc08c8e5c34ed3d154214bd6bb16d0c8dcf4288d12655371b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef26c0e9f0e6683ccad9bcb6ebb5dacd00b8474b261f19d9be37a6f7fe5125f`

```dockerfile
```

-	Layers:
	-	`sha256:0658e0ef1366f5d8e7f361cb0f6a500437bc6f97fee3872c0798f8b3d333a747`  
		Last Modified: Fri, 08 May 2026 21:56:35 GMT  
		Size: 7.8 MB (7769303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a88a060134f41d086087f17e8f73557ecb1e4f535a6ab7b8af4d8a858eed3c4`  
		Last Modified: Fri, 08 May 2026 21:56:35 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1fe7f29061fecd8e54d9beeaff84f9849a558567dbe114a35c7aa8c63817515a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132102866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f2e190f594d05b97c025e7f80b60b1b481879557c150a34af0267f87c051d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31143502952cbe5df185dc297d98ec2482b596177bb3d2884695855e7091f1`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 23.6 MB (23636413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6753753dc173af6d2d0689a1eccd6337abda3fd742e649454b834a7d6c6afc`  
		Last Modified: Fri, 08 May 2026 21:35:45 GMT  
		Size: 62.7 MB (62728028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:040fdfbff4d7597a4de4a1dcc745d798ea6f899fd8cdc7473a4b01f3caaff1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ba0c433ccddbfe427b0d9e76ec02c63aa08abaa41b9e7aeae531b2b174c6b0`

```dockerfile
```

-	Layers:
	-	`sha256:bc90f722266717e080a0c335899abf19f6139af9b178d10fc2d9089f44db955a`  
		Last Modified: Fri, 08 May 2026 21:35:43 GMT  
		Size: 7.8 MB (7768772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2bbf6a799115797380d572515d79e817eccb3a7bbd397a58dd44bc0ca9a678`  
		Last Modified: Fri, 08 May 2026 21:35:42 GMT  
		Size: 7.6 KB (7647 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:33c5066a134ee1ce60bec99daecea444a476ae820303bbf162f1d606184a5c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142284976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77a2fb5120b15d13a2b98469164d5708afd5a3566160826c7be2d113ed21aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a98260e922b07e1d8dbca1dc72a275470c4825fdb693adf4abc57259be577730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44aa34cce014ebe8faa13cfa3ff35159c58ff69cf4312a964a9a8c20f126cf28`

```dockerfile
```

-	Layers:
	-	`sha256:7e202c9e95beb212024f11f6d26aee982682171f1494c2e06e96858c397851d3`  
		Last Modified: Fri, 08 May 2026 20:32:41 GMT  
		Size: 7.8 MB (7775940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436989bfe83df0252ec93677ad8738ec0f1a4143077e30653eece8656149adc4`  
		Last Modified: Fri, 08 May 2026 20:32:40 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a87bc1d11c2390cb650edfef824f3f9d844c829ce2b67aa2de17fc23c8adf71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147426105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a14ee8eadad8ad44ccc133c1818883b0ac445a963cb8b232e4a05488f233710`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802713bb4712073d4a0875914c45b85ffab64ce3389edccc50bbfe0147fa12db`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 26.8 MB (26784941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3633f2ad7dfa64f7e00b07a5405063f2d661e1f1a5e715c57ad65aaaf0f60d5`  
		Last Modified: Fri, 08 May 2026 23:05:42 GMT  
		Size: 69.8 MB (69815583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dda762da1dc22db33dbda377fa330165e655ce3c42fecacaf1cbc2597483286a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74917a74c401b72d6688e695f00e6ac49d0223730bc33f3fdfd3dc45ee1e2571`

```dockerfile
```

-	Layers:
	-	`sha256:8a722bd871dcb456322956f171e2c13640b6d844930c4b06baf7df27b2d191b7`  
		Last Modified: Fri, 08 May 2026 23:05:40 GMT  
		Size: 7.8 MB (7764399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73d58983ca481e76cac7d01fa54cae523151a271ee518c924230126571107718`  
		Last Modified: Fri, 08 May 2026 23:05:39 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:07a9aeb22a7541b6c18264d14c8d3904bd696d7d108d9bad8b85ac09c7ccd12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153177546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8281861ce42aa545106289fe6d2ef6692dbc013cfda8cf89c38b0e6c6908ac6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e7e07df0234f8192ac6b8d0fa0e09c4847b899e2e0718e39e5caccda09936`  
		Last Modified: Fri, 08 May 2026 22:32:23 GMT  
		Size: 27.0 MB (27014633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227313c51a1419e3870baa3444012fd55dfddc51f3e0064592c73f0b1336a3d0`  
		Last Modified: Sat, 09 May 2026 03:29:25 GMT  
		Size: 73.0 MB (73039748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:964a74ccb0c9c0484b93d4439f6ac1152a58ea8183f1541b71976d484eb9dbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7783005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f743fb35dda46991eef05c6b6a4ae18e7a84063630fa74a54cff0ae4dd1d332`

```dockerfile
```

-	Layers:
	-	`sha256:d96fad5c27f68161a40bf6040c6829fc2a50fb418215af24b86693232ee872ea`  
		Last Modified: Sat, 09 May 2026 03:29:23 GMT  
		Size: 7.8 MB (7775390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f9853f45b5a6e9e853288bc4c1e627b61fe7649b4650b4a976dec6102252eb0`  
		Last Modified: Sat, 09 May 2026 03:29:22 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:55361b68210c1481a36963c9cc8e30d553d7649b76f355a2641ded0c7272202d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139402096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33f8596cea0573b8d5f7b2733f4494e2d810ebdebe863f73410e644e5fa02ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65a6960ab48642ce777aa0804ac70dd6a804024f7f7b2d479b352215d7656bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53aa4e290b570d2c697406000fd0c0ffcc3ef2c1e75ea21ecb99e6656cac45a5`

```dockerfile
```

-	Layers:
	-	`sha256:1233e5e0bf5dec259acbe932a2671f00de815409feb1cd18e37838729366dcb9`  
		Last Modified: Sun, 26 Apr 2026 19:09:52 GMT  
		Size: 7.8 MB (7758103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb471324dfff6d73b9a1665ebc12b955f09ad5dfeb567322d790a27a02bfa526`  
		Last Modified: Sun, 26 Apr 2026 19:09:50 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8217322bfeddf599e5e21662900a9b0f6781c6bee35acb8edc9fc72a29322e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144802768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633e0ac21ea9d640a7352982770210bb99243e26129d56f17ca3450f2da6a265`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0445f3803885031cb22352d4abf0c173876f6316acd6230b59fe9c5654bfec7`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 26.8 MB (26802639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3bbdd2fc257950c611fd6795ac67747b411ad1789b54a283e0cb1bb22d4b2`  
		Last Modified: Fri, 08 May 2026 22:34:34 GMT  
		Size: 68.6 MB (68627825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c6fb7f03cb956f72e0272fc8b1a823fb8abc8a4315d7771f7d89468f00177fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37b89460fb28928d4a95e6cfcb010388a51833933da4683f43212b84bacbb87`

```dockerfile
```

-	Layers:
	-	`sha256:2f29e4afde3358627d691e1afa1c245456f443f90110d597205ef05ad8a0d07c`  
		Last Modified: Fri, 08 May 2026 22:34:33 GMT  
		Size: 7.8 MB (7769178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dd94de26188db42b44e2c8a3175f503b32b9f81a160e25dde1c1da5ba4bf0c`  
		Last Modified: Fri, 08 May 2026 22:34:33 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
