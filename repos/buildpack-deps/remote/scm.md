## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:c95359043ba8476eafecd2c210685cdf2a1c51c8bde122ef26c6e09f65ba8c71
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
		Last Modified: Tue, 09 Sep 2025 05:05:25 GMT  
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
		Last Modified: Tue, 09 Sep 2025 06:20:22 GMT  
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
$ docker pull buildpack-deps@sha256:389c2ad4368f4cb543d27a8c30b8815cd568f87073bab75e668205828c66ef8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153131932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf6f961f88562c2f85fa3f9dee86d88f4135a524dd278e0fdc74d730661f390`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bf3914a916f37a54163b2eb02b685f6e0d654680e02a5e51b78387e81e4077`  
		Last Modified: Tue, 09 Sep 2025 06:02:47 GMT  
		Size: 27.0 MB (26993871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31355a04af67dd51f580585ba523dfd2b5ad7d91e873cb7213748a572df48bb6`  
		Last Modified: Tue, 09 Sep 2025 15:30:51 GMT  
		Size: 73.0 MB (73033628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dcac6020136f5ce440bd562972c327c1f85f67ffaf33dcb6dce8b600f90f724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e865f3f3d60d1c52b9a29471308dd60a12ff51e2c1d39d4e3d30e64253bbfee`

```dockerfile
```

-	Layers:
	-	`sha256:6f79db21df52e34c779eb13dab56c2274510b92b2f08f14555abe62d61a5df7a`  
		Last Modified: Tue, 09 Sep 2025 16:20:44 GMT  
		Size: 7.8 MB (7774119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e188cdb2d48bbf77c2783c837a72e2602ff34e7a6be0141327f3ddbbac94c2f`  
		Last Modified: Tue, 09 Sep 2025 16:20:45 GMT  
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
$ docker pull buildpack-deps@sha256:e8b964ae2c4798c15f6bc2078a1d4e5d4fb428d1f61cb3be5ce9e171361332bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144762726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c78b4bf9bb0a775a91e7580f77154676946c4d642338baa3f2bc46f5345224`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775d8e7868b319a235eef909d5a12163c48c579e84d18d78ed794653cb126a0`  
		Last Modified: Tue, 09 Sep 2025 06:02:49 GMT  
		Size: 26.8 MB (26780367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76c2286bf1bfe1b0d2250435d28c0af55c645ac84ddeac003b9da9b68c9c87`  
		Last Modified: Tue, 09 Sep 2025 12:08:32 GMT  
		Size: 68.6 MB (68636032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ec7d152d60c81cc963542e18963951b5c62eb336b5593b3214b44d3fe9fdb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35a968e5da833f05a2afaff67c2da84878f8bf854da6f775dd89c73c84fa985`

```dockerfile
```

-	Layers:
	-	`sha256:5e27e07c126ce165959b6f495d56fc5f76dc0f58cf86bdfe9dd23f69a09e9ec8`  
		Last Modified: Tue, 09 Sep 2025 13:20:39 GMT  
		Size: 7.8 MB (7767909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4c72852c08ab1638e1529a1ee76eddcf6d002971a508821b4bd26f6ceb274bf`  
		Last Modified: Tue, 09 Sep 2025 13:20:40 GMT  
		Size: 7.6 KB (7619 bytes)  
		MIME: application/vnd.in-toto+json
