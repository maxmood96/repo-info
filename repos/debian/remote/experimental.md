## `debian:experimental`

```console
$ docker pull debian@sha256:78031608f00cc99a89bbe67463a4bb30cf33fbf8990762ef42abf07885184de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:e5b39eed4a5e7c1a0c77e394ce0405e95c00b427b0c59e8b3b64bda638c6172b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52429843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d296fc6b37718626b68d81efa6c1c0a07832acb87b655c3aa685a2b756fe8a4b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:23:55 GMT
ADD file:97038e10ef5b1dcac530c1eb1f457a998d419abea6085bbbe937116f2734da4f in / 
# Thu, 13 Jun 2024 01:23:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:09 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8a16955337e68b0976cc5d012b5c3e3c48345581507a5671f69829c93d67d423`  
		Last Modified: Thu, 13 Jun 2024 01:30:11 GMT  
		Size: 52.4 MB (52429622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f501ae50f47db8b467c7e8397ad1d69a941760dfb21e29a15c34b6c1891c066e`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

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

### `debian:experimental` - linux; arm variant v7

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

### `debian:experimental` - linux; arm64 variant v8

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

### `debian:experimental` - linux; 386

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

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:14be8029d0a6d4ce2e82e491444846522a54b8bf80c5ab379d8f206a1f9cab43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51279428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f41c28748e85fc170a0c91256bd05785752e55d4fb7d1313b1570156fe4ba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:44 GMT
ADD file:d5d3e02cac4443cadbda6b89811c5d054d1db9db3bcc1927947b232c06d0720f in / 
# Thu, 13 Jun 2024 01:18:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:19:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c7d43b9a5bb5053e2c3962b043f5a84589a756c4fd34f55d353670560e9d2f3c`  
		Last Modified: Thu, 13 Jun 2024 01:30:20 GMT  
		Size: 51.3 MB (51279206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10aba5e63281c08e3cec361df70037367097ed35cb675aa9c8102a20b61f73a`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:d6c43947e566f3b89058b9149a8a5019b3fa6cc7dcf040c221706491f0f06931
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56297184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720f2421d1dd06e6abd964e714422b1d324a9b0c73df52a1f9bdfed627c2df0c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:19:50 GMT
ADD file:c0f742f5a573473fe32bd2303e208818bebfac551d2e724b46c7592fd23c03bb in / 
# Thu, 13 Jun 2024 01:19:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:20:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5a4f4bea5771f3cc7e0e3d3df946acfbe0781a7bbacf73a3dc2076694f16a928`  
		Last Modified: Thu, 13 Jun 2024 01:25:56 GMT  
		Size: 56.3 MB (56296961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d596c5a188a1fd4490a51ed76d1316e5f7d309a21b04bfde90f89330021ac30b`  
		Last Modified: Thu, 13 Jun 2024 01:26:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:d8564c043b96e14451bf5b27733a899f90960b5ae6513f3391ee4147f4769d43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50715979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059146f68a9320361e08ac2909e90ae292290c4f114d9677e3355af40d4bf34`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:33:36 GMT
ADD file:bd75ce513a1cd4e1dcf03472bc2246bef166b6cac30321e05001eb699626feeb in / 
# Thu, 13 Jun 2024 01:33:39 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:34:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:417bae7710696ae32abd510e3ba1f59f127a3be7dca2de95632b8dc9f4baf55a`  
		Last Modified: Thu, 13 Jun 2024 01:38:32 GMT  
		Size: 50.7 MB (50715756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c5224f3cc9a1ce6f8627fa691d3eb97c5163187da471d2befb01c4ecc14fe`  
		Last Modified: Thu, 13 Jun 2024 01:39:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

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
