## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:6308d7321cb05a12ec75a5df5ad560a9f7669e73031260704fa1ee9d915f0f67
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:9b578349adf1cf3489417fc37f4c60ab9e4f653366064d0c7b652e38b92302c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca53621086249816853b6883fe47735679bf2f1b63929a2e73027355c568ddd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4a5497d78b4af323da3bfaa3b128810b53fc1052d7464352f9865d5fb43be8`  
		Last Modified: Tue, 21 Oct 2025 01:15:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ec43cac3544c6e0c29d76eca5cdb28e58fbde29bcb93b971bc9e392396e37dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cad5de319b483cf199d549e1c065660730d51bafe659f5c5072313404bc7a27`

```dockerfile
```

-	Layers:
	-	`sha256:31f7e9fe3dcfaa6711080f80e0d1317b8da20fa1561583f08f7d8cae4d6ebebe`  
		Last Modified: Tue, 21 Oct 2025 09:23:44 GMT  
		Size: 3.7 MB (3733431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16993ed66ec71559aada23d9b88e14b4ca6b39368a5c85de67a60a90859ab4d`  
		Last Modified: Tue, 21 Oct 2025 09:23:45 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:39251ef71048e5a19e4a3fba1858c5af444a905dea2ec7ca4628892d381c54be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb29eb8be5786642eeab4e4371c2e3147d9204d05e5f0e28e365c849f8794de1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d6b0ca95b13ee68ac33e867e046c01d5a40daee1d76922dab47dd1edf2533e94`  
		Last Modified: Tue, 21 Oct 2025 00:19:45 GMT  
		Size: 46.0 MB (46015580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a5ec4b061ae3cd8aabf7816e98f9cb7c21461e0a01aa7ef9e91491fab410a0`  
		Last Modified: Tue, 21 Oct 2025 01:15:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:00cf3317fe024b1a94abb25303e6a96b591a632fe29ed9d9eee861c5a3de6468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f82fb31012a1f39a8de00a22042f6ab5c67e751b02e44dd345a3f8aa85f043`

```dockerfile
```

-	Layers:
	-	`sha256:508d51150f388f61e7d73efac2c7dbbf3e0fd6b6c5ecebf4c139fca9c1fde38d`  
		Last Modified: Tue, 21 Oct 2025 06:23:39 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d11b19eabb61e297b29da68aafee503e7d941e5bbc47a33047d6d9956a88435`  
		Last Modified: Tue, 21 Oct 2025 06:23:39 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:aa6288f2ee6a38820a646c32e6e8d2c455cdb75a5eea8009f0d0600ed39f24d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21743c82e6053a7411f082a60b084303a14792ce045b158ae4522b4976a4b15c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0a19d71e3760fac3a3e0997502eea2419e1d44832eedba0e00b224c04194a5`  
		Last Modified: Tue, 21 Oct 2025 01:16:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b35abd30d243f07116119be5dae858c109f372f5bf202e5ee34424a3d0307a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67c7c48cda760b131cf22c0dee53c3a38c6b716d91526343e0a30e3151b4f4a`

```dockerfile
```

-	Layers:
	-	`sha256:68a4f37c51dc0c582994f3e2aae220732689331343e98eddf9c3880382f834f7`  
		Last Modified: Tue, 21 Oct 2025 09:23:52 GMT  
		Size: 3.7 MB (3735610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da93fb727d0adb16b8f6e9d24307075bb23ee8f78357f29c10ff1898b8a931f`  
		Last Modified: Tue, 21 Oct 2025 09:23:52 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9d9b5e33910fe2f6bc2626ec3edffe70a065a02d2dde8448f3f230803e65fd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd1c3b471afbbc32bf3f9da1b1ed29ebc798a90591d9460d9f8007edb740670b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1bd9403ff5f78109bbe329c548e569d88c585da8eccfcc5285c1e53cbed3db`  
		Last Modified: Tue, 21 Oct 2025 01:15:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b9611b40d66bcbd9a92103d90265924478fc61d383cea47e383df2dbfc4cf77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f42a27df752cd4b6b091fcea377e46ca9c6eb01890bee7d9c5457f8792c912b`

```dockerfile
```

-	Layers:
	-	`sha256:55850153dbdd6f484d940a31464ff2d2f2b2ccc1ac744498a8ebcd58fcb27fbf`  
		Last Modified: Tue, 21 Oct 2025 09:23:57 GMT  
		Size: 3.7 MB (3733646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ec4207ca5827fe5258a53e1f26af309ada4f8ce72eccfe3d5655496f794f82`  
		Last Modified: Tue, 21 Oct 2025 09:23:58 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:32eb66a7ec9b2693ada481d610983b05cb478915785ab5bb44fd5ff902f25a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49466943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44227910c3d35885d1faeab64c17e2991e646bf78a244eaff632f74a0a00fdca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272c419d5b4181646f08cebdb83291b3fe220462440bc2a72722785011b3eb0a`  
		Last Modified: Tue, 21 Oct 2025 01:16:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aafd0b7d4e975e8128a8f51b8821ebe1f457672a64278588a68cad6c29ab48a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deb59699647d2c138f2dc067ad856c67cb26e07566e4a5b7dba5dc559a8114c`

```dockerfile
```

-	Layers:
	-	`sha256:92c8f60c78c22a5bf1a8db54c979787beb5715255c31c37ff649bdce22352af5`  
		Last Modified: Tue, 21 Oct 2025 09:24:02 GMT  
		Size: 3.7 MB (3730628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b039d7f98b8b8e795ccbba1db6da8be97bb9c2544f7eff422782f21aab41735`  
		Last Modified: Tue, 21 Oct 2025 09:24:03 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7b44a5b1248a85adce704282385fbd65b3fcbd53adb0e465f830b48356b80ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42a49df2d32d9c89e99a2367876df53230b2d289104024b9bb4b79311724054`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b21ec7cde651bba78c2172870d970898cec8bbf18d8eb75ead7505f7b1912a3`  
		Last Modified: Tue, 21 Oct 2025 01:15:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a9f1abc166535d4c26b79e27ed18b8ab58fa387b501834045a2aa594a6f999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd0f0ca4be26a322e6ec1959eb06e46c39812141b7e658a17f932f506e28f90`

```dockerfile
```

-	Layers:
	-	`sha256:9fd43369573c2a0ca965bdbf14d41f1a4468fa47753c90a71ad36adc20620ed9`  
		Last Modified: Tue, 21 Oct 2025 03:25:39 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cd6aef2d16c3b56697f5b4d235cb7bf5ae6fa9c053c05e3f61757b22d0636526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342a3e0630fd67b633240486edbfe2355dfe2fee346280a1d3ccfe03d1d5fca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe40523b540dbe90a8ec0a939b28ab21b1c6fb7529b952e925c7754c4e6ce69`  
		Last Modified: Tue, 21 Oct 2025 01:16:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:38d5069ff1700f3f9dea30da05e2324ca27f61ca35617811643f98db5e6e00d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602a3ea92b47006099aed58ed9e5792cda00150808e6efdabd5425561abd596f`

```dockerfile
```

-	Layers:
	-	`sha256:c010df8b98aa8aa83a78dd8f9d50b8d73efcddb2bdf7eb21232174f81775ee86`  
		Last Modified: Tue, 21 Oct 2025 03:25:42 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd64eab9442d5d085202b731b1bf781f90cbc25b914a45027ee24b7f218816f`  
		Last Modified: Tue, 21 Oct 2025 03:25:43 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:64bb220e6e94164c2de011cc89a9d2c1b3ea63713bce456b09f886319f44e6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d7a3da41c25ab548e9a1e8919e7323e7a6c1f41caa13e3902c63655daf60ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494a85c391839355765ebb6cb991b6e9fe3997dc0ebc5601102e36ca496cf31f`  
		Last Modified: Tue, 21 Oct 2025 01:17:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:729b1794d8f4946bdcbfdc86622a4f82ceb72d0e070100deb27507a58c0a6f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa40f807d640c122847b1c4dfe082c2ed6b46e8e7e3b85c6edf4713a1f54b34`

```dockerfile
```

-	Layers:
	-	`sha256:015d11b72c60cf93d20bd28f5456deb8237c56d06cac2eb9b138cc4e7afcdd6b`  
		Last Modified: Tue, 21 Oct 2025 06:23:58 GMT  
		Size: 3.7 MB (3730269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f857dd84655426f03d656ce5d0a0cd645e6abdb1f990aed81b985eee7703e63c`  
		Last Modified: Tue, 21 Oct 2025 06:23:59 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json
