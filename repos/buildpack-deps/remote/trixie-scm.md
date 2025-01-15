## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:1e47febc17dcd79a481be653438f33dc5d80e62bed470869d06ec493f89610e5
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
$ docker pull buildpack-deps@sha256:d7e160df91a90ffd562646d83295755cf928f26e92d9d7def7d14edf196f4b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141313557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7259b56a8d1ae555214a1955f4061c1228fc1ea8f84badb6a0b907bf00f6bf6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9146d6057920f25892ed3e631287d1e0e740bd11f7e3dd39c76c478675de8456`  
		Last Modified: Tue, 14 Jan 2025 01:33:33 GMT  
		Size: 48.3 MB (48276092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b2bf2fe5435a7871b88dbb724a93352983bdb5ad01681e2165e7056a7fbf25`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 26.0 MB (25972171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032bdd1daea694fee79d797bd4ea26270b8efc19783b84bfdd169027d675bdec`  
		Last Modified: Tue, 14 Jan 2025 03:20:11 GMT  
		Size: 67.1 MB (67065294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5de278a85e2958b1b67fe2436b38c5e1e4f60dad85ddb5b2b1ddcff7cabbf62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2fb7bb765b4014f77e77efc488f781c60237286908edeca5fe37bd77503bb`

```dockerfile
```

-	Layers:
	-	`sha256:ec60256c342b18984685b607dda2f33201bb024371958faf4f5ec8ed3b5ce6c3`  
		Last Modified: Tue, 14 Jan 2025 03:20:10 GMT  
		Size: 7.6 MB (7627580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cdbec1ea4a80bf20ca133d0b5731afbd464e30aa9eeebcd929077377d3ed43`  
		Last Modified: Tue, 14 Jan 2025 03:20:10 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ec43dde54f5358d89ed43a94ccd15db00edfc1aa93c301b892f78a7f9a8dbb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135593288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d982248c58038a9a10541f834ee410b7e7645d430afeb3648a7750e5a93230`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76cad3cf5a6ccb480f47b45bb1e37068b6554531620fd6fa1a71d8bd07d07d73`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 46.4 MB (46441720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb8fffcdf3a616be17dc58906cdefa8833c6afb82ce71878155d250e95d14d5`  
		Last Modified: Tue, 14 Jan 2025 06:09:57 GMT  
		Size: 24.7 MB (24664103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f91cfbf6c5d0b11eb36fffec7e0d991a9d0c8dc91887a15d7aada2df4fab3ec`  
		Last Modified: Tue, 14 Jan 2025 09:34:29 GMT  
		Size: 64.5 MB (64487465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8525ef21115af0672fab2c02e869bdb723f21c32ab8b7d82bd0ed0efadac426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7641435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563a9ceb76aaacd29a5c55af5382b3056da15595fcc3c4bdf3dcbbd1320ebe6a`

```dockerfile
```

-	Layers:
	-	`sha256:4eab91536efd52ddf8163b58cb4adcff88608ba0298817fc4fc5d0c6e71555b4`  
		Last Modified: Tue, 14 Jan 2025 09:34:25 GMT  
		Size: 7.6 MB (7634063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b90a9b332cded179a8569c67700f028d325847cd82a8057dfec260c81dcddd`  
		Last Modified: Tue, 14 Jan 2025 09:34:25 GMT  
		Size: 7.4 KB (7372 bytes)  
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
$ docker pull buildpack-deps@sha256:cab930fec1c9f29c032f5953b0110a38c29b9e830f8e38d47e06c217871c2a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145656706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb8bd67e08f6533c9d08e32c2dde86ebb325c4c64bfa6f7fc8de2758559d8f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b7bebb3fb62b18c851bbf703cf6a1caa57f7ffda09b0b23b4e4cf1051c666c9`  
		Last Modified: Tue, 14 Jan 2025 01:33:38 GMT  
		Size: 49.7 MB (49675708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628707934f13167c16796e4cf79505bf1ee994868dc399d6e208f3c459420999`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 27.1 MB (27114070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207f322000966464f5b86dbc320a5e9d43083269c9387f23cf70a903c8da719c`  
		Last Modified: Tue, 14 Jan 2025 03:18:19 GMT  
		Size: 68.9 MB (68866928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7eec913162affbc1dff5e79f167ebf583259118732e2289342b740f4de1591b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf44885418d985ee6be4b1bbeb4433bf45ede34e9f6fddad99d4ae42f8f668e`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ddc899d85cfbec0add6fd2da32d7ea3006225242626a7c1bc91f72cccf1a2`  
		Last Modified: Tue, 14 Jan 2025 03:18:18 GMT  
		Size: 7.6 MB (7622335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d8d17abe38f71a5208b24a2cd6860960c4f5c9eeddceb1c27a9ca47a58dc7e3`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
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
$ docker pull buildpack-deps@sha256:80c411b6393265deca26db79087467b934c75934fa1291c44b310b4d4c577f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143611807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47696d2aac2c67e834843fc15c480a3cba5411444b338135bcd6b1850cc65ba7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a96882092e58b6b0f460c25e0b3fa57215487e6282387621e5c4dd2314637493`  
		Last Modified: Tue, 14 Jan 2025 01:38:54 GMT  
		Size: 48.3 MB (48329740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c639414a48a5e91286e442a3c2a376c94650966c4fede85d34f85e98bf430e8`  
		Last Modified: Tue, 14 Jan 2025 05:01:37 GMT  
		Size: 27.1 MB (27131328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a0617227e41b6c45ea475d62d65ee6e02048cb238dcbfd9f884635a3d44568`  
		Last Modified: Tue, 14 Jan 2025 09:12:11 GMT  
		Size: 68.2 MB (68150739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:05070a944e14fe7f82af0f38a8e6140ba5a7b325dceb4fdafb61fb47a567af30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7641520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9546c3517551d5a64dfcfcf288a6bf66bb06c125a933771e44eeb2e74ad762`

```dockerfile
```

-	Layers:
	-	`sha256:e0f21743fcebf336b0be295151246ff366071355fcf5d9153bde738fe6ab7d5d`  
		Last Modified: Tue, 14 Jan 2025 09:12:09 GMT  
		Size: 7.6 MB (7634206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e4b811b54cc22b9ebe0b02ef93f66683045d3459a7919afc7eaea27014598c`  
		Last Modified: Tue, 14 Jan 2025 09:12:09 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
