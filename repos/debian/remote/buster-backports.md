## `debian:buster-backports`

```console
$ docker pull debian@sha256:7acf48efcbfbbb6eccccf86f86e00265f67f792f3f08d8661fd81bb09559652a
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:b03c3e061340ad1867a6baa7fe8cb2dd215f67deabb979078fc50f99db67b0de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50440646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ca8e33e8bb20c84c712d80c9be4272287d26647f37baa480ae1600aa2b7025`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:32 GMT
ADD file:5c5cde050dbdbd5c7c0d9c723f436d37ab4a8b1a498647a719771eccce99d9cb in / 
# Sat, 28 May 2022 01:20:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:20:36 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:982cba7e471c6d3ce96014cf58b2e4e115a525e60da2e1e08716818f2c057a6b`  
		Last Modified: Sat, 28 May 2022 01:25:39 GMT  
		Size: 50.4 MB (50440422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872ee90ee5ee9ea4b3274dfc87a12c1dbd9aee5f174836437bcbc330db4b5c50`  
		Last Modified: Sat, 28 May 2022 01:25:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4484c118f360917d2f001e0ae3cca28cf2c19bf80ca13f2109f59d55d5866f27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48160854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3293125bd691697c371da5aa064a1250c520e45872ece5ec533a1d764475bc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:03:32 GMT
ADD file:ad4ce97f6ea5c59c2f067ac3448d897881ae301cb606e52556637f74cac09774 in / 
# Sat, 28 May 2022 02:03:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:03:48 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec27c4ead5d8a5ae35fd4bad58cadacd3d006bed1911fd9b07b5e4f74921f7c9`  
		Last Modified: Sat, 28 May 2022 02:19:24 GMT  
		Size: 48.2 MB (48160631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca418cd0582b6b82c6b2fab3683dde0bed2676971dee2f6efcda9ff66f84b836`  
		Last Modified: Sat, 28 May 2022 02:19:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0c5158b602b67820a2d87c8d4cd562195600b2505e412eeea4ebb91d0a370b0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf6ccac2edd52bb3ad69f82dae77e9a4d8210c256d9aff1b9e2c9ec3ed5b0e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:00:18 GMT
ADD file:3c8ac0c219015f8fbf065e01216d362016d6068cb4e73ea6f0a56893c235a2a7 in / 
# Sat, 28 May 2022 01:00:20 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:00:35 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:59fe0b97900eb1b641ad94d8d8f3bd9dbff0472e481c4c4c38f2372ef790900a`  
		Last Modified: Sat, 28 May 2022 01:16:20 GMT  
		Size: 45.9 MB (45915564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c2f763c440da2a4e9a0fda390a39cbc4cff2eec626742ca45e7d304e4b91e8`  
		Last Modified: Sat, 28 May 2022 01:16:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:17d60f7c9a8dad1e2ec28e0b9e4b9f5e765cce599ab0b0d3868589a7d32b2e06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d39a45273b60b45ca625d3836fb54fddc2c988eca0c3b2f8165ed1310a10bf0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:40:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2572b176e5f0663c289ac7d37fba29edf2388af7d3dd5922ac484b1dee10ac`  
		Last Modified: Sat, 28 May 2022 00:48:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:f97e411dc15dbdc3b1de345e5e884eaeb2096958644cf8719f59b550d5a3cad3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45559a375aee7ce69325197ba649afe437952061c54679f975355bc13dd74848`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:45 GMT
ADD file:3995ccc1e3f12a1e3f28dd818223bdc5454a7651248bfb98fae7c14961c49bba in / 
# Sat, 28 May 2022 00:39:45 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:39:52 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:045913a916496008850e7e3b499b9acc93c72b4018eda833a11c562a6d8413b5`  
		Last Modified: Sat, 28 May 2022 00:47:08 GMT  
		Size: 51.2 MB (51204248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac8d51807f32497c5d46e99f72a30bbad0017e16f7f0e97bb5b1cb6f9925fe9`  
		Last Modified: Sat, 28 May 2022 00:47:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:793925374ed61631322528692956669a7a0acd9b7be9b24c51c25b42c99ff28e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49073597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabcfe7a700c36d0250e876eecb78f16ab9fae29a39534f404b395d04a410665`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:11:47 GMT
ADD file:e86c610403bdbc84066b42627ffdf92eb051badd2f3d1fcc964fba096215c297 in / 
# Sat, 28 May 2022 01:11:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:12:03 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ab17b7e8f7dffe546de1529b66b42c5d3aaa0aca409effcd962eae29b834d3e`  
		Last Modified: Sat, 28 May 2022 01:22:17 GMT  
		Size: 49.1 MB (49073373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd01d9ffa1ec4a25a4846e413f9bd72fe9cd2e2395c53cc8a5a8350a0a6251f0`  
		Last Modified: Sat, 28 May 2022 01:22:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:afad8def858b38fe2ddde918f243b99369100b4b8860ebfac8e9bf5502a860e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54177218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0707b1f3d97499cc4de17d56714e2d60943ea0ecc07bbeb76495788548a023a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:18 GMT
ADD file:111395200ed598f754f449a2c278d0de3716fe88c66495506bbfba93a1be60d9 in / 
# Sat, 28 May 2022 01:23:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:23:43 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a84717e4877770b3a8a9f0eb6890cb457d0bf1ec5c2013b56c1a2353beb5cbc0`  
		Last Modified: Sat, 28 May 2022 01:32:57 GMT  
		Size: 54.2 MB (54176994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35888802903ca13ba4b30da9e79c35b75cff32819038cf375ea6446f94ab00e6`  
		Last Modified: Sat, 28 May 2022 01:33:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:a0feb520b7fe97ec7fb37014d91bc5358f86c948b4dfff3d2fc5221f287a0a7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ff90c7e3f98a473d92f2e8f79d42aab9b376053332cf4ea708a8c0b8a67a2e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:43:20 GMT
ADD file:65712051a170cb9d0b18d0085bc26171598119b8946fa55b5ee959661b48a5d2 in / 
# Sat, 28 May 2022 00:43:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 00:43:34 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:771d2d61f47933c8d05a5f7e35dcb16848a6225e7531db8e5971d528982538e9`  
		Last Modified: Sat, 28 May 2022 00:50:02 GMT  
		Size: 49.0 MB (49006810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a644fc1b893fb3851590745b6a1cf8d7297398ef7cbe4dbf3c9940d6b1c0ee5`  
		Last Modified: Sat, 28 May 2022 00:50:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
