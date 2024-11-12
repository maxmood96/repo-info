## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:b552b6823fb60af019956bb013cecc79cc7ba225ebfac9ae952f5bf22c72d783
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
$ docker pull buildpack-deps@sha256:e9f57fadeb4e2571a3ec639deb0bc50041f8eb09f1c35e7dd31f63f51219c7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66708282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a041b6b0da1491b1f95275953492d2a5af327c22639fae585debed4b0683d27e`
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
	-	`sha256:e17a4ae99f3dc5642f3037bdf67fdb8d526cf44879dc2a2a82dd78799b94cb90`  
		Last Modified: Tue, 12 Nov 2024 00:59:40 GMT  
		Size: 47.8 MB (47762858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a3ea44bb2abf7747807b4adbbe717ea3308dcc90d88289979cc43a641049`  
		Last Modified: Tue, 12 Nov 2024 16:01:31 GMT  
		Size: 18.9 MB (18945424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43d8aae958a0e128d324dc93a72825f729ab6fa94ca19355525166bb05a47f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b10f2357762de298e91d49a699d21a40cda9a432c28280f401740f16e5a614`

```dockerfile
```

-	Layers:
	-	`sha256:bf93bf2e4fce3088d42a757f8456cd7a2023638444e133ff88b357911a40ea9a`  
		Last Modified: Tue, 12 Nov 2024 16:01:30 GMT  
		Size: 4.1 MB (4053988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751e72f96ac24e34e31ae67f31c52b074761c75e5706d996f2d7158d36e3ecb4`  
		Last Modified: Tue, 12 Nov 2024 16:01:30 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f2d64356db4518efc4b1d5c851bbec90bffc5a3786a1d40a66641c2ddfc581d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74010502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755881583c95b82ca8b14fb557a3d30c6d7372621bc567aded061824b5eb9e13`
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
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2180b05bcdf8eaedc4db9cf7f65afe026827aad32c4e4b7f24679e6ea2c63305`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 20.3 MB (20250755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88c0a9ebb6e4d36deef41d358c47e1c05da025bfee528155d8dd8ae4a515c78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23d1f98393785b001948920b2a88dc59d5b07744d55dcaa5407498fb1c5c887`

```dockerfile
```

-	Layers:
	-	`sha256:cf4589ea08d8203c40a828f62b71489ecadea32a9e41505f049036274b6fa84a`  
		Last Modified: Tue, 12 Nov 2024 11:17:08 GMT  
		Size: 4.1 MB (4057863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e1e9a818425575ef20fea5def0c73f7b9ed82c20a2be689147698cbb1b6340`  
		Last Modified: Tue, 12 Nov 2024 11:17:07 GMT  
		Size: 6.9 KB (6884 bytes)  
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
$ docker pull buildpack-deps@sha256:a4f1105859b8534b986cb747f39eeb29301d977a7735a4d128f7a9b8cde3fde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79301505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b6e4d2082fca0422d715db56ed40d43739efbf27aeb90a1bed244f273c5c7d`
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
	-	`sha256:ac2d911f8489db0bbd6f313128660ffb4f315b3d99baed39d7128c198fea25b9`  
		Last Modified: Tue, 12 Nov 2024 00:59:35 GMT  
		Size: 57.3 MB (57309355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f3e8aa1353894772b7fd9d91dc6448cf8573234fedf1ba1c8596471c52519`  
		Last Modified: Tue, 12 Nov 2024 08:30:11 GMT  
		Size: 22.0 MB (21992150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2a081bdf1d2cc2fd96de5e53f9ad7551c0c1a4edf1d7e6e4e7b1b039d1a8817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f435dd30d7af7fe9206c19d35ee69326d7c1322625a8ce82779e9a352afe5b`

```dockerfile
```

-	Layers:
	-	`sha256:89d1f5a9bb4126e98982aeb9314bfa7d6ecd1747d5476ccf95e8bdadbc5a0c40`  
		Last Modified: Tue, 12 Nov 2024 08:30:10 GMT  
		Size: 4.1 MB (4056253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a91d4883ebc57f8ab63c60eb7aee2ae34e1523993d2abe0379238091fa712ec`  
		Last Modified: Tue, 12 Nov 2024 08:30:09 GMT  
		Size: 6.8 KB (6835 bytes)  
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
$ docker pull buildpack-deps@sha256:584fa4000f2547dc5479f02874a482edade85498ae0ebc4df274f79647fb3ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74690422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0022a7a4ff00d7705bd101cdcaa1424b4499051d4964d76bba5c85e1d5288b04`
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
	-	`sha256:01b62be41cbf7168e02a9fa648a1525f0c9095aef51faa9027bf3a9ff89c6b84`  
		Last Modified: Tue, 12 Nov 2024 01:00:18 GMT  
		Size: 53.0 MB (52980914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa52c56b4fa2fb05d933bf62d254d5f4371a5a9e6992ccf74613eefe11aaa96`  
		Last Modified: Tue, 12 Nov 2024 09:02:57 GMT  
		Size: 21.7 MB (21709508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:138584e0a4f75cbcf1075cd15e1a74e213a01490927fd7a2e7cb7cfc2f20ca9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf8abf20b9018f2f62da56f1e38c88bc5b0f2b665cd3aa99e863dd2d57a1832`

```dockerfile
```

-	Layers:
	-	`sha256:0c53ff2c3883ba64e4c118aa75e4d48c078ec5aeb46b97155e2600f1a4197361`  
		Last Modified: Tue, 12 Nov 2024 09:02:56 GMT  
		Size: 4.1 MB (4053894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f3c58081085a03c94c082ad8f5d4a525cd67ff9c8789de1a9dd1e752fe8722`  
		Last Modified: Tue, 12 Nov 2024 09:02:56 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json
