## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:98480a63588e0a05d8e2d525f5446b38da7aecc1af800401e54709066e389111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cefdabdf0dd3c0be2093674bd463a08706c6823b51ef5fc98e48ffc279c7b2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140301369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873827b625b63287b3afef0bf4cb27db9fad9dbd5c4d914199e2e3ad3886952d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b881a2f1232350ec7e4aefdf5b77bf5210861f5960ef5f73da8c0d1966802d8`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 66.5 MB (66470763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:86827b548c07c2a481cae7d5aed48a4134e1de1c2408c43d0149d39d11eb5be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7597828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6b88eacd87f5f5f93b910719a867bece0a91123b33c13459cd08adfccd1dcc`

```dockerfile
```

-	Layers:
	-	`sha256:511627375d7bd2a499e03c8cfffc6fba5567efd8d47aa35eb624b4dedfbeec23`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.6 MB (7590531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3af11e7fde68c3dcc1bcb722db1234981bee58c66281bb50a9ac93c213e05d`  
		Last Modified: Sat, 19 Oct 2024 02:06:27 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1a0c5e363a8c8458928698c18a4a8e521685db479a3e4929571a9edf7be07e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133702859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecd7b81df49fc9583d1ed7d438d04c77a3510d7c84eff4854a7cbdb89fd0882`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907cc8268897b865af11c617e0b6df9243de9b6a7c9d42c7a265f1e626be0e8`  
		Last Modified: Sat, 19 Oct 2024 00:55:48 GMT  
		Size: 19.6 MB (19568622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f2bedc6e003c8fcb6ddc00648906d674fc1d4c5b2e82a6680469e7f789b52`  
		Last Modified: Sat, 19 Oct 2024 02:56:49 GMT  
		Size: 64.0 MB (63986649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9369d4f874cc01265f2427f626d8649c9cdd3722f987f0d4b53aa17f58a1a519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6c6d1f54b094e28a0a046b11471758394539a5e24a2d8ac19ce9002a04517c`

```dockerfile
```

-	Layers:
	-	`sha256:40318f210768de3c2d4f236c08a46c811ed3d6b77f90eca2d352e046bbd4b523`  
		Last Modified: Sat, 19 Oct 2024 02:56:48 GMT  
		Size: 7.6 MB (7591440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894b2057d9859fb2183c0e57461992918a9882da2a000d88bfade69135b7fa9d`  
		Last Modified: Sat, 19 Oct 2024 02:56:47 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8aadefd3e343da4e9702c36796018961a379e983ab737f71f2f3211b60d7593a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128051993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e644e21ad23ef2338385f0c3e116bb4580648461d4de4ce2c03a6bf9154c9e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd60cc121d929130eeee92fc8225e4ed5482cd36b62a951095ebafb943c0a1`  
		Last Modified: Thu, 17 Oct 2024 03:38:59 GMT  
		Size: 18.9 MB (18896921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32490c623445d27e949376c8158021571cd8530fc358794dc7642b8bade85da`  
		Last Modified: Thu, 17 Oct 2024 03:39:18 GMT  
		Size: 61.5 MB (61463673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86fb5cafcfd67c91f88f662be09d8efd8f81f8a44fd56b5eec7bb1cfeeadc222
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140385741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599d6e0616d8c9af6627283576f1f866128aa3124b23b7eb286cf69ba6ed97a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:35 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Thu, 17 Oct 2024 01:12:36 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 04:33:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd949d90425f27d9499ed62d5edc09c30effb2a25cacc5cdbcec475f72c714b`  
		Last Modified: Thu, 17 Oct 2024 04:37:48 GMT  
		Size: 20.2 MB (20199608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318bda2b7787f1d062cd74c8c3d67fb18e99d812d82717501702fb68c487f68`  
		Last Modified: Thu, 17 Oct 2024 04:38:02 GMT  
		Size: 66.6 MB (66556648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9aaa755d266f547c1623a88949b4896927a675bb6fd3bd3783dddad9c2480671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144071948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aeaac6bc6c4ee0f59e06f93e4c2d110ad682bf40ec1764237e779701249494`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29126a4a4aef17404bd71b479313e117a2f9ea628fcde52f725427fcf1c14fc`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 68.3 MB (68288819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3eb3ece465260e3901ff62f2585ad45a0bfd5b6b634d72a26ed94741a1ae0ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7593234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a0a9bc4cbe59a31877f787277224df9ea7b136f550c13853d5ec0bfd917c8`

```dockerfile
```

-	Layers:
	-	`sha256:cc6abc65fedce21ea5c2f45dc7b45f01c13382ab72ecd3623e069de8d70500a0`  
		Last Modified: Sat, 19 Oct 2024 02:06:40 GMT  
		Size: 7.6 MB (7585959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ddc7234c652467e21b26b6012685d27a4c664f836195c5ee43a6425eb01d17e`  
		Last Modified: Sat, 19 Oct 2024 02:06:40 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90e7b41bb44f0aabb12b036d985456deb388ccec89696004083da5b293198773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138325814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bf84c04011b93921d0604ae5f4b5ff157d7ce4141958a4446f7682abc63e18`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0552c8f1cd92a1e8490dffddb1bdf464601603e6f79a1d72baa7fc8463fe5fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ddef53b5b2c40e1838553c952ea8f3401900b10956137e1528e15ff24bcbd`

```dockerfile
```

-	Layers:
	-	`sha256:793454691f682b72aa95b4fbab2aa8dfbd92025fc02eebcd17d82fb50e48bb05`  
		Last Modified: Sat, 19 Oct 2024 02:11:03 GMT  
		Size: 7.1 KB (7141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7288ab3e7e6db09def5b1cc544eb80aa04bd3ef646e07db6f8f6e7c120233aba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151019005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6b9491c5e468741c9c562c0c94e57dddb0d70870f444371ba0aaeac35377aa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d6fbbdfd760d192f962f091ac6ac50b83943b30afeeef05cb2189597ca0d4c`  
		Last Modified: Thu, 17 Oct 2024 01:52:34 GMT  
		Size: 21.9 MB (21945036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d006d9437ccf6825ce93da875340581aaede61b1bb556c25053444f5d60f2`  
		Last Modified: Thu, 17 Oct 2024 01:52:53 GMT  
		Size: 71.9 MB (71897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f41963d04008c34614a5bb83c83566a25d5bdf9e3fd2c195645f296d411e795e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137347404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24da5a220498ee10a0349c6924b4f69cd9ccf123ff35dd6d905d518f132d6f97`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cffe06738a4c488c5af7baf511864fe81ba7e38149f28d93443e35a8d7d414`  
		Last Modified: Thu, 17 Oct 2024 01:54:09 GMT  
		Size: 20.0 MB (20025281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cae9f617aba80ede947d89c8c1533181fbf6bbf33b4f52cd58a464daf4cadf`  
		Last Modified: Thu, 17 Oct 2024 01:55:15 GMT  
		Size: 65.8 MB (65759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:85a735d32e2fa43089bdb4f3c65714eb70eb4e91a2ae2ecab4f65c2f5b5b1f0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142061706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec962159d905018bf7a4dc6ea49aeca8aa53023ded7a6b21ac8fe3f824aeb1cb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:33 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Thu, 17 Oct 2024 01:46:35 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72407aa6b20ec8dd251f8d046dc6a90dc4762b5a40f3de1875d57e9707b2249`  
		Last Modified: Thu, 17 Oct 2024 03:49:29 GMT  
		Size: 21.6 MB (21639364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebcc27b289c6aff3a3be7c20455e5a315df5f3865f769b958bcbc9fa8876cad`  
		Last Modified: Thu, 17 Oct 2024 03:49:43 GMT  
		Size: 67.6 MB (67570361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
