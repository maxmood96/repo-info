## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:f72af3130f098aca96b7d356226f9a152d55e8977d5e9010704e566ec781ed89
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:94cc0fa8f02ce441b4c65161aceebeb5a39da61382a33884e353f87e43476392
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49557582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce1a8b46e4a61bb2021678c45e0450c7606b761653920f33c4145a3e314b864`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:29 GMT
ADD file:cc1376ecb3d9e93e4160573c110da753ffeb2efe2223351f1fbf483d89f1a756 in / 
# Thu, 27 Jul 2023 23:24:30 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:24:37 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:785ef8b9b236a5f027f33cae77513051704c0538bff455ff5548105c954c3b1c`  
		Last Modified: Thu, 27 Jul 2023 23:29:02 GMT  
		Size: 49.6 MB (49557354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec98594c9741e8ebf7719ea4869fa51dbbc8807c197f0fdebb05a88111b8f7f`  
		Last Modified: Thu, 27 Jul 2023 23:29:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e5e4b292160e67063adc711af4079dfa3cbbd09a07ee1b354ab7cf46c4f4b111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47415165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b0fa7cf8645a7250b6d14ccf3aaf04f8b4b4e9233e8464264db700b1f09328`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:21 GMT
ADD file:7b6666a92b89bab40a1b4dda36930e1b5a7b9ab40ac8dadd2179767e027de097 in / 
# Thu, 27 Jul 2023 23:48:21 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:48:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:882ddccdc867712377829e4abe9ddf1190166c3dbdfc4cee67aafb08e253cc1f`  
		Last Modified: Thu, 27 Jul 2023 23:51:04 GMT  
		Size: 47.4 MB (47414939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb85f4da865e67ae39a19ab142371b2be12a6d3dd7c7df992c1506e9abb173e`  
		Last Modified: Thu, 27 Jul 2023 23:51:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e540018da582fcbf618d81d5023479189e361505630a9f0555928b0c5f6d8f9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b163b2f711047bc8065b520218915f39452c86122457dac06f80c1c414aed2db`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:34 GMT
ADD file:be1c9c3d1025b24193774f5c0d5f790387924ed669771b461b2c599068512dc5 in / 
# Thu, 27 Jul 2023 23:57:35 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:57:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f76b23045cf894a3a989a9812af93c6b2eb7169116a938d01b03e6856046fd3a`  
		Last Modified: Fri, 28 Jul 2023 00:02:46 GMT  
		Size: 45.2 MB (45232980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea58d38ec859f210cc52e1a76a5ab74614c2b0f5720cbc51114d207c572b251`  
		Last Modified: Fri, 28 Jul 2023 00:03:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fb93b6de11abdfa6786af9abe7264ae9d6345a3e90710abd946e72e050f9f3ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d59c924420dd4bff7454083d47d74149c5e9d2dcac3d8d87d86ef20118ab7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:42:51 GMT
ADD file:fa545fc37115e874135945921d2cc72df8dc5b16d4354b2052717c7a57043e0d in / 
# Thu, 27 Jul 2023 23:42:51 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:42:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fc9ce7290e7e014f69623715ba619a0d3488a7b6ecbf09e55e11160365691192`  
		Last Modified: Thu, 27 Jul 2023 23:45:54 GMT  
		Size: 49.6 MB (49591268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4a640d6f0355aa8fa8fe440c1b71d60898cc5b9a57b938f14ada36e2ccb6ed`  
		Last Modified: Thu, 27 Jul 2023 23:46:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:e03126f4bc33d8894c02cd23549e8540942031f47cedbe2b421e01640b5720fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50568100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5494de602a5284e16480122b472dab8a45162d99b0679298267fdfba80f0eb01`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:38:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7d6c49e24a2151c35a39fa8319ab01734b8dfbe9aace25ce2084aab5b1ca69`  
		Last Modified: Thu, 27 Jul 2023 23:43:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:17e23370c9014f987dc77abaeca379798466329d32f10917ba25117099823b0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49542277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d58cdcf197262de20f2fba652e775d682f0511337ac49cc77183a120a769c9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:10:44 GMT
ADD file:3568f288ff9791a341f5cb0e99c0a63e09a68f3816d7f7a9971127b9b98a04b8 in / 
# Thu, 27 Jul 2023 23:10:50 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:11:01 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4dbd8372ba202a8b430bce8d5c5b8a4bfdbc6ef2703180665e5964d51bb0437`  
		Last Modified: Thu, 27 Jul 2023 23:21:43 GMT  
		Size: 49.5 MB (49542050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a505d717e2b037d2254fc887c2563dc46b05cf65699459d7d272a314a230260b`  
		Last Modified: Thu, 27 Jul 2023 23:22:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:52b1e4a0dfc07a16303a6c2bb7fff5b99886ae83c39a87f02470370a794e2674
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53543571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4598d6e9bd2a8e1851f636103abf1f479a74f7b327a348fff56cc386d99823`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:22:41 GMT
ADD file:b20300808df8e1ce5b5ff534088c39d6b04467476af024e54545f7857f78a508 in / 
# Thu, 27 Jul 2023 23:22:43 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:22:51 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b6d31d119ff78cff1435e4eb51d8918916c2d5057cebf12b76d5352660fb90de`  
		Last Modified: Thu, 27 Jul 2023 23:28:46 GMT  
		Size: 53.5 MB (53543346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade5f8824804f6b322a3ea1f2bb59c83960518cd29c33673ed6f7d5d3b0b637d`  
		Last Modified: Thu, 27 Jul 2023 23:29:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:8601290479e01d538a702d29b650792809d295788ddc4431ab66c0112b5a0abe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47922268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e382a6893d1bdb9d52473603ca8496d52328af231a8e34d97535fb8699744241`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:46:54 GMT
ADD file:7cc985c20b5bf9e4dde7f388e4a49154bad3005c95f50de92b01ecec9212e022 in / 
# Thu, 27 Jul 2023 23:46:56 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:47:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:93e4b40dfe5599c220b1b5acf9563fe87baf3eaa3fd2f0df5e8c0c6640a9d9ff`  
		Last Modified: Thu, 27 Jul 2023 23:51:59 GMT  
		Size: 47.9 MB (47922041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec955302b9f6ce24ef5b0cca2abe18b6777ed1d14a665e8bfd76333a346362e9`  
		Last Modified: Thu, 27 Jul 2023 23:52:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
