## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:c12e41fda66150a93b9887b0d57fd13ce695184b04f4ea9aa43733e06dc992a9
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
$ docker pull buildpack-deps@sha256:7f0c5f5b15c39ccc5c3a013d4af32f7891db71f3e1f74d79ba08d14f6ad85d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74952294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf9f21a3885c9141672418247d340a911829ee1ccfd2c43ca73f505bf587ac3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f96ac6730a7fb0f2e51b2a6ccf7e60ca4af05ea0bcdb6cba8840eeb4da8c28ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38047f9c2bea440fd33d2a9fec2162af246447f93159991a8e5235d58e03cc2`

```dockerfile
```

-	Layers:
	-	`sha256:808e13126e7569401f5d480b50475ab9e426dce0dcb7ed63daff315c9bda3c6c`  
		Last Modified: Thu, 11 Jun 2026 00:42:49 GMT  
		Size: 4.1 MB (4120137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a2b658ba8404a8536044259f395f14ab49155644e116e419a1c26455f93bec`  
		Last Modified: Thu, 11 Jun 2026 00:42:49 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm variant v7

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

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

### `buildpack-deps:stable-curl` - unknown; unknown

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

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e6aacfce5b8ac845671b402d8cd1cd0dea8da7ab05bae5a9b2f2625315fa2553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77633214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338e05fd29c2415556827fb6519e6b4ab0026483f256a4b33a4932d8cf70f681`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54ac1ec51d3293c1ade0065529ca23d5fc365d00997ff4e5a290cef3692dc04`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 26.8 MB (26797651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2fa51c81875e36c94170c9da8ab9e6a68690fdbf2d03fcc3f1e3bd4fabc7f73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647e8bdf347253ef6cbbfac197de96e45fcc1add2ebcd70a8cb535dbf1b1dfd`

```dockerfile
```

-	Layers:
	-	`sha256:ac39cfc85d0f575d891ef8dee2a3ac2c6e79233aad27f5f5b5b2f36d3c97294a`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
		Size: 4.1 MB (4117244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc65e5b6ccdcb01bd17baf649f6ba5dd521760bbc4687ca2bfb35b7851e1509`  
		Last Modified: Thu, 11 Jun 2026 00:45:24 GMT  
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
$ docker pull buildpack-deps@sha256:5913d58d59ddae2319066f2dd346b4422e77283180426cf584910458247819fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72762649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf970a831be66dc6c2814b55f491056281165dacb5f3d8725ba8ece5599e762`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e6afb0d9fe2fdfebacf2ccb9782fd129d9e416f637c13f72c2f0427e69c04c88`  
		Last Modified: Tue, 19 May 2026 23:49:54 GMT  
		Size: 47.8 MB (47796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db76586e2d1a29e7feb120e0fcc7fa49e8df54823efd2e1b4e13ca0fe4ab60d`  
		Last Modified: Thu, 21 May 2026 14:02:51 GMT  
		Size: 25.0 MB (24966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aeb89f7ca961a55689e67beceac412aa435cbb1b9d9c0c2366cf5bbd99e8f922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304edae774843d44b1e746650a46654885c2f5000600d1d169a26a7fb312497e`

```dockerfile
```

-	Layers:
	-	`sha256:38453c92ecc2cd0e5f4de5fe6a9f77f2432f78aa57fd2b83dce80a08bd558f13`  
		Last Modified: Thu, 21 May 2026 14:02:47 GMT  
		Size: 4.1 MB (4112541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4950b1c8a9b454671a622ade0addccc4f83ff935e3a3be8829438bcc2bc4ad`  
		Last Modified: Thu, 21 May 2026 14:02:45 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:28e9ff46d0bbd73620318e7c47db5556a4cc7f9b07b0c5f6b1755a27f356ee9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76189815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7759d3f0a3ea7b92f010f9c6a3aae18b17ca3813019401b4c571631ae9eacf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58925113278ed74d68122ff77b22976b064cb872b273063a3ab182209055ee`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 26.8 MB (26803918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c68fb8e22a2f9cc0e68f2c225e0d5af5fb7ba45d380df4eded343a95a5f1e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717ae389eb9a5266e17d0c85d2f6f1b465d2ef2bd99905178effdcbdc3cc0e30`

```dockerfile
```

-	Layers:
	-	`sha256:dafa35f3d65f1f68cdb77505a1e6696d68b97f8a3506428508b6ba7a4151d899`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 4.1 MB (4121547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c0e337de1d8dde06667aeeced03e0f8741331b58ec187e02c48f04b5aadec9b`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
