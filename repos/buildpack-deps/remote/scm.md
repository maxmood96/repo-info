## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:b326ca8a8a646c07552dead9e51173f88eb2852375f6242fe271017098e3c0d9
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6f9fd607b2e260d41c51207fb74010ba06931047760494f5f6d59854e7d55db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142669922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17b5dae59b0cdb9c61fe7aab5655796b7f9864bbf0fadbf0705959b5f8f97a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a0f047b8d00633084f5eafbddb0826df9c8b94209cb0e6ecb6dbbdf90b5318e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43b606fc1c0a7ddcb70363f16487247ebca594563585e66886297e8dc0b496`

```dockerfile
```

-	Layers:
	-	`sha256:d0e0a063ae02ead956703ef31fbc66e346bb89e74f74ef7f179052f8bd3e86f7`  
		Last Modified: Mon, 08 Sep 2025 23:33:41 GMT  
		Size: 7.8 MB (7766996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306d71bacde505ffe77f0196ebf9977245053d6caa0349e3445673e47980a170`  
		Last Modified: Mon, 08 Sep 2025 23:33:43 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7cc1c00fcae11d09f1165ba5126667a11bc3cd0214ab671d09d3d4f6941a6d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137101531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591c2414f5fc2990d27460647e0dfb8dab2a497aafb93e07158763e470d90d04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:93fee7f039682b45509657d20627a8677376fb460d8b9d61131616286dad7986`  
		Last Modified: Mon, 08 Sep 2025 21:14:46 GMT  
		Size: 47.4 MB (47443594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eda5e1ec6a0c1f6af96a205011570e8f52ef368e949e16b2f9a27f81c436e0d`  
		Last Modified: Mon, 08 Sep 2025 22:27:55 GMT  
		Size: 24.3 MB (24340053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3785869f46d3cff8cf04db023410db2428121ca3226b5aee31d9b3b66102eb7`  
		Last Modified: Tue, 09 Sep 2025 01:33:07 GMT  
		Size: 65.3 MB (65317884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db22d2332677213df1a5a7a91c9744e5c58cb49f57303f02e9544b9e18ca08ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd563bdb16befa1b2a978d123253b0648c3c81f8601a301e1f8a3fdf13c1005e`

```dockerfile
```

-	Layers:
	-	`sha256:5d6d62c2ea968ffd0fb30526fe422b73f289186ac1c99fb8d81f45ff44b37089`  
		Last Modified: Tue, 09 Sep 2025 04:21:20 GMT  
		Size: 7.8 MB (7768034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:996dfedd91cd0817ec8c218edb95f61e77e93eb2fa259d60698a9934bedf4f60`  
		Last Modified: Tue, 09 Sep 2025 04:21:21 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5675190ed78c6432984b71c40aefda17d5b0e8b959d115b7c68392687a169616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132045349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4d83255cfec2487ed537736edf4b5a4efdba9391f38fa7739b43e17c6d2806`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:395f9ad3c9d37c6ea60897f33e8b189e9cd41fba6c60ab63882fd95de8ebb9f2`  
		Last Modified: Mon, 08 Sep 2025 21:15:43 GMT  
		Size: 45.7 MB (45711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87266d99f84095bec303de1733ad218d485653dfb6da729b7a066c18810645f9`  
		Last Modified: Tue, 09 Sep 2025 00:02:54 GMT  
		Size: 23.6 MB (23614030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0847685b749ce0208c0ad2a407e89f30279b1c8515c5c33f13a9c9b4c5e3da02`  
		Last Modified: Tue, 09 Sep 2025 03:21:45 GMT  
		Size: 62.7 MB (62719599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12c013865ebe19ff6dfcaa245b08f41f0897ae095b6bc335eda54a7e3ccc7f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acfa66e3ddb198ae58ce5d167c4ff9068503d4afde371d86a2aa66a322f95ec`

```dockerfile
```

-	Layers:
	-	`sha256:31c0221678b6550b7e669e701a9e25ea573921ef6b51317a02727b473b58d662`  
		Last Modified: Tue, 09 Sep 2025 04:21:28 GMT  
		Size: 7.8 MB (7767503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09df06308ba7572e05c80386a19c08ed731866804cbf4792cd82f8f13d6f901c`  
		Last Modified: Tue, 09 Sep 2025 04:21:29 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b563d52ed4a53a09473bcb058037e6bb062e9d1d684f849d5ffe726afab11079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142242188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e232b177ceafbccb5b64671eb57c7cf2f1b75175173e59080f9de8856f35dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd36c08acb8bfd3ecaef97bc215303e9b1c59f47cb418c4692d97f29cb1b17c`  
		Last Modified: Mon, 08 Sep 2025 22:26:04 GMT  
		Size: 25.0 MB (25015321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd600967e6c49c98883d12d3ca7ba50395f75eb436373e95780141122745a6`  
		Last Modified: Tue, 09 Sep 2025 02:13:16 GMT  
		Size: 67.6 MB (67583121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:24a0cc906632a5cd9d9775d7397441a68685409d64911411c498f2933722c0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8954c63afb59c29d2b2f643f1e81315f5c6dbd57e118c927bfbfcd65b909ce49`

```dockerfile
```

-	Layers:
	-	`sha256:c58e443ade0cca89f0599903438da42b63111246fccf7306eafd601143d51fff`  
		Last Modified: Tue, 09 Sep 2025 04:21:35 GMT  
		Size: 7.8 MB (7774671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e61ea3af55373a2ff7bc0a9d615dd325cf760c4ce12527df815c7bd1a53cc6b`  
		Last Modified: Tue, 09 Sep 2025 04:21:36 GMT  
		Size: 7.7 KB (7712 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fda2c69fe2b752efa351c15b894a99af91e40c1ffe8ef1e2d1e78d4af1fc605f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147362714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5623477ab7c2320437c9f15efc187828e02ec0bf7c8f1cdad6dc00e8bfcd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e6ff4859ead75e29b179b0636a999dd68cde264f9c74ad8882d9d5dcfc9c7`  
		Last Modified: Mon, 08 Sep 2025 21:55:26 GMT  
		Size: 26.8 MB (26773510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4adf19bf3e6f542f3c00d3fc4bb83f2ec48ccc9675502c518d9eb368d0232a`  
		Last Modified: Mon, 08 Sep 2025 22:13:48 GMT  
		Size: 69.8 MB (69794254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6900c203af645c469a272b3cb7c0d92bcd69e00da8834434232ae169ecbf238d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f523af6c419986793fbd895ff833096ef737ab718e9fcde5899d48d5de91f1`

```dockerfile
```

-	Layers:
	-	`sha256:79b5ab8b3e12323b9d0fa93d70b8d033ff0480ee7938c58e3676a86c842f440a`  
		Last Modified: Mon, 08 Sep 2025 22:21:26 GMT  
		Size: 7.8 MB (7763131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa330df97b8541268516671a77bd1a83ba31b01e93b7f125ebbb8f9f8c6f8ecd`  
		Last Modified: Mon, 08 Sep 2025 22:21:27 GMT  
		Size: 7.6 KB (7593 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0cc36125401f4d776acc30749357e358b2b5aef0dfc1bb95608a8f3289207a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153114911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b125dbf0d20b254801459e7915f7ef16190c5a2aec3bec8eebef4fd038d1d5e4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a50c904b64f68da7132c659ac9b38c086173bda9976436e8680647f3f573917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ca70b14505ac2dffedc2702d7de0cd4ff80120acb599dc0e64cd41b37afda8`

```dockerfile
```

-	Layers:
	-	`sha256:862894971ab60871fa55dc006cb14e82dddf0c11a29b835e0f4b7cd166cc5dcc`  
		Last Modified: Wed, 13 Aug 2025 22:21:27 GMT  
		Size: 7.8 MB (7769495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d15029a24e12e7cb5bfdd206d8c32e2a1d17dcbe92ac7f2e54fa6569931f8da`  
		Last Modified: Wed, 13 Aug 2025 22:21:28 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e6e13751172800f302a25a3d741930290eaf667f5d978f95e829cc5629f58664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139373194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831ce6e3a9312b6a9b524f0f611f147c52273342216355a74877726a3eb67c34`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e41821bc74a26f64d4f81be6785aac1d7f09df07149a206784ae23523e36a`  
		Last Modified: Thu, 14 Aug 2025 14:47:51 GMT  
		Size: 25.0 MB (24950584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0b64daccd6b787f78c1a1622c08097763f53e2dee005bedbf3141bbaa8af2`  
		Last Modified: Sun, 17 Aug 2025 07:49:06 GMT  
		Size: 66.7 MB (66658307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:363e7ff0da3f0b9dc04d366578a1027f34f8dfccd1cbd01f94e74547ebef70ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be69240ec38177b85b96e68eb7a6cba9bc177c7474c7c61e72eafa64317621ff`

```dockerfile
```

-	Layers:
	-	`sha256:ae9094cc76d07aad9c0624124adb2d580c4b92911e61cb4d88fc1e8776038217`  
		Last Modified: Sun, 17 Aug 2025 10:20:38 GMT  
		Size: 7.8 MB (7752208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4817f9bb2cf3f32599c6b9c3be7d34693ce07fc3c00dc4319c42e164102fead9`  
		Last Modified: Sun, 17 Aug 2025 10:20:39 GMT  
		Size: 7.7 KB (7658 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f510959464e5ff3bfc8f412edc7d9857d0effe287bb98e2e648c518b05143657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144744739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a88b8201a29cbf1464f108ee179107e79d0b96b3ecae8221d209a5c6afb1d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b561211d78a0e0cc14edb0d910e128169d7f6295a8e1bf461c5a2b74b359dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba8f659757967e3477edf4771e3d57bf92a45a747ee7d6995a46586a5f59010`

```dockerfile
```

-	Layers:
	-	`sha256:462080382afcdc6684e9bce4b59c6d700b29225d043b80106d2bde519ef37f71`  
		Last Modified: Wed, 13 Aug 2025 10:20:46 GMT  
		Size: 7.8 MB (7763285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7c82f08bfce4a1583495bd2b880afba5f4f60f4e95a5d8c18c07acc013f323`  
		Last Modified: Wed, 13 Aug 2025 10:20:47 GMT  
		Size: 7.6 KB (7617 bytes)  
		MIME: application/vnd.in-toto+json
