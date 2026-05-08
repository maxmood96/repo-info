## `debian:trixie-backports`

```console
$ docker pull debian@sha256:c8bf17dbb5ce6b0da81966747a43a56049ebbaf5420314b062b581aa29ed7ffc
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:762775cbd3a0ac3bd21c71c8dfa939ecc127726a6af0639770c42b1729ed6b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49302543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9a8b7edc98930e9efa71558f2b52f9babce46fb50aab3bf11d5d0754820424`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:14:39 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d065dfa91645a17ad25c111e3710fc087974714f0be3308a335a156b915e308`  
		Last Modified: Fri, 08 May 2026 19:14:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:74cbf2ca4817ebecfb4606ebc83e5b2a7555b27407a6c12a5daad6ca5efcfe02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93fdf9f1401558b4b75b87635093d8ac963c1638f626df3abb1a3bd6efeba00`

```dockerfile
```

-	Layers:
	-	`sha256:100df0df420c419f5b39e7287cb516b853f0bf986f62e6dce520004fdc615b3a`  
		Last Modified: Fri, 08 May 2026 19:14:45 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121d75fe686a78cb6aa86ad7b2b3d8a86bccc0cd79ceac40fd02f5a53d61446b`  
		Last Modified: Fri, 08 May 2026 19:14:45 GMT  
		Size: 5.8 KB (5783 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7b1e02ed5e57a1895e3cdd3e91b7ad4a8a1d81ccb5dfff04dd54bfab395edc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47466516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ac5747460532e2197ac2bd4a885a67f267a24dd720f60a335bc37840f9518d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:38 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ab1ea4901b2e5ef4c23bc85e77bccd29b5e37409a6599c547024038487caa48a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9972ba47db8e055cbccc7803a8ed6e834af2cd5e9524bf3c292908fe8b7e32`  
		Last Modified: Fri, 08 May 2026 20:25:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:247a87da711ba4fd127be0ceb4b9f65b91d6fe65f944150cc748265eedf482f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2640045ce22eaaaaece59eec08ebb3525b723879ec59b057a52a9fcfa1e4bd`

```dockerfile
```

-	Layers:
	-	`sha256:a6f1dc831aaf373ed620dd16f561a41804c844a720ae2918be1493cfbaa8bc3e`  
		Last Modified: Fri, 08 May 2026 20:25:44 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:168ec72b1ca9f9d2cb15da9e9453fe4cd184dd9ebb58b63053bdc13669c41eb5`  
		Last Modified: Fri, 08 May 2026 20:25:44 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:13746549513e293dd12c181f8905b2f2a37105f69ef732f254f277fbf9f77c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45738649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2aa0aef55f9defba1b1b46e530847bbd546872873c6edf29b19276f003eda0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:15:03 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014360185d1b4e421ccd735db3534449fdbb1441d65f099c39b39b024206692f`  
		Last Modified: Fri, 08 May 2026 19:15:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:01968e25cbf2bebef08d384fcb22a8ebef12c84a69e01cbf25a9f9b98208ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec6f9dc4d1a3491b60a3d763934c8cad5a3468729b78297677b5f641fec374d`

```dockerfile
```

-	Layers:
	-	`sha256:fa7f3a93a01320efb35c18620528617550c32a0dfc7d3c493b03903d796645a1`  
		Last Modified: Fri, 08 May 2026 19:15:10 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61374b4acf1233a7c8b3d4ea26038db389e335bdf660500ded85b5e28e673f05`  
		Last Modified: Fri, 08 May 2026 19:15:10 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9b76bd6693779811c78da3793173e0a29bc030d684ca2c0c24ff51e87ff33c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49669670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed70ddd4dc5ab7c89e7341fa6f1abf407008a9f8169320a5c75735af58a67e64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:15:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2f6dccc05eb9b2ad9ee16d78f31a14e580390b81c60bc38cad024a788ebc3c`  
		Last Modified: Fri, 08 May 2026 19:15:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:90abe8eb5aa89ab9e47627b54b0c4badbfb54bf6605772aa1a54fa8743e7c6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1257bb2e36553415735058da221d2d2d53231ab790f998c2e367760e22715ced`

```dockerfile
```

-	Layers:
	-	`sha256:915d555724231617163b7744c3aa175809d6c5c8cf820485908f27163cd61307`  
		Last Modified: Fri, 08 May 2026 19:15:07 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2abbbee99e44d35effeeccd13c90a6f87f1ab0801d20b93f8e86dd02c848a7f`  
		Last Modified: Fri, 08 May 2026 19:15:07 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:a9c2972cd46da3bc690f747596452bf7832b05726ff540285825d42389d477ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50825806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b93ff7d0d07210cbb1f6e986d446a56a95446aa1ada0ae62fd2fdb30530eb38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:15:21 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcd65dd5bbe8a3af3d5374c5174ece99dc4f9fee14eb5370188a45b5d3f9039`  
		Last Modified: Fri, 08 May 2026 19:15:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9c3a7ad197089d64fa4e77e24e65889a67f29065499c984f609684f98ea2d75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f46365ba5e8e89d5eeb3c753b08c3657f39f08ae042dea964f6e61923682c1e`

