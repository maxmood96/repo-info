## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:6a6feb65189934484413bd8fc454c885bf7aaf6a07414ec0893edbf3d38dbea3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f406f5090326933d3581499518f7d2bacd5e2292cf883f74699afcc5e9acb58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152502428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab2130d5188079697b68dc1668f4d59147acbd1141d36eb9d2c840719e2ed61`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bf1407f5d0a1803a6c62439e0f74bbbc4e011619cdf8ff34937549c5edb22d`  
		Last Modified: Wed, 22 Apr 2026 01:39:36 GMT  
		Size: 26.9 MB (26858023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb520314033b68a9910f325620ed50a6717748b6e8e41c11cc49b358fe8947f`  
		Last Modified: Wed, 22 Apr 2026 04:45:33 GMT  
		Size: 77.0 MB (76973825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:646f0cdfbcfcf93a82336011b7f93bd432b430c913d82f49a195a1f8dea881e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8273503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4beed9d37d5f6e1b0ff55f8e2d060835927d4710f382824311300e9a6058d28c`

```dockerfile
```

-	Layers:
	-	`sha256:fdf1fdbd48dd9a15c42bc6e320729b5245b77d307f7af06fc52518f3c9764b1e`  
		Last Modified: Wed, 22 Apr 2026 04:45:32 GMT  
		Size: 8.3 MB (8266249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859e1c5a38521180e49eb6efeee6e0f2685625043aa2d85525ca9210c3d205ae`  
		Last Modified: Wed, 22 Apr 2026 04:45:31 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a1e5e7955190901eca12f1e0a42286271d71a6ac4190ab2c03079a6e423798ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141663187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f383fe5006febc85d5177a41cd6e3c69556bfe7c327f5cf34225ce9b50c3e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 02:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:954ecf3bb623246e76e048be8db255040be0be61ff8078225017790f93fc2baf`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 45.6 MB (45607386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4a57ff6691b334a65a098db05baf2d825403eba2a4b68b46ed1f8e5631b721`  
		Last Modified: Wed, 22 Apr 2026 02:19:27 GMT  
		Size: 24.6 MB (24571415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7503e8d389d3b018f5a8af46a1adf37cfb06de0bf229b0de9a3c362974c271e`  
		Last Modified: Wed, 22 Apr 2026 03:52:38 GMT  
		Size: 71.5 MB (71484386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4256fccd730853585ad9191003ba39583a8a2b99b26bd07b7e62eaafd6ff5a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8273472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf8e64d654ec7f53167761aff9541f49bdc398135d93e40cc86a1c68c267caa`

```dockerfile
```

-	Layers:
	-	`sha256:3154b13aa1ddb0603452493493d84797f5ede52b25f932f2deeb17087b087ba0`  
		Last Modified: Wed, 22 Apr 2026 03:52:37 GMT  
		Size: 8.3 MB (8266154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbf6da1c76d9faec8eb0ba0adce59af5da80785f2f27cfe2c3cb3e92fba5f26`  
		Last Modified: Wed, 22 Apr 2026 03:52:36 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:52b04cf94094aaa1b565c26d53a00d2397d9bfa30793d215fdb3fd9834fdd6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150953150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1731e6d33aa35a01d4d19b7300af84ba2a88b09f5d6ee44472cd613f89adfb0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36d1ad0e4ab39e59341cbcc6c49601be7cf05a2f81f334bc0215a0d3ddd3d6e`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 26.1 MB (26142281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5418b7c9b07059adb828d8a810a5c248d9886119502e1a246c8454ec1d4f00e8`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 76.1 MB (76099498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a19426f63e44c6bb8743d386339bb8b77a0d607948b947a5b8b961e7e03e6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8286365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f49dffdc8c7dd12e15ecc8ad418bf8f322fdce007364c8def2d7ce708ca3e62`

```dockerfile
```

-	Layers:
	-	`sha256:6e4168db317a2d19afadb9b890e585e9b6d3d2f4927f0ad1ba113f2212c36711`  
		Last Modified: Wed, 22 Apr 2026 02:32:49 GMT  
		Size: 8.3 MB (8279031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6697cf2ebb6947b723b36e3ca653af370ef9873936654416fb9fede1defc27d3`  
		Last Modified: Wed, 22 Apr 2026 02:32:48 GMT  
		Size: 7.3 KB (7334 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a6adb5b1926f5a941056fc606cca0790ca8d097c6971b1281ac776bf3af05692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157619362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6620da289fda1fa40a0553bd613731be4b202af42232be8747d7b62a4b8c9d2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c9bb2730bc0ff710016a40d05d0bbd6ab5db1f6ed39dbb5569902bdddb97cb`  
		Last Modified: Tue, 07 Apr 2026 01:46:36 GMT  
		Size: 28.3 MB (28287053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61d37ae8d9569041f72a5d94976af076721a00ef2857d8844925e31d049b859`  
		Last Modified: Tue, 07 Apr 2026 02:41:38 GMT  
		Size: 79.3 MB (79338598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b933105e72c0c76e8b69e1f8be612bc7cfda3ee0c2d3fb9372cf31bfa3956b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8265330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae27655ad111f5ef4b215ce0336542ab798dc7a5bd8a1f2236be00ef0b9aa56f`

```dockerfile
```

-	Layers:
	-	`sha256:40c0594789e1a7ebad8e0b791c2724494187500fdc5cb6fd66b6f78427897c41`  
		Last Modified: Tue, 07 Apr 2026 02:41:36 GMT  
		Size: 8.3 MB (8258098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2024a1fd5114c06d5234895d45c1b9c6cd92d819c5c83320ff31f90c473a812d`  
		Last Modified: Tue, 07 Apr 2026 02:41:36 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:122e244fc93813ee016a8cb036cbfab4ee94bbf3d4ceed0638e75c00040d7dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167178347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3827815f15852c385e77ef5bb1cec8c028a90527ccaa6c4ff946a870298e40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 04:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8091a6b5ece83586bfb56b6975e0b2d9bc01c78d84b526c5c6e82463bb755232`  
		Last Modified: Tue, 07 Apr 2026 00:11:11 GMT  
		Size: 54.0 MB (54001950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3485868c65e901d140674210bf2ba257ab5ac6120dded36f6536c4e9c5178623`  
		Last Modified: Tue, 07 Apr 2026 04:23:16 GMT  
		Size: 29.4 MB (29412504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03748ec5472f740753f922099fd48a5c13afbc87f15362a543b090bfa949e6b`  
		Last Modified: Tue, 07 Apr 2026 09:54:16 GMT  
		Size: 83.8 MB (83763893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6833b6ab7f873e4a3c4daf3707fedcef2c2258ec3e2b2c11719ad53c51b3fb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8254809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57b3eacec2f70479dc0dd9c6324d6cfa21150510d0d72390ddd19cba50e7333`

```dockerfile
```

-	Layers:
	-	`sha256:6a8431297b2621ce22619070dadf6124df71fb7e14a572f0830dee51ba8a00e7`  
		Last Modified: Tue, 07 Apr 2026 09:54:14 GMT  
		Size: 8.2 MB (8247523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ff2f52f0dfffe1d4d9c536eb1134261ad6bb054953d4f592908f7e2e338d31`  
		Last Modified: Tue, 07 Apr 2026 09:54:14 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:bd36ac998598f67ce6a427579393ced06012fe3f7e6401da49d295212ae80fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148969028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6960051a38d6301962ad6cbe20b3c702c35d37fc6804cefe227d35ef3dd724ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1775433600'
# Thu, 09 Apr 2026 01:50:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:52:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fd96dd3de127541ef7e3bc5f9bc63bfe49b8f35d0526495ebca95ce89fe40405`  
		Last Modified: Tue, 07 Apr 2026 01:43:52 GMT  
		Size: 46.8 MB (46786906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b785d28162b0b158cf1aa6f3a70ac887d4e1f003e08018a8a82c545e382db`  
		Last Modified: Thu, 09 Apr 2026 01:52:08 GMT  
		Size: 26.6 MB (26587111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9eb0dbc30d738e4ada815d4c1a60b004d3e4e257ce261f7e827b021d2d90`  
		Last Modified: Sat, 11 Apr 2026 02:56:20 GMT  
		Size: 75.6 MB (75595011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a788016f4c6ce9bc1b692499c8b19149f44cbda68fdb957a914b758c3cda889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8259724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e24c56f2a296478b5231b95eed303886ce95a182b5050e71a5073b727c12b0`

```dockerfile
```

-	Layers:
	-	`sha256:16af37a506a02112d412fb0982bbcbcbb8c4c7d45bdde9ddee743424824c4e71`  
		Last Modified: Sat, 11 Apr 2026 02:56:10 GMT  
		Size: 8.3 MB (8252438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05362487f36f0158ff2ab5c530ce1f48cdafec9f4c2bd78336e0f736f1c957b`  
		Last Modified: Sat, 11 Apr 2026 02:56:08 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:74614d40819fbf486bf929e5e2beef38e4c64b0fbc1eb17c97e5126df14ee84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152938672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0873371520f2a378f0a22ecfbe1cbb34a3034f5c70d6f63851c1845c70fff77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 03:05:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f4e3a27ede4ed598ceeca73aae5842ded1c7c01f18c06d6c08d11ba5ee2f57e`  
		Last Modified: Tue, 07 Apr 2026 00:12:04 GMT  
		Size: 48.4 MB (48425378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3603919d864d726efd51563d3638c0f58e2671f83ef3d775155f64a94b910d45`  
		Last Modified: Tue, 07 Apr 2026 03:05:17 GMT  
		Size: 26.8 MB (26795763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae2afc6f5b4c5dd73680a5531235390e280e79ddf6ea03c9527bb4f35951d71`  
		Last Modified: Tue, 07 Apr 2026 04:55:17 GMT  
		Size: 77.7 MB (77717531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f9908b449b23e02f3194b05f7e713dc741aa44a2838b6c1e2e4e590829d19fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988d99d31644a0a4552dbf7ddece10d43bef120a455a93c3b92c9ffb8001f635`

```dockerfile
```

-	Layers:
	-	`sha256:568e663603631caf5360131efa56543dfba2a7fbffbd0927c172ecd83ad26eff`  
		Last Modified: Tue, 07 Apr 2026 04:55:16 GMT  
		Size: 8.2 MB (8241257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee67fbd2fe2215f9f70bd023679be7d12b17bd4c235fad431c7bd5b7e308fe18`  
		Last Modified: Tue, 07 Apr 2026 04:55:16 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json
