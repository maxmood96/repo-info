## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:e0ca7ae27a3b028635eeae13a627dc9f5aa7796cd620dea344ade9e8636754b6
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:82532f34b2495513e7f5e4a87bba3dc8b4e640edf1adc627e8e7dae1b322fe6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152475408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baef7a3a5e0168a6106de790a1e0bcf28980526089cab706845da1713f8aca6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd9ff4ed5fe9d40159f9f23c065d56cc6738732b6aa6aa03dbabd14807df17`  
		Last Modified: Fri, 08 May 2026 19:40:58 GMT  
		Size: 26.9 MB (26931106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5e74373817d223614205755063bd680dbeaabd9413354b6512787e7493e72c`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 76.9 MB (76922259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef661dc9ad3904ead537551795775f86b29a09e2ce35b6ab45f7931ec7cc314f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8283620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b2321d55077402c7cb3d27ec1b39c442900eba467afed392d5713b4f72e63d`

```dockerfile
```

-	Layers:
	-	`sha256:fd71afa0c5e0e62c7cd39a43e3098cf981693bf65ce17948abde21c46fe3c849`  
		Last Modified: Fri, 08 May 2026 20:26:44 GMT  
		Size: 8.3 MB (8276354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18cbb7ac58fcb92c62c5257726d78b504deaa9a304042ea5346bc585cd3eeccd`  
		Last Modified: Fri, 08 May 2026 20:26:44 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9ec9834cdb971c2b82e4eab91dc51417e768d8a6900b1b94f9a0e7fd6c0e3b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141657129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c62cc336885b737117004f6949be74dd0959466177b473f78352ab69d1a660`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1d504d75b0bac1a71363cc538d085e2c22d8b451c5112cd1892dea705c788f73`  
		Last Modified: Fri, 08 May 2026 18:37:09 GMT  
		Size: 45.6 MB (45559652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9e557f096b0076a9b942cb90588ca852b5e2621c1b8f7db68c5da56f1d563`  
		Last Modified: Fri, 08 May 2026 19:44:57 GMT  
		Size: 24.6 MB (24627884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7656597f355ff486609cac9b41999af529a6b55f6a5cc1c7888048b9d1f921c0`  
		Last Modified: Fri, 08 May 2026 21:35:23 GMT  
		Size: 71.5 MB (71469593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cb22362688f4eca5389f911ecb0f8da6c6b90dd453978a0930f8c52d18bfc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8286036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d86ddaef22a643431104e2fbf79ba5dd26e3ef049682b2457c7c1ad7d2c23a`

```dockerfile
```

-	Layers:
	-	`sha256:4e17e0e64791f5389e9a5368415a888379e9332d70cfa123bf297f6dd5e3ee19`  
		Last Modified: Fri, 08 May 2026 21:35:22 GMT  
		Size: 8.3 MB (8278707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72534d2f4808b76b5a03842e303cd0d3988b707c698e08b382206da1cd37f53c`  
		Last Modified: Fri, 08 May 2026 21:35:21 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f40824fb9e925c0005548f9023577983cd8c22b2cbcd0f28a40ae7a12e936279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150967284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1a2d73a70fadd4ddfd479f67eb599ae327a6694e2dd9cd45a66c12cbbf8e28`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1cc0aceec664d055c261d350fe983921369e3615a68574b4c33a17a625489`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 26.2 MB (26215967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a7c71d7585d5a3c2cd0c50f396ae3fc659aeb54277293c1791833880128752`  
		Last Modified: Fri, 08 May 2026 20:32:45 GMT  
		Size: 76.1 MB (76091566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ffaf2537581a7c82d305c646bcbc5e698f911e2648a2582b4eb6e8a388df0095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8295846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f76e5ae5ffaf494b3b33285f64f3ed7776050ad34f271a275b59791a3690a70`

```dockerfile
```

-	Layers:
	-	`sha256:d2e6130ecfed42391911fd5ecee4bb46896c40565bb5446979834bda7ed99371`  
		Last Modified: Fri, 08 May 2026 20:32:43 GMT  
		Size: 8.3 MB (8288500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028ede57bbf435c64849522fdfaaaa82bd71bcdb696e5b3c1563bd7cbdc41ad9`  
		Last Modified: Fri, 08 May 2026 20:32:43 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9ca565a82c60c2eee151a1b11767c21bfe499f44565166f1368feb8ed396f975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157308494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cc40317e5864b4a5965ef255070307d21c7663882fb1a50e39a4de1d79c2e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:43:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce975e5bc9e5b821fdbe31dcc55ec740aee98d254347a49a09e2157accffc9e`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 28.2 MB (28247335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accb2ad2fb3504d5babe277108227672c99e7f6267841ebac568eabee2b26666`  
		Last Modified: Fri, 08 May 2026 23:05:47 GMT  
		Size: 79.1 MB (79136938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6c3a01598d9284c195643e2fd702f1f58fc0acb2623368cb2a57deb47a4c90af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8279081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8172831ec457e0ab5b7eef3db2cbc22fc4accd983e74c388abf49aa03c33b05`

```dockerfile
```

-	Layers:
	-	`sha256:5edda19f98a86cd7947f6d80385b8031cd24f4e8684c823b59b8aaadc72c9dff`  
		Last Modified: Fri, 08 May 2026 23:05:45 GMT  
		Size: 8.3 MB (8271837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa4fb997dd4b8feeed1c8434da0fd2575674dd526c75f7f351283fee29e4652`  
		Last Modified: Fri, 08 May 2026 23:05:45 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ed81decc83c5315d4884b1a5125ba7e26c68eebefd07dfbd5eda97c2e6aa0b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166625818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd849fc10fa7d86887b1cb7568d7dac48ac464ddbd5b07924f355944b1b4fa1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 22:31:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:27:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b0beeba61b823ca3e14a339f1111ae37331fca42dd43aff18c04950bc3c9921a`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 53.9 MB (53926974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f3b32fb543eab144095fd22346cb5e6a9d20cf9a632717c0a11d280547f7a`  
		Last Modified: Fri, 08 May 2026 22:31:29 GMT  
		Size: 29.3 MB (29268977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9ada7fcdf049694ac82397db78a7b39cd1a082adab6683f0a1f738caf441a6`  
		Last Modified: Sat, 09 May 2026 03:28:12 GMT  
		Size: 83.4 MB (83429867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5b92cc41cbb6a1a0f25f5e06d31eb95cbdabaade6547cc70f868e2347d6acfc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8268615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5126f250e08e88deb297fc1290fd7a8b4ebebf4f4a1bea48129a6607c9710c4b`

```dockerfile
```

-	Layers:
	-	`sha256:5a9dba45d60af1ca16aaac5b361ae6b4a25638c84fd56ebaff05485eed4be9d5`  
		Last Modified: Sat, 09 May 2026 03:28:10 GMT  
		Size: 8.3 MB (8261317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c048b9514f8d85bc5fa951da215b9366e67fbc22209df5d5c9cedfd775fbe809`  
		Last Modified: Sat, 09 May 2026 03:28:10 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a0ff15214d005cf8a270269c3a62333ebb70653b9a1a0ca8701f6ac87112f587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148650595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a024470884d4b8199ab93772008e455d4614e4e2640eec259ede6be7c83f1c4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1776729600'
# Thu, 23 Apr 2026 16:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 25 Apr 2026 23:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:04fb0dd36a6b62569331264b3dc244d1f567b4ad68c8c1b27f9d22978f421544`  
		Last Modified: Wed, 22 Apr 2026 02:14:57 GMT  
		Size: 46.8 MB (46771523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67bcef726e432bfd28120bec18ce459483cfe5851a88769e35186b7e9186e99`  
		Last Modified: Thu, 23 Apr 2026 16:16:58 GMT  
		Size: 26.6 MB (26575473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c088d66fe4b03f57a1b249457eed3a1d678ec813dfb34d56e5a011edc2f10bf`  
		Last Modified: Sat, 25 Apr 2026 23:10:22 GMT  
		Size: 75.3 MB (75303599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85cdae5bb11cd42432c3481485847d67aed8eab18e31e8669cbd217be20c0c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8268804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b9a0dcf0d500e290b2c88be60081a5a658b73cb1db2309a15fa8a12506e12`

```dockerfile
```

-	Layers:
	-	`sha256:2487364d0d1b100d00512533ef51cc6b8729dec979454d82708a8ee4e1da7b6b`  
		Last Modified: Sat, 25 Apr 2026 23:10:13 GMT  
		Size: 8.3 MB (8261506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b3792c0eb3138f9ad629bd5c4bbc9e0ea8eca06d767924744f6ca3761390ed`  
		Last Modified: Sat, 25 Apr 2026 23:10:11 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:376c303c02306d5cadc89b95c42d09c9fcce084f2b195bdade256f7bb6d8ae34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3a0a02cf6eb0d8411a149971c1fc7f9f4554cdd75a6258a41afad776dcc5ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 20:53:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:33:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba3092798c7b7e427c9591ec4f0d9efaf8a9b59416038e46d07c57fb149b38ce`  
		Last Modified: Fri, 08 May 2026 18:27:50 GMT  
		Size: 48.4 MB (48373532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea40167dce774b75145b31dc946ba69ba4700a809db349b4a3bb2a9ef77497a1`  
		Last Modified: Fri, 08 May 2026 20:53:38 GMT  
		Size: 26.7 MB (26717627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30067cce4acd56b3088a56a702bef852ed218d3ff66dd3e1c87034bbff2dedb1`  
		Last Modified: Fri, 08 May 2026 22:33:58 GMT  
		Size: 77.5 MB (77468385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:19cba5028e123599d97392acb27ecd9bbc34e8e6f32219655acbdc03f12c028e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8261473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c584cd2833fca75621c91e0f8d919e8ef2834b75eb4eab863d69da20e95c46f`

```dockerfile
```

-	Layers:
	-	`sha256:6daf866c6bb25f9a4a4ce20d1053d7878934edac7cbbee0271a4eac6d936622e`  
		Last Modified: Fri, 08 May 2026 22:33:56 GMT  
		Size: 8.3 MB (8254207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1de79ddec1011fad16c8a6b01ba8fccb56306d8e5a82527da4d98d984744cc1e`  
		Last Modified: Fri, 08 May 2026 22:33:56 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
