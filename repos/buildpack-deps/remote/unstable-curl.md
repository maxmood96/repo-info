## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:a44b2383887477260f69cd7a6dbde35c1fd6672e8354dff3ee6b5244d0fe7612
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c1288fc2b1708e7951604c5c1bc570584edd10e5bcd54c9177a5e06e7d0a6ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75718090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c89afb4e88dab8ac303418228d23f1b561bd027ccfe13d335059388a0999fed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7ca04ba629f5f7cdd4aa096cba4636e37f730219647da205f4cb7f89dea8d6`  
		Last Modified: Tue, 07 Apr 2026 01:47:20 GMT  
		Size: 27.0 MB (27007442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b26a6a62371fdbdb2e8a927cf71ebb96c190653c740d56eff1bbf37008d1c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32abc32b00c49193c3224a658b32dd3e2c9caab244fc454242c952cc7212ddcb`

```dockerfile
```

-	Layers:
	-	`sha256:3419bdcce7b707dbb83f7e057b7924b01cc5d65a4b9d7f83d67035771e98156f`  
		Last Modified: Tue, 07 Apr 2026 01:47:20 GMT  
		Size: 4.1 MB (4066290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd70c1f0fe2b60919001461b52925a0336f126f69e8127e2c98394469c843a4`  
		Last Modified: Tue, 07 Apr 2026 01:47:19 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:387da019fba66d0664f66a37d0b9dba0ffdf4a745d59cd3c544629d6cc81af35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70329144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce51a1a61d61d0679e87b171917af019ff54c6f83841fcb0d9e079fda99243ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d57b8f402ed3b2e5154e90fbc7b01b4f8d5c01264728a34f6ab1adc5ba51c506`  
		Last Modified: Tue, 07 Apr 2026 00:59:34 GMT  
		Size: 45.6 MB (45637964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc68b29d82a1982370d6e1b760ed4153b5652ff3b2c9443c5f434615b7c9d54`  
		Last Modified: Tue, 07 Apr 2026 02:01:52 GMT  
		Size: 24.7 MB (24691180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cdb3cd584425b0c71e06c293a61271644c8f3df4fb0ce125a831c6e3014e3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b08bd2b58955c1dac0186f49820d4ce04e54b4e064d373b2f5f82b697a73ed`

```dockerfile
```

-	Layers:
	-	`sha256:7f4cfa7195d3eb4e6e76117253beb73f8f7d0805fe39cc1765b5a9ad8174a4b9`  
		Last Modified: Tue, 07 Apr 2026 02:01:52 GMT  
		Size: 4.1 MB (4067780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b13ba5b081bf10cd666251116d2d89e50fd3cd811e39087f5c5bbb0dd1471a`  
		Last Modified: Tue, 07 Apr 2026 02:01:51 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5f513d41426384ab385d35f48d6e5999ed4c3309ccd0320c0bfe3ec883b58b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75044202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ca7e9e7b6c43e50790a39d6c0e29e75b4ba6c741d162bb38a1c0f9ec21d2d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:50:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82fc2e1b0c8b2b1d04da85219313625f50f9cb567044095b396e8e551b7fb8e`  
		Last Modified: Tue, 07 Apr 2026 01:50:20 GMT  
		Size: 26.3 MB (26299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1ca0a13d05fc7c07c733e86902eaea13b9c770e44b2c088435a7c41f5833426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d3c13fd141cfab63d2b06d956b1f9ee341102ff34b6b6883804a33569c168c`

```dockerfile
```

-	Layers:
	-	`sha256:f602700ba9db32f83117cd1aa0a734d344d32f363d541f8c6fd0708135a53657`  
		Last Modified: Tue, 07 Apr 2026 01:50:19 GMT  
		Size: 4.1 MB (4072930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb64feb548dbb50336441585449fe3bddfbbac93fe38bad7c7456d5a2e210aa4`  
		Last Modified: Tue, 07 Apr 2026 01:50:19 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:341f76a9b3f546b12108f54b58d466111a28dd2e5f2ffb4120fc09dbba21c368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78280764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de063d160a05c146a836bce7b6cafafdf44e349c5319bdfeab3b34d52f95ca8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b6110ea3b3e29ee9303e272012a3288bf7218909462f19d4bb3104166348873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1c58eaea9ff77c9c571f496b3cd1992302faed55c805bfb55a456480b2c951`

```dockerfile
```

-	Layers:
	-	`sha256:74409808c8cd9e845a59c21798b156274b16db5827e350cefe2f8229450130e1`  
		Last Modified: Tue, 07 Apr 2026 01:46:35 GMT  
		Size: 4.1 MB (4063403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7529204a2e5f56e4ad8fb4cbe946d756962259927a0583d82bd85a8491065cfa`  
		Last Modified: Tue, 07 Apr 2026 01:46:35 GMT  
		Size: 6.7 KB (6738 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:988b4f8e959683097ba947aff3b5b4d95ed23b1aef62ff82d6a470250e99e33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83414454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e476accfd389b5215b57bcc6366680e29e64875af431f842d6ffce235563fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 04:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23e3f56ebd2f98cdf3ad1335de653a5beee1cf4588a9a1a3f5458a27c157fdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900ffb9597b986a8901cd557f8d6be62a29895f4de2bdba82ded1304e5aedc7f`

```dockerfile
```

-	Layers:
	-	`sha256:9195b61bafd083f360532ae39d0cdc2b029f5642b03cfcba931fb5d685839a07`  
		Last Modified: Tue, 07 Apr 2026 04:23:16 GMT  
		Size: 4.1 MB (4070133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6fb96a206ee42b4ed7005dfe411a4e3d0f39435b2c6b50e122cc022c8aceec`  
		Last Modified: Tue, 07 Apr 2026 04:23:15 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3abecce4a09efb3bd3d5e04188b1d9b7b87fc3e593c95d1fe76f3759abda0250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73383777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef67b61e50a26b0ba6c07d131feab2f90f512d88ec86bdc013f7403ef22c965f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:841ba95affedab9f4249c4c606ebf4cc415dddd1f44cb3edeed8f5199c8d1168`  
		Last Modified: Mon, 16 Mar 2026 21:58:56 GMT  
		Size: 46.8 MB (46778346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550401bf99e797417727d38582b31e96ea6704ee9ebdabb221407d77e3831412`  
		Last Modified: Mon, 16 Mar 2026 22:32:13 GMT  
		Size: 26.6 MB (26605431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6b0ffa894f9decfa2b28ac0c0f5bc5ce504dfc60d89af7790e5f4869a9892d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b48be4467fb6fe91cd23243f073cf02c501d0d59e1c86a0d7c51eff85d4e70c`

```dockerfile
```

-	Layers:
	-	`sha256:da2c67c2dd75bea79fcd9b5a51e3052e9f706a7a09010da81c10fe8181f45a4f`  
		Last Modified: Mon, 16 Mar 2026 22:32:10 GMT  
		Size: 4.1 MB (4064195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6108eb082eac32fb7873769df182d22ef41dc355bfbd19dc80125e628a79eef5`  
		Last Modified: Mon, 16 Mar 2026 22:32:09 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b872e9069be506cef29004446d2340a730db93d8e19917ec07c324924b1c73d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75221141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b353dc6c67346d7ee284a99c79fd900199b5e16ff21b5132b85df51d95398034`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 03:05:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85c2219f1d9a9d0ea2cb1ee76b3b408c53f86d586470c86a099c069a3c4cdfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7d0ea383dca09cd21175bc9103b691eaf48cb47489ad50acbf551c28f4274c`

```dockerfile
```

-	Layers:
	-	`sha256:4339564fdd9686741aded0d4463f265fab9cce17b7fc9d47943145677952e014`  
		Last Modified: Tue, 07 Apr 2026 03:05:17 GMT  
		Size: 4.1 MB (4067701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d00fb2aa65f424531c360e833ea8f3fed05431a745c5b5318616c6b2643189c`  
		Last Modified: Tue, 07 Apr 2026 03:05:17 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
