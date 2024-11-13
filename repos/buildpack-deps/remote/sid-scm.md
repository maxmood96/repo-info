## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:1c1ac3f96a55033b5a71fba4382f64bb41cd477a3820000c0d406c71deefc9f1
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8ab7ea446bf8fc89524695d33da2ef73a78861037d001ca1d09acdf7d7614c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140527220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f3d6b5bdecf0d50cba2b30fcfef9e6c15ece0fec037adce41d28e2fb76e848`
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
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df9c0ffd5cfef9ed63d0dfdae57285f543f78320d947c5c4c2ab1422641cb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:01 GMT  
		Size: 20.6 MB (20596172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0899f4ba4649838a893d7f1a70928afc27b147ea5051eac0853a716ef24ac8c8`  
		Last Modified: Tue, 12 Nov 2024 03:58:48 GMT  
		Size: 66.6 MB (66611604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:983d3401a2f2ef93b8b63c76b3eaea3455a247cf97c2b075dcbcc144f508ae42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7621436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767f303cc728dc43cf2a4fd72997cf80938888305f42cb037c7aabd481ab5a54`

```dockerfile
```

-	Layers:
	-	`sha256:f39cef2c674b6a5197868f663359c3af90f575a188282358e57c0aa4ce6b0328`  
		Last Modified: Tue, 12 Nov 2024 03:58:46 GMT  
		Size: 7.6 MB (7614139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32690f39b8e5187bfe3b6b0929620b5230e9bf80dafd63d62c533cf04b46233f`  
		Last Modified: Tue, 12 Nov 2024 03:58:45 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; arm variant v7

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c104a59a3c4fb391a52f93cbfb13639f2687fc4366f11bd4751a0070ae46295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144456027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b888da81dfbdafdde34e7d00d58c2571e37c5eb4452bcb663b3985887540668b`
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
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24546888a84a1c2171ba5648f213b4d3b8fee560f454ad1c12f583f6ce895c81`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 21.7 MB (21725392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885dfc308254678967ab6d79ba6d40d73a4ad263c111beedb94327edea737b17`  
		Last Modified: Tue, 12 Nov 2024 03:14:27 GMT  
		Size: 68.5 MB (68538589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c24aadad36af251cd9bf21f434e87afe3221731362b3949ed6041b42e0106d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7616166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048981b783cc2bc2805b479186421c83a673d18f0c7f4ff8aaddaccc1c439cdb`

```dockerfile
```

-	Layers:
	-	`sha256:c118844549e4437f38e352a7c47675cf37b87544393f46164905c9d0236b7bec`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 7.6 MB (7608893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38ce5f76d34336732dd1258471ae700b6196172c7e61fece81d951971e0645c`  
		Last Modified: Tue, 12 Nov 2024 03:14:25 GMT  
		Size: 7.3 KB (7273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; ppc64le

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

### `buildpack-deps:sid-scm` - unknown; unknown

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

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ab2c9935ec3cd5ea01e59c813479dfdbe44a93881633c9ab35a027bc963fbb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137343646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b025b9611b4913fb2e9ce20401ffc0abdc8d1d1f86c8933186f6b02ff7f4c8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c05579e9b49f41a2b6960286d8ab9b1d090127915ab4b5f2c9ec35e3db7815`  
		Last Modified: Sat, 19 Oct 2024 03:48:10 GMT  
		Size: 65.8 MB (65756980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c2cf945f847e73794eaad19c99277f7632971602dd13cc6de4b1f441087c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7588619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00950719b6663cf9a97df3b358162af671f7ca9b8b02fe2daa10b4ab5abc3f80`

```dockerfile
```

-	Layers:
	-	`sha256:953dc6ddab24f26925a8b0c459f5e303f3adc5374831eed917b8e26a9c0deaee`  
		Last Modified: Sat, 19 Oct 2024 03:48:02 GMT  
		Size: 7.6 MB (7581279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3224b770b161aa53b6afc3fd6cca8fa7a8e2c13cf53415c7f406ae104506e5`  
		Last Modified: Sat, 19 Oct 2024 03:48:01 GMT  
		Size: 7.3 KB (7340 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

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

### `buildpack-deps:sid-scm` - unknown; unknown

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
