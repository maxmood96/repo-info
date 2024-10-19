## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:09c665801f99b13aace18d0e534ca5fba8a95ccb9f491844b58d9a407a6681cf
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
$ docker pull buildpack-deps@sha256:4969fc1482fe79df2f83454d450d1bb1a0bd65812c9965ae1acecbb37b03ccaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73830606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c95b99c5f7fcf27f8df865460d0bef48e4fe0499bbe6de82a9a812aabc372a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fda6398e5597471e4fe9a09bac438b822a76bfed6ac08368ef40b1e9ddea52e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e230e9497a2cbdf9af9438fc5a0ccb4b9846b644ac01b445504fbe028091fc11`

```dockerfile
```

-	Layers:
	-	`sha256:bf5ea3fac8fffc480e851a74e960ed5d1e7f9b10adb718c0c389bb83bc052b6b`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 4.0 MB (4028672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c832042891b017cd09224285e67cb4bceed33f487315c2467b0339ebb7a651`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9fbe3208573220b4f9bc991ffbff5b241a40dc9207a1412852dc5e1dcfb848e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69716210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ee3aa87633d009b362e51572dc98a9cacd568e8c58399568da58bc7055fb22`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:704a4556dc0a7e5eada6cecd5287d4b85008c956b40b973ff74e5d10709940d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4038180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e52b0f8e26eb0efb788150f3213c247649ab0db37b9738559d888b15bcec526`

```dockerfile
```

-	Layers:
	-	`sha256:5c0bd3e2f79edb6da9625f1f9e47004acdf5cae6c326bd0785fe7cf585ac3400`  
		Last Modified: Sat, 19 Oct 2024 00:55:47 GMT  
		Size: 4.0 MB (4031537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4621ddefc20eb42391d2bdf32281c9b15abec3dc9d43bcbe5483b50017401b`  
		Last Modified: Sat, 19 Oct 2024 00:55:47 GMT  
		Size: 6.6 KB (6643 bytes)  
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
$ docker pull buildpack-deps@sha256:01c063600551a346c195ff31d7934664465feb4d46a18371953fc30674669422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75783129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac719fac021c9c93427216a8e5a75372d2b1fc4bc2b30e006d6702885ef0db0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3940383fafe27fab3db6136b4524849d3a389a5ab50381c4b7077ed77cc81825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d1f1a9fde212e396e9203d732493e24f84b97ebd6e180174870254520a01f8`

```dockerfile
```

-	Layers:
	-	`sha256:e63b6a0dacd997549b8c0ebf2e2be3f0126dc1e541b72958354c090675d89fbb`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 4.0 MB (4025085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9bac0c42f3e32de80fbee483246d465199d456a4729a7ebfc077321f8618c9`  
		Last Modified: Sat, 19 Oct 2024 00:54:55 GMT  
		Size: 6.6 KB (6571 bytes)  
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
