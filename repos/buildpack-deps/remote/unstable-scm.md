## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:fa2e7da3995ec232edc114644d7aba2911f5c8277c95e69ed8e85b714c0d7279
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

### `buildpack-deps:unstable-scm` - unknown; unknown

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
$ docker pull buildpack-deps@sha256:b3c420a89727b5dc5067f3f9dd02acb063f57893e27884c02d8f2104e5e05870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128046045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738f1c2cb570c23741cfe2b7fe5652af9bef05fa04bdba68ae8b35b33e93925b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5bb5787cc9d2878988b37d2049fa1d6b67ff3450f012cef9603dcff05b03ef`  
		Last Modified: Sat, 19 Oct 2024 00:57:32 GMT  
		Size: 18.9 MB (18893656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f7ad36a85c1a25fec35fecdd0c231974acf44c7aaeec9321464cf908e0e452`  
		Last Modified: Sat, 19 Oct 2024 06:39:20 GMT  
		Size: 61.5 MB (61460990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9db4cf0319144959de60546593784cc663d31b4196f01692f0735bbb32f55ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5a3d725a4310da5f1831130375142b0c20d3b76ad85c1979e28711f6289983`

```dockerfile
```

-	Layers:
	-	`sha256:fc2860af086787f7758af329dc104412d3c616d8f41f41ca89aad651c478bed6`  
		Last Modified: Sat, 19 Oct 2024 06:39:18 GMT  
		Size: 7.6 MB (7591192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab2ce55dca633eda9a90680cc443df4c7645b5e860e2cf82d4861989c3d253a`  
		Last Modified: Sat, 19 Oct 2024 06:39:17 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:802c828bc2d5c912348dee436053e3aa7d82d26837f894566a3f6381b19a0ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140380464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877345af7ef312c479c5be927342731e90dd345572ff8fde69dde61a4aa757fe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19663fa8e0a57915a50484edf1e2599200b05cd9b029d04f6246f46e4ebd7b8`  
		Last Modified: Sat, 19 Oct 2024 05:19:11 GMT  
		Size: 66.6 MB (66554364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3bdc370b125ed8b8193e8750270c2d8ec3cf86815e299ac1b5e01a42224844b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739a6c936ffbddb93e2f0497b97a3910e5b4a89d807763c9a97116823c23aefc`

```dockerfile
```

-	Layers:
	-	`sha256:95ec60fa71429ed1b411dc8b543221800db7aba2271e78572346255708271d50`  
		Last Modified: Sat, 19 Oct 2024 05:19:10 GMT  
		Size: 7.6 MB (7597088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0473ea6aaf55e12d5241f62663f89556fbee6b5d58ad766cf0d2a66168faf10`  
		Last Modified: Sat, 19 Oct 2024 05:19:09 GMT  
		Size: 7.4 KB (7389 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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
$ docker pull buildpack-deps@sha256:61c4d6cc10809fc80188a1f1df6ff950e471673160ece56deb79ca5016c570c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151014445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401aa0cf32bd8f62d6d25d11a2ea6a4da7974387a28639bb95f8a688e37437e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f3cdfb0755564cd3c4456a7fa23e621d79e4f8f43bd8107c734f66d381334`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 21.9 MB (21944061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fc954d509992bc0347fcedb989b7696ca6b5029587c5a3cacd05686fe99e03`  
		Last Modified: Sat, 19 Oct 2024 04:08:51 GMT  
		Size: 71.9 MB (71893560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e62f5f0e017c8f9977aa9d27e6c50468ed4359de5f9c2b1a32dc27b5fb8054a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7604971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db29662bd0d5a88b98f81de3267e604cd42271eab925a6a159518cbfd266f788`

```dockerfile
```

-	Layers:
	-	`sha256:dc8587b4a60b823bd27bf8fefb21c0194fb50c644ae53b07ece8f07435740e12`  
		Last Modified: Sat, 19 Oct 2024 04:08:44 GMT  
		Size: 7.6 MB (7597630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388754175027e015f6a047f0977907724e96b2acb63d81d8ac85b1169cb57a09`  
		Last Modified: Sat, 19 Oct 2024 04:08:43 GMT  
		Size: 7.3 KB (7341 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75798f8edcf34cc806383a3cb0d582183149dbf1634de5c038911c2d039a57db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3c4460532df5edbadaa408870e0284979bdf475836695ee5d0a66eed35f17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a7102bce19ae53b519fb58ec97dd26aadbdffdfec95cd2613f51b842e60866`  
		Last Modified: Sat, 19 Oct 2024 03:47:42 GMT  
		Size: 67.6 MB (67567932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:678287387bbebd1636e0fe5a2aeb073194add8b6f5c394616c9e1c23ce56b241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5a40b14913c0e75a4b4bfbe1fb8e67f0bff40be7dd304d7a42dc794b6abe0`

```dockerfile
```

-	Layers:
	-	`sha256:849570392004a4d0cd1b888908893e70054109b2a9280a5ec80ecc396d7baa25`  
		Last Modified: Sat, 19 Oct 2024 03:47:41 GMT  
		Size: 7.6 MB (7591606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcaf34e81575ac3e7c8e9cb223f3661f4b719530508731fbbe38bec3829d0ac9`  
		Last Modified: Sat, 19 Oct 2024 03:47:40 GMT  
		Size: 7.3 KB (7309 bytes)  
		MIME: application/vnd.in-toto+json
