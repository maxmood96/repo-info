## `debian:testing-backports`

```console
$ docker pull debian@sha256:fe3869ecd1922d998041c37227f589cdba7af39bdb462f36e6d05e422327eb70
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:4998ff7659e9643a520624017839e03933770bbf4d3ae9c92bd891da847dad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49247131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadcca22ec36be5bbf378ec9df27e3eb81ad73c3c240b0d5a6ca09835d3c24f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df56d2e10300383b653c76122e6b5696d7113980a59e9e16cfad3e99742758e3`  
		Last Modified: Tue, 03 Jun 2025 13:33:02 GMT  
		Size: 49.2 MB (49246909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5e116bcb710b5c1ec70c27ad4f7047c1cd835b0e66b1905242441357865b48`  
		Last Modified: Tue, 03 Jun 2025 20:04:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7a3deff4ef5de6aef335341bf9a9ecf5d567c4992ecd9251737d03b82c4d8c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8644745dfeecc24ade39b504965ec2c1d47ca16d60a6f6ac5d9de1bd8d0ec1`

```dockerfile
```

-	Layers:
	-	`sha256:2b42bbf7979132d5f3934b9d658abc41467c048b7a4e27b22abfa81c0c3ace63`  
		Last Modified: Tue, 03 Jun 2025 21:22:18 GMT  
		Size: 3.1 MB (3084263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd521a34f94a041c1fddc015adf48b118dd14cb00b178a15daf5109239140af9`  
		Last Modified: Tue, 03 Jun 2025 21:22:19 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d2073afa1c321e6aeb5507a052824c3d995d113008dfcee8b35b4e56332f9165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47438360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1457d5afd6a4d092499337bf009fe25ebb81347868545bfb3da547ad48ae42d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f551888f4c0d5c86f32da00c22f7264a3e65d46e9d274354646efb8525e1347c`  
		Last Modified: Tue, 03 Jun 2025 20:18:32 GMT  
		Size: 47.4 MB (47438140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c4724d3bb0bae708969634e9ebf37b1061d291554b939bc0e512c45097c43`  
		Last Modified: Wed, 21 May 2025 23:12:25 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9c3f8c9d022367aa536f000bc8e3bac661a1ac694721b73046a2b89a0bbded5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3099461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133ff928eb0180d8820ce7d334f9d8f95abedd68aa314d59b221563bea7966a5`

```dockerfile
```

-	Layers:
	-	`sha256:f2a51788dec99a3fac7e086430aa8cac19893e988df0fdce2764bbc2a64ff34f`  
		Last Modified: Wed, 21 May 2025 23:12:26 GMT  
		Size: 3.1 MB (3093572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9fcd548bcccdf9614088ffab50de30c63ec494c7324bf8a37d1ed73e078a2bf`  
		Last Modified: Wed, 21 May 2025 23:12:25 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4a9c384ec46d20f8e4804349fe70e91a19549645aa72ffa0843bd494273087c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45691040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1fab7aface6e0e9966580f667657f11d39143d1ac055e5b087978dce787ed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1dfe21856cc4ed6573ae2f33f8093689d55f7862661b97455eac46bc449498ad`  
		Last Modified: Tue, 03 Jun 2025 19:01:13 GMT  
		Size: 45.7 MB (45690818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08a77e1f600ff5b4d75268c41e844cd9b9d3ca74e35b24d7053e4d433180b58`  
		Last Modified: Mon, 09 Jun 2025 13:09:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a72a41ac9b3ac93c22227f481d116a431c711b85db313b9796f439e730cb24cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513bb778bf83b1b36807cc197a6c3a48be7ab3f59089121dab84a3414f9ad188`

```dockerfile
```

-	Layers:
	-	`sha256:86b599ec77472024a925238f7c60ff1918cf09f06a5a43bdbee219e0aed79ce8`  
		Last Modified: Mon, 09 Jun 2025 13:09:36 GMT  
		Size: 3.1 MB (3085637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deba14f31547e48f986e936aad9b593972001161d1146219e2b6b3777eaae8bb`  
		Last Modified: Mon, 09 Jun 2025 13:09:34 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6b1fb2491addaa77991d98b029c4094709b186a9017ced9bde297611118e1566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49618514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32810d314c435d12cd32cbefdc655850bf941d203a4ff94724864fe59c7368f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3f6b3f3a36e322107da5dfb855c52cd71df93c73a06d6a82855f69268b41d80f`  
		Last Modified: Tue, 03 Jun 2025 13:47:32 GMT  
		Size: 49.6 MB (49618291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52f16a759dedea7fc5ff36093fd9c6ed69b34960a5b05c6a5a8512f2ed49cf8`  
		Last Modified: Sun, 08 Jun 2025 03:15:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7a380bd25c3b98ee4000fe6c027d55cab73c94374098ff66b2507a453ce6faf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f02798263814a09862c070084fc4f47661a4905ebe6ac0be0ef7dba9ff8889b`

```dockerfile
```

-	Layers:
	-	`sha256:65fd47bbab81e0b54e83d105d14c6355daf35ee39b2732be67d01ad899806d03`  
		Last Modified: Wed, 21 May 2025 23:12:42 GMT  
		Size: 3.1 MB (3085744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab81f3d205b8f7e27994ffa6023ba8843f6cc0a80624fe13531599db8dbf272`  
		Last Modified: Wed, 21 May 2025 23:12:41 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:ed6e9d1e62903fddb3d531da6fffe36cf349dad7417630528c1addaba4bc24d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50761499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a5e554f5f1bed3c4a35cfc1e773eb934997f87a75c9b04e3cc28bb749a36e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:278e8b694381561cc2328a2cc05b5ba77cbae5dc5cc4a795b111b10469d8e755`  
		Last Modified: Wed, 04 Jun 2025 00:12:06 GMT  
		Size: 50.8 MB (50761276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0f8d990fbfefa5f4ddb9ee7bb7992b7a20223de526aa1a0c8c3c3ad3d6ade5`  
		Last Modified: Sat, 07 Jun 2025 08:01:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:353f9ce0edfd77e06f9b6b0631037066f215e6fe8e6f31b6211396a94b4b203f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a757a9600b2f42ae07e7c4fc43879c189808951223869b3186f4ec29a6ab53`

```dockerfile
```

-	Layers:
	-	`sha256:592fb1c7941dbbc8da18bc173c6fc870ee271dc3d7e7a268d6e322463f255621`  
		Last Modified: Wed, 21 May 2025 23:11:54 GMT  
		Size: 3.1 MB (3081467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb968ca3bf8ab329db31fda172f6e7e5de17783ff84816bfe96636393935e05`  
		Last Modified: Wed, 21 May 2025 23:11:54 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a54685571edd9bdb5d3189d13afcf0fb0697fbe914fcf60ae6153bc3fc227f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53080763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f86244bce8bea8617ed52bd7333ab63478f3cbea0913a20e7c3098fb9ec946b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6a533743cd8d66e1407986affbdb4273987e0e3aa7905a4809596a56ecaf2568`  
		Last Modified: Tue, 03 Jun 2025 21:24:01 GMT  
		Size: 53.1 MB (53080541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1282de1c49ea6b31515899ff284319998211cde8b581997f02c9133addc8ca`  
		Last Modified: Wed, 21 May 2025 23:12:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:76d414c9db861b0af06e158fb68e91fda653f745701c58e4f0209a30f8bfb11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8dd68a792bd82659ab8888e9f9fe2993a4f870f9ff1d68def6e878e4544e27`

```dockerfile
```

-	Layers:
	-	`sha256:05d385c5475e3814aba9d758296dd824d6437f2e403d44efe379f5a1cb90aed1`  
		Last Modified: Wed, 21 May 2025 23:12:42 GMT  
		Size: 3.1 MB (3094144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9279527f08fd5d55bc86260be5c07670f5d1afbbeebd7732681df640978ce3d`  
		Last Modified: Wed, 21 May 2025 23:12:42 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:423f2cc612db2b8ae19917639a75bb7f138b728df619a8857f68f78543084551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47731627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd068bdf855624fcc4b259c3ec03d5073a0ccb4178dd2a1927e4a3a9f05dcd84`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1d2530ee1887adcdf73616ed4351982e12edb25412ef8021e3a83d734645772d`  
		Last Modified: Tue, 03 Jun 2025 21:23:58 GMT  
		Size: 47.7 MB (47731405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08a77e1f600ff5b4d75268c41e844cd9b9d3ca74e35b24d7053e4d433180b58`  
		Last Modified: Mon, 09 Jun 2025 13:09:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ff6f43e891edc56cd7020f419074a7c43004dc3c223ffbd1cc0f0d3150f9a1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e756e88fde5d93b7447588363780e7b58764eedb01b60e68550be6c0747272b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e58f9fc82b1324b89e2b7d6c12fd662b0ae9feca2991051f5b66cf9596f1c02`  
		Last Modified: Wed, 21 May 2025 23:14:12 GMT  
		Size: 3.1 MB (3076584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6537d170b80beed64edfdf0178ba0bb3baea74b8d3289137facdc17a18bfcc3`  
		Last Modified: Wed, 21 May 2025 23:14:12 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:4c2e6bfd3e2ee521fa09e02333c445ebc5c0e68dbcb2411cebfe58066b6e825a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49322448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a6419a71717b01dd789ca3f2cea144183efc57857f50755414509d270ff6d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8c7c5c720e3ebad3a2e1fa96d133e48b73226c9ee75449abcbd73a5d7a88ef3e`  
		Last Modified: Wed, 04 Jun 2025 22:26:45 GMT  
		Size: 49.3 MB (49322225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd1bd524feea32f440020a6d1c71c2f2c410c909dcf08164eeb2d282ed08a1`  
		Last Modified: Wed, 21 May 2025 23:12:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ca83400cb4f088b17d0fcb53f09d4cba8f1b1f6712a2be3eb8ab073407d75348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd671054c8493462281442e792a9da6c0a72c94ca1bfeb9d736a5e146d11ab7`

```dockerfile
```

-	Layers:
	-	`sha256:5c4d0d673f2b3fe0374bec6b3bca89820c7adbbe270dd9d7efee31fa99c37e1a`  
		Last Modified: Wed, 21 May 2025 23:12:49 GMT  
		Size: 3.1 MB (3092082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd12fe4ae1c85c58e53d56d8f43c5f027ad88a986a4bd62536afd07e5c8d6c6`  
		Last Modified: Wed, 21 May 2025 23:12:49 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
