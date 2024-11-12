## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:22aaf2aa52187fd4232514ad986a4a45efebd57f5c0e5615e70eb3771c4a1449
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9f132228a17ef7148bdb181e503e91853e85e87c2bc91361f6705a2ea4818832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73915616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33126cfb84f42e1dee4d3bcd8e62d6e742b0c0fc0da59e149a079f4174ed740b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39c0a59346b52c497cdfee9ee501696a0137d33c4d869b8ccfb052b35a48c57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d64c3f557019664b8ed03939a488b65f662ae5ba8df3f8558e7eb7f4ef96f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6c5e88c9e7aefc1e66a2fb244bc4a7ee4a01996d4d1643d54fd9141b9d68c098`  
		Last Modified: Tue, 12 Nov 2024 03:14:00 GMT  
		Size: 4.1 MB (4052968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e06a147cc0d21461ddf7350b95eadd2a56c4f93dd20e46f3562015b2a9cc19c`  
		Last Modified: Tue, 12 Nov 2024 03:14:00 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6fa397aad3f688ae8c5a6a419b92021b1cdd17421ded456fab3c2ba159b1728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69787701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4def3959c1ec2cc47ca9f650e6e392ddcdf199ed79296fefa9f23c546bc85b9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:957883ff2bb35b1ce0198b37996e8b3b914135501561c94a4a330818e42e78a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e70fea3252b42f59d8b501dd5ad764980a1381758257617d06e4dfa151cc2c7`

```dockerfile
```

-	Layers:
	-	`sha256:88ff8e75bfa6830f20cbe46c2c6274c66debaf6f7cb42e797f70f8ed1ee639ac`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 4.1 MB (4055190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289839fa0d0c8815427f524a3c398ca48fb266a4cc30b70e149da06d2f68dec8`  
		Last Modified: Tue, 12 Nov 2024 06:29:06 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77c60cc265b95be3b104f0c8621b935379cee41049a173a232dc5ec430fd706c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66585055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80a481113f99d5a8cae3310407042e0a289b71236d59c1ed76c30c45339a239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa977a262dd181b45467b256087bca990abede89e133911524cdd68e44f417fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253aa76a9639b3e075a66b78d5e33f7d1c5029dd58b35967c686755f5c25c939`

```dockerfile
```

-	Layers:
	-	`sha256:88a067eab1dd02b5d086716eef3db36d32ebbb0f1c6015519cc361eb70246783`  
		Last Modified: Sat, 19 Oct 2024 00:57:31 GMT  
		Size: 4.0 MB (4030333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad857591c01e9afa58b31c832b0a59d253a0df59d62143775e95f07d9629f49a`  
		Last Modified: Sat, 19 Oct 2024 00:57:31 GMT  
		Size: 6.6 KB (6643 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bc7f373af02269a239ab6419112615ca6690809a8d95bf7f43f1377dd2d6f476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73826100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08daf7da3e665395ab5a0d8cc1d5f760a074733172716e6fd4467fd79b96d66e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d70cfbc938d76d89a533bfb2fc5f1c306ff2beed08d6499de05ee55cdf580a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8716ecd1dfdc9cc5c59cec4b6019e1bfc0b6dc6055fc96fa508f5361182df192`

```dockerfile
```

-	Layers:
	-	`sha256:b591e9052a8f907be44d4656ffc3d018c55b54387630fff05f2d2fe1759dd869`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 4.0 MB (4029090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56316a4f7de5fa0299ba7bea33b33e2864d292edecf4a7905dd390fb3254c0de`  
		Last Modified: Sat, 19 Oct 2024 01:11:42 GMT  
		Size: 6.7 KB (6664 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:713ac9d8ce038686ba88e304844d03029927103f715e36c6e3e7e643f648cba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75917438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbbb27c071a87a94f9d4da6a554ba80e231a4d61d781ef5427f2ea0cb7bfad9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e72acbe40d1dada9f63a05e02f9a246749c53f9785c0f442cc4a3c00ab26b48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58971737022f0686ee08a7e75b6b49ac4d35e293b2ac50c454cd02dac2be18d`

```dockerfile
```

-	Layers:
	-	`sha256:f398d7abacfae0299acc85184a23c92cb8040f679acc31f49830129acfcebcea`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 4.0 MB (4048708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d240f2a814476b467a314a67e75244714b4479add937403e3b8169171e9cce8`  
		Last Modified: Tue, 12 Nov 2024 02:37:52 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9ae3cee97b6b487b5d217ef86e5c40770bce1291c93921f4d8d77305d0db5352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73045522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c4682cc57a81be3fff028130561f3c6eb09ea9654477dd9e698f799cadabf2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1882a78a33be52eda30fe2c75c6c6d9967f3fd85b20979f451f5c04dfeccde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 KB (6414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b736f996c2064246c296003a1cb4fcddbe3de476eb5b235d73b2a7809cee65`

```dockerfile
```

-	Layers:
	-	`sha256:06fd9bdf5e3ac76086b9540a8eefe0355daaa3d4beb72966f549ffa8f761c5b9`  
		Last Modified: Sat, 19 Oct 2024 00:58:27 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ccdc18d44f05da28c8219d90069f0d4eb9ee4316de834fbd642b3727c20d07a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79120885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c18cc132a9ec9d576c5f9b9c0490878f484b401f205c7de9ca5200fd8115402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e717a437695f2a383aada0d5bb16603c9d9a4f27abf449da59f9f35a74fe4668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e0b0e3c257dcd1365270fe00f03dbe0755fc39c63cf6a714f7595bea11985`

```dockerfile
```

-	Layers:
	-	`sha256:26a67519c427272540f33332e387d267a478d06ad577953e244f4ad7f64ab60c`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 4.0 MB (4032542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec11ed90a7198f124e1e507d4a9a67195e261591152ad27aff7a599b3377cb40`  
		Last Modified: Sat, 19 Oct 2024 00:57:48 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f2563b5986e1cbd6355ebaa519efbefd1ace7d95ec4dc05fb43d702a17656346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71586666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201578f73abedc744f4f2994cc04bf7653e03e6fc71c488b56b938fa6133682`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07e79f5072ea67bddca2130da2f9d315fd8222cd0609708a470e88dfa7353806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8dcf549e44ce65cf2139914167a0d0f4b1a4302bf162cbab4d7642cccbbb69`

```dockerfile
```

-	Layers:
	-	`sha256:4e7d1496ab905e4028f005f5a14166826563eecf34a3ccd9a6dd3ce4b9c1412c`  
		Last Modified: Sat, 19 Oct 2024 01:03:15 GMT  
		Size: 4.0 MB (4022143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d30c866b540503398d1018dd68b46d07f0f51532b55b00079c6208979ebb5f5`  
		Last Modified: Sat, 19 Oct 2024 01:03:14 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:bd2690414a6039d75b84c97bdaa113a12b72489d077a52b352aac6b045265d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74491620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290e9362d4f9db9760c8fc711ee0feb3425e972e82f673ff4917fe4a53e4cc2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:372f3917080ed9eb9334f2c5f62c4d74cd82f0cb2530167d4024f63f3560fbf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4036833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ad897ff0a89dc21885858a1e52dab7c9c8f5bb20638df51acb70d74756d2d9`

```dockerfile
```

-	Layers:
	-	`sha256:92a80cba733f641e49791d7770b207706dac2cc27956dcc0d0194f817f64b791`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 4.0 MB (4030243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8dcbcfacdd30256d369d06a17871979b477713f3b331489382dfe1f6da6133`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.in-toto+json
