## `debian:experimental-20240701`

```console
$ docker pull debian@sha256:0e5ab7cae3ff338a1ea2da32f23a3133d2a0505aaaa0f6d5772e1e8a4f870599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:experimental-20240701` - linux; amd64

```console
$ docker pull debian@sha256:a9c6cd2bde08c29772e2c6083180525c3a0b72be7356b6bb38589823a2255ade
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52634801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39577cfc514165db95b786a0fc4a3ea540b09b54259c2659e0ce669b4a0740b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:27:23 GMT
ADD file:a1ca0b73691fca25554e4fe69ba4bf9645767248dbac7a4fc08739a03a5a48ec in / 
# Tue, 02 Jul 2024 01:27:23 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:27:37 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:91e525dba966e81e964d726faf9cf6bccf6540de433804618e2fbc398a705f15`  
		Last Modified: Tue, 02 Jul 2024 01:32:17 GMT  
		Size: 52.6 MB (52634582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadc00186fe87882f76212226f4f4ff1338ad8e70e01b46212bc8d1905da6b1f`  
		Last Modified: Tue, 02 Jul 2024 01:32:40 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240701` - linux; arm variant v5

```console
$ docker pull debian@sha256:b0e929801d6752f07ad0249a4191db1474dc0ead642db2b051d03279e66fc60e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1829b963e03d49f9348a8f4910661372783c97aae6681ff4c076120fec20c77`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:50:08 GMT
ADD file:0711d09c62a4bb4e656089a61615858b32fbd356b78a842b1720b8ec8e513863 in / 
# Tue, 02 Jul 2024 00:50:09 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:50:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:54e07640829df1faeac37c4cdc03973c6fc8ea1f99fb7b6381303ebb1b88dbd7`  
		Last Modified: Tue, 02 Jul 2024 00:55:11 GMT  
		Size: 49.7 MB (49697293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4f90f385440bbbb9015040fed7b2bd9baa7ef8ffbc94cb7bf3bf8a4d2cffc7`  
		Last Modified: Tue, 02 Jul 2024 00:55:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240701` - linux; arm variant v7

```console
$ docker pull debian@sha256:0407a1dd59d7c4e6eb578ccad91939fb388de630a3dca6f518a850dacd897b35
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47184087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5154521f1bb289fcc8a6c5fce4480950923bf9d819c37f79af3babd8bb064c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:02:01 GMT
ADD file:32471c97e7ead1650b311e1de0c86cbfd933ee7fc2a2e68982254ac93b89451d in / 
# Tue, 02 Jul 2024 01:02:01 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:02:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3b3c692bed551c9146a37859915dd944af364ea78f1d6c9adc36cef97cf99b52`  
		Last Modified: Tue, 02 Jul 2024 01:06:49 GMT  
		Size: 47.2 MB (47183863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca01338c61c5ba9a25a199f88aed256aa987c72288371329db5f1b08f7009bc`  
		Last Modified: Tue, 02 Jul 2024 01:07:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240701` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c596dcba3d0ed157fe419eed296c0a6e0b337be825999f1d08371a5d289fade6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52888978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667d3f7a8a58465bc4084959373fba7026ccb1496c84e6fe32d2d62d49fd7260`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:41:12 GMT
ADD file:37a3ec80e65267ec9d7c28bd0b750192c2487497e693e6a1ff33c1c6577a5f73 in / 
# Tue, 02 Jul 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:21 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5fe80dcf0eeb355dcaadb0826495e624bd860783d79819def799bff077c8399b`  
		Last Modified: Tue, 02 Jul 2024 00:45:47 GMT  
		Size: 52.9 MB (52888756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8081d8f930e2749d752b5e53b89017ec11f8fbde56756a0dbf2276db9a52ad0`  
		Last Modified: Tue, 02 Jul 2024 00:46:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240701` - linux; 386

```console
$ docker pull debian@sha256:9462e3f2d934e7aa056a838c8b82da0859d55fe7f88c4876ea35693fcdca822e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53522608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c7e0a328266b0f56adcc121f5eb2d884a7865c2ecbf4ea6e8f5f6c540f0936`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:41:15 GMT
ADD file:ed4955db1415584b9cd830d1e00c08f63b8d732721200e594fab4f073ee9f1a8 in / 
# Tue, 02 Jul 2024 00:41:15 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e2b0a460644e392ecaf9df3c85f5cd8ca8be7d51ddaa98b3e2fc71069058e770`  
		Last Modified: Tue, 02 Jul 2024 00:46:46 GMT  
		Size: 53.5 MB (53522388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f058d5f9eddf4296324af253ab218b515b5babc08d8a1443d53466dfc80726`  
		Last Modified: Tue, 02 Jul 2024 00:47:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240701` - linux; mips64le

```console
$ docker pull debian@sha256:aa9df9d3c8f2ca98cdb5e14d34d6c58656646e9f775c96fb514e3d7b236aeaa1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51498300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a50519ff01ed183e95788a7c250adeeec01ee1618cd781ce7922862cdbcfe29`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:32 GMT
ADD file:6cdd52c74b2c265ef4259bfe7394ce17643efada3eb5968d8642a534424d4f78 in / 
# Tue, 02 Jul 2024 01:26:38 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:27:22 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2bcb99f9728eb9fa862b3e5e76d4262cbb9da6bbe27dd77b2be5b7dbf1c870fc`  
		Last Modified: Tue, 02 Jul 2024 01:37:46 GMT  
		Size: 51.5 MB (51498077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2fb51260d9ab0054ae20c1b2b66dc35e233027f131516805cce7ed0ecd252a`  
		Last Modified: Tue, 02 Jul 2024 01:38:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240701` - linux; ppc64le

```console
$ docker pull debian@sha256:47cf934baec797f2238a2d03518e9c34259e4b55717bb974ba41f36be88bbed7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56551202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ded3e0dd4f12fa528346a105e01666c58cf85b529aaf43c4dc47bf68f82fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:20:20 GMT
ADD file:c0070da874c4ad236a922a784394a0abebd3b8cd195ec61bdad9faa5c941261f in / 
# Tue, 02 Jul 2024 01:20:23 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:20:37 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e69497cb244a45171e730194e4c5744b64964fb6288bddd82d51a4cfe01a6918`  
		Last Modified: Tue, 02 Jul 2024 01:26:02 GMT  
		Size: 56.6 MB (56550981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8da926782319956afba77176446a8e46523f01ae5c9ed09dc0406d865cf74bc`  
		Last Modified: Tue, 02 Jul 2024 01:26:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240701` - linux; s390x

```console
$ docker pull debian@sha256:0caa13d6524d99b7c20ca99db8bb340589b32c6157708f490cad12987dc97d68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52278440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c05432c8bd5675f426caa7d5bdbdbbb3f161598074867e08f1d52cb4305145`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:46:49 GMT
ADD file:ad209ab93f89e8776b8a867419d31a274f23919b9989ac3680f6e0efb5f70988 in / 
# Tue, 02 Jul 2024 00:46:51 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:47:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b181ea82409ade9cffcab80ecada081e73228204cb0104072f148950902bb177`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 52.3 MB (52278219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd905dadfcab2efa1c6912335006c96099fac5bc03f8699ca6c73c8ab8d6fcfc`  
		Last Modified: Tue, 02 Jul 2024 00:51:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
