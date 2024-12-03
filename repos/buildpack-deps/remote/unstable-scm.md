## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:8888f0e9951cb592bdf24d21dab9d1d6f83a486a4a0247859f7c47efd304a998
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:98ae8322e21402d9d1a47ae330578c281bedd95f82e7551694698c1c73d150b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140712020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff602ec12cae508a5eff7f955f1f3b4a7b0116e7f63fd95e3aede38e2531f3b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b96ccb05d400b1173a82c26d045cd47d1fcb41dec65a7bdc799295c8199e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:08 GMT  
		Size: 67.2 MB (67204217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7f7f8c9fe198f76ea4d557014b74867442af6b19728ed19e19b5db24d2c9787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7673901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9655e2d30b820946d8a9271aebee6149dad6dd472e02bd0dd2490a28bc82a1`

```dockerfile
```

-	Layers:
	-	`sha256:9b8dcc9e196bdf56ae35756553a098b57ee3322218cfe81f94b8d219dffaf1cf`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7666604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb4b8ce456f309d5ac4f45927a3297061e4c2e8acfb4c80126d9bf3ee145d25`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:848ee71fe2c9412ccf8a147c76f6ec97c3acd3ebf83a5f18775f0c48b308e851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133852044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e043f8c929df470ba036b874156f397c9e570d1adaf2e85b886e5efb33f5d473`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:48142c53989e584e5008e025d7add416317666ef57f1383dab96cb3b5dd1610c`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 50.2 MB (50178305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e719f1a345c9d868951b12d49877be0a8ce88c74c1d28554e382cb36c8fb0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 19.6 MB (19609396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a80294a22345764a6f713791d5e78ceccbfde6983b0bf68a23d16e31cb7a8d6`  
		Last Modified: Tue, 12 Nov 2024 11:31:21 GMT  
		Size: 64.1 MB (64064343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad4c5dc36112c0c74e99ac96fc1805df43ef5c11db6b7fcdba77b0eb0c0d3713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de220d7aa70d91d334a8498c9ae1e10d8f8c53b8508bceece7f84a5803c9f1a9`

```dockerfile
```

-	Layers:
	-	`sha256:2b742fb0e0d70644066c1472b3cb6559ba91cdd89925f703883bb76e11cfd5da`  
		Last Modified: Tue, 12 Nov 2024 11:31:19 GMT  
		Size: 7.6 MB (7614405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cfee709989da69a1418471850a2f2c0f2c90e1bf104a675f2aa68f702e9f8df`  
		Last Modified: Tue, 12 Nov 2024 11:31:18 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49cc8b09571de3482143acfe7100f15f8d3a156ff6bea401ccb6279e58a7fead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128289386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d80ca6ceef7a2fb53ff08ce96ba5c1f8d2bada4782470ee227e2c258631e63`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e17a4ae99f3dc5642f3037bdf67fdb8d526cf44879dc2a2a82dd78799b94cb90`  
		Last Modified: Tue, 12 Nov 2024 00:59:40 GMT  
		Size: 47.8 MB (47762858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a3ea44bb2abf7747807b4adbbe717ea3308dcc90d88289979cc43a641049`  
		Last Modified: Tue, 12 Nov 2024 16:01:31 GMT  
		Size: 18.9 MB (18945424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b86dacd9090665be47b5966a673c201e9be17e12af3a6b155bc5749678a52`  
		Last Modified: Wed, 13 Nov 2024 07:40:03 GMT  
		Size: 61.6 MB (61581104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db36f314f12e690b6742c569de4a89729ea3e94e60224e1219d288df46355abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86ff9d0f3ddb306fdd03d1347b681887a9eb99cde3335aab0b077a1b74c390`

```dockerfile
```

-	Layers:
	-	`sha256:a0b51d6858aa210986bb5e9f3dcc57e6a24f20cb265918e257765d594eb56d2a`  
		Last Modified: Wed, 13 Nov 2024 07:40:01 GMT  
		Size: 7.6 MB (7614159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df37db634d787eb3c7ef7dd112ef7905a94e7a0e272ffc18fc80ff7b9b41cda1`  
		Last Modified: Wed, 13 Nov 2024 07:40:00 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ed02583a3301a58af1f78b2831949d69602419ed37cdcc4574fbb5ed0c797d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140631734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6562e7440624718f3b0e9c5ad06d219634ce06fac5bc551a7fd4c03f4b24533`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2180b05bcdf8eaedc4db9cf7f65afe026827aad32c4e4b7f24679e6ea2c63305`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 20.3 MB (20250755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da6ab97bb0c21d31a38290cf57289900a53f954b993db59f27f8cedb1eb175f`  
		Last Modified: Wed, 13 Nov 2024 02:43:36 GMT  
		Size: 66.6 MB (66621232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a466cb299f29ec1bfc4f452f66a7a880326388a75746522d7d4a7136e76d1b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7632550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb012cf882fbd5c3fcd38a399056fd3d186b4b2c0426e02776d2b216ef72876`

```dockerfile
```

-	Layers:
	-	`sha256:d3b82869d1f4db5269f5aa6dff3fc540adbf2ab697d2aa96b0b1c9cbce9dfdba`  
		Last Modified: Wed, 13 Nov 2024 02:43:35 GMT  
		Size: 7.6 MB (7625173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2711be53b98ca0bf93591f21aa86b59536b36a289d9b8e77be88a2ae4f1274e5`  
		Last Modified: Wed, 13 Nov 2024 02:43:34 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28aa3b92afdeceb776855973c3b211c28230c89a81b458bb7e67b11d8cefe2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144558793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc5aee69b53785c60a0927a7b5c28ef293efdde6e25767537d489ed2d6e1d2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dd8a498f4405479d9e2bf04b4ed73d5dc63deb1d79c9d70eec7ddd7add1c35`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
		Size: 69.1 MB (69057622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1de5a48dfe09b9f75e84d47faa561d68418835bb76363623eb981f370a7eeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91810c997ab4ca1105aac3782040f194980cc9236686d98672c7a9c1b2c8411`

```dockerfile
```

-	Layers:
	-	`sha256:c5867b09adbc4524a9ca98728702a0177022b1afc0e4e8385d9a61636c8345ae`  
		Last Modified: Tue, 03 Dec 2024 03:17:07 GMT  
		Size: 7.7 MB (7661345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0640817c4ab08d0cfc6d0fb5beaa13797d1e7a88cd7885d6a37b80373ce2b256`  
		Last Modified: Tue, 03 Dec 2024 03:17:06 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:433ef6755fd51ee668442ab78797afaefe11b5c906a568bfdd7a237d0bf2585d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138580415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa27cd16bd38d59fe05330b5e6a7515ce6692065b0462890843f49aacaad3ee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f6d00c97864e98dad498c4c1087cda2fb16f2ac6e7a71ac1353418dd4215995`  
		Last Modified: Tue, 12 Nov 2024 00:59:58 GMT  
		Size: 52.3 MB (52275237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee73bc743170bb5e4087d57c95a63d610fb1282220d73ff90af4707b831d99`  
		Last Modified: Tue, 12 Nov 2024 18:03:00 GMT  
		Size: 21.0 MB (20950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aac7a2dcb6a719b792ac16c19c2652ad08047befbc851b6ae687255f6838b0`  
		Last Modified: Wed, 13 Nov 2024 02:06:14 GMT  
		Size: 65.4 MB (65354987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a12220edb3617bcb4abe259389b0324a33c89d2862e9e447f136530f0e9d5086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee2e3fbb2de24c02ca4dfddd469bc058dff82a8fbd1c43904ca6aba92fe3e42`

```dockerfile
```

-	Layers:
	-	`sha256:aa271072ee92dab888071bdce24b99dec92fe97e837f30e2da96cc1793727ac9`  
		Last Modified: Wed, 13 Nov 2024 02:06:07 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:070c7700d7f47048e9a84488481f5eeca3f322a2db8cf0063079bf0485af6022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151160749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461e9769ea2dda7d988b6bf2cf460318a930a39b684be2f7a4133a884c4eb101`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f36575664f661fb4663abf9a54ae38f6714b2f1a53511cc1ffe3d8ddb1acb8`  
		Last Modified: Tue, 12 Nov 2024 16:11:05 GMT  
		Size: 71.9 MB (71859244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e104f83870e9f99a4669b944a6bbcbebacf57fc258995d778499ee21445f42c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7627984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c47416740f5541249a4cef52d3b7e47f7681543d006c0c3ec02ff1b67bbcffd`

```dockerfile
```

-	Layers:
	-	`sha256:92fb0bcde05bbbbbd4d0f942437bf003e06cd1076856b50441ea3830631de34a`  
		Last Modified: Tue, 12 Nov 2024 16:11:04 GMT  
		Size: 7.6 MB (7620655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a50d8c663179edf632a443d2292c19b83099aa6fc312e4f3fa057911bd68e2`  
		Last Modified: Tue, 12 Nov 2024 16:11:03 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fc674a43ff201f8797f66dd82257b4196d80d7c095fc868cbe749cb36beeda09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17059d9a1dcc6bf58ee32ba614a1fcbe226f8043520b842b184d3a9c6f28ff4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f14784271331931f12f38e0de1c6c4183501776dd43b01c47876c85796c8558`  
		Last Modified: Tue, 03 Dec 2024 06:42:00 GMT  
		Size: 66.2 MB (66176026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fbd26b4002d80a7a7d2202c479c7daee401e8a0b0b2bc1e4e4d3dff743cc317f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7664095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79590c6ba7424ad6bb084619f4ed4331d5e05aaad65648779da965666f5b52e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee9a4121ef32c4ac3a622baed8c3121fa68a4974fd0e3a4c5b2491d3285a4d59`  
		Last Modified: Tue, 03 Dec 2024 06:41:52 GMT  
		Size: 7.7 MB (7656766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d83211651559187f1abcb4d829c94f914b0ee443046ecda9f19c4daaef0296`  
		Last Modified: Tue, 03 Dec 2024 06:41:50 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:809b7c31d9e24e1c0b9a381529e8c372ada83e99ae34c265fa03d28ede93bae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142437437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee26ff51ba3abc15f65b60da0d6c2334b6d3e0dfbbc6e596804cedc6950d983`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:01b62be41cbf7168e02a9fa648a1525f0c9095aef51faa9027bf3a9ff89c6b84`  
		Last Modified: Tue, 12 Nov 2024 01:00:18 GMT  
		Size: 53.0 MB (52980914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa52c56b4fa2fb05d933bf62d254d5f4371a5a9e6992ccf74613eefe11aaa96`  
		Last Modified: Tue, 12 Nov 2024 09:02:57 GMT  
		Size: 21.7 MB (21709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371f5c95f0d6355567bbfbef044cac10682ae55767ca48b41b71050883b57bf6`  
		Last Modified: Tue, 12 Nov 2024 23:33:49 GMT  
		Size: 67.7 MB (67747015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f6a3f486ce5e8caa4469fa1f85186cd38dba21ebd474be2e1162b85f4378681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acf667f95c64f39c2ff6b75ca7d9f9ee2eb2e7ba2176dc9fa537c4ea7e95911`

```dockerfile
```

-	Layers:
	-	`sha256:f9992e8b5c7d28198183ac3089602e18119a6fb307b90d3ae21ba41b6c9ec935`  
		Last Modified: Tue, 12 Nov 2024 23:33:48 GMT  
		Size: 7.6 MB (7614569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:295d005f001d303475e19bec16e29b7189f7f7b50c974e70971c62abd0273431`  
		Last Modified: Tue, 12 Nov 2024 23:33:49 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json
