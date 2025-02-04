## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:d7b1848913e9a5757409d3ebf1fe95cbf03b0d255094c75d90a86b41c8b3a7b5
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f487291be51e5d478800f7c65b9a503ab6235673807bc1276e81e0a165624a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141854519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60aa521c539bbb22fc2d13831a07d461e35a6f60dde2bed5c7351dde8611f14f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbda3f387ceab9c039dbe56e4c3555afaa795a6af95ca16374c71c1ceb40cd0`  
		Last Modified: Tue, 04 Feb 2025 05:20:47 GMT  
		Size: 67.5 MB (67467177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:970ef7fe550fa87b4dda566cd405b8ae6f28b8aee97254502f87fca5a6cb6de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7670994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9569b64e2970c7a04074ef638fe351f938cde9a55fd35b9e3a6e2a1d35598118`

```dockerfile
```

-	Layers:
	-	`sha256:cf583dc30a65517b178c214cfeb2ae61f807f7ff0b8399e83bade971a711b176`  
		Last Modified: Tue, 04 Feb 2025 05:20:46 GMT  
		Size: 7.7 MB (7663680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42405d7221cae1b07937ab33f691e1604bc9bf2ad52e2026873942465a64cab7`  
		Last Modified: Tue, 04 Feb 2025 05:20:45 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e880624c6dc241604b850a8cef96855202f8a48abc46d611cf70e79dfcc7e077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136349127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d34ac1c32b6ff9467ccf5a5594c9771fb9021215e7ffd7c7389b123a200000b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17d90b594a7d89931d5de1b198b2dc07a97b965a1b004c4da3948056c117a8d`  
		Last Modified: Tue, 04 Feb 2025 10:23:00 GMT  
		Size: 65.1 MB (65103555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:164785459bb6b6d0f90da7e56eee4d7769da486e2f0fdf3d2526b87780cd6f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40000da731b6ab54e168ce98808313d9c4f419da4bfad48e01858f95acbe9d86`

```dockerfile
```

-	Layers:
	-	`sha256:7323964efa1407c77824afce3e74d3d93019898273512e6e067825cc358be661`  
		Last Modified: Tue, 04 Feb 2025 10:22:58 GMT  
		Size: 7.7 MB (7669362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b489edbda41a57517e3aa2211157756cd4a998ff40b48e2ae2b4ea4082aeeefe`  
		Last Modified: Tue, 04 Feb 2025 10:22:57 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d453a71279f51a33275b104128b0ef32161442779adfc2eca21e932784dc76bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130281606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9ebc683d6a2e74f3f6523b76e88dabbcd91ef15a5b3f5ded12eb0d86431ca1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c787837970fa306cc5256b55f5173664552e3e16eb197389ac0c21aca92a24`  
		Last Modified: Tue, 14 Jan 2025 16:18:41 GMT  
		Size: 61.9 MB (61894400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:375bd3b5de1e4ce62154a317a2eedf0fbbc645ba28a336dfc7f57083debea352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7635007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea55d1a9628c01c5e7ce251049e6ccd4398382e087631485ad1c0e2193be47e2`

```dockerfile
```

-	Layers:
	-	`sha256:6bb2101881c8c8c0ffd4bc5a8101bf663900fd2aca831c674d7a718df973f6cf`  
		Last Modified: Tue, 14 Jan 2025 16:18:40 GMT  
		Size: 7.6 MB (7627633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ae19583f8bb3be289a75674345c6ef019990014243072a9ab03287e1490e6d`  
		Last Modified: Tue, 14 Jan 2025 16:18:39 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d70a8d9b484c5a769d008f881b427c8ecbce176197d8464dbecabe3acc2f5ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141189718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae5585f17239bb791e7d4137500f2b26d5bbe9857b7c3b81e66b75e1ae44a32`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53cf00e5414c63ec005c43ad8342c8e55028d137e29e95d889d4247b0586d248`  
		Last Modified: Tue, 14 Jan 2025 01:38:51 GMT  
		Size: 48.7 MB (48661509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216ff9e1bca52cad6d9119375ff8a9fe28c8b52c130d5380d5ded38210e688e`  
		Last Modified: Tue, 14 Jan 2025 07:01:19 GMT  
		Size: 25.4 MB (25426483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab5443d60c3808485433bb956012bfe58b69cebf352b638a921b47918c7b109`  
		Last Modified: Tue, 14 Jan 2025 13:33:15 GMT  
		Size: 67.1 MB (67101726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:71b473c988201a15d0e20854c52a1e6f719e17af81f6b027cb96157e56a1d0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7642809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a2500c367298cd1fc64543c18629eb985446986c8b845641b92ccf0347b2d2`

```dockerfile
```

-	Layers:
	-	`sha256:0c061376a90509fe3dde2e194e4939ff029461fcc3800e0f40ae80e36a483e6d`  
		Last Modified: Tue, 14 Jan 2025 13:33:13 GMT  
		Size: 7.6 MB (7635416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4308ad8e7f7805b5fd297337cf6f2cde3691af0c299efa78aa756c4c035d0284`  
		Last Modified: Tue, 14 Jan 2025 13:33:12 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1ed16b0936c8407a72004889edad80759c99e5438a9a70e386b7ae83319f60b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146340563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f95befdc782b90fc6a9406d931871ece11c0fa8745cc0f868e5a054e49bbc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4913bde8dd9201a45eb15eecac64dfe0033ec3938f3fffc5d62cb37095ca1ed5`  
		Last Modified: Tue, 04 Feb 2025 05:15:41 GMT  
		Size: 69.4 MB (69401603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c444a74ef507e91e25d322d7a1b1810d0152c6086cb9217466eac67f8718923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7665717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b7ce1fcd892fa25e8af962edc78a25e4d9b016b6647ea39c5b7cabf5d7b532`

```dockerfile
```

-	Layers:
	-	`sha256:a2408e37c2fa9db1a5073eac5690fc938e92771f4870a803b110f295386963b2`  
		Last Modified: Tue, 04 Feb 2025 05:15:39 GMT  
		Size: 7.7 MB (7658425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f03c5a7cb4320006cf4ff2e0e0755de4671f7f3552f66c41de44623e306df771`  
		Last Modified: Tue, 04 Feb 2025 05:15:38 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4542f8065a818db739219a01e1b40b60efec5afadfcc4529d720a912a39ab61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140293949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70012defa400db789835b3fce6a207e007f4872ca46448489c6c0af0fbb96add`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ed8eab45779c4caaf48a3dd1f3e53c5b4079b75e32b657bac3bdc07a0f1e4b`  
		Last Modified: Wed, 15 Jan 2025 02:07:24 GMT  
		Size: 66.0 MB (65977015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7cc83ae9e313ec8a4b0f9dee34a4c9c2af59dcda58e3a038fb4c36710dee4a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd3378118053b582710f3fff850eceaf69604c78fa7b42fc57a97a2a20686e2`

```dockerfile
```

-	Layers:
	-	`sha256:4ba40c128050744b384986d01d36e73805b787370c0dd4fbea02fcb7fd83acb3`  
		Last Modified: Wed, 15 Jan 2025 02:07:18 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fcce0daab7df71c0a4d24ed7b777c4ad2f8e4e07c45ac14ca2f0984222d32abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152098758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4dea55014e43fd29a446e2658ddc4573c27a9139ba114d7a6515a269fd6e4e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:826e70a2bdfac0f05c49b7611afcf30a311c862a1beca6fc4059e4b6cd0e1a4a`  
		Last Modified: Tue, 14 Jan 2025 01:40:51 GMT  
		Size: 52.0 MB (52043133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126b14e556a94eaec41c5a29f9164224f92b1080c74dca2491c3f7b9120c320`  
		Last Modified: Tue, 14 Jan 2025 05:32:11 GMT  
		Size: 27.5 MB (27531238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7311c304e2cd2735e9d0f4a75554811f3be94be0d57e4fd8ff5989c485af8c30`  
		Last Modified: Tue, 14 Jan 2025 09:44:47 GMT  
		Size: 72.5 MB (72524387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a001f2f6032e4930c80eebb2260702f3186b60b4d076204054369677f2e582d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7647664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff99e2b1587ec2a5c003050bc95171349435c39da73c56936d00f2a3ebdb3141`

```dockerfile
```

-	Layers:
	-	`sha256:64579d1288b78c8094cfe263e14ab072d6d69bfced7f13b129680dd8bfb1a06a`  
		Last Modified: Tue, 14 Jan 2025 09:44:45 GMT  
		Size: 7.6 MB (7640318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ba8f2daa2f44abd8160ed1034994c1d4c473f6eab21718fe570387334939b62`  
		Last Modified: Tue, 14 Jan 2025 09:44:44 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:841b670efa888fba12f3ca424d021bea46e276c2a406876d2805ebd30661cad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144183374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a538ed29c23de0033afa76c98443583277d7e4f244f6de7b22975a716779870`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371642bbb4f2496e43eaeaa75efac59f54344b0c0beee1184503290cbf7343a`  
		Last Modified: Tue, 04 Feb 2025 11:38:14 GMT  
		Size: 68.6 MB (68552428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b3506d5e6cc98bbe1f6132732531295f20e63be600a8132ce4f9e43c8b7f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7676823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099bc7a3a7b814638927fff3374f349bfee6919065f69fbd17ab7afe592ae384`

```dockerfile
```

-	Layers:
	-	`sha256:9c9e3a34680550da80f6d8ed94a748afe42e82068c2fd150cf281d40fa61cba8`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.7 MB (7669509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0d790adc26bb3f35199a82b70f773864a308950b877536a295c0a79358143f`  
		Last Modified: Tue, 04 Feb 2025 11:38:12 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
