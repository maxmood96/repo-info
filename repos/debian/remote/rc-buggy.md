## `debian:rc-buggy`

```console
$ docker pull debian@sha256:e70016d9c84f768fcefce851ec8c978fe26e501c2a139c17290664b7983bb9e0
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:9d66ba41dfc994c5fc9422d7725de40f01c3c2ea4053e84ddb0e3014398d2c8e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51391215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807e7e919e46442b54b4c280a6cb0e5ec468babac45e3dacdc0785e2080a3f31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:22:30 GMT
ADD file:1b99a100214a4a86a413bf6a826c70d07fee06a8c4e6d1f3ed1550fb08f9818e in / 
# Wed, 13 May 2020 21:22:30 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:25:09 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:268c82fb25093fc20c25872a9f96ca2bef121a19a81a91079b62afb96b725135`  
		Last Modified: Wed, 13 May 2020 21:28:35 GMT  
		Size: 51.4 MB (51390987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9654326c409372b98f92f8ff1497c187e6e86558120867946596e22b3b73ef4d`  
		Last Modified: Wed, 13 May 2020 21:31:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:97a4d1c1041cac175560e33e06291f147c2560730be797d0b0021a727bb81ff0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49937996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8a17745f2d0ffbf93b9b698794f8953d9ee7f7596478ff64837a777a547aad`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:30 GMT
ADD file:a75ce77565b83a916eece2d56e963b63f9ee7367ef197d8c290ff79a800514a6 in / 
# Thu, 23 Apr 2020 00:54:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:57:48 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e7313629a61ef455f6387257ffb8f19dafc5546554a81db1483683758531fe25`  
		Last Modified: Thu, 23 Apr 2020 01:02:16 GMT  
		Size: 49.9 MB (49937767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1f3475924d1e2f9b8db7ec20ed8b3f48a9e4b650d5747cafaab0d89e09441c`  
		Last Modified: Thu, 23 Apr 2020 01:05:19 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:b76ed3e09a7928028c32b526e6e28d85bb213a519a50f9ee675c771d51569f51
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47161434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28d03551a9148c03fcd660101791ef6d62a96f45e850701d8794f9a85c118fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:17:11 GMT
ADD file:5c1bf8e876f6ffb8a54374fd8f26d78a98dea1fae6787eb5fc225b65db262397 in / 
# Wed, 13 May 2020 21:17:12 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:21:24 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bc0a6102c512ac7a18c58c8bfeb98c10b25edd28979b9a105af510e9c56fd786`  
		Last Modified: Wed, 13 May 2020 21:27:04 GMT  
		Size: 47.2 MB (47161205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e6b9bf25251cff29fb4deb5a6cefcf8db0b65deab97177f491eb43cd2f6acf`  
		Last Modified: Wed, 13 May 2020 21:30:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d7d8acda4af9ee11930bed8a332afbc3c097a85a0ec35ad47f177b0129782bb1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50909370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2959c44ad382f2ff9cd0f2473326b4af329a6710dc3c10149edfd56f1c27c7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:31 GMT
ADD file:b2be126f717b29a49979e4124d91ab7eaeaa56922ce97a6c9756f621c8481f0e in / 
# Thu, 23 Apr 2020 00:56:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:01:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:03219b383ad9717495dade4e3f10c420901a34fda6c7c20c16cb0b59ba8b1abe`  
		Last Modified: Thu, 23 Apr 2020 01:04:22 GMT  
		Size: 50.9 MB (50909142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae7564dc2c204dab712625bc916ffc13e79949090dabe51690d54878adff2ad`  
		Last Modified: Thu, 23 Apr 2020 01:07:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:03bd9a88ba599d38f0c4b27581b08aae3895722367a361fa12615fffeb6014bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52481796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594c6a5318292642575156ceec23fc9eed88c7b8bca75a59d97bb9657d5ec765`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:41:18 GMT
ADD file:bbf57f6406dcdfbee8d207ada2ed9150a3e775fa2cb6e0784c3e35e1c3216d25 in / 
# Wed, 13 May 2020 21:41:18 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:44:01 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:430f489239f0254d72f3974fb8f614ac80ef76f642ab0bddcc4f20a8d4a3c68e`  
		Last Modified: Wed, 13 May 2020 21:48:41 GMT  
		Size: 52.5 MB (52481574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202da6ad79c19bb41cd09dad05760dcbbba97bdc75998a55a5d1733128b37e8f`  
		Last Modified: Wed, 13 May 2020 21:51:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:90e412baec0f5321b038cc6476580146d362c98c8d56453d9dec8f7780a919b0
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50696382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228489023534e060d13d2abb1a0aa1d08a9cf962f10d684c17ac4549c26dea4e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:11:00 GMT
ADD file:66d4b8806942796ca49e31a046824a633333dba393126281f5c12e26efea8e7f in / 
# Thu, 23 Apr 2020 00:11:01 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:14:36 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e50f308fab9e31aebf27548f07771af5a99a609ac88a60bbf74cd4f85125c24f`  
		Last Modified: Thu, 23 Apr 2020 00:19:59 GMT  
		Size: 50.7 MB (50696153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829fee13e4b638aa2628bec43c991127b889d4d9929eb89ab3250be85a0cd78e`  
		Last Modified: Thu, 23 Apr 2020 00:26:24 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:f6f1d79b5a64502c72a14fd3db6b2340733cc4f916ee282c73c8fb203d446efb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55855685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953c7eea94bfe4b3f13e0f4b13c39b0ff1fcb6f043971f05ae045559ce4289dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:45 GMT
ADD file:d55bd2bc22fb060f41d4316af4a741b519580bd2eaf76cbbbf9e3b88355447eb in / 
# Thu, 23 Apr 2020 00:38:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:46:59 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1757960a31f3d7e8a61f52b30d276d1605aa71eec0c10f82c131db13d7402512`  
		Last Modified: Thu, 23 Apr 2020 00:52:17 GMT  
		Size: 55.9 MB (55855455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c84ac0746e5c6c02f8805afcc9641a92a565ca43ded1af7ecd7436c609f9b3f`  
		Last Modified: Thu, 23 Apr 2020 00:58:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:d27c39210b0b5b16221068f9af17a7a9136282f5f8ec37871040274512d9446f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abea07d13bfc2cb102323ad96a35f0c85b404778764669ce9c0c11411a88ada5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:22 GMT
ADD file:e7473e4f1acf1308ed319dfcc667696c733d4173125423a8f1b2c67039e5f498 in / 
# Wed, 13 May 2020 21:43:24 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:45:48 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:23e07cfb1ab58da76b3f9f0fdc8f5c154643a262a86037b7b6d1c26b5959a166`  
		Last Modified: Wed, 13 May 2020 21:47:43 GMT  
		Size: 50.0 MB (50002084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d320c5b8267307e80a5e34c3d8c9facc3699a93da22e9e036221d8810a2c54a2`  
		Last Modified: Wed, 13 May 2020 21:49:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
