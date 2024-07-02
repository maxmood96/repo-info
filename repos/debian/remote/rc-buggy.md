## `debian:rc-buggy`

```console
$ docker pull debian@sha256:c20c6b4de05a9384504a29a376f6d9a6ea75c0f20bc4251de76fd44a11804ec2
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
$ docker pull debian@sha256:aea7b4d3eb53420728aedfc2fce8250d9190b8f80360668811a316a76deab32f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52429831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a82f0958104a058e27a5fc83c6921cc9e9a41dc18cf56275c441cfd6b236c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:22:28 GMT
ADD file:06cf5b56eee98058acc2138b22939b094380deece3b7569cb8f72001a1b1ae81 in / 
# Thu, 13 Jun 2024 01:22:29 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:24:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5d01f86c265bdcd9ad24686bfb950b1af7886771bc1e983efedb66d6751451de`  
		Last Modified: Thu, 13 Jun 2024 01:28:09 GMT  
		Size: 52.4 MB (52429606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a8fb7c7441a2380115af3c15f15ed98ac6899749bb7b1b7dcf5866923d5558`  
		Last Modified: Thu, 13 Jun 2024 01:30:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:f4035c5d6aed9d29213ced61082c6486341ad08a8a5298bc1ce8ca7ce50fe61a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49697496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09e4150730e826f2cabf37a0bdfc31637e6e133226d3ac3a3052f7c407e3fc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:07 GMT
ADD file:e97cbdca31cc34df027df8a29da79dec8686613556a85f9e94434bf7952452ff in / 
# Tue, 02 Jul 2024 00:49:07 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:50:20 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:00d6074b8078def64a01fe6a6ae8b9b4c88fda262cf81e16d90c7e7f16541209`  
		Last Modified: Tue, 02 Jul 2024 00:53:08 GMT  
		Size: 49.7 MB (49697271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29de1832f5323620a02003479d0778920812ae4e3cbd84283ff124bddd0e48f7`  
		Last Modified: Tue, 02 Jul 2024 00:55:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:ea114feb7f4491fe5e66cc0c3f8279c745c64b68c71f1ea58c8f704ee6d2c70a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47184058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2269ae2e62a75922dc0dac8f427740d2a710a6c5ae9dbb22b729690ec1095ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:51 GMT
ADD file:204b9bd9d9bd808b15b0257739243338e223ade24ac2085e9c4ee95ac07d2795 in / 
# Tue, 02 Jul 2024 01:00:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:02:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5771d15f45cf5483d59c36ac7d7cc82b87747d80582fa22fc972b5752cd511a6`  
		Last Modified: Tue, 02 Jul 2024 01:04:51 GMT  
		Size: 47.2 MB (47183831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0bf528ad76d75255154f5124193b16a0f41559b9c067c77ee6dc6b4f6fb0b7`  
		Last Modified: Tue, 02 Jul 2024 01:07:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d31887cc3b135d3a2c70c04cf5e7ad2fe51c291cc5bf317bcc0f466038e8ffc1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52888982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae2970deaf2c64307b3c4ac4c0e8b6fed5590bbf877e891954eb8cc8492775d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:14 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Tue, 02 Jul 2024 00:40:14 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320ddbf3f0b65fd9902a80dc192a3a05da430039f5fe2a61179bf7bb54a8516a`  
		Last Modified: Tue, 02 Jul 2024 00:46:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:787a49bf71aba9664988a747dee036ea1a3f671b8049f493357e1f9276e87ded
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53522614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800250e0c4fbd1ac50996a7efa10bb7e25983dfa155b8ed24355d6eb97d362e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:49 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Tue, 02 Jul 2024 00:39:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5532a24f9dee1a094dd7bad3f5497a2c10b67735b6c851ea1975174bca0fd8`  
		Last Modified: Tue, 02 Jul 2024 00:47:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:8c545fd7419a8254eb1d90c1b0bb5394714d7744eebe688e4168ef8822801c08
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51279422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638bcf18a5180e7bb0aa936a9e604370080c12aa3287643a4263834f9f12ba30`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:13:44 GMT
ADD file:bc1c5f4f7dc974780be655fc08cd2e36c5d04921a942dd0065534fe0f2520661 in / 
# Thu, 13 Jun 2024 01:13:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:19:45 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:371a3512d511da5522a67af4d5945c86f5bf5015bc3be3dfc08ea50797400367`  
		Last Modified: Thu, 13 Jun 2024 01:25:20 GMT  
		Size: 51.3 MB (51279195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a643c22a167fa9680e7b3ad492e2bb880f2486db6df704bd8f187c1be519de3`  
		Last Modified: Thu, 13 Jun 2024 01:31:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:025792ad8c304c7947de3faa90b7a0a004b2008408c5ddbff9e1c331b51db417
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56297194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99035b4f570ceb6e9083b5133ad0fc9b7b3c98b50defcf1f2056965323be95fb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:10 GMT
ADD file:17f3c29affbf057347abf006bc2aa243347ef42e5dcd37286af3c79f3fe983a4 in / 
# Thu, 13 Jun 2024 01:18:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:20:12 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:edab80a24633b63ae0ba8926dd3e7105717650d226694cdbfeaa41301a651162`  
		Last Modified: Thu, 13 Jun 2024 01:23:25 GMT  
		Size: 56.3 MB (56296967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481eb441a904018acb5308ec1996a72315d1184984c63cb0968135130d43b053`  
		Last Modified: Thu, 13 Jun 2024 01:26:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:3f63d99048adf9c847a0f6e2fc010ef1424ce02f8b3ce5cfdcbb143d4ebb631a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50715973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647284ed0942cd7dd126e970ba9f1682b5bf626209e5f608d71c684017702293`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:31:50 GMT
ADD file:5f145818f2852834c826623d73119954ead96eb9bce2d43c78acb87643e22613 in / 
# Thu, 13 Jun 2024 01:31:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:34:50 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6ac783982847dc2f82c444819c90a10bdd382db79de84981f527e1462e567adf`  
		Last Modified: Thu, 13 Jun 2024 01:36:23 GMT  
		Size: 50.7 MB (50715744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9d801e28526b0a7bc3e8c1c4a635711e9c31dc51c4e0baf6cbb8ff3fca9204`  
		Last Modified: Thu, 13 Jun 2024 01:39:45 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:714dff720e2f85485129bc4ac722b1a067293f079b43a7277b37e4868f46bdae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52278423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5804203730e8cb1fc140d06801d2cdf4f4c3e23c32e724f203fa8b0b02a9909`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:56 GMT
ADD file:474217365b4afce182f60b776ab37f3a44774c328ea278e1c48bc8410023f4c4 in / 
# Tue, 02 Jul 2024 00:44:58 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:47:16 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c5f70336c1fb5eed68802971c844bdd7f3b8e20b7504d889927c061344c0235a`  
		Last Modified: Tue, 02 Jul 2024 00:49:53 GMT  
		Size: 52.3 MB (52278198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308ef18c279d80e3910b05b5db87ebf840bd5bae5522aba66150dc52664fb9c`  
		Last Modified: Tue, 02 Jul 2024 00:51:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
