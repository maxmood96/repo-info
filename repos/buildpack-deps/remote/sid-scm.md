## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:675c441389b4a6ab6bd0e809e26fc0e05582fbbb9f2877b635e72a06bcaf7d4c
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
$ docker pull buildpack-deps@sha256:3172aeb659ebd16d00337d7cc34b37bc4344aa129bf32383852e1df549e7cd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140777453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac6b6267ec84e2668e73cd1adf1a5292d9902bbeaeec13b49a4da8ced772a0b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5cb15ca6b13e712531ab64cf0ca7c69c2e82cc28e9adaf6b4610737a1ba0734`  
		Last Modified: Tue, 24 Dec 2024 21:32:33 GMT  
		Size: 52.2 MB (52225405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a81d57692e85975a86c41b040ba4d1697f343d6fa8db79612558993ad0d1444`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 21.4 MB (21415241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b414df4f5677fe59988b95799e3893179cfd33808399b76d8526efe756540435`  
		Last Modified: Tue, 24 Dec 2024 23:16:08 GMT  
		Size: 67.1 MB (67136807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11b2301478d985327f8f8906f66ddf3f2613783795ac38826feac7bb3a813f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7639819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d4f4823102df517edf188bd170257916ac2f10a455cd70d209877aad518327`

```dockerfile
```

-	Layers:
	-	`sha256:a650565431162fd0370d4ef39233df9b18c312b7d6408527a55c212e8ecaf4d5`  
		Last Modified: Tue, 24 Dec 2024 23:16:07 GMT  
		Size: 7.6 MB (7632522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:386595a3f4f451e678f72c070f11766ce39a1da79cf2b2d9078fbcfcd7150c60`  
		Last Modified: Tue, 24 Dec 2024 23:16:07 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8997ea752b39ef39d6699b84881299fa7c626b9d5e32b9b2abdb7d06d97a6127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134058345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24b4fcef98578bf85854eaff58819dd73b380836c8b0d4dbe68a53802066171`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc33f333779e1bf21a11cec34fde351758a9648cea4a206cd5ca5e5c267d5ca`  
		Last Modified: Tue, 24 Dec 2024 21:33:52 GMT  
		Size: 48.8 MB (48771903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48cdc7993c776d6ccec56389e66a4c68ee1ceec1afa89a25ae9e60ac171c2`  
		Last Modified: Wed, 25 Dec 2024 01:31:21 GMT  
		Size: 20.3 MB (20307127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3bfde18be32fb9febe492f8f4a14b4e0ea8e6484b78dfcceca3b9ea06b7f0b`  
		Last Modified: Wed, 25 Dec 2024 04:50:04 GMT  
		Size: 65.0 MB (64979315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:27f73228cb8a1da14fb10dfbd44c14ab5ae5c28361883d3252336214314aa2c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7640155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7598582080348e670489b1849312bcadbdc48d873cf783a15e8c5655b3b8d8`

```dockerfile
```

-	Layers:
	-	`sha256:93545f80e154ff1a8825afdb91b23ace1c38554de0710789b3872c90047aa15e`  
		Last Modified: Wed, 25 Dec 2024 04:50:02 GMT  
		Size: 7.6 MB (7632798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18051bc67d6c86163b4bd5b37a24ccc37f5b8b88a82114e8e9b6a565842551d8`  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eee73af26ed00733360dfc64d7d4e42f53482efb28e71f64ea037d036358ea79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128670300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5120c42a5af4bbfbdd4fc9d74929a06edb0f21e8625d22ca16231b10d863d37`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd381bc5446358c906dd1f7ac3878d03bb1e1267963891069c3e6e2c97919218`  
		Last Modified: Tue, 24 Dec 2024 21:35:32 GMT  
		Size: 46.8 MB (46763305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d419ccba1fe0df7cd0c879e1f8261dab91d1fe412b8df835212e60f95b90dbb7`  
		Last Modified: Wed, 25 Dec 2024 03:45:03 GMT  
		Size: 19.6 MB (19608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367601bc4f065e38e007f59c54dfa0b3ad1eb3805f4c77d1ffe0c358844eeb5f`  
		Last Modified: Wed, 25 Dec 2024 13:02:51 GMT  
		Size: 62.3 MB (62298046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e3ffce5f6e75c6d62335248ac830f81f37e5ec9902e81552c60b038906b77d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7639931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef91ca6162d85641a1db7edcbc2273f1d99456e8b22e8611e0268ceeafa6bd16`

```dockerfile
```

-	Layers:
	-	`sha256:66122bbaa60a08c42b7e78ef0f156af343e42f3f153e787fa2773a865edd97ff`  
		Last Modified: Wed, 25 Dec 2024 13:02:49 GMT  
		Size: 7.6 MB (7632575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2298d4cbb2eac5a05c766144c3ca706c5e4b5fc5ef9c59f2f5ece3e2f9721246`  
		Last Modified: Wed, 25 Dec 2024 13:02:48 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:44c7ae45af3da73e2d51b1b9c5842728745107083c70d34081ebaf17e834dcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140652595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1340e1963e159f97fab016487d366b374f3f6435f19f15316188646c2e32761b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5111921f4f194856cc1156a3664c32c64df54cbd5ad15f8c94081cb0e3440253`  
		Last Modified: Tue, 24 Dec 2024 21:35:38 GMT  
		Size: 52.4 MB (52432315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20d0977c0428e556b738a4854988cc1f65b6192c33c235195555a4b1c8e5d58`  
		Last Modified: Wed, 25 Dec 2024 01:50:20 GMT  
		Size: 21.1 MB (21052154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053c3d6a126675dc183ace458ad37733e728fe47e857880914a939b478acc30`  
		Last Modified: Wed, 25 Dec 2024 08:13:21 GMT  
		Size: 67.2 MB (67168126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1776e2dc4819df5c6b21711a76f042798ecf466600571e7f8788054e7b76f0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7649015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57245cfa3b330f641db2bf6b55dd1d75a572ff1cf361bc685276716d090bab09`

```dockerfile
```

-	Layers:
	-	`sha256:dfb2fc27aebe2692bd862d6e7cd63a6252f3028637ce1d68481cd5fec924c256`  
		Last Modified: Wed, 25 Dec 2024 08:13:19 GMT  
		Size: 7.6 MB (7641639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b96154f5bed0bee9085337acc56c2ec9eced1b611f40f1bf9b8f915d0911856e`  
		Last Modified: Wed, 25 Dec 2024 08:13:18 GMT  
		Size: 7.4 KB (7376 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8bfa59a490e13b9cd8ba10ab45f3771ac6591355585c3d7ad1cc095ce6969fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144544872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f0102a243e2baded5dfd0b8ac60d803716a8881a404f592914143749268e84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:314d11be1a34669d77f82c7dd25250c0aca0d10b528a45fcc768df2c73d1a359`  
		Last Modified: Tue, 24 Dec 2024 21:32:39 GMT  
		Size: 53.0 MB (53038809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794215da1008afee770eb56416f34dd01e9c2b54727b8c520b5cbb72c9a0c70e`  
		Size: 22.5 MB (22515087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ff84ea00dd6664e516545fe56b76d43f131cd690417ebf04c5ddfefe8e3e2e`  
		Last Modified: Tue, 24 Dec 2024 23:16:18 GMT  
		Size: 69.0 MB (68990976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:676b50d8d342d0f66e04efc5c0237b4bbdc95b018b7260e1e0c6b9a2f6ecb5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d5a4ed4586511e22297cae409761f15e160a366cb4129e133748ccea044a7f`

```dockerfile
```

-	Layers:
	-	`sha256:cf325be20fcf67a9b92cd0022740200094afda694f861a93269b7791aa0b660d`  
		Last Modified: Tue, 24 Dec 2024 23:16:16 GMT  
		Size: 7.6 MB (7627273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:296bfb47fb878576bc13b20ce122459b4e7daa31831d24d4c858322849f18126`  
		Last Modified: Tue, 24 Dec 2024 23:16:15 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:18793d3bf4bf5e25195e4e7de27928138f62bf0bb790532a2bfc90182428a714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139629522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb8d2194cbc3c583eaabd739a73c0c7e255ba00b47b5ea0fc1d964876106973`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2225e4bf9a501ecd52da3f4301136a4a3ac3273d704acaffdf95ff67153847e7`  
		Size: 51.8 MB (51771333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8315cddf1f38d3ec912dd995fc72b7c70105918274b7bd71b5f66a9e8789a52c`  
		Last Modified: Wed, 25 Dec 2024 11:47:53 GMT  
		Size: 21.7 MB (21740832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bff240cec674232066373df9095fc00a6e03c4199156cd01f197c25fb6340c`  
		Size: 66.1 MB (66117357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8d78ee840803aa0c532881eddd9e7a9ca63f637a58e7544fcd6d7a62b2f120ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d52bd8980b7f832a3915bcd636203274dd25c068aa074efc78e38275a111f98`

```dockerfile
```

-	Layers:
	-	`sha256:ab12b73792d73d13a49f6dc0834b27510c61ed5b5607b2436a20b03a1bbd299e`  
		Last Modified: Wed, 25 Dec 2024 19:18:18 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aa242c6dc1fe5760dc5e863f489fd2de9f652496e145216ffdcbc87359657b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151393723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5056f3622ac7f023a602986005d7ee399996a5ab6197d9338bf546258af030f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8080cf22cba920897d6f69f8cd18b32c615d4fe71eec9143a4055b490742fcea`  
		Last Modified: Wed, 25 Dec 2024 00:33:18 GMT  
		Size: 56.0 MB (56045011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec24b97fe03e846eeb6353a5a5009e4324e4fb188c11fce7c104a3a8159b2eed`  
		Last Modified: Wed, 25 Dec 2024 06:15:11 GMT  
		Size: 22.8 MB (22807309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e50f3565c17459e6c7bc9c56584bd324fe52f1c6e466111fabada8021af303`  
		Last Modified: Wed, 25 Dec 2024 09:44:46 GMT  
		Size: 72.5 MB (72541403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f8cf6ab5c9be991672128d8c145630512304c230bb526328cb1c82e483caa8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7646389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c181c0b06930582bb3dd96049a513df9da0aae7fae0e8ca6ff4ab11b5b87b99`

```dockerfile
```

-	Layers:
	-	`sha256:4b37c0f29ead7edb6481da6b5d13e90e7c5d13efa1c7e7051c67665310845474`  
		Last Modified: Wed, 25 Dec 2024 09:44:44 GMT  
		Size: 7.6 MB (7639061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1765824362c98faa8e44187ca4e2f7d7e6c9e45792693ba822496da2ea0e0c8b`  
		Last Modified: Wed, 25 Dec 2024 09:44:43 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1c11dc0f6cbccc5b2666d1000b1a8cabfc7e0cd69cf765e6f13551179129bdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137712618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050bcd9ec7b82998c38f40a2089324ac25931cc174dd8636cef601e3fb5e5402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34dc7eee421e2547a72cc18fd960cb61e4cc000ae2301ebea5c1db40e2f928c9`  
		Last Modified: Tue, 24 Dec 2024 21:35:00 GMT  
		Size: 50.7 MB (50711803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b3be9202d049cfd8fab2840745aba862531c266ca24caab8785a1201a2bb14`  
		Last Modified: Tue, 24 Dec 2024 22:26:29 GMT  
		Size: 20.8 MB (20829455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a9bbab72f01dce27644d4f039f493ac5e6e54ff93d5cddb115f95af7c7ff7d`  
		Last Modified: Tue, 24 Dec 2024 23:21:04 GMT  
		Size: 66.2 MB (66171360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3045cb2fa1924b6ebe89757d807fcb7e1684649b7dc1197ddcc0b68d6d2237bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954774fc0b1411cf87f88c7fddf147a9a67c94c2fbd8a6fb5f40c87de61bc871`

```dockerfile
```

-	Layers:
	-	`sha256:f20d78cb250d0ecf18d1a75ac9fbdbd15ba56aa0cd81ec6ce0c50c55f7c6d087`  
		Size: 7.6 MB (7622643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865a6e8b3a3ac009d21d4ace920ddce3a7988bccf7b1729f9ae28f1d25db9d8d`  
		Last Modified: Tue, 24 Dec 2024 23:20:54 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d19ee50e9c87be055f057c2176a0f83ce2858755601752cd59ae5344700e52b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143122605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd67a3d9f7958f8cf6734e2ce105a3ad5ee75476c28a8f7edb133b487715e2ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d2cec60b297953cc4fd2d941f10377b6dad5bfe41703a7cd8819244b88d9c21`  
		Last Modified: Tue, 24 Dec 2024 21:46:45 GMT  
		Size: 52.2 MB (52169916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a975a9a4c83047fb6ec13cd27d1e9c9a446b78d685e928ba2f4297e75463ff9`  
		Last Modified: Wed, 25 Dec 2024 00:17:26 GMT  
		Size: 22.6 MB (22621261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a51670f291e5f6590a069589cb9515f14909c76a4c6118030edb7558e2bad72`  
		Last Modified: Wed, 25 Dec 2024 03:30:15 GMT  
		Size: 68.3 MB (68331428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d7bcbc3c83946e452da71f2bf465e27279bb49f04e53aa544c72f693d9d6a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7640237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e816f9dd2f8bf480790d1421cfe02157a896b465037d4f030c5b7ef7a91e622d`

```dockerfile
```

-	Layers:
	-	`sha256:44382edf72e8bc1bd925493adfefadc963ac2d6b16e279c2c2467b984e7537c4`  
		Last Modified: Wed, 25 Dec 2024 03:30:14 GMT  
		Size: 7.6 MB (7632941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e2605ab10b2c60e4ad1c657eb445beba2b73faccb861ca71e9b914d3275430`  
		Last Modified: Wed, 25 Dec 2024 03:30:13 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
