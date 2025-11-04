## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:811f6a9d4f781425ede4c25a06fb0491949e6d3bcb494cc867a25abebe120419
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
$ docker pull debian@sha256:bb4e7794d6918d5413fcc66cdce04e410f47384f128377329efecd1de5e4dbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485004586656a7cbab83807e687c265081f63966d9ff961051731979b8ed5b67`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:29 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78a2953302995173870704d521e7fc56019ac471c81078447ac72b905893c5f`  
		Last Modified: Tue, 04 Nov 2025 00:16:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:302104611b2bd556645a1cd3410c169c0afc86d037131dca1b26df94b4ae63ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078c1d08afca2dd1d280a821e3386a4bddeb5e73b36ffb298c321604fd692a56`

```dockerfile
```

-	Layers:
	-	`sha256:6889fd87b3b64e79b5ff91affb51db0041a87187cdfc294139de21a2da69097c`  
		Last Modified: Tue, 04 Nov 2025 10:24:33 GMT  
		Size: 3.7 MB (3733431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c346866fa37034b1c2ac5effa681f2660824ad3ef96680d79dd14e8953b2579c`  
		Last Modified: Tue, 04 Nov 2025 10:24:33 GMT  
		Size: 5.8 KB (5803 bytes)  
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
		Last Modified: Tue, 04 Nov 2025 09:42:46 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe0e830db236f0593181460bd48900e01c1ff0b90d98f382cb6b8f96ff95c20`  
		Last Modified: Tue, 04 Nov 2025 09:42:45 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:32dced5b11cad6d3753f46f567b5376a0efc73463a490892ce7faf27d097e7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af8204b6afd68f1d7bff0d2cc859201af642652f09c5cd19f4c92f1a5bfce3c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:16 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2819b98925dc0bb41fce0b92a19a2e30ff7d7d7172dade0efec13d4d3a67b4e`  
		Last Modified: Tue, 04 Nov 2025 00:16:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:604c213b1fc99062f6b966c4fe455f6d6ab93811c1a800808ab8e2739e713659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98823980be0f5676a5737aace1e0aafa24586867646aefa20f10e42f0054a68`

```dockerfile
```

-	Layers:
	-	`sha256:8b87500d869ee962f492c96e2d1f54405567a6e681acc1589210bd5ad1286346`  
		Last Modified: Tue, 04 Nov 2025 09:50:37 GMT  
		Size: 3.7 MB (3735610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d15b100d05b07cd9d66fdf647952c374a32c575d177a5722b9921fa501635e`  
		Last Modified: Tue, 04 Nov 2025 09:50:36 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cd9e5f516f9025ca08825836bb34888abaadbca9a78b0b7de674868481a23b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c45925d5be27ba8b5578be0595f419ac00eed4c3e1e246890364f8ec1d5b00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:48 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735035e755c75747a1c061bbad8815fc85b109dc62f50d35d74848b0a860daa`  
		Last Modified: Tue, 04 Nov 2025 00:17:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4a586e64528ed55374d392da305e369aa6256086d877b2e9f577694747d6a0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8cf4ca219e0e41218c922b154afeebc61f676cf61312adb63ed7758a415607`

```dockerfile
```

-	Layers:
	-	`sha256:31132a8ae43683a7f7b7b49a5191e85df6b0a9a37ef48e59ba4016b4df882b59`  
		Last Modified: Tue, 04 Nov 2025 09:48:28 GMT  
		Size: 3.7 MB (3733646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0555cc7e8e0f347d4bf698e164821f52c0ac918561b64aafe8ff5dd731537a2`  
		Last Modified: Tue, 04 Nov 2025 09:48:27 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:f89e403b88296e6090a0d543c82e471cb83468933f0207a2cd1081abfcc15f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1418932e2f868ad688ad86ec946ccbaa8dda241b94e36c69d694cc119beaa04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c503e575ab7f4f377fc6d4ad3f29a5053f19ac934415309bc24ebf3d44a732e`  
		Last Modified: Tue, 04 Nov 2025 00:16:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d09a56a014c9366def0e0c8a8e8c93cbeda7c1f2ab9f7f1745efc639a85b85ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa2653042599b5544ebe4f804147d87816db85d3144eae426f276c03f0d8d53`

```dockerfile
```

-	Layers:
	-	`sha256:98f06e6ef7e2f6498ce5b9ba9d247ee8e8c9f8356686e8f4406c02790da548ac`  
		Last Modified: Tue, 04 Nov 2025 19:04:06 GMT  
		Size: 3.7 MB (3730628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1fc5fcbe185c9add057f877709b7b419067d86e10d08a063e9973546647851`  
		Last Modified: Tue, 04 Nov 2025 19:04:12 GMT  
		Size: 5.8 KB (5787 bytes)  
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
$ docker pull debian@sha256:f057b9f894bc800cfa48e288d6bf64da25545dafffadf94a44f21dce937c31b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aef7b4a44fbb5804adebb02f1ef1841c70e36960986b8e6ed183cc0220c402`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:23:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eef8fa7df18201ef439463e1165896d92c569df653db8c16c31a1059098af1a`  
		Last Modified: Tue, 04 Nov 2025 00:23:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:82fc5e491ec22add72d9da229fd9926f26eb5558da348be28c40eb5b7ca6ac21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8dc9785112242279be18959896f1d91f2e3a1113c1b6967824468a7c529b41`

```dockerfile
```

-	Layers:
	-	`sha256:7fb8335ea950b13d0d2d37b5e0615e60572278195db1318f23b47aee881110b1`  
		Last Modified: Tue, 04 Nov 2025 19:04:53 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121169e4ef75532862084d7e07e5c4f326360ca8c7b3228d37d6140e3ffa28b1`  
		Last Modified: Tue, 04 Nov 2025 19:04:59 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:d886d544b2400125b63b5d0648203bba037a3ede9a2612cb923c149fa706217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f290649150003a9bc20c11e542c3ea66797d788f890d808e3f508ac040c25e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41960c4a450ec1308304b0c520739b603755b48dd8f61dcb3b912133287c0ab1`  
		Last Modified: Tue, 04 Nov 2025 00:24:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e49064200dccdb9ed1a264af95407729f2494d61b0dc1c42d8956bf4ffba32b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af18a85270a862d6fc66c60e3124e2f632d17b25f87c555ee8b2618f08e8da9`

```dockerfile
```

-	Layers:
	-	`sha256:3b58a5a001364167ea0ca0f228740959609209b239a7a2d519b5933f3ed278f6`  
		Last Modified: Tue, 04 Nov 2025 19:05:19 GMT  
		Size: 3.7 MB (3730269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3ca7a1f49203a65e81cdf11f330ba13b98a26a8771731e22cc479291312dc95`  
		Last Modified: Tue, 04 Nov 2025 19:05:26 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
