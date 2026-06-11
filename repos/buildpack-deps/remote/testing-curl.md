## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:cb3e1ccd27b98c3b3bc73c3c59fc68c6dbe3d3312ca5f946eb50915f190f94ff
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1d6bd5b73c1e25690c8ffe35ea5343f57fe4ba4ae4627184151b2f84511b58f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75697956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85a697028c8f9294dcc049664fe94313c58591822ef1a6d13de738de70303ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e7f09040bcd4eed376c1a5f9491753b37de5abb58b8a75ba459283597e98a`  
		Last Modified: Thu, 11 Jun 2026 00:42:43 GMT  
		Size: 26.9 MB (26918682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf9d781f4f4a64e15b2cae9928b96fe2b2c746e88940780a52d498b471e0f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2076f7ba44c80dd8c2415f31ece0ecc848c2cfe492e0e6d339397aba57bf9619`

```dockerfile
```

-	Layers:
	-	`sha256:401c7d29aa38e4590e42fa17128f910a98b3a7383dda26097e15b2d964683f70`  
		Last Modified: Thu, 11 Jun 2026 00:42:42 GMT  
		Size: 4.0 MB (4048957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5c6d68b644a91b4d906f34782e8ff35211befaa5d948b518a7926bedff63a7`  
		Last Modified: Thu, 11 Jun 2026 00:42:42 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b47a76ecdeee4e2d3b07849cc05db2e2d78e673d57eb79323c90550176c7343a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70206098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f1e16c98f0e03325e4543476bd76a0398581a3a0e1bd2f3d33b15be137bb4e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 00:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b6df9d4a408084133e98c8d6c8e0e3de38b9e95851bc2206e09b39135c71bba1`  
		Last Modified: Tue, 19 May 2026 22:36:31 GMT  
		Size: 45.6 MB (45603185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd97129e166740f6b7d385932f0e29058407c0b25cd1d04df0d94fe382e494c`  
		Last Modified: Wed, 20 May 2026 00:03:41 GMT  
		Size: 24.6 MB (24602913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d4c9f9cee7135c22c7e77cc25e0a4245693b608867710a7cfe76286b4942f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4075674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99a4905df2d7bfd28ad46ea052faada1c5e0d2d69d962d3e4840e59b65cd64b`

```dockerfile
```

-	Layers:
	-	`sha256:8523adc3dbc44e6b72491295823c3024c383b6ea8d7505c330eabc1798f6f66a`  
		Last Modified: Wed, 20 May 2026 00:03:40 GMT  
		Size: 4.1 MB (4068837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff7795e4d1f1e73f8dd394001418633bf362fbff00deba368a6efbd5fb5655e4`  
		Last Modified: Wed, 20 May 2026 00:03:40 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:62f874930f9a4fe26946a54ae9d23fef34cd59f0d339a2caf622a7e05cedc5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74976426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738b7273d147ec05574fdc119b7f33640b21b3060775869b6ba96ddfdb6b8c23`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:44:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436ebeebafee761b67c6633aca1ce7141531b193dc4a7a4858fb1b0cd75f8462`  
		Last Modified: Thu, 11 Jun 2026 00:44:25 GMT  
		Size: 26.2 MB (26180818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c84a7284129b371f2ed3d2c227c6b27f1a247c0217bdf70e9d51750635651f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4061168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f8a11587a45f66e3415e8b1f2bb8ba06ba43150e3eb0de80b2a2360eb9afc1`

```dockerfile
```

-	Layers:
	-	`sha256:38582bb92da554036b1f5922ada2758f858e707974045313701a5f72d7021845`  
		Last Modified: Thu, 11 Jun 2026 00:44:25 GMT  
		Size: 4.1 MB (4054316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588f90a6efe3ea9f9b690ec20a59f4b46b474d77d713d132db8a3c3a1ad15272`  
		Last Modified: Thu, 11 Jun 2026 00:44:24 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:19129cc2edf7e7e22de9a344ac863a9c37b1fdcfeca38197b26d379dc86dce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78209914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019f7b9e7b2429abcd8cb126172ceced0185b3127c8882355364a694425c94a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497fcbfcc0cfec531a77167884014e2e81ee738aa6aca34516d78ed1b945bdf`  
		Last Modified: Tue, 19 May 2026 23:25:23 GMT  
		Size: 28.2 MB (28207970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e9a0c0ed0f8d71d90ad1e8ef8224cc8036b74fb683a27c88cb069abf69978b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096e93ed366eef8dc165306be8d07c431bede3dd35b57093bee50b48949ba72`

```dockerfile
```

-	Layers:
	-	`sha256:d5cb1ef13de4e086165b2e2dbc103d3cc8dfc15ca15dbac860fe4b826b0e0a55`  
		Last Modified: Tue, 19 May 2026 23:25:22 GMT  
		Size: 4.1 MB (4064453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243aa5407c6ee779c5f72043f6c8a9cc019230b7e54c8c9b1aba8f9d51b0892e`  
		Last Modified: Tue, 19 May 2026 23:25:22 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:06884bb5825dfc83b29cbe9876a84d4d3c18f8c103564f93212a05a287f0e186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83307175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0eac9978d3df6c3c5beecf75cc2b7e9180adfe2405e8cfc052d516a952dfcc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 01:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e5564b9da7290f7430ffd86cfc5f2b22a68586fade0aa81c8610704c43fd41e`  
		Last Modified: Tue, 19 May 2026 22:35:40 GMT  
		Size: 54.0 MB (54021281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24877c775bac285836892c60f877392eff4299b16fa48a35fb91c222b64558d`  
		Last Modified: Wed, 20 May 2026 01:13:54 GMT  
		Size: 29.3 MB (29285894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:deb767b77ee7d3d15d954f380586383eda588718f55038ed98cb15cfb3583f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4078013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de4fa22cf203a1da724a1cd8d898b5f90ca5f827582445d249b1d4c24ffae88`

```dockerfile
```

-	Layers:
	-	`sha256:b148244f9798c0a87c4cef4940917ddec8782087b2180a789476b5d9a69ac2c6`  
		Last Modified: Wed, 20 May 2026 01:13:52 GMT  
		Size: 4.1 MB (4071208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183d91d35f8dc6cda15706bf31c5ea3ddd8cb27f32995cb2d4e60677a0c19023`  
		Last Modified: Wed, 20 May 2026 01:13:52 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0667033362d6b463fe6235c993be673382f0ee1749384d943391a3eccbb68a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73285352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79475f1c6f62d30ca1c3f37ab42af5322e9efe9350dfbd0ff7807331eb9c2207`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1779062400'
# Thu, 21 May 2026 13:54:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:233e2e85000f46d884ecdf2b81662e2915ae4bce2cfd6a573318e4ae99ee6839`  
		Last Modified: Tue, 19 May 2026 23:36:02 GMT  
		Size: 46.8 MB (46833187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa3768beafc01f566f53361a18d9c7150398a0575500ad1f3d3da15fa52ceea`  
		Last Modified: Thu, 21 May 2026 13:55:52 GMT  
		Size: 26.5 MB (26452165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b75148b515b8ffdee20cf823e741ae894f747d766c94e99e53e9d9a3b19ac02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4065860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ac5c27180f312595218fb833efbcbf5c9b0dacd09cbe3c34033fb4851d8345`

```dockerfile
```

-	Layers:
	-	`sha256:8ffe4ab35d6cb5261bbfff35c1563746ea7d30b81517f4ce15ca1a2f3fd70009`  
		Last Modified: Thu, 21 May 2026 13:55:49 GMT  
		Size: 4.1 MB (4059055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5e6bbeb2b614b360a50971e2476a3078cef59405e6c310564d43f0cecdad4f`  
		Last Modified: Thu, 21 May 2026 13:55:47 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:61062f67b299d0dd69097af8e6f73c6b8c1fda54dd5acbb5147726b41118872f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75129193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf439a1fd6f4ca82d31a3559bd5655610d2e3274b877bcf5cccca78d723b8b5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 00:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7394ea10bf5bc140ccf55e31841e993aa40f4cd465376d373dbae4fff2479c30`  
		Last Modified: Tue, 19 May 2026 22:35:35 GMT  
		Size: 48.4 MB (48440526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fee0ef4f478ac4a827949260fdd413d25005b05e8864d837f644813aef5311a`  
		Last Modified: Wed, 20 May 2026 00:18:29 GMT  
		Size: 26.7 MB (26688667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6d9c463451ff35df8bbe3505fdc468877666d419371abdac869ccff166a22bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4075535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58dd3f29e4d4dde664a2deace214363a61c4b5ec9ffe53348ca9ffd1df6f687`

```dockerfile
```

-	Layers:
	-	`sha256:95311d4d4cbee9bdce269862e8c20310d1026f2ab8f3437c9def0f411f910a40`  
		Last Modified: Wed, 20 May 2026 00:18:28 GMT  
		Size: 4.1 MB (4068762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f488c1a5678b8e9a956ae42d002857769a88d97fb6a75e18d8ab4a8105f196`  
		Last Modified: Wed, 20 May 2026 00:18:28 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
