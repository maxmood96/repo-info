## `debian:rc-buggy`

```console
$ docker pull debian@sha256:5e11acae2f3f2e0c48c14ff0f72c95ad6504e586a5c19121308a2b5e025effe1
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
$ docker pull debian@sha256:24cd399744447d167aa414122b56d5ef60c2f5e8814d7dbfa4173ff29f6cecde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52836414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2813a7c9f4157654a72714c43d12e636a03cbe22c88c88691dec74ad1db2c14c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:13 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Tue, 13 Aug 2024 00:21:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:22:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5d240b1f8d1b62baf9c896a43918795a5abba65bee50ea231bfb42650cacef`  
		Last Modified: Tue, 13 Aug 2024 00:27:38 GMT  
		Size: 226.0 B  
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
$ docker pull debian@sha256:eca6a7a8531952f24a01679d6e90cec5754e269943f665ce335d11a8f8fe08e9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53738701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4bdb189ed3db91030e911fb989d1a3b71c337b7dad62cd3d4974991b971d0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Tue, 13 Aug 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:41:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f009963566851fae53863d9a42678800092b94d5dd95ed84bf2fdbcbe636f8`  
		Last Modified: Tue, 13 Aug 2024 00:47:01 GMT  
		Size: 227.0 B  
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
$ docker pull debian@sha256:4a7b5b09e38af7f9d2d0b5cc071a6a42646c427b3c08ab79f1e91114c23bdd40
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f054369e5c93fc4d0dab3a2c26b5c35e79aec4e63ba069c7df04c88c0aa5de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:11 GMT
ADD file:e6eea681cf56e20007639454c01cfebeefac45036637c0c5aa781f32e61086f3 in / 
# Tue, 13 Aug 2024 00:23:13 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:25:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f94a26791ad674a64a864ec5ea20fbd30c5f7f3fa34d6b6d03306d943685df53`  
		Last Modified: Tue, 13 Aug 2024 00:28:16 GMT  
		Size: 56.7 MB (56729826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55e3f746eade185f364d05ad9bba14695d4a71f9a09b259be9a57f12e6e494c`  
		Last Modified: Tue, 13 Aug 2024 00:31:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:f43a584110e42c4d2189e9270de6a9db8f7a5a2a2a60300c5b93a227bddfd688
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51106386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503a337ab462fc38e736405c337eaacd33e4619ef5a4793ea6d571ab5d646010`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:01 GMT
ADD file:97cc40f71485a0c47367bf7de8cb1715072dce719d216195de9b049516a29e45 in / 
# Tue, 13 Aug 2024 00:11:03 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e7e6753663bf71667278434bd9ec3bfbf244788b1855805c384ac83204bc13ef`  
		Last Modified: Tue, 13 Aug 2024 00:16:18 GMT  
		Size: 51.1 MB (51106160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225cc588450bd0812cd66a46abadbecf609e2f72517f2edea59aa46a321c9a64`  
		Last Modified: Tue, 13 Aug 2024 00:21:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:366b458f9c9bf175e174b15581b07ec2f0d96dc3a08fce29641ec5e14220cb3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52756814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53fd26250592c3402a6f31b4104e9563f716d9dad5f7d9ddb4ff7bce8bf1dde`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:44:11 GMT
ADD file:22e5ad49d0ca958c0a6f6e6b30f8ff191ced56a0355a55b9de94b5753608a9f9 in / 
# Wed, 04 Sep 2024 21:44:13 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:46:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9d384a3df86e2f0599dbfcd66ea74d1e111f1fdf220d3cb1876a56217b3b0016`  
		Last Modified: Wed, 04 Sep 2024 21:48:46 GMT  
		Size: 52.8 MB (52756590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a96da39db2e6f1a73bde03500242156b2f7417ca03c45badad1fdca6c4b09c5`  
		Last Modified: Wed, 04 Sep 2024 21:50:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
