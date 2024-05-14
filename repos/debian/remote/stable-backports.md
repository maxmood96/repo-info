## `debian:stable-backports`

```console
$ docker pull debian@sha256:06eacbf5da40543c8c01d13d712b0043545c8dbcc158989714d2790d5fe75f0d
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:4af16ffab548f3748005f407eff905412675d5c4cbc82c8ad21046ecb3aa7e12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc114442c8c50a5e0b7da1ea45319e327fa760176feb63796734ad875763b18e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:54 GMT
ADD file:f461a46593d0f88f51655eb6e5aef85705fb1e59c6643347685aadc84546d7de in / 
# Tue, 14 May 2024 01:29:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:29:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f37cd38c722b1e1d9c2cb61ad8337e6bede774b7680a90cc4f6c1741b6f53dc9`  
		Last Modified: Tue, 14 May 2024 01:35:39 GMT  
		Size: 49.6 MB (49576375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314dbc1cb312e64b9c2bd9f5ff2c9b70ec18aa9cd4ce6efd54bdc2655f1a2055`  
		Last Modified: Tue, 14 May 2024 01:35:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:604b0beeb0ebb018ec283c7e93e868285276a45d6c3b05f1362e291e68ac8fdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47338487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af7e0cd24b6bb0df555357329e5f2cae3c56eb2634fde0ba8fdec939560e54b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:28 GMT
ADD file:670f305e4d881e8d3332b9bbf6ebed6423b74454bb5cfbc26e79dc372868bf69 in / 
# Tue, 14 May 2024 00:49:28 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:49:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:242a77ca4c5d4565db468e6fddc47c88fed44798817012424b1d021568f5c687`  
		Last Modified: Tue, 14 May 2024 00:53:37 GMT  
		Size: 47.3 MB (47338266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dae053c113d8b49d89fbc0639ab550a770a32b71f54e400dbfe739681d822e`  
		Last Modified: Tue, 14 May 2024 00:53:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:df547b34b6d00f4145299366cc1638ede5d3f95cbe882fbd095475a732bb3406
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45174971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d28331212a4d21118da7a073abb7c0159c7a17cd8d2d847bf1135e71edf17c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:17 GMT
ADD file:a3454229b52c0c3cc209b93f679fec086ec4588a52fad0e27f486a0126809f74 in / 
# Tue, 14 May 2024 01:10:18 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:10:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:16129b13cfe1de98994a5a627f1918730302f286b6dceab016f6f136cf481547`  
		Last Modified: Tue, 14 May 2024 01:15:51 GMT  
		Size: 45.2 MB (45174747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049b81a0a455f2f1bd4539152eaa3b23a90102b55dde9fc0bf61cf78831d3972`  
		Last Modified: Tue, 14 May 2024 01:15:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bf9616bc04673ca7d4ba05ed507ff646456af609cc2d25d637f4fc1bddd0486d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49613628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe47066e920534ecc008080607358d031ca0f7ad5c5333777eff51e35cde915`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:54 GMT
ADD file:cac006727e56e9497796a445c67d3d27d2ee94523ed69a5e63622697bbb0650a in / 
# Tue, 14 May 2024 00:40:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:40:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d6e0b0b83207337cadeeac66038f12a62c2366c4441ad10d25ec883bbf318968`  
		Last Modified: Tue, 14 May 2024 00:45:39 GMT  
		Size: 49.6 MB (49613406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb26a7676e879e2ee18f1ef9522b297752a1b7773d92c3d192e156d915f6be16`  
		Last Modified: Tue, 14 May 2024 00:45:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:26af9a5a0f6aea34d9b7dee73ceea72766554842ae956a1211a27cea6b21f961
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c38601a953ef84c2a0a2a9856128835fbc5fd8b94bd6bd7ea191494efb35e7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:06 GMT
ADD file:c82f3a65301fdcb50ad9ed6e8d58cf760a55f02a0d932898f6ae1954f651698e in / 
# Tue, 14 May 2024 00:49:07 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:49:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2cc4f5cc38a258ef4a372bf00ce890072e5dea8e7e5127444139b991513c6ca9`  
		Last Modified: Tue, 14 May 2024 00:55:33 GMT  
		Size: 50.6 MB (50602464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc03dafeab6395499899416655b67e8d992e42d1d2f5d254eedb7d80b0bfe1f`  
		Last Modified: Tue, 14 May 2024 00:55:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9d1ad6a07f3d9b315ec2b91024ea80d8288bef36b155bebbdcf8033d98ca6b32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbceae1d889665b9faa4378952eee88925ce903ec37f227806db3980431d76b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:15:23 GMT
ADD file:f9ab0e52feb5538919bdd33ae9050e122b8d1d91fbe7944881cfd1a509b38586 in / 
# Tue, 14 May 2024 01:15:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0044db510d84fd2650bea36b923b327105917f16876a1ad4973dceb29f8cfdf5`  
		Last Modified: Tue, 14 May 2024 01:26:55 GMT  
		Size: 49.6 MB (49582333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d03d46d1098c10df1ac99a4a5370c4c4bd8f21df5e1021999d3a2a776ac4109`  
		Last Modified: Tue, 14 May 2024 01:27:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:473703bbbbc9ea58732e89a98e846c8692affe49a8014084ac75a404bcfe6c04
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53579961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04504473d2bc573b2913e94455fa23bd86922d9941c2bd0ccb2144e73625d2b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:24 GMT
ADD file:1afa9009ab53fcdad6de78a608f8350f53815389a9d5e5fd0da2b32f30a0829f in / 
# Tue, 14 May 2024 01:21:26 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:537829f6a196273679c3ea881b442fa5355f023e3189ad87e0817f2626dba031`  
		Last Modified: Tue, 14 May 2024 01:26:24 GMT  
		Size: 53.6 MB (53579741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e14db29de25656c50ed9a5f5b2e1eafc6de3dd5be1033b454220ae089d1cc39`  
		Last Modified: Tue, 14 May 2024 01:26:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:000b81570166c3f889c1ea9a23e4d4f935dd9cfd6ca44a0a9de1b99abf3476e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47942407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d4756508c674128fba7dd255c8d7801f5c2a39f61636584ccef207852752e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:44:19 GMT
ADD file:65f387cd014ab72ccf5c0b3e9cf794399f9408114cb2285312b1a62445697812 in / 
# Tue, 14 May 2024 00:44:22 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:44:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b76d3a9735c9d5a2583aeb31e2fc0fefda1719efe826d0d5732854f3cc1e0459`  
		Last Modified: Tue, 14 May 2024 00:49:09 GMT  
		Size: 47.9 MB (47942187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb7afe5517dbd85b09e36ac109f053feffc1e40b3d9ba99c132abc586c37199`  
		Last Modified: Tue, 14 May 2024 00:49:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