```dockerfile
```

-	Layers:
	-	`sha256:a47d32c91d69c3897063db6b9a59d3a60c1925941bb1d3d9005b7bfe3af182d2`  
		Last Modified: Fri, 08 May 2026 19:15:28 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ecee3ba1dacece276eb6b7f8b2956e3e7fe705caedd0abe20888040b19c6d1`  
		Last Modified: Fri, 08 May 2026 19:15:27 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:abafe74a86277b46ba0d3d49179c400208037ef38e475b8f3b3cdd0413ee277c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53123389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf94ebccb8e55134c0f7016d03b9941318e824d4f147cf59b79133bc34650c06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:03 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f0c99724e83810cae235ac31093994234126a706aec8812ead3ab601b96a47`  
		Last Modified: Fri, 08 May 2026 20:20:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:472ec27e4183e06f070ca3850173c0541ae37c649deaf0c92d78bae0b604f1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce70873019c0eb8f72b839d08a29edd637532f9140be4cb752871033029271c`

```dockerfile
```

-	Layers:
	-	`sha256:7b4e0b4bbbde2219f940e2dce01509c3b5e4186d1c38a470291b937dbf277629`  
		Last Modified: Fri, 08 May 2026 20:20:21 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:766f846dbfa14a8ffd18ffa60d3968d447b6d30e705871c6683a348bee6ef67a`  
		Last Modified: Fri, 08 May 2026 20:20:21 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:12958450b181a40a831421b5e879ecc31c05d84f1a0c34fec20bdaee632177dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca59481aabf06cc0b4a5118a4fb45b7bc7a3430ae802e44336d6daa2e593ceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 06:01:36 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0c89056b1a32f4449f98665686aa354cc42579d832e5ee4d84260d617afd7c`  
		Last Modified: Wed, 22 Apr 2026 06:02:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:84a8d662b8ae4952e567382cebac85abf321042a96b37296a9197c3df730bd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606ec302d310ffc7238c69988d1e701310c3e480a1718f8731a466c9d3a7d6e`

```dockerfile
```

-	Layers:
	-	`sha256:7e988e9ecc776fb0302191297756f7fd497c1ff486a73553b1f2dbbdcb4205f7`  
		Last Modified: Wed, 22 Apr 2026 06:02:30 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c83edabc2b7ca35a71b09b03f5d205b90f703af0b303e9cfa68dde89a0a617e0`  
		Last Modified: Wed, 22 Apr 2026 06:02:30 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:b9e352800e8b8f78f729773b87b60d4a5d82d1c033085b0d379018441d01200f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49372528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583be80bf49f3aa5cc1772846813a397a0a502216fd5e824ac4ee9fd1c07e58c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:14:17 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963ff8b690a7b064950179590291c9026642a0a8b521b7f85316382eedf58c91`  
		Last Modified: Fri, 08 May 2026 19:14:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3bbeb03a9cc06efd247f43cc0dea0752ec566ebeb346e55fac526ada85add2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02154590441cfa32bb87dfd8ce18cfdc41918fdf20efc85a8adadd7e9fb3a5a9`

```dockerfile
```

-	Layers:
	-	`sha256:1008c3700ac964ec9a8ad4660587f85c5b64eaa559de96e3412de960d9452da6`  
		Last Modified: Fri, 08 May 2026 19:14:28 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe0d5b7ff63651ff44aa8f59051367f05ee388dcac54244bf7a7a0a47aa8bc7`  
		Last Modified: Fri, 08 May 2026 19:14:28 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
