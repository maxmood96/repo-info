## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:56054fdff112573e78b4ed628d9d6e55476fdc7ea8c591000198119a0ee7071e
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
$ docker pull debian@sha256:7248a408f09d474be7d007ee779a199851ec9009ca875feb58b60d4052b689e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee95127450482674b0686fd7010032f0e4e8844cf82eeec3f747b06690177d6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:20:10 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d0780482d9b97d506bfd55bf3b805f2de1b9731c75e1b5800b5d53bb5388e1d8`  
		Last Modified: Tue, 04 Nov 2025 00:12:37 GMT  
		Size: 46.0 MB (46016089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5740b655a9481f63493f4d587c2b76373f5a32a7d27b0fd166b524630d9b3e6c`  
		Last Modified: Tue, 04 Nov 2025 00:20:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:04564067c9daff96daa2c96f6fcdd3f68f65b3ddfcffa2f8e5517eca799ce233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1538dc7ba627716ae0588a52576c72045e2ea6f9b9fb6dc52bafc6d1c16b2c`

```dockerfile
```

-	Layers:
	-	`sha256:93c500bf568339f1671756f4294526a0b9953168e2ab04fc0e9eac1412eadef8`  
		Last Modified: Tue, 04 Nov 2025 00:20:18 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe0e830db236f0593181460bd48900e01c1ff0b90d98f382cb6b8f96ff95c20`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 5.9 KB (5860 bytes)  
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
$ docker pull debian@sha256:568a3f676178be4d1021ce0c51f2244c2adf8ef2810155148994d0d10791eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48761509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a132790aafc4d29dac5b1d2a3d440b327bf63ebae6d98cab02eeff235c7bc6d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4dda2a1b7438becfe8c22a70ae85ee418f80df0feba9ce91b9ffc92338d47792`  
		Last Modified: Tue, 04 Nov 2025 00:11:16 GMT  
		Size: 48.8 MB (48761282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1a08a097aa51a26f1bf121eddba164caa1a6becead90fbf6d68b703360da6`  
		Last Modified: Tue, 04 Nov 2025 00:17:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7fde2e0b27a0b2bb8e4050eefd91ea53d9b99e3e6b68132530f5dfd19fee7612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007b794c4d4201f7ecfdde08843c488ddd78881330aadd1f0b1a2e89fde83b88`

```dockerfile
```

-	Layers:
	-	`sha256:f457a041982658e9d122b2af88e0c3f809815fa533211a46e80c8ede69c3e9ff`  
		Last Modified: Tue, 04 Nov 2025 04:25:44 GMT  
		Size: 5.6 KB (5628 bytes)  
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
