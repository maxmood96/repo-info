## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:8494c74807a2bb52fbcc3edd840dc94f4dd470262d8fa82c81a886966a005500
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
$ docker pull buildpack-deps@sha256:26d45058ac32504dc42064a8b95c8d17a95da91c70530519695b8d8886f08125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137100206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c6a0d3db6124b2f49d9198a41901d99109b319ac296420459e6ea9f15df160`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49b34b9ef926ce7ed8f011fe61446ff5495accfded522a04a8414730759ac407`  
		Last Modified: Tue, 12 Aug 2025 20:49:02 GMT  
		Size: 47.4 MB (47442425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10345871b22cfbefdba6d9f2d575fe7ebd340d456d55037a519d266903c1f87a`  
		Last Modified: Wed, 13 Aug 2025 00:01:36 GMT  
		Size: 24.3 MB (24338768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa2b20bf2d33c358d141989badced2a336e24163718df277bd1fffd0bce46c`  
		Last Modified: Wed, 13 Aug 2025 14:14:52 GMT  
		Size: 65.3 MB (65319013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf62e2191f193229c0f6839079518a01821cd67c6929e1032298b974fc6bc668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f65518eeea0800778a210197dee1ad538e5ff125ad4584a4349c11ee41f04f`

```dockerfile
```

-	Layers:
	-	`sha256:a7e4bec31f61a3ccba4491f5f802ce1a4a31b7e8cd7f9b48e61d4ac5a44de3b8`  
		Last Modified: Wed, 13 Aug 2025 07:21:02 GMT  
		Size: 7.8 MB (7763410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243172bc13bea65d988a96253ea46161d8d32dee3a0e1b50c547d8a6036623ab`  
		Last Modified: Wed, 13 Aug 2025 07:21:03 GMT  
		Size: 7.7 KB (7688 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ad8811a97f80b8a3f3419cd48e7d674063d42f51ba85a8c72ea6813995ef82bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132044177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c854371f45ee747d9569e23b76fff653d1c43cd98c83a91e2a3234b925fc6e72`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5b9be1510541e0cf9124401086f13ecd25e052836bb49b39753cbeaba30b210c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb98ca357c915339a07b2e40d850f2e29a07fbb4284f5b30741f079b4fb9e587`

```dockerfile
```

-	Layers:
	-	`sha256:0e7fb0b56d27254b6f710e69ae44a1f19e3e59de9d482ea450cd10c4b22d7109`  
		Last Modified: Wed, 13 Aug 2025 07:21:09 GMT  
		Size: 7.8 MB (7762879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1f6409d05f7a22e2ead1ac63b05cb8bdabaf95b320da916ec655d924402c98`  
		Last Modified: Wed, 13 Aug 2025 07:21:09 GMT  
		Size: 7.7 KB (7688 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bcc22eb96e576fd29f05f2c83b6851492f67be0499777dbd595142e87dbdfc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142249841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98da3e524bc1732dd1c8e0d5bc3ab9dd4940fbe66a7f88ff88902819e0f9acb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69a833c2174b74c6338d26232207a19c2d4fb304e04337d9973f59173bac07a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff561a19f6d8908668735378ea2f4d415857b57a58e913b9df9939ebdf1f3a9`

```dockerfile
```

-	Layers:
	-	`sha256:aeffa4b066b8970a27c458eaa5a1ffb71273021c1c40ebba2f7f1b63ab7f7734`  
		Last Modified: Wed, 13 Aug 2025 16:21:04 GMT  
		Size: 7.8 MB (7770047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf685c68e8e40c8503acecab39a034a54839dbc59adafa29bfc57a28764d831`  
		Last Modified: Wed, 13 Aug 2025 16:21:04 GMT  
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
