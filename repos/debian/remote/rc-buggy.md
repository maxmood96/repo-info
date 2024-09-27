## `debian:rc-buggy`

```console
$ docker pull debian@sha256:f259348b5447651d9c4127bcc5acd5fad2f95c8a3aa7457c3bbbfc7e1b0a3f92
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:2145a349f70eaed73879ef5ac12fcb59e52d942bec4490415e55b27dc815eef0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53157076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74de7f344f2fce2768c5eae475f87203d681dc39590f1f17686a512a51508ced`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:41 GMT
ADD file:ae19349870cdfda1b68970255f5f5e8f9cd15173da02e9e3404d59044fd19f67 in / 
# Wed, 04 Sep 2024 22:31:41 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:33:15 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b801efa715ff197e658475851b26398377386b508d479b783c9178607c76738d`  
		Last Modified: Wed, 04 Sep 2024 22:35:42 GMT  
		Size: 53.2 MB (53156851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef1ac38d53081e557c7e83ceadc5231da4faa9f61c426ce4e2f98552fe66e0c`  
		Last Modified: Wed, 04 Sep 2024 22:38:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:6b9a2b0da1bfa8d767e486d8f5179210b42f78b627c3f09215924979a7ad7f26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50112643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3294b00aee7c3edbcb4fcfcb21d06e8da0d5a4d0909c0a79a1522ad78117169a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:13 GMT
ADD file:8e4509f73b7c89f169188002c34bc8d03af1dafaeb6a9966b6690f196913262b in / 
# Wed, 04 Sep 2024 21:49:14 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:50:27 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2257c73c251c8a677a6bc4308ec105c9b65d8a38c219fae44f204b71a1e09836`  
		Last Modified: Wed, 04 Sep 2024 21:53:07 GMT  
		Size: 50.1 MB (50112415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09205e6a6a7513348431dee15055d195c20ee45b2592be57736757b8c8d3c92`  
		Last Modified: Wed, 04 Sep 2024 21:55:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:4d9dcb7ad1b6bcaeebabd69053ba0e202a055efb6d12bf6086f2d15e7780b2b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47606233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebd5b1e817eccb0822be3cfbfdc1e4023d4bd670a004fc319b8dca14e8d27d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:58 GMT
ADD file:f0cfa70a19518f2db4a813f0c5ad2bd292465f48e4249c9e0d9007c839212dd0 in / 
# Wed, 04 Sep 2024 21:58:59 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:00:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d301726964d3d126bb25d90398b0f8668a5991c47d9f237ff6b62cb806b4ac84`  
		Last Modified: Wed, 04 Sep 2024 22:03:18 GMT  
		Size: 47.6 MB (47606007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a39215ac26fd059cd9c61860c9b90856d0493348c1861b670602bbe5f77b0b`  
		Last Modified: Wed, 04 Sep 2024 22:05:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:016c02b2140d813f4fd1feceeec5105939a01dfb2faacc0b6d659d26a1c4cf9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53597457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bd4c836db1ab9647058708f3ada1b278d275376d0e918bd8a197eac6278697`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:29 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Wed, 04 Sep 2024 21:40:30 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:41:38 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb17a76187357338a6dc469cb45b107e05b2ef537f509fe8ca317f74d20b8bb`  
		Last Modified: Wed, 04 Sep 2024 21:46:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:ac01334ffe417f457ed4f0587018b76c3ee766d45484d85bc104bba91b4cf9d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54033485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed91ceb916e94fb684fe0a0f88f257f05f08b45c64e926529b3fe52dd1ff142`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:45:28 GMT
ADD file:2bc6b9eb390a3ccf12bc1146e52a121a20e72c5ac0e9e0cdde8678b8a64da9f7 in / 
# Wed, 04 Sep 2024 22:45:29 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:47:06 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3cd4933de503c208d05c5e30920d85a6bfda122663e7dee7dc0ccda09e2913d4`  
		Last Modified: Wed, 04 Sep 2024 22:49:47 GMT  
		Size: 54.0 MB (54033260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0973b60e2239b3d5ed845b461726225e79eec6d8ae136dc26d1eb5accd40462`  
		Last Modified: Wed, 04 Sep 2024 22:52:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:d69f9fb87a33713abe0ad1f6ca4581dc7cc852bbbd4d2bb6f45b53d4d71f549f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52121302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf37fab2a491a32e828a12f46f512c1ab9f6f313d9cb4f5ace24305b6e779ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:16:21 GMT
ADD file:cfc638665fbd1de945c77faa66094fdc1c2a7a3e61a02e7558b48593a3569760 in / 
# Wed, 04 Sep 2024 22:16:26 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:22:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0fe676035759e9ba94505d30bcdda1c4551dcb03be9195f24905e870dce00126`  
		Last Modified: Wed, 04 Sep 2024 22:24:56 GMT  
		Size: 52.1 MB (52121073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6935ed18b2ba8ce82d7a68e7e98692ba582b3affdd40b012f0670b38d89ecc`  
		Last Modified: Wed, 04 Sep 2024 22:30:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:74609172a2137a3890874595b76f4a5dc459b5a41e0cbef5ff5c47635689eda4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57091228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4bc7bf94e96b290b03c2864f4e296154897f8e028ebcc2903ded4acb78bb8f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:57 GMT
ADD file:453c36dbaa10f4b5f78376389c491de28c32bc4115eeb5a4f9dc3a13f8f33c82 in / 
# Wed, 04 Sep 2024 22:27:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:29:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:70bcb153a291f652093922260a9f87ef3e1b69ec4d2c2aaa4a1c06a4f81059e1`  
		Last Modified: Wed, 04 Sep 2024 22:31:53 GMT  
		Size: 57.1 MB (57091003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5d855d32901dc1b83930c51d213fa0b6611091bd5a9fcaef70cb82bafbcd0c`  
		Last Modified: Wed, 04 Sep 2024 22:34:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:9960c7f43044ff0a5ac6aea01f00ce5210b1bd3981d693b481d5ecf50d54be7e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51474081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed927086a9230c0e687ad0726fd59afbfcc6a988844efef3a97821b7bc3b42a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:06 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b9acecfeb10367a53293de4aca7b22eb21ebb799aa3404405682cff688f98f`  
		Last Modified: Wed, 04 Sep 2024 22:35:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:f2647cc61eaec57e719486c03c4f8c68864bcf633ae03e5336a38ef42c1b5ed8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52808367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51daf818376f357114738f0760813860cecbb2dc34e3ca9577dbf10fceee01b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:46:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b387dd58d93846e056a1b675973738d691bba2853dda6dc95fa9d8291edbb4a`  
		Last Modified: Fri, 27 Sep 2024 02:49:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
