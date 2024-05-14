## `debian:stable-backports`

```console
$ docker pull debian@sha256:5e57d010ced545979e9a74949a4720132e7305882c50397ce3811470dbd425a0
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
$ docker pull debian@sha256:2ac9feeac45a5fd1be81b124f115609baf58e5a77ec7ea3b7a94ae439bb15494
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752685ce9675b4b65ba073d83f982faf1665600ea79508badd37ea6b0f98791b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:00 GMT
ADD file:d69b73f95cac930a42b91ed7f0f73cb83484100d69e0ebb9c47d6feef1771e84 in / 
# Wed, 24 Apr 2024 03:30:00 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:30:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f70ca9efdda4d28a921732364e4704f15c0703fe3a8cbede502b78466602092`  
		Last Modified: Wed, 24 Apr 2024 03:35:42 GMT  
		Size: 49.6 MB (49576272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746db019606ad9424fe312dd205406fc515530b8ba9dcb139c48cf0f64b8f661`  
		Last Modified: Wed, 24 Apr 2024 03:35:50 GMT  
		Size: 222.0 B  
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
$ docker pull debian@sha256:a94cc491072d34952caecbef7aae97a611b87e3e21e50ee0bde270565434075a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45175266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37c970c6ecdff9fbb4ebd70098b628db025971dfe7b6e924af6cec9983f516d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:08:43 GMT
ADD file:3c374447f03f3b71e68579489c1740133dc1e4b328b2ce418069d68265fc6115 in / 
# Wed, 24 Apr 2024 04:08:43 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:08:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3cbbffac45653e793064bc6ac7f351b925eef3a94224fa26b995e0ef9802e7b8`  
		Last Modified: Wed, 24 Apr 2024 04:14:14 GMT  
		Size: 45.2 MB (45175041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423ee67b4b60f6e0eca954184955fa3fcaa5ca531509aa9f7f69097d43b4d3a1`  
		Last Modified: Wed, 24 Apr 2024 04:14:23 GMT  
		Size: 225.0 B  
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
$ docker pull debian@sha256:c4acd7b782c7838fe4cbc9ced74bf5c2ef0d03f899df0ee326f4ce552a9c2674
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49583028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb759f376b558f07cb63d28df9b05840299bf5fc788d1bed56a0bc5ff6bfbe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:18:28 GMT
ADD file:0fc3a29fd4805efb8fba8020dccab3b1b6fc2c0828c9ead519ac7a16c4eb5cab in / 
# Wed, 24 Apr 2024 03:18:33 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:18:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:48bc9e8cd1d92c59f529de438a611bcc91f7735e8b62e60f69baa2baa57d7e5f`  
		Last Modified: Wed, 24 Apr 2024 03:29:53 GMT  
		Size: 49.6 MB (49582804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525626e950f29eade5a5536417c60e02c98185916e7b797459be746f3231258d`  
		Last Modified: Wed, 24 Apr 2024 03:30:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ad6f6694869aef64616ffa437b609cff08a51e4a9a845096fe0ecff29ec7929b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53580344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14645a47f84f9cd416a3463f03fd38ec09a06ae8afb008e49ceef5bae7ea0e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:22:55 GMT
ADD file:49b92159424eb973fa890025f1a59cd18824358e23e55a092257c2c3d200fd37 in / 
# Wed, 24 Apr 2024 03:22:59 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:23:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13fc0cef51b1e2c4b5ca78eef06b6140164a8ae5974f935e21c932e74592c6d1`  
		Last Modified: Wed, 24 Apr 2024 03:29:16 GMT  
		Size: 53.6 MB (53580119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc739ad9659b73625801d7cafef5f7ccb9ecc9d14c91d7cc332fc1e5ae0a1ca`  
		Last Modified: Wed, 24 Apr 2024 03:29:27 GMT  
		Size: 225.0 B  
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
