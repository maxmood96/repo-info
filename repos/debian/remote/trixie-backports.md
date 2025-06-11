## `debian:trixie-backports`

```console
$ docker pull debian@sha256:f51f25d3845ae233858ba02b875101a362c14464290e649cf826cebe171e9b87
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
$ docker pull debian@sha256:5843eecfda7ab4d06ff4c86b88890a636a18f45a2eac8390dba9a6259f3f1d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49254082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8d980a0e3a5bff8a01ea8827c74ee769276ca38c554c66ab6e2c26bfc923ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4127c7dd0c0eb60c47e7862bb538665715f9409a91f59b2a44e2cb2dbc64327e`  
		Last Modified: Tue, 10 Jun 2025 23:26:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f85aa6d9a13939a17531f824fc82ebfadf160b8dbc496add729a9900c0a1bcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a356117d065f8cbbae892d12690aa828b9163c1057da0352b952aac0a7d7bbf`

```dockerfile
```

-	Layers:
	-	`sha256:c0f26519e38c1d37d37c023265e32c50ca52e6a00d354fdddea42ef0d01b0696`  
		Last Modified: Wed, 11 Jun 2025 00:30:10 GMT  
		Size: 3.2 MB (3167836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b06c68ac969433b89a3d237c05042c2701515146ba79329f1d1e2f07b517c694`  
		Last Modified: Wed, 11 Jun 2025 00:30:11 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fdd82dd652e7fbe037c349ff1f48ba284ab842f32673871855b1589546375fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47445633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bae725debefbb817be1771da625744481ee0ae35103f9f4f7fe81e653a3414`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0b3435ddf0421631c0396c34acfc4d54793f2c51e2a8b92677402c8f9e0513af`  
		Last Modified: Tue, 10 Jun 2025 22:50:33 GMT  
		Size: 47.4 MB (47445410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1c01943bea3f4e6d49ada56b1864a5d91d1d578eb8f359259f8896db2bf79f`  
		Last Modified: Tue, 10 Jun 2025 23:25:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6027b7d7e3bdeb3c683e187cfef3cde946f8078c3fcfd0e23a4b226d446380a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a436821c1bb7ffbf9f8b8e505246c45f8b97458de4908850121a4b76cae062`

```dockerfile
```

-	Layers:
	-	`sha256:36be02924706ff30ded0544ccd99a8a3b4fbbc4dcb6c5852e57b7cebf7f613b0`  
		Last Modified: Wed, 11 Jun 2025 00:30:15 GMT  
		Size: 3.2 MB (3180026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edcaf64f7b8cae1fc5e3c9d3baa69e486241ed713fec40242e86706409ca39c9`  
		Last Modified: Wed, 11 Jun 2025 00:30:16 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4d69c6b22100899237b4657efd0d09519e0310e25e2c9e44178eb3bce5bfd5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45702268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac17024d818023cd7ac3763b3f276a2e4560d40736fcee6219fa95f693385203`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c6c3b2ac1d8de7f6b9efb67d4f8df7036728aec7a9268a04eebbdddea82d555f`  
		Last Modified: Wed, 11 Jun 2025 00:29:31 GMT  
		Size: 45.7 MB (45702045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50f042885bc32fba40a816fd96f4cb83c4b4274c6f976f0477852a73f5cbb54`  
		Last Modified: Tue, 10 Jun 2025 23:26:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8e61fbe345c6447dd89b47d0461dd19349d92ba5eed8e58da0088eb295e8208a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e875a741521d2afd4f2c5c095852c66b4b94a56038c463f6b430d8bbd3d29ba`

```dockerfile
```

-	Layers:
	-	`sha256:9364c87fde9c8e3a9694c5573234b3ea6216fe67a7f0bf52b7c5c1514da46eef`  
		Last Modified: Wed, 11 Jun 2025 00:30:21 GMT  
		Size: 3.2 MB (3169210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7f01855cfe97ab82c2f6f6b72a68eed34d268a4b82d0d0f339540ac6f51e16`  
		Last Modified: Wed, 11 Jun 2025 00:30:22 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e7924b35184d9c20222967fadb3451c7ce29091adae2d47070c0015ba3058fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49621753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285ec19fc66f3c23ee6f600b569b512bea3522491c7156189773a61e1ae12ae1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854e7a28ae98d37404d2a52e65fb290adff237281a108da4ccea32cd4432be39`  
		Last Modified: Tue, 10 Jun 2025 23:31:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2251635fef6d241df32c99dcacfa2696bc66bc8bbadd8e8b7e06c574c0b4edc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3139ecc60012dca5d94e5c03d253f61a52dca5052ec195015bbf4f392b11d833`

```dockerfile
```

-	Layers:
	-	`sha256:2effc9e1c5f89b6e2d98c1d3f12f385e10f3b3678c57e54ffb4c5a092d2e56f5`  
		Last Modified: Wed, 11 Jun 2025 00:30:27 GMT  
		Size: 3.2 MB (3169317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f4af9398dfa697715eef1900ca3c032bb05b1c2d4831c9eb264829a3836ffb6`  
		Last Modified: Wed, 11 Jun 2025 00:30:28 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:2b58198daeafd5257481ced50d26b2e46b967e1422afe7730f20895115e2d80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50765837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a871d08a76b19fc72d01863544aae8e3ebdbe2ff15f97580ebaac5e1f6407753`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f24aa3f80422a60637035cbe1e280f72c031e00f6d803abf75d114fc69f38e79`  
		Last Modified: Tue, 10 Jun 2025 23:26:07 GMT  
		Size: 50.8 MB (50765612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db702b3a43d0929072b15c2daf81aa5b04572f8b744e6fce1eaf65d9608f9a5`  
		Last Modified: Tue, 10 Jun 2025 23:26:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:56306cbecd49946febba52214ceb46a6f9979a7fa3ae89a0e44813bcfcc8bceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3170850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba839908b9307672c15f80eb36db957ea91f76c85e35c3a6e15e7d0b1d3a19d`

```dockerfile
```

-	Layers:
	-	`sha256:74f8163da370ac55ab6330074e97d6ac9b481dbc8605933b46ae49d4b2c6b8a7`  
		Last Modified: Wed, 11 Jun 2025 00:30:32 GMT  
		Size: 3.2 MB (3165040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f05da6ac807728aed93467e4819f916a6bbf615921708939a00e4e90bb92851`  
		Last Modified: Wed, 11 Jun 2025 00:30:33 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8c1ff817934e3472431bb5943acbc6b1fb09c8164c24bd828f6e5a09a9bbec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53091158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b25a7c58caa43ebaaf5431796222805d1ac14e1a1fbf1d4b296715bf88d37f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3507eb0b2914f1f0c7a95f2a293c0e88f19ef85661023a562eee57882943039d`  
		Last Modified: Tue, 10 Jun 2025 23:26:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9b3d5b34ea31e758dd08493d63b6e8ea7d458c24f9e3ce170601b79471684388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3186451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c098c9c2fce77ac2ed0d164cb1eee25bee06043ac05044f84d3b4fa021bd69`

```dockerfile
```

-	Layers:
	-	`sha256:ba14f7738007386df53286bd1076e847ba1b724757bf679e8c0e51566c3db7cd`  
		Last Modified: Wed, 11 Jun 2025 00:30:37 GMT  
		Size: 3.2 MB (3180598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfbbde1fc2d68b88dbbb49c1125d6f3117b9b546a14fd11ce41c9ffbdd4a7fad`  
		Last Modified: Wed, 11 Jun 2025 00:30:38 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:83d2b26e3e4c8ce0dcc1d86064135c09de10bbe1d61263162da47c6b1e2fe87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47743569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cacd5fd167e01f9aff3e79fb08d9d5beb0a18e3735a2626707db3631c8a608`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:183a50217c4846c3775204631f79c9cba563face97fcc3de4421f000af401588`  
		Last Modified: Tue, 10 Jun 2025 22:56:31 GMT  
		Size: 47.7 MB (47743345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ff13ebb08514cadab530bb94cc7b48799bcbd20677e8f08c279e4ac0903ec6`  
		Last Modified: Tue, 10 Jun 2025 23:28:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:14fc99e26f46a370f9d295a8474215cf67eba53b1fe3db1fca6a1eecdfd9b5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c944ea6aa4b1520051d8b6de8fbaa65a44f2686f78b3e433ff8b67dac767e1d9`

```dockerfile
```

-	Layers:
	-	`sha256:48642d9815bddbcc24cb6c2366e5754b4302a495e71604bdd8e6d78fa8465bcd`  
		Last Modified: Wed, 11 Jun 2025 00:30:43 GMT  
		Size: 3.2 MB (3160157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3203870b63b07f489fb64cf4d11c1480b5cde9b397118572570389aa794d5ae4`  
		Last Modified: Wed, 11 Jun 2025 00:30:44 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:f45dc058a37000a963ebce0ee8682e8b590379e9a3babc7c4d9b4872ab193f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49329992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067c1af9a72df9c9bb73ba0961b48c2812ad9ea18123ade3333a5e283cf6ae8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4903b8611a11aff147e2cdf55754c67b86a5b6edb3584f1f256c15c4d4ef62cf`  
		Last Modified: Tue, 10 Jun 2025 23:33:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3675364623adc7da820aa55a77089391c30505b32dd6088a33f7f148a1abca9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3184363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9edfc192606469719c50599e8877df14e89b979625e2cd6cfd9b008b65208ba`

```dockerfile
```

-	Layers:
	-	`sha256:83a176e3622b1cfe6a5d48dbe29816a34d99ed6a910ac8d8b07ae00447aed8d2`  
		Last Modified: Wed, 11 Jun 2025 00:30:49 GMT  
		Size: 3.2 MB (3178536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa72a82ef8f7d2a09c2c011883737d001b55a1a8422f65ea7ba321d23517b8a`  
		Last Modified: Wed, 11 Jun 2025 00:30:50 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
