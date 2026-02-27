## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:50719f8be04e1ac05cbdf37cbef91df317f85437530b32267dfaa05445f53624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:forky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bbdcd05cbcadb099d29b70b384937efb6ca34178720d2cce91a3027a108fac90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151771178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709ccd33ec538f278bd87ed597f94b8552c22c8a1a85f54abe03d76c0086f3f5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:501906f379a13fc3675791cbd6304f648074973affcb965be0bef8b0aaa34ab5`  
		Last Modified: Tue, 24 Feb 2026 18:43:03 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812e820910835e26da6ba184eb7321a186fd35437a98105291c93a0a34f38b7`  
		Last Modified: Tue, 24 Feb 2026 19:19:41 GMT  
		Size: 27.2 MB (27222255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36180328906d965e580f744725c6261f12098fe1efe44eeb2da08199e6ee80d0`  
		Last Modified: Tue, 24 Feb 2026 20:04:28 GMT  
		Size: 75.9 MB (75871742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:284dfe32befb9e5e0bd45396d9eb61eee48df66fe0973293e704879c18268756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2c120614b7c301add4f9564afef9ebbd41de9e25cce764bd4b78eb45238933`

```dockerfile
```

-	Layers:
	-	`sha256:3eeb006c0acb6736595965f90f86df4e6a5e2378c08fbe384f077c09b1db7bc0`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 8.3 MB (8270396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3ff422c397de1f8e1e4c6ae93d3f6e79cf1c310c3ad148c45e393ab62a78cc`  
		Last Modified: Tue, 24 Feb 2026 20:04:26 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d972a11d9c49b239c7e4bb737040eedbe457c50ec14073027deffd98194a8731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141025281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5713aed6b09d47c2bc2ef62981d6f92e6983cfc65ea6944414b3247d89719837`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:04:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b74010850dba4ef4e0d65d4c6bda126a2de154bff6afcac42cad46a2cbe16fc5`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 45.7 MB (45653048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2692d078b62360ce66efa48798cce1ada6ffaf0e61c3560fb4e15c2ba9d74`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 24.9 MB (24920360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25208c70da66ab3bb8d85158eb796fdadd82a017ba00747c64f1e57f5bb9ee99`  
		Last Modified: Tue, 24 Feb 2026 21:35:08 GMT  
		Size: 70.5 MB (70451873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:561635dccc7c504b707a32cf1ee6fcc32075d932ef266c1362142466e352decb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496cf8970d3aa4b488b44b3bf645900d8aedb4c24f36e383246c86472c90d36`

```dockerfile
```

-	Layers:
	-	`sha256:25a92df919ea2c70fb20c25be6751f7b315823f8ee5397b8e198dde84b125a78`  
		Last Modified: Tue, 24 Feb 2026 21:35:06 GMT  
		Size: 8.3 MB (8270283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af3698bcb0675b8c2058b91b4b6f5e907aa9ab1b19abf59eb28d55a33a5cf48`  
		Last Modified: Tue, 24 Feb 2026 21:35:05 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:180121acfbba682827f3cbca1c154abcd045d91a268d57e87c9d53d6268d533f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150413929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54fab06d95f023382591c9323456aefb68e4d7a1c69f196b763177d04cb11aa8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:24:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dc3ce43fbcc581a6cb3e0909e03d7e31c0ff1d4d76469e15d6610d1403f2a7e0`  
		Last Modified: Tue, 24 Feb 2026 18:42:39 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa1e5eafe63e2070e8b626137e2f3ba642d42241f716e9259b73098475d4205`  
		Last Modified: Tue, 24 Feb 2026 19:24:42 GMT  
		Size: 26.5 MB (26532448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a430476590752e06253b24b421667dbd99ccf0ed685081b9027c9e6c0c4608`  
		Last Modified: Tue, 24 Feb 2026 20:15:06 GMT  
		Size: 75.2 MB (75176455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:032ba371e57abbc2d85061d07f2c3f3ff2f32c00e1e5bb079b85bd3e52469b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8295799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65034fd9a118a4f6e8e813288a30f0a3867598388eb7e1fbd9248d0bc2d0a46`

```dockerfile
```

-	Layers:
	-	`sha256:fb41628e0b6aa6e9dd883e80511b68239cb1a9914b2f1f5bc87a7a8fe78bb1d9`  
		Last Modified: Tue, 24 Feb 2026 20:15:06 GMT  
		Size: 8.3 MB (8288453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3234d700fbb6a984305464fcbc56a2eacb96642711cfbbe22e0582fd7579ef5`  
		Last Modified: Tue, 24 Feb 2026 20:15:04 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f4e1956f02f6e605ff264cd915304bbda6d77bad4d4027e317949e56cddf9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156381564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f9d07a66054eef19d7ac58711fd0876a39b0ce940d0cb81434b3f39fa7359a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:143f133830d056570eb26009a5886b146c40a6e16bbee60113f54a6baa1643eb`  
		Last Modified: Tue, 24 Feb 2026 18:42:19 GMT  
		Size: 50.0 MB (50011968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9094d4208101e32ebf3f9d4d940d804f0a8bcef435b536316812340ebc9e6f8d`  
		Last Modified: Tue, 24 Feb 2026 19:24:54 GMT  
		Size: 28.5 MB (28495165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00249243cc2c65987ecc868e9f3e1513e31c071138c52e8314c3d36de9f9f3c8`  
		Last Modified: Tue, 24 Feb 2026 19:57:24 GMT  
		Size: 77.9 MB (77874431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b8a38d25b71a8c4bceb108cee6883e006728e55c17d984566f3d08bb851d826e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8273142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20eb35814f80a8b4ea72c5c951abbed9c761ee230e624bb7e85c8c5f27232616`

```dockerfile
```

-	Layers:
	-	`sha256:7fc4cb499a69a1df0241f20eb23b5b8138fc23f5802f2007f2316337ce4ea380`  
		Last Modified: Tue, 24 Feb 2026 19:57:22 GMT  
		Size: 8.3 MB (8265898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89589dbd0f3b8c002aff6c3ad4a63cd9ed1cdac6e761bb799f2e5c092f38ca6b`  
		Last Modified: Tue, 24 Feb 2026 19:57:21 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a468fddccb632d0932f8d79abfcedb597ccde229458a1ef221bebe67e4812468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165098062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8c12188c97d9225146be61ae226d5d43558131149749444b59c6c63f6c266f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 21:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:56:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1e7241652efbb83270036a6221c3c25c51e9feb8307ee3c94f7e0d52832e1af`  
		Last Modified: Tue, 24 Feb 2026 18:42:31 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa31de94cb423730059f9604b4ef3f6954ef0ad086f5d48144efd62317b2c2e`  
		Last Modified: Tue, 24 Feb 2026 21:20:56 GMT  
		Size: 29.5 MB (29513933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930837d0aa6df8d34e08c85803ff9b80030a83f236fe93d9e1ea4d7134b958c3`  
		Last Modified: Wed, 25 Feb 2026 02:57:28 GMT  
		Size: 81.9 MB (81942342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b145104d4a61a071c3a539ffd728a0590994ba0f7b57fd78863f7124b904dcef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8263228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe251df83eefee2c969f47dd375b552f3b9c2730b173702f845cdc18f8462fbf`

```dockerfile
```

-	Layers:
	-	`sha256:bb30ffb78e196e7bca5b1837051a4516217002fe9a9e3a60082e8a712d83e57e`  
		Last Modified: Wed, 25 Feb 2026 02:57:26 GMT  
		Size: 8.3 MB (8255930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4227948ca22c9c01a3c3e6afdc83e26d437148eb3cac4d6ff78cb59b855e0191`  
		Last Modified: Wed, 25 Feb 2026 02:57:25 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:177d05aaafa9818c52d50f4ce5f79f0fe60a8ca82c0dce6342467de520b92525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148067987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e1ebba638edfa65792a52d846ae6a0a5b10b449675ed1a3addfd330ef6c0a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 26 Feb 2026 21:34:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:db31b4401b1ad39bc8394e302320dc063e12e2c0464e6a8103701611daac2f3e`  
		Last Modified: Tue, 24 Feb 2026 18:43:31 GMT  
		Size: 46.9 MB (46914404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ea7a6a4533bb42137b98ae7cf7eb86a1fd6eefe9d713522264d613c05e62`  
		Last Modified: Tue, 24 Feb 2026 19:09:30 GMT  
		Size: 26.8 MB (26774378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebef486f83ee0c702c262a6d5550673a0f1b78368f99bd1ce71d5e966d05ab`  
		Last Modified: Thu, 26 Feb 2026 21:38:15 GMT  
		Size: 74.4 MB (74379205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:469569a06c6787b422b0669dfac0891bb8f7010bd46ef62ba7298573391508ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8266741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46b4ca291fb9babbd8b4dd681d3a5999c65c26b43f852ab628decd4b4de6a4`

```dockerfile
```

-	Layers:
	-	`sha256:601623976dfd0b9f7c1d2ecc337c57ebbe21b2db9bae5a53e8532b4706e4ee24`  
		Last Modified: Thu, 26 Feb 2026 21:38:05 GMT  
		Size: 8.3 MB (8259443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96c2e4e2f376ed6ce03b2d49755ae7d9467563fbf72b70968672be6ba4855960`  
		Last Modified: Thu, 26 Feb 2026 21:38:03 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0304e5ebf534afffd5eb7a51e4335c7585e11f47826a5c6d430333de2942710f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151886623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdbb99c84dfda07733ebc00f41ba8ad27670468f9dd76996f7c51d9913d60fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:57:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f21354992e07f04a7de86938f41ff3c72cb8dc33252e2b2320b4169695270de1`  
		Last Modified: Tue, 24 Feb 2026 18:41:36 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bc3d23a1ad94963e56617c5ddcf27c1a360185386d60459632a29eefc99c91`  
		Last Modified: Tue, 24 Feb 2026 20:58:20 GMT  
		Size: 27.0 MB (27005253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96339ee6032387e57235bad6fbe6a63b35d2154d0ed8853524ee337a527c18b6`  
		Last Modified: Tue, 24 Feb 2026 23:52:57 GMT  
		Size: 76.4 MB (76433018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e0aafd7b0804d174aac8260d986f30b790630a55bc2bb13340ede0d60ee03cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8256940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d02f20cbb97843fa9a642dc1aad7f7cac414bc20413a18a3bc084a0f6b6d7f7`

```dockerfile
```

-	Layers:
	-	`sha256:9fafd6d781857825374bcf123aae3b6ac36c45e94e57a5a82d87610ba4f20db5`  
		Last Modified: Tue, 24 Feb 2026 23:52:55 GMT  
		Size: 8.2 MB (8249674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c5041427821808ebe9a9f460c97a217a5779217b46610c60503540b03fe9ea1`  
		Last Modified: Tue, 24 Feb 2026 23:52:55 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
