## `buildpack-deps:stable-curl`

```console
$ docker pull buildpack-deps@sha256:6265d7fdceab01b97636126334a1ec0a5e6aef86e4fcbbd0075bff11c8499cd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6357db40fe8fbb21058e4226f3e98d5a445b9a41ab74851db7777b0b259b94a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74919511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0b05b3a1a69443f6b60b4f76aefb6914a79116fbefd14418b25bd818834ebf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33970743aee750df25f6c661132b7401c8fefe930e5f4803f4c8b6f567a6b55`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 25.6 MB (25621678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f500bd3f747a2ae0f3228b5cd26681114d496f8206b068a16ba4bd9946e3dda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4127036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af846196626bc7620acafeb8e24541061485bff5c9452b1601462263624e76de`

```dockerfile
```

-	Layers:
	-	`sha256:faf860eb26a6c7e8bb49cdef00603cf3fde716b3bb4eb5a32d7574e153375190`  
		Last Modified: Tue, 07 Apr 2026 01:47:21 GMT  
		Size: 4.1 MB (4119951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9718647c1cb3ac04b49e340171033537a93f88ece57bf720afe88fe9ac484ce9`  
		Last Modified: Tue, 07 Apr 2026 01:47:21 GMT  
		Size: 7.1 KB (7085 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e2b2d31ff6786d69a3c7aa4a5c35e4b5f397b3ca56a478b7dd4dd003e8285824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71825078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260a8569bbc9134055d53c9ca7defccb760701d852e1cd175fb9c0aaf3b1e7b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:45:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2d99f94edc3d8dd6e6b758a4671793ae83d782d6d01f35ad2caf70b714b475b`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 47.5 MB (47460892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c635b73b8a91f67dcb5ba2db26dcc3f74099816e3c14bb345601bfa9d19e569`  
		Last Modified: Tue, 07 Apr 2026 02:46:09 GMT  
		Size: 24.4 MB (24364186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95b31280036a21e8454315f123ed942568941ac6ee88f0f10f6c77ac1583be7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca572e51f3e48dc8312c267eb985fffe95ac263471a3a6895f4d6f504df0672`

```dockerfile
```

-	Layers:
	-	`sha256:527fc1e77cd8bf153398966aa20ea9c2d8e084adf299c747cedc97e7be181dae`  
		Last Modified: Tue, 07 Apr 2026 02:46:08 GMT  
		Size: 4.1 MB (4122941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72fd710f7983795f446961a2cc40ae9cbbbd11b021ac3a2ca9d3792c87d1825d`  
		Last Modified: Tue, 07 Apr 2026 02:46:08 GMT  
		Size: 7.2 KB (7157 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7eec42cf7fb375a756c9cf6e95bc8704e0cc8b8190112cae63d09c93ebd74a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69369970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2fc0f544ee135206d28baef5496656d9db13b2f99d2a2421d2a571a8dcfacb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e67d94360d76080a847d9e2746fc095d0663156f501d28fa6443bb38156e1`  
		Last Modified: Tue, 07 Apr 2026 02:02:17 GMT  
		Size: 23.6 MB (23636973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28d1b2de3d6cc2c43780a17e4a15a744dab5768908ae1353672d1565bba92580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7834ad2f47de997c97fd1f60faf4a60d022dc1bc466a7cbde87b6fad2cd80a`

```dockerfile
```

-	Layers:
	-	`sha256:483e87dd20f28e615d462db763c4cf16584915c8ff75c179c1bd4be8e1015220`  
		Last Modified: Tue, 07 Apr 2026 02:02:17 GMT  
		Size: 4.1 MB (4121452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b90d688555260540252c11a2676aa33c919fffe8ab1ac7c7aefd9531a4d9780`  
		Last Modified: Tue, 07 Apr 2026 02:02:16 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e787b80b2adff735ea79b04c419d68478b4cfc6422660c25a16c016f1df40b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74688910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02c0b54fed07cba25e0848c2e3da853bd045d475fe83dde762b01ffe6328d7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:50:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ee5883c1f173b0485b465221ddea5443b64c95935146f0bb3655baee3647d`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 25.0 MB (25023654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9967108150e56dfe55b6cfdbef9fcb6c2666a851d93d9ece69340edcb080325b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e17519639ea69bdc1955e904419819688e9adc46cbd997089a536730b0ad032`

```dockerfile
```

-	Layers:
	-	`sha256:0c9f9114dbe5c46c0df50039317346fb92b74b23d3ea0c28745947da24e0ba48`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 4.1 MB (4121493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7abb661a400dd6021010685e187831f6dac8056470eaad98755c7a12e724312`  
		Last Modified: Tue, 07 Apr 2026 01:50:26 GMT  
		Size: 7.2 KB (7178 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ef4a562251ba325b97ec882a86e0398835f2033f1903d0270c6c56b012f5b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77602467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9103f5b4d70bb09905518a8a329f4d2466abdd5dd20d0a13bb3e01310b376e01`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467268048a14f0a2f523ec4fcb1cff704a19d6fe503c164c3374551f40e80aac`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 26.8 MB (26783379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7231b934c72b819a261130d93baa9a78a238cacd81de0266c3a2f365e10a3314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0829a33e83373cf930fe8d8d571f1703d2615df046632875e8ff9d3dd345e1e`

```dockerfile
```

-	Layers:
	-	`sha256:44763a27d7ad233aefb5de76878ae595d38fce9a278553c17ee4fa224b126410`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 4.1 MB (4117058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1130c9e3ea6fa11f53a5ac25bbdf8d51746e1b699e0523df929f6b1edce922da`  
		Last Modified: Tue, 07 Apr 2026 01:46:38 GMT  
		Size: 7.1 KB (7059 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fd3c42f20f54fcc8d8532587131681891950963970cb704592edfbb60f4971ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80132517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dea625ca66709ad7848ebad74eaa5809d9a9497811e9d88ed0519c014ffcf03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:23:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d48e002e290b21e23e75ff9380f01aab2e64ad03e18132510445c43ca967783`  
		Last Modified: Tue, 07 Apr 2026 04:23:27 GMT  
		Size: 27.0 MB (27013848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8679e4157d5d1f624a68cde0ec9ce5ffd6207d54b1363f25ace58bf01c7a1336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5498365be2f88512e34e024997633a702b813727af71917e2a12a503db8f566d`

```dockerfile
```

-	Layers:
	-	`sha256:501477fe3e81e0e594ca333f5cbc26964ec74c5b47be2fcbe0af0f3fd181b940`  
		Last Modified: Tue, 07 Apr 2026 04:23:26 GMT  
		Size: 4.1 MB (4123799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df46446f1d723440c11c48e7894f678142b74fcba10d1339110b2b61200f567`  
		Last Modified: Tue, 07 Apr 2026 04:23:26 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:dfd607fbec4e364d0b0395ab5fc8f32add2ea351f74abffe10044fda3b4b1106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75911391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e97ebc4a6d1c23e7e19e85d8ba3327deede39d4ddda19f83ab1b319d102c4a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 00:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b086e95c6ca0165102a5ceced9274da65d6d9a865b88c14f181ecba94652bd75`  
		Last Modified: Wed, 08 Apr 2026 00:46:07 GMT  
		Size: 28.1 MB (28118765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e93fc18da2e58c4df1694ee2e451c85e25cafa0a11c9b83359608c46b672d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92eb19b803457fa59fbb3d3522a22f4dd230f0125de5cd0028c721cd319bca58`

```dockerfile
```

-	Layers:
	-	`sha256:a1624fb1017504967e23e0c130084870d81d168fb8f6fdb071437a16a4500ebd`  
		Last Modified: Wed, 08 Apr 2026 00:46:04 GMT  
		Size: 4.1 MB (4112463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b253441409b3e581cbd1f8a8b06b97878ba256d60d933248e3ddb66225a0d1`  
		Last Modified: Wed, 08 Apr 2026 00:46:02 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:33ac278dacf6185dfe8fa91e56eb745b7cb414a6ca1598d08c847a35632cc09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76168148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05956c0d71aa3558034b62af6da25c7b71aa28807d7762498e4c6f1927082fb8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9a487bea803d0a108535f515bb38cbace4ed2fd0cf55a04f448d8a910181b`  
		Last Modified: Tue, 07 Apr 2026 03:05:59 GMT  
		Size: 26.8 MB (26803044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:309975376b897595039e58ff561c97f59e73ab0c36470ca688e1dade9c3fbcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4128447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fae14569baf0f30d88475c038f8085968186ab6abc27a7aeb4e53cae732977`

```dockerfile
```

-	Layers:
	-	`sha256:ef0288f041de77c188f3808d74c3cdd2821ad7544fa27ede512efccfca217dc2`  
		Last Modified: Tue, 07 Apr 2026 03:05:58 GMT  
		Size: 4.1 MB (4121361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd5e11d80d95b80602c126ed21054ce9bda8c64e1f44f96c714642da3598abe`  
		Last Modified: Tue, 07 Apr 2026 03:05:58 GMT  
		Size: 7.1 KB (7086 bytes)  
		MIME: application/vnd.in-toto+json
