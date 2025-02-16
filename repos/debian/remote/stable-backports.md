## `debian:stable-backports`

```console
$ docker pull debian@sha256:55d776abe6e6f2473aae650b182ae319191d92ba56f370e9105fdb179763b042
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:85d05a229cd1e545a468763dfbf0185502a47430fb3e862737a570379d902028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48479910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f584413f9b170fb3d059b51dad7c57b5890dd943d92d4a78b2ef08f68e92103`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:15664b7659e3bd05cffd002dbd5eb63b0c0b257e60a471c6739def21dc566a4f`  
		Last Modified: Tue, 04 Feb 2025 04:28:13 GMT  
		Size: 48.5 MB (48479688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3362bf55305f470dd4271f582835f3a42b08f0d09bc49675bd850499ca7e7ee`  
		Last Modified: Tue, 04 Feb 2025 14:36:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:60639066367091222457fd044060e049eab03b1df7db6f096392490fba216c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991778eadfbe74c4c4ad9a23cc252b6f67a87c2efa5f19c74c0b98a59de84c4a`

```dockerfile
```

-	Layers:
	-	`sha256:267858e9ab27bc223f270af5e658d0ad3e5a9fa25f31d32b445893b0533be15d`  
		Last Modified: Tue, 04 Feb 2025 04:21:39 GMT  
		Size: 3.6 MB (3619206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d1ecfad49d11e65fbf0851c22bfbed8590b64298dcc8cba5bdc01c611019b1`  
		Last Modified: Tue, 04 Feb 2025 04:21:39 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d2d4331bab62864435a0d803cc0f947b3714ed1082a0a328155238fdf232b1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46006799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea45c7867730b6d1698227511dd974f59d0295e61d7b4d78687b1e61b28b3df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:91db678bc5139051632be0d74d14f143de2d6b10af59344c7902b0034ff906eb`  
		Last Modified: Tue, 04 Feb 2025 19:41:58 GMT  
		Size: 46.0 MB (46006576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109aa64d2527161ba63682b7d82320f108690a2af7cc37578dfcdf925d72865c`  
		Last Modified: Tue, 04 Feb 2025 04:42:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:341850c6978a6464e7aeeaa593c58ef21565d758220cefa1bf19ca31076ab7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d885359a7b1235b365e7926305f879c216f22a89b51c5eea2465ea853ba93266`

```dockerfile
```

-	Layers:
	-	`sha256:29617dec5d6dfabce744cda25872de8eae4932474131ccdb4fe370f4e1cb9027`  
		Last Modified: Tue, 04 Feb 2025 04:42:22 GMT  
		Size: 3.6 MB (3619407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1341e23482ca1aceb571cabca0021f10b64aa9e00cfcbe1c95afe3a6c27a76a8`  
		Last Modified: Tue, 04 Feb 2025 04:42:21 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:701fc3fce2103d289d8382612df57753e4685cf33797e68ad340bf75f2bdac1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44184275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2569c98ae77c4bc97c2e3d0605493f52fb51d8f13f959d588fc84bf61fed52`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:67233f4ea6c9cb8cfef1bc9f23f922545d9c94c02cfd1d0dcb6a972fa303193f`  
		Last Modified: Tue, 04 Feb 2025 22:20:51 GMT  
		Size: 44.2 MB (44184053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bec94b895f770fcdf817ff97461600becc583b616d046c35b2b5f455ca6fdaf`  
		Last Modified: Sun, 16 Feb 2025 01:41:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:30e0e845bbba9a5353a6bc1430c92e2774291463918299b4ff5e1466ebdfd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9157a1d73a424f005993b94fc574b656e6cd4276392ffac34402b8a1eb6bb56b`

```dockerfile
```

-	Layers:
	-	`sha256:7e127ab166677a703af4334ee3e2d844880d3eff95c25c8f5258735646cb608a`  
		Last Modified: Tue, 04 Feb 2025 04:38:42 GMT  
		Size: 3.6 MB (3621385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eae4a3d241fa41c5213f48e72b8c524064517a7a56d163b7de34a6e573a5ed5`  
		Last Modified: Tue, 04 Feb 2025 04:38:41 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ae034d6bd46bc2f060f7c171a23ee8b64b936362ed39297946b5adcc3d578607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39451112ae30f22ba6b88f01363a8b4d275c0787e1a8595444f5fc8e8c262ce2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3ce4739a2fb5337f630ce6a8c0a3a59c079f60570774ac6ce826c0ad3e7d62c6`  
		Last Modified: Tue, 04 Feb 2025 05:05:44 GMT  
		Size: 48.3 MB (48306555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dd49832754db880c79bf3ed24e64183a4b0a9c697f91b2c64d5914710928b8`  
		Last Modified: Wed, 05 Feb 2025 20:30:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bc80dbb565ba47a81cb49adb1e64144d48129899d83149e99d4eef37dc9c7fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942fc8fcaa65a3fa7f98801449ec081d4a21fa42e7f7d8198907f7c4ec595582`

```dockerfile
```

-	Layers:
	-	`sha256:802657ff1f983f6399e956103e25a7040b856f4e141e6113dcf62a508253cc9b`  
		Last Modified: Tue, 04 Feb 2025 04:31:40 GMT  
		Size: 3.6 MB (3619421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5adfe5722c9f4bd4e1ea47951d47906165cd7bdc836372c87f62e31b7cc96d7`  
		Last Modified: Tue, 04 Feb 2025 04:31:39 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:ee5ade08c3ac98fe5de72fd4258fca8b4ed6c1fe1a732e950b733a6e73ab7c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49457680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3066ec7b1ec14c1766a31d3b4f77d9f497e52c7c47a971ac6f7b3bd0b90eb5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b2592673769d5b11854ec1c7491225981e2f0755ed19d58cc5f0830ce21e0e91`  
		Last Modified: Tue, 04 Feb 2025 06:07:17 GMT  
		Size: 49.5 MB (49457458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3cf6c60999450921fd5ae98127e738fca37f2edc3524bc26a1d46a663d2`  
		Last Modified: Tue, 04 Feb 2025 04:21:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6babf2260f09d7141f2dba88df4f9246ae341a51d24cecc10e2a85403396bb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7248ce80be6eeb063d7f82c009b7443456a2b101b7527d827dbae9d5316afb8`

```dockerfile
```

-	Layers:
	-	`sha256:0a9ff32948c94ad82bbf1866c6fb6a68b4de8e6cbd531a323343368633cb52b3`  
		Last Modified: Tue, 04 Feb 2025 04:21:47 GMT  
		Size: 3.6 MB (3616367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3e75af1578021f8fc3bb2e8880c4eab899985cf97e0f3872245d87f2bd96a3`  
		Last Modified: Tue, 04 Feb 2025 04:21:47 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:06e71fecee2c3c684100f9cc61d0d94f81d20c96de74a26b15b7a6a82b657cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48758024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a5c82d7d9a9051aa39b4340063299514f612476b09699a26fbbe6cb57c0fb5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f036f5a30f3d8f42f4daaa108195d20ab9d38d4925e1f9113bf8cf3759a36e81`  
		Last Modified: Wed, 05 Feb 2025 02:07:03 GMT  
		Size: 48.8 MB (48757802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3a8714f9b47b5e7ccbcc7fb4dea01088e5feac3a6f3208b8b72e503af4e39a`  
		Last Modified: Tue, 04 Feb 2025 04:31:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a118215eec5e341ed9e87d9e3ba3af5491100c29a65573ff7d7d0c24d6d582f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48968f2e9fd8e23e5973284f4a9f070f580c36d35248b263b39d267c4beaf14d`

```dockerfile
```

-	Layers:
	-	`sha256:3213ca52d1f14ec17d03846950c192fc718e4832900b9010ff355d9301d1c07d`  
		Last Modified: Tue, 04 Feb 2025 04:31:59 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:1c59c1946914478c9e2def7e80f360f07e568cc1d967bebbda3f1decd46f0e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52313081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9653aece1ec49316732af586791afa7ecef328105d115fe63c20eb532281d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:56d71f789875e3671914be071d06e017acf964a954cf916d2adce9171c45ed5c`  
		Last Modified: Tue, 04 Feb 2025 21:20:54 GMT  
		Size: 52.3 MB (52312858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ddaed6e591371cb6638b2dc80abe29ba97b2e85ebc4eb1aa841ea75b58a63`  
		Last Modified: Tue, 04 Feb 2025 04:22:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5f4cd3daf060fa1c5185a0f6659d70198f8641022e87777766fc6869fcaa40dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21000a813dedcc02dcda7557ed3a23908a76700dd044ed317eea3850f94a58e`

```dockerfile
```

-	Layers:
	-	`sha256:8d5cc1f52f6b97a1f645bbf97bae5f804da249c1c2138df49b5a6f7177b482d4`  
		Last Modified: Tue, 04 Feb 2025 04:22:24 GMT  
		Size: 3.6 MB (3623466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16893ded8ad8aad034133ef73a74736bd7595fdd436788f4df4fd4a91c14e2e0`  
		Last Modified: Tue, 04 Feb 2025 04:22:23 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:068aa14a5c67302c498dccdd57e87a1e3d5a187ef272fb91c3e7adfbf53036dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47131717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b579c0dac389b025a5fb7be3f4fe2deffdf35802719073d79e7f33da886a4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d4a29455f76b5518707e7957b6454e32a58bc74d0201bc3f77f343ca5616549d`  
		Last Modified: Wed, 05 Feb 2025 02:07:04 GMT  
		Size: 47.1 MB (47131495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6579f5a58cb43637320b7b6310d4d33e8f17dd74cc92acb7732a52b4d02ccd7c`  
		Last Modified: Tue, 04 Feb 2025 04:27:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dd04289f57717ed9a8db4e395267becaddb70bc5d6c8dce11caa4d7f9165d111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f35123cd27ccfb51717d70c69074eedba647b3e5c4deb72e3f28b42b15e162b`

```dockerfile
```

-	Layers:
	-	`sha256:9bf413b41e960e22c0050472e3e0e25c80d188a275484c53e27376f6f5a65aa3`  
		Last Modified: Tue, 04 Feb 2025 04:27:00 GMT  
		Size: 3.6 MB (3618936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c19d76cd243b41b2b476b024bff303eab4221df04acf52194b8303e7593b1b0`  
		Last Modified: Tue, 04 Feb 2025 04:27:00 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json
