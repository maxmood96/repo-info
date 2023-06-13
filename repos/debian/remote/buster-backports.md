## `debian:buster-backports`

```console
$ docker pull debian@sha256:19645ad4ee069c4a600a9c6da10eb9bfcc9ab394040251bc897a93b88841ca8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:b6ae1575d22d91adae646e0993b0c2dcec143feba43b184cc2a0d96b49602d5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50448733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3be49b81e4b30d1762f3dfc1a8964d062da7a9e060c6db53d9ae74ca550a97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:19 GMT
ADD file:54838b3dbf7839dadd0b29835bbe53ecbfdfde657ef8671ec5ac3cf5867ea069 in / 
# Mon, 12 Jun 2023 23:21:19 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:21:24 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ac8bb7e1a32398e26c129ce64e2ddc3e7ec6c34d93424b247f16049f5a91cff4`  
		Last Modified: Mon, 12 Jun 2023 23:26:48 GMT  
		Size: 50.4 MB (50448512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64496441f47c86f65b41921332380eef24bb1ddb720fd0c1392174c180922221`  
		Last Modified: Mon, 12 Jun 2023 23:27:00 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2de3fbb1441a2899b36add5fa5025618bd021b8fb06f31bcb4447b45c02b0315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2954f974cd3b737fd4950bd0f3e42dd685e653ccc1e0c591fc757d09e03d04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:59:02 GMT
ADD file:c3ae258462983c32de8d633c17dcc414087b5ccd8fd76f708981c7f20c7e86a4 in / 
# Mon, 12 Jun 2023 23:59:03 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:59:09 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:51e8b9db05761e5bb6c498f0c3f479641e693e39aac9800c97e87d5c936ba9ac`  
		Last Modified: Tue, 13 Jun 2023 00:04:43 GMT  
		Size: 45.9 MB (45916072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c38e9ef49696b18d82f79e8342d5deb91d6fd83f28bce958128dac43a3c9c0`  
		Last Modified: Tue, 13 Jun 2023 00:04:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a5a9c4833de0112ae2ce5c6414e7fb35cd6621a15c658a97e1b20de0efaa98ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49238628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9e7ab0562b5a1b39a35db005720d8c17775f80d5c6217e6cd55c96bce29294`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:41 GMT
ADD file:bb3cb9e6abc423742d7c1b6bc006a7cef70038c5621c71a90a2ae7c1ea29ec63 in / 
# Mon, 12 Jun 2023 23:40:42 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:40:45 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e8371d57f7426517aead21bff5af0cf321625cac166c86214c439fb67db84243`  
		Last Modified: Mon, 12 Jun 2023 23:45:01 GMT  
		Size: 49.2 MB (49238409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5cec9dcb24a633e7e56aa1b73177a1ca694b011e0aefed457fd5b0061df0ea`  
		Last Modified: Mon, 12 Jun 2023 23:45:14 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:4705dd99f61ad3bb0d155376d6eaae60d58e62e5f9d33d983d3a171c008338eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51206210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b900c0e5e1a3c1d73dc0aba90988b428f23ec8700ef489e4bcfafdce24c043`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:16 GMT
ADD file:c4d7ce8374a492278fd0b54ca10fd35f995676380e4ef134e484fd85ed50c58b in / 
# Mon, 12 Jun 2023 23:40:17 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:40:22 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:121d519ab26049cf059ad8c480f995a2bb103d39a5b57857d7ac27ab2b0d35f0`  
		Last Modified: Mon, 12 Jun 2023 23:47:27 GMT  
		Size: 51.2 MB (51205988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e700f289ea17a660e80ccf6be3d01dbd39d4e569aec2a742a5f60a04e62133`  
		Last Modified: Mon, 12 Jun 2023 23:47:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
