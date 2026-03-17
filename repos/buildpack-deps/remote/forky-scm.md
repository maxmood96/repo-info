## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:f53f5b12767ae77a8477b2bffc56e9f240a0b37b5c8544f8ff9544d8078eece8
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
$ docker pull buildpack-deps@sha256:f742f40beeba07b19126787ac7e823eadbc9f0578bb0f913dabaa2a9716b5dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151621022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6971c28514ffb6d1065857ba217f4430719fb8affacabf85b2df5686bdfced`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544a38ddd1390105762bdf349d1e32b7cf1a9f82dddf930c31b8042b03c6965`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 27.0 MB (27048499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60232b2b35a4cd7a3c869ce028715219f655956cb40f5462e6fb4439cc2e05f3`  
		Last Modified: Mon, 16 Mar 2026 23:25:44 GMT  
		Size: 75.9 MB (75947432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83a6819866723aa7c8e6b70a5ba0bc5137ae1bd8f3b802042103d5439e3834b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b4d3b117e8a3632ca482f716d5c3b24a6753e9a66b6d4dfc24f5030faf4c18`

```dockerfile
```

-	Layers:
	-	`sha256:f410d640d0c920269a7ca463d1ea2081b7181ce906abbbb66c08d7a1523c2cf2`  
		Last Modified: Mon, 16 Mar 2026 23:25:42 GMT  
		Size: 8.2 MB (8221986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4f1e2e050f19ea36145674240003d759a0fb30bb39cad40083f6ecf1a1e781`  
		Last Modified: Mon, 16 Mar 2026 23:25:42 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ddc5b616ac0ad49cb68ecf89665731a2afb054368faade0412d881a3b375351b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140805894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56793671a9fa9684277b6a619058c9ec37b2a70a28b396d1ad81e8c49c1d4194`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 23:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e808829cfe5315cd67981f1a90877f9ceed482400b0f64a9a61a5068bf2e2381`  
		Last Modified: Mon, 16 Mar 2026 21:53:22 GMT  
		Size: 45.6 MB (45555225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3a3183174d50dae2f383480aa0bee03715dc30a220abfb476587db07c5672`  
		Last Modified: Mon, 16 Mar 2026 23:20:29 GMT  
		Size: 24.7 MB (24735775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8188e372c017c494407b24b2b30e203daa280d4883793d18b074e8e8f15361b`  
		Last Modified: Tue, 17 Mar 2026 00:51:48 GMT  
		Size: 70.5 MB (70514894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2ffff020b3074deeb9b31c6808ad55058e946cfda3a54bdc55a2c0beab9b53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44108251c606e5839d36fe7983cd9651c964c59ed66c493a824c8498a36f451`

```dockerfile
```

-	Layers:
	-	`sha256:be4e618ccdba37435f7dd97dc4501ba617587029614e0c66a55f64ad6259ab34`  
		Last Modified: Tue, 17 Mar 2026 00:51:46 GMT  
		Size: 8.2 MB (8221867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7410e48cd50b17148fd51ca50d2909a1776855bbfcbe7599dfff268a159bc329`  
		Last Modified: Tue, 17 Mar 2026 00:51:46 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8485373b11f8bbe92586b5a6380ab076449b6f41c98482d92e91c301e5f68edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150226038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1e31949840a410055eecb2f434ca3475ab122b81271360c939d2edcf7122af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873916964a227a18ebb04ec1f407f168a33886e300682cbd4848c61bc623f448`  
		Last Modified: Mon, 16 Mar 2026 22:40:19 GMT  
		Size: 26.3 MB (26344588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4fb7d902f3cb9bf3e0daa77ba127ee8230f61ba12bbb5d9f7dcefc084f7373`  
		Last Modified: Mon, 16 Mar 2026 23:31:17 GMT  
		Size: 75.2 MB (75222389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aad8ddd1c2e6b05f4d35fe076221276c9920434139cae2788cb2c5fa99972914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8245290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3172a3925d19c5aa332612865193f92af49a48f7e1fd7783a73ee735601e718a`

```dockerfile
```

-	Layers:
	-	`sha256:440d7592bed5bbc1426faae02f5dd0a043a27b075abf6828783e782774c4216e`  
		Last Modified: Mon, 16 Mar 2026 23:31:15 GMT  
		Size: 8.2 MB (8237944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197fae3cec313f2fb0c731774686fa495fa96c1475ffcdba3c279dacdde5f764`  
		Last Modified: Mon, 16 Mar 2026 23:31:15 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:53ec2ea0afa9eb04d97c8cc26a01da06679441589e26770dba76ed9f5e575da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156194790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa1c6f328a9e00d3d8faef9b1f3d7a284112eefe4bf8a265137c772ac7f0da7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63597877e9ce45a8d644c87f2edaa1b6f60b392c0f8a5049196e27710801057`  
		Last Modified: Mon, 16 Mar 2026 22:44:13 GMT  
		Size: 28.3 MB (28310412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b32036cc7858dc14c7d8b709498aa52c52147bbd4f9cd24a39c522f264cf55`  
		Last Modified: Mon, 16 Mar 2026 23:42:04 GMT  
		Size: 78.0 MB (77964507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9511e3dc373915f918af34476baa8c3a94698dc41f586dff1aefe9152d478c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e17ccd76df524f715438933c6bad36c2dfacdadc4f94336b0972d868a91bfae`

```dockerfile
```

-	Layers:
	-	`sha256:efa47cbfe46c0985944ceec49ff8e465d9eb02de34d616d62c662c3aa7b240c6`  
		Last Modified: Mon, 16 Mar 2026 23:42:03 GMT  
		Size: 8.2 MB (8217497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b349412d520f6385e8cc50f0de56daa88f450026c353e4207bf0ecc3608dbb`  
		Last Modified: Mon, 16 Mar 2026 23:42:02 GMT  
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
