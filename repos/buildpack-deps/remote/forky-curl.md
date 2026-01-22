## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:91e6f74baa97ba22952b3833f427044f85409a43567f25de76d576c4db5fd430
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ab7b44a13f480335f9d8e8001f25350a81510f607cb1b1a7956ab52c72fd026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76123279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fb846a6e40aa03325a9f7a7728017779b977e0f7525d400af1b927881f6404`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5cc7988ae660728c0f960c88dd8ffc588e150f0fa908011ebc32d0a0227664`  
		Last Modified: Tue, 13 Jan 2026 02:10:35 GMT  
		Size: 27.3 MB (27286782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ceada52ca8e876e28efc512c2a8a49d5555ab1da962754c9b54c45a3fd25b085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076b40d5e1a06ed9e3b7f44bbd197e318be16691a2a9e72dc3272469b1f4e8ba`

```dockerfile
```

-	Layers:
	-	`sha256:2db330aa5e41cc8999d3d2fc14cc5123457a868856e8e065ac57aa1628d0263b`  
		Last Modified: Tue, 13 Jan 2026 02:10:35 GMT  
		Size: 4.1 MB (4113306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:906783c7551695ae9f42cc4fafe9b74fa4dd11d7c24f75b152575309747fa281`  
		Last Modified: Tue, 13 Jan 2026 02:10:34 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cbe04a9bf89de22f4b13b3ab14d491820906c45d6dbcad96b47ee17ba30d2795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70025504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df8d217c80ac87a88b95ea0e085ba1268be4bf02801455ec8c6cb0f41b42dc9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a41adf61a59d65bb732f71b8fa9e215ce26d7adaa7742f1d0d7dd0c7dec51f11`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.1 MB (45128498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f426cd5bf7128cd82a97f8d8519866322dbcfdac81bb42dc04e8d0b748092`  
		Last Modified: Tue, 13 Jan 2026 02:58:25 GMT  
		Size: 24.9 MB (24897006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:93c0914c3318e7ca52fe0035aae07127b875a297791804e86c173f947097cf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696c9fd2e839a1de97ce8740258fb1da22978f52ca5963417ae7428a36a2745c`

```dockerfile
```

-	Layers:
	-	`sha256:14d4827a1096aea91cea0e4434f87c7dfae7991d0cb21130aba09f01a98d310f`  
		Last Modified: Tue, 13 Jan 2026 05:23:13 GMT  
		Size: 4.1 MB (4114802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478988d3381f88e20df2a00977f8b5663772ee5f541880e1110f01d89e2613cf`  
		Last Modified: Tue, 13 Jan 2026 02:58:24 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:db5b8614dbca247876cc4f0e7da5da65ac7e3764b6c2b7b683c944793b4c6a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75368949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55ff8575f2cac5bf877b1b8ea03d951542c88c00746a51fbac8bcc52aaf61e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:14:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ddda3e83ee00d5d39dbd5cc1fe3a7c03a3c55275d87214b98204362e0a3f8`  
		Last Modified: Tue, 13 Jan 2026 02:14:34 GMT  
		Size: 26.5 MB (26548140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbc78cbd76e95ba82bed6ed031a15344634d46ae470be9872e2388c763c652f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85954fc5b95d4b3f9183e56ef0ae762871312ad06332cb8107f53c5c3b1499e1`

```dockerfile
```

-	Layers:
	-	`sha256:f87c552a35940de5f4a9c8f449cd9419c997aec84cd8ebf78efb1d382271df7d`  
		Last Modified: Tue, 13 Jan 2026 02:14:21 GMT  
		Size: 4.1 MB (4114199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f192634aa558543123991a30261a0a0edc30453922eb4b81c871be20ce5dbdc5`  
		Last Modified: Tue, 13 Jan 2026 02:14:21 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e2019107cbe38342fe484106949fccdb12fa282f0cbd8a56f7a283192530c267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78412155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d798babc6febbae60a9aeacb1e08a3aa31d788acd254c3b85cb6c5c4c4d1da7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:02:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f497e693fd9e81b15eb76e6f64e3f07e2363e9777ec10af3b185695fa33f90a8`  
		Last Modified: Tue, 13 Jan 2026 02:02:45 GMT  
		Size: 28.5 MB (28467609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e7b84b970a24ce70fd8ee17196ef1495f65b6dfcd3eedc94bd5a2b81c53ad0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c2738866d0b206e136ce391a21fa579029e9695c81030d4a5104058e062aff`

```dockerfile
```

-	Layers:
	-	`sha256:039544d5737d0143710af6163e453980eb57dcecd3060d1c5ac9e0edbb5e5a44`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 4.1 MB (4110420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460428acafabab690c147c63ceeeacde699a1a90d42326bb5836adcede967f7d`  
		Last Modified: Tue, 13 Jan 2026 02:02:37 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fa393c3d90045e5137371b6205686b3cfadd80700ccbda0f3ce07611baafd811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82945891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bd8dcf3a14c477b54bfd71c731384dac82a7bda8f5b27cad71f7f7125602b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 03:37:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7bf02b202abcdb3d6a49a7ce4605beb0852cfcc4e8237bffbef88f800d821593`  
		Last Modified: Tue, 13 Jan 2026 00:55:52 GMT  
		Size: 53.5 MB (53516184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34c011037bb419c8e273f4c6f037f35bfbb4e208b971ed3dded7a3716d2b26f`  
		Last Modified: Tue, 13 Jan 2026 03:37:37 GMT  
		Size: 29.4 MB (29429707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98dbe6a904b61011dd6b38348049af3eb54a5a34673deb865d0c8d82070c2f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3130d9ddfb8cacdab532158f47f7dedbf56a220f8312e11c9d70d32720b3ff`

```dockerfile
```

-	Layers:
	-	`sha256:22c7e22a69314e8a45c92dcfe0dc86ff20e4669b9a61345197a922ad9bbc0c70`  
		Last Modified: Tue, 13 Jan 2026 03:37:36 GMT  
		Size: 4.1 MB (4117153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122ffc77bc237da54e2c7fecad0f7ce0a791ed5bb71e15f3b3ff11a27a879a75`  
		Last Modified: Tue, 13 Jan 2026 03:37:36 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:026cf6fa99395d5d2ef8f97b64774c7632093f2d0490df262b3317532777a839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73586837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50abe52e9256a092275477e0e30f48a2d950030c714330502095feaf2d87a3de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1768176000'
# Fri, 16 Jan 2026 06:40:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0d152d1dcac9b1a7bbc763f3f2f3b2328b12317f387036c0ef1af1b70d3cf327`  
		Last Modified: Tue, 13 Jan 2026 00:52:30 GMT  
		Size: 46.9 MB (46854463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2df243ee2ea0a1e6a943f1e15516b1ef52c050634f2ee4c2fb36ff3ea6ef909`  
		Last Modified: Fri, 16 Jan 2026 06:42:09 GMT  
		Size: 26.7 MB (26732374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:905c78d215d821788692318c4e793f90c242ba1b28747c67f08e195e29e36347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d01c3f9ec0f64a45cc7953e0ca9e8a1bd9f0c56c3e4b33f861fb3d5efb0ebc3`

```dockerfile
```

-	Layers:
	-	`sha256:76e0438407c15b1049e0953f18500b3d861a88dce72652f9a542473cfd1ee78c`  
		Last Modified: Fri, 16 Jan 2026 06:42:05 GMT  
		Size: 4.1 MB (4104988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989cffc41e4f292f03a72b84e3d9f079e59191feeeb7dac734c1ec52a5b6f17f`  
		Last Modified: Fri, 16 Jan 2026 06:42:04 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ff5b4d466f49d82787e4d23c6c2824abccbf678777f8f89a4535fab3c6998c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75381247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a70c772e08cd6c32147fd4d8f2ccf9db75d10b860269bc0f2994bd08f6a8dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 03:47:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3dcc5871821327b982eb5b773ab24bb0eb85ffa1e8b8f4ae6dd4e94832450146`  
		Last Modified: Tue, 13 Jan 2026 03:10:06 GMT  
		Size: 48.4 MB (48389296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d22fb8fceb11ceaeb6109becb26df50c34175655fc06dc916318e56c9cbb3`  
		Last Modified: Tue, 13 Jan 2026 03:47:21 GMT  
		Size: 27.0 MB (26991951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:605f93d064735611fb1a86ac6c9361289492b7e81cd12988269d7a1abb58ac68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c520e21a926a938efba4b91bd1282956162717ed7c3728db271b11202529e286`

```dockerfile
```

-	Layers:
	-	`sha256:4efde32ff4d592cadac3b0ebbd4bbde3f803bbfc00a220de463b087d97950432`  
		Last Modified: Tue, 13 Jan 2026 05:23:47 GMT  
		Size: 4.1 MB (4114715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac36b29aa2caf666850d9fb84a86e49a2811a02b41036c34d676ec14edb9c1ec`  
		Last Modified: Tue, 13 Jan 2026 05:23:48 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
