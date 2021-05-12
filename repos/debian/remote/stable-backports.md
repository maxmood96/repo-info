## `debian:stable-backports`

```console
$ docker pull debian@sha256:2a4a22be0e050e7c7f63d2f51f18c29e2c81a13d341bb96918a2ea7b973378ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
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
$ docker pull debian@sha256:856259f93aa7119d3735b0fcc57c03cf9769751b6f940ce7654b4a16f6377e2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50433470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e6ee504379f06d30a7adc9850c17ed82379e1130f1c53fa353705a5dbdd2f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:35 GMT
ADD file:007fd9067ea2fa2ba8836cb8f3f216f25c564458a07c444f285c20a9480f931c in / 
# Wed, 12 May 2021 01:22:36 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:22:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f307d194cb749b2f8343a9d50dbc1ed0714886c85724dee2d247fc5b02223178`  
		Last Modified: Wed, 12 May 2021 01:29:12 GMT  
		Size: 50.4 MB (50433246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd166f087c1ccf9039e3bc78ce4d10fdc6f31aa5d3be8b7c085cf128b7334e2`  
		Last Modified: Wed, 12 May 2021 01:29:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d5a1f2a49139a1ee4a575dc4d7a5dd096c51829a1962514a94106535b7f26f74
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48150985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08e119cb9327d77f2422ae18e4630a941314c5ef5e696d1982d1706ae12032c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:59:20 GMT
ADD file:0bd0f3cb977beb1c3e25534a6867bbe0d3e2525d562ec24bffb0504b6f9015b1 in / 
# Wed, 12 May 2021 00:59:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:59:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:009a59c9e15263839e7a00f08eb0a79ce8ba4a87f4bb9f6fa5a2df2e03d21ab4`  
		Last Modified: Wed, 12 May 2021 01:12:12 GMT  
		Size: 48.2 MB (48150761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb8f362e758c9663742da9fa8dce66b28c0c46821d9387cf14a79a3ce87dd7d`  
		Last Modified: Wed, 12 May 2021 01:12:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:27fd2a5afb7d618b27575a98eec3b1722dd77ed59791ede19cc4538c029de670
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45917162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c27c09b36a5567fe268ef07f61cb7afe9d9d04508aeeab2ebbb0ea98b93777b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:09:59 GMT
ADD file:4640791a791b6b1b28d7feb007dfb4b0a1dcf477c79de8ed58e6a65d9b40eaa0 in / 
# Wed, 12 May 2021 01:10:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:10:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:700102def9786f75db3733bd13baa56937e0262f9e035d264386920a3bd9ad93`  
		Last Modified: Wed, 12 May 2021 01:20:43 GMT  
		Size: 45.9 MB (45916937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9606ef584a9113e0cc6b915ceb6368c63e5454f26059e919dd6d16279eb86e4`  
		Last Modified: Wed, 12 May 2021 01:20:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e779bccec729ed22044e95930f3076df1b6a491156d4b3380fc85aa47ebef98c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49225575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd1e31873cb1c83ca82eb4ef9a7a91aae7a0c5f823e0648176e6f9066046d62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:55:03 GMT
ADD file:30cda42b7b8d62c71947c9d5ac4b64da007dbddb037e4e9f4e177fc3cdda16c1 in / 
# Wed, 12 May 2021 00:55:04 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:55:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fcdd346ffdac892ded17deda4bbddf2b7f7a9f979d94cb69a5eb066166056a2e`  
		Last Modified: Wed, 12 May 2021 01:03:38 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabdff3280f2fa49bb844c30cc4940fa1ed35771063ffe232765aa9dde1455b4`  
		Last Modified: Wed, 12 May 2021 01:03:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:eadb16131e3a734e4598f598276f0999a7ffe68fe876ad634ccc1b29b244fdc5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51200256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a4e869e1be5752fde803559cf78e57d96b8fb2be6236b34e56d1285576997`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:41:08 GMT
ADD file:62fa136d1552b405d3a8e82a710b9328fd682e81843c46f5c1a967203db727fb in / 
# Wed, 12 May 2021 00:41:09 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:41:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a94fc2b04fa63e74d2634cf3cc78ed10579c4b50a5477f9c5e6331581a0f230`  
		Last Modified: Wed, 12 May 2021 00:48:28 GMT  
		Size: 51.2 MB (51200034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5e722b643dc96c2888d9b18e5c528a27eea8552046cbcb34afc47bc0c8d41e`  
		Last Modified: Wed, 12 May 2021 00:48:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7c9006fcdc6ca6dbbed6b15c3ec92dec16045d852037d83658d17e4d44083e6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49082061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc1e955c15a23c2d837499c4219df83124bbfd2bab33cf03acf3f2b5a55f8e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:11:05 GMT
ADD file:7e1ed3bc4a813e876b93a77ef730c7d95dd6baf140e49fdbb284420057a410e5 in / 
# Wed, 12 May 2021 01:11:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:11:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:643ce0ed5e5005e5cddc849b80d04b78b63e38bfc57735c5cea0f192ffb7be85`  
		Last Modified: Wed, 12 May 2021 01:18:34 GMT  
		Size: 49.1 MB (49081838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5886acab162c43b1c58c611a2c7c682a4ae8a2b6abde7808fbb4b4f99e707f55`  
		Last Modified: Wed, 12 May 2021 01:18:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:84cc12e0bca3579cda8ec9041878b077dad315062c39b9b599145edd1cf859d0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54180343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5286837a0673b38f2b062bd6ecf96caa6ef8f2e40bef57b7f792beac6d7046f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:36:24 GMT
ADD file:49cfdf3e7cc0f6d676373561e4e98bc8ce86fa0397e130550e14fe05fa2b792e in / 
# Wed, 12 May 2021 01:36:48 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:37:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:44116be31a5e81eb3703a70925fc5d276a1fb8ca1d32fba98c7acde463c6a0e2`  
		Last Modified: Wed, 12 May 2021 01:47:45 GMT  
		Size: 54.2 MB (54180119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477b1a0c5a8acbf221026d329b756040fe5ae0c40da80a3be037313e4e44b4c9`  
		Last Modified: Wed, 12 May 2021 01:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:0a6ecbdf704ac830db66f1511ac38da9eee4a2e39f63c14e069a7069b92d30b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49001172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7716a75fe956cbde24f04ede20b33d3292fc8e401714a8b4c69325a1b5d14db3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:44:32 GMT
ADD file:2cf13d33666e634cd483a25d7bc272ce15e5d5880d3434112babe0d0b278d785 in / 
# Wed, 12 May 2021 00:44:39 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:44:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76e0b3d56007e7a527ca0486de48b956535a309e3e541f783e5842b6585e4909`  
		Last Modified: Wed, 12 May 2021 00:48:40 GMT  
		Size: 49.0 MB (49000950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a53b31a254239715777d2e5c549152ca920b3eb5b995ebf360191a7630beb29`  
		Last Modified: Wed, 12 May 2021 00:48:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
