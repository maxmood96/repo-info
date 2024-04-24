## `debian:rc-buggy`

```console
$ docker pull debian@sha256:51564dfca29cddb912853d189cabd8ffe2d84741b208cb865a07c2eacde38f88
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
$ docker pull debian@sha256:600ee2adbe160d3d32c469c11d17a89aaf3bb91b55240fb4fbc052c2cb5038af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de802bc341ccb08a77290672fb5472c3e1577422282f842ba921fc9930007096`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:29:41 GMT
ADD file:2bdf145484732bc44972c30edbf4ac0d4400e2c23e993bf3575794199944fc3c in / 
# Wed, 24 Apr 2024 03:29:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:31:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7930dce44f2f1c310f4efe60708c4f2a496a0490b6d354b92c75cd37256dc108`  
		Last Modified: Wed, 24 Apr 2024 03:35:15 GMT  
		Size: 52.6 MB (52577130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a2a7cd72e879f18a74976b842b19b3a1f619ddfe9ee66f13607eb2f16c3f5a`  
		Last Modified: Wed, 24 Apr 2024 03:37:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:581fb1d795d5dbff5c7de929c4aabef0d74558e4898984a8c751077979bbc3c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24cab6556512e1f2b9e1d84811e77d9c5c9ae4a0fe9356944f65032f3a2b8b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:55 GMT
ADD file:6d78ef568e1b0c99bde27819bc47c6a881dad9dfdcbb9902ef13727853e9b7f9 in / 
# Wed, 24 Apr 2024 03:53:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:55:20 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4094711d041a5e7837195f3f8afff735217273c55a635f8ee4943e12e12227f1`  
		Last Modified: Wed, 24 Apr 2024 03:58:08 GMT  
		Size: 49.7 MB (49688192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704893ffbf161ca9c842924330e01d7b1dc0926e3890e869755c74a2609dadcb`  
		Last Modified: Wed, 24 Apr 2024 04:00:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:8adf63a9ec0e7523aa5930e35c38af2a30fe7083f20765b46881c85dfc0cc53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46488438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03949c4110701dce58b22d605843fccbc3756ac279d5eb4b341fbc15f9cd8b70`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:33 GMT
ADD file:b651a9e79740799ad0cf7f17474e58eefdc73e4611a56f8f166422f38c62fa53 in / 
# Wed, 10 Apr 2024 01:00:34 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:02:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3bb537406eccf44a062d659169f21696e8c3000511c07deaf7acadb77364db29`  
		Last Modified: Wed, 10 Apr 2024 01:07:36 GMT  
		Size: 46.5 MB (46488213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d132ee4ed55f117d06e08ca443f5d5d62264d59cb082c36308fdb9a2d92c0d`  
		Last Modified: Wed, 10 Apr 2024 01:10:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c16c2e0f3ab4e6df907769ffa09d6c553b1b42b125801f2f5ec126a7a7dfe370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52137223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bb193cf6c65a4e588670f3f578faf750e009eda47e77c1d998f67b5bd681e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:31 GMT
ADD file:69ea41e74fa7a7601d1adbbdf992359f0c16c551447466cb4aaeac1914dc2377 in / 
# Wed, 10 Apr 2024 00:41:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:42:41 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:de2b6ae488daf95901751cee985416dfee51a36f7f9f15e60031279618e00a20`  
		Last Modified: Wed, 10 Apr 2024 00:46:49 GMT  
		Size: 52.1 MB (52136998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd3ce6f097b077224c8c325f058c7e0b3df43a515a88a90d047ce33a97397f2`  
		Last Modified: Wed, 10 Apr 2024 00:49:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:97a755c81634845c3309494cffe31afca891f237e6944693a62d2223854708e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53469402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2b61b4b494fc0eb282870b5ad68766f5dbdf2a859cbee3dc4a18cc99c9c4e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:40:33 GMT
ADD file:d8ee7d4701df61ad645e587b8b9747ac72c6dbdc2d358f14834282481c37711b in / 
# Wed, 24 Apr 2024 03:40:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:42:13 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1468f2e7ad62241109cfe49228c179a1529c8ad99c7e30f87c274cdba78b9582`  
		Last Modified: Wed, 24 Apr 2024 03:46:38 GMT  
		Size: 53.5 MB (53469174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c07509a934cc64f06b9ce265c33425330a1beddc494a7225b029dd0478c62c9`  
		Last Modified: Wed, 24 Apr 2024 03:49:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:1a626f7709b28630ca5e2d99ac468a8d75c65d21ee08502ff34474441ae2fd0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51498675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888bd951d84102b37d689f6e6d36e5cb570f1730bc7e5cad0b56236f5765d641`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:17:23 GMT
ADD file:6ee5f04f14b1e874e152ce4477f27a16f4f4f6e4e49473d9e0d4f54bc8c7736d in / 
# Wed, 24 Apr 2024 03:17:28 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:23:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:04e21b74f69d4354ef0e677ec5dab4b460bf993f23d559662b8fd1e622263e43`  
		Last Modified: Wed, 24 Apr 2024 03:28:44 GMT  
		Size: 51.5 MB (51498447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494a83318c51e53b2eacb087c46d2d72fad9700ca4fa04d6cd43f0475f5607a4`  
		Last Modified: Wed, 24 Apr 2024 03:34:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:8f4613a59e5ac8396b0b35062c80a5860f80e9553692019ac27308a9c784e8cb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56489458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24c53abab93e1bae0fdebf712b0b454086d0d19650f9bd40f402ebaeab439c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:22:30 GMT
ADD file:7b560eb5bd2a2213add3248349e22fae85a27ecd1155298a4bddb816d7a54856 in / 
# Wed, 24 Apr 2024 03:22:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:24:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:765cbb6e5130c0f3c7d92d3db7754f09101ef280d3dc88044ce2e4f3d010efb2`  
		Last Modified: Wed, 24 Apr 2024 03:28:43 GMT  
		Size: 56.5 MB (56489230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd5925f02d75fd77f75081f461b4a45a40f6b3ccb40e2dcf39597c2473b07e8`  
		Last Modified: Wed, 24 Apr 2024 03:31:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:70eb42d131033dc91993315bfdeb2d8661e11fb6ed4a10dda530aacc9f6aa043
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50665618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35edb47b4f3694bc21028cf3015240e5c3343098a9f22dee53dcebe78413bc25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:09:40 GMT
ADD file:d90cd6aeee4d6792791ea2b4b9b5059a36f027dc9b9bb977ca1e8446d6911cd3 in / 
# Wed, 24 Apr 2024 03:09:42 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:11:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:95fc214d1cab5d6d820b79b86707ae2364689381f1652820f201941397cd8e5e`  
		Last Modified: Wed, 24 Apr 2024 03:12:28 GMT  
		Size: 50.7 MB (50665389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e6c2dc53fb042895f27c223670a1afe9525f17f7af30ac2b4ee2b6a34e86f0`  
		Last Modified: Wed, 24 Apr 2024 03:14:36 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:1a773d15dc266b5a4b20e75f5addcc7d255db09214d61271dd377e45144445ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51982122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30be9f410c6441a7269db8a04c6461030e76f51858b1b5dd5a2ab0bc77d171d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:58 GMT
ADD file:59f3ea732a9a69e000f55f6c77572ee58d91ef44832ade7eaf9ef53517342662 in / 
# Wed, 24 Apr 2024 03:45:07 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:47:56 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9460d35145d54c9079287c32e655a7ef3ab5a3e0db954bbf6e5f0d93a023ea21`  
		Last Modified: Wed, 24 Apr 2024 03:50:29 GMT  
		Size: 52.0 MB (51981898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6794aa8d82eedfac39712c53a804b478e3faa342a66fb8bab1e8a82cde6300c7`  
		Last Modified: Wed, 24 Apr 2024 03:52:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
