## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:c95dd007d6f2b0799110d55d7b97d273854c5ff987f2a3e4e04d357142a0dc54
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
$ docker pull debian@sha256:415f273db07b2156312fc0901c0c6028535686d3d23c582dc165416d03c6f9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48494508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114a7f49d82bcb82266f04a368b0f49ef5384878554111a4c32f6d90a99ed05c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea659f8e1fe77f31fe5b0d1dd203e0100381a35f3701f6f7927a460a65fc11f`  
		Last Modified: Tue, 01 Jul 2025 02:11:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:47f31a265b860131dc90c24d3e3913d2a08b8e307ce0c9c5a36764b4e9d89132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f93f416871c7e8a5da1763cde394fd9f8d9a3333cee4adf301078f42a146d5`

```dockerfile
```

-	Layers:
	-	`sha256:f3ddea8db4f9dbbc039e77eb0c1b049c7f4ec8945b5a9effc105e4eb2799831a`  
		Last Modified: Tue, 01 Jul 2025 06:23:36 GMT  
		Size: 3.7 MB (3726838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c12d729c5ca603b242628a6634249c9a2d228e0da3f70fc5559b20001d6fae`  
		Last Modified: Tue, 01 Jul 2025 06:23:37 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c36be58f4592643e174628b8b6d836f6095e36783c35541c675da61fa424cacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46026782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b085cde4795a43712cbd3448014fda8624fa79ade72560fb6cdeec7e5dab244c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01d208698d30e75c289cb2ee99e5f2a75a42e11f8e1b4145f8fb1a881298b833`  
		Last Modified: Tue, 01 Jul 2025 01:14:18 GMT  
		Size: 46.0 MB (46026558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ea0295938f15e924d135b127fd7c78cba2ff8e52a43cf047679858a11d7366`  
		Last Modified: Tue, 01 Jul 2025 06:54:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b48d165f8868a318c76530a8a96d5cc9afd3e0ba6f142b58090a0e4e9625441e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e19625ee3f71083830aa4bd4edaafbfaf3ec7220b0498b0e7cc4557294f3c9`

```dockerfile
```

-	Layers:
	-	`sha256:c0cb684fa0c79a5da4c819cbe0b6059d733975c601d01f67dd8c9357803739f3`  
		Last Modified: Tue, 01 Jul 2025 03:24:41 GMT  
		Size: 3.7 MB (3727039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c7a348d6e5c0978f332d1d1f46fd2dbbec289342192d8e336137916bfd9875`  
		Last Modified: Tue, 01 Jul 2025 03:24:42 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a49d7c2dcd8f1f779cf48b52b8a591499d28b1f5416ad977e699c39f344395a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a914bb1f5a532b90e3f78f450156328d0ee182770959babddcd449e231b0954`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bc2e28ca8cdb751a10e1e014b374d783cdfa924e032e1f9eb674e7fae1220927`  
		Last Modified: Tue, 01 Jul 2025 01:14:29 GMT  
		Size: 44.2 MB (44208177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aded5c4aba0fec85ff0af7161cbe58437ac629a5f1e94b93855b8e143f85ede`  
		Last Modified: Tue, 01 Jul 2025 02:11:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6d038e7876334d7bbe856a4afed35c0182185892707dad103e6c3c14b88cbf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3734916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024ce608a2efe8df4a81722980f28709eca2b0cafca81af8003ee679b8deb783`

```dockerfile
```

-	Layers:
	-	`sha256:ebd541b4f98519de3f252cc957b8d5ba82af461e1779bf198973e26802810e89`  
		Last Modified: Tue, 01 Jul 2025 03:24:46 GMT  
		Size: 3.7 MB (3729017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e16f1fe9f622568d8bd6642e7d7c5add7427c8b1e043cca177592b6255843d`  
		Last Modified: Tue, 01 Jul 2025 03:24:47 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2b31b901fb7d4aa1e79e1896760ca83a117e5b668e2e52583f073458c59adfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48339010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1371aa858888e77c906c45510337425df188d954e4141558d0e015596644d883`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd1d46cbf15b27aabb6b792bbf71f5fe4fd1ef78673245be73eeb5864c206ca`  
		Last Modified: Tue, 01 Jul 2025 07:00:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bf8d6ffe1449dd6ebb148ce16490b78765bdc6145e413fdfa6d8ff5ce4f4a43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6e091de226d726d88e405209babca7007dc18f8743f29bda896494a2edca15`

```dockerfile
```

-	Layers:
	-	`sha256:4048fa39f43e0b7de2ae87264fec88bb586248bca7094955c261d605fbd77597`  
		Last Modified: Tue, 01 Jul 2025 03:24:51 GMT  
		Size: 3.7 MB (3727053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af246bd8345dd3d9382c95fc5ef00853998f4f8916856b201a9277250dbe8587`  
		Last Modified: Tue, 01 Jul 2025 03:24:52 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:af63a5bedcfdba614170c873de17e42a876fe2519ac2683702d535c603cbe102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4186d7ad75c0f271673afc5ffed2e2f938c9d13fe4cd542c4789d0eae7f44f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aa58a2a551d2fd1e97169fcf2be8b0cf6bb79c3faae022b316b8dbc4f26db7`  
		Last Modified: Tue, 01 Jul 2025 02:12:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:64cef9b6564fe1ffbee23f2677d85ba2e9acbc0831501ffc8b81afbe945fa21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b11e34ce9c68e83b88d5e0001d33fa5142331db3140ae3a2053cd0200f84835`

```dockerfile
```

-	Layers:
	-	`sha256:3777f61358bea30d7e6bc36e36c505e6780ec57f8ba52dc532c9643d7611420e`  
		Last Modified: Tue, 01 Jul 2025 06:23:50 GMT  
		Size: 3.7 MB (3724040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ebdd4e9098185d4f8e33b301b42a3441560006ffece80efffe0ed586a9ecd70`  
		Last Modified: Tue, 01 Jul 2025 06:23:50 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6eb39872cb160eec94a6b8596efb6bfed97974483ef3438cbe8711ada1deb620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790dd1402eadaab8982e77b68c14fb7c5c902f685efc92193c8562a53ad300df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:99debc858569995ebc7f6d9290cbc19f540a471b716e06514603892b92705c6c`  
		Last Modified: Tue, 01 Jul 2025 01:14:35 GMT  
		Size: 48.8 MB (48775546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc3f0be1fbd3b555e525ee5d4f97abc5819513d04b5e93190ff602e43cefe6a`  
		Last Modified: Tue, 01 Jul 2025 02:17:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a23ef4c3b724d35bc41eaf488ac3d69e88c96d87f2e66ad5b8a3435a1c2edb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7365f432367ec44bd28c7864fc64bd6b93ebd2e5c11ff40863b43dd480762046`

```dockerfile
```

-	Layers:
	-	`sha256:92ae75d43f1f2d916005ffa74d4e408881db7adeb6eb4a37cc3dec31303587a8`  
		Last Modified: Tue, 01 Jul 2025 03:25:01 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9a9b91cb7c9e664b30ba24bfd3dfe3a57b041ee03b061d26163e44c0a055f95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4763047f92f4a8a325061d14206bec498251d10d7656a9c52a9de8467b4989`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01739691d34dfd628ff2f95ba569c3b1dd0d03de64cb2e3399863ca85b517a45`  
		Last Modified: Tue, 01 Jul 2025 02:12:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:89f1b2bc84ff7b5c21a6c4803f61c3fcb85fe2abcc44254c18e1792f4ecb3486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b992f38f6c1602d07371780f2a45baae24e1168f588ca1687c4cd21af4c1d55`

```dockerfile
```

-	Layers:
	-	`sha256:510df53397eaadcdec5470c4772852ccbb02acb5ee519ab1104168a379957782`  
		Last Modified: Tue, 01 Jul 2025 03:25:04 GMT  
		Size: 3.7 MB (3731184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51a37c8ba5162f56132fb486cb83c49b657565edbd46595a47a7f8aa9078003c`  
		Last Modified: Tue, 01 Jul 2025 03:25:04 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:f6e5b54202536e37a5e5f833d74e430020bc206b979b66434d4bb6af8da57614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ce1b1f95ed61e43a797f8a297e47a583c5771edca8ed21df3816981e071947`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b255fdb6c1c95bc69fa56be64f8eb7abbaf4cece7dde792071d0c8592c4ea3c`  
		Last Modified: Tue, 01 Jul 2025 02:12:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a141ccb47c2be9c5e93a00320652ec9e2d6f84bc5e0b1ee13f6e761323d49862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdc68af3e304a2f3d3eba546867abad80cf26a0156c502c720b46f6628a0ea6`

```dockerfile
```

-	Layers:
	-	`sha256:07c061351fde20a752a7980de5aa320e26266bc4fca8282da42f7e3cbf00437f`  
		Last Modified: Tue, 01 Jul 2025 03:25:09 GMT  
		Size: 3.7 MB (3723676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38fd10aeaf15eb9dc19b1159830dce1474780b8a6f090041bca7a502a81e5bb7`  
		Last Modified: Tue, 01 Jul 2025 03:25:10 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
