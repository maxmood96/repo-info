## `debian:rc-buggy`

```console
$ docker pull debian@sha256:e92a4bd65609e1573d8f9b46e56b8c88786feb680d948f046fc72a6b45522793
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
$ docker pull debian@sha256:5ce0abf8319c77b202b17ffe51257b3695b9f5963b86a2582b71fe97115a9f17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54793492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9bfe95257ee56f4ce8c97b8335291973a5ddbaa9ad45ee8c5f6256b4f818c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:22:23 GMT
ADD file:66b4753e4d225919cb5470c007009d4dbea725cab1d3ad1cd3c0ac3b35192aa5 in / 
# Tue, 09 Feb 2021 02:22:23 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:24:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e9e6a013db8a50441790405f039006e736170b55104d06c80015cacba6d5b0f4`  
		Last Modified: Tue, 09 Feb 2021 02:28:28 GMT  
		Size: 54.8 MB (54793268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac252411fe7847b35f8adfb2906dde84e5380c9d910ec687cd0193b475a8ae2a`  
		Last Modified: Tue, 09 Feb 2021 02:30:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:437b7692301a9282309237ec4c4503c85ee94aac19188dcbcc58405ab3649043
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52324361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b43f15bf5d330cea8e10f740040196d36f3fdfff5bc9bb1c3eaa118ea3669e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:53:02 GMT
ADD file:8a666bde5248b085708640c42b93c850be2265e6a4db5b59c48543ddc8ad0148 in / 
# Tue, 09 Feb 2021 02:53:03 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:56:33 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3b915a09886212577bb3e4444d6bdc576b17746fa48c0239c56c968d81127e7e`  
		Last Modified: Tue, 09 Feb 2021 03:01:34 GMT  
		Size: 52.3 MB (52324134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1982bda88431787a0c233cb83036523cb803b0a044a58d7ce7f097568b57ad98`  
		Last Modified: Tue, 09 Feb 2021 03:04:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:94083ebefbf502e4abe5adee8a8e8b966cb90229d92d3c486db3a9d63fb9b086
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49982958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebca72f8fdf97fc755c3b05555fb6da45aa4d45c2ba7fe1ebdf1f9088dea5e9a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:03:31 GMT
ADD file:37f3b4ac2683802bd4615102851fc9dcbc409a3964e047866697c24a568fc90f in / 
# Tue, 09 Feb 2021 03:03:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:07:08 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b8fd51bd157e6a71bf72bc04c009bb65c4766fc14c9fa5e95c0bf36f393f7ab4`  
		Last Modified: Tue, 09 Feb 2021 03:12:11 GMT  
		Size: 50.0 MB (49982731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d77687638453ffd362a87a916fe91cb7d5283814d076b4e084188ba51f3373d`  
		Last Modified: Tue, 09 Feb 2021 03:15:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a9cbd83cdef8b500000c9d6f50f08df2fe5dd983783c43dc81e172835b08098e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53468069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171f64dcbe84014e8079f0d18ae7c97f07b3b1ef1698b8f0cc318a3f4138a915`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:06 GMT
ADD file:988aaab917b0b86b69a5ec0bc1b562df25e15f11cbd3997c0eb79c065697d66b in / 
# Tue, 09 Feb 2021 02:42:10 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:45:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:16d849c3d9b47a494d04ea09283a62946c42f5ebec529d6b0f5c094929bc8e48`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 53.5 MB (53467842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986fcfb64bb6793710036846a9751a5ea8ceb188ed2d11a0d99059a32556832`  
		Last Modified: Tue, 09 Feb 2021 02:52:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:7e02bce8a6b4b91719533ff79262fd3d41303ef5d6e206e279ed98af96cabe72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55792237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae442bf6a8d0142dbf39c536be52bc264a801b80f3fb4d4135a231dfb454237`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:17 GMT
ADD file:d3470c47b61c2df201e9fe51e9dd198c152bae2eba84df9bbfcb591bfb29502a in / 
# Tue, 09 Feb 2021 02:41:18 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:43:29 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:14213d5e86eb4e1e7c43e3524429378786d8674960445945ce050c587b83884f`  
		Last Modified: Tue, 09 Feb 2021 02:48:13 GMT  
		Size: 55.8 MB (55792012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c7cc0dd43d6e18f0b9d8404b4a12229e0b3d8995c3ab31b99cd773531f8838`  
		Last Modified: Tue, 09 Feb 2021 02:51:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:fe43331291e5e33f35eedaa308ed476bc09aec8ccc8ca828015989150bb7bfa8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53039004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcf540accf86f19dd56c5c8b61632cac06b38f492ee8798d727643574357749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:52 GMT
ADD file:1bed7e8245b9fdc9b6216dfe7c7a97a236870647ca9e7641f98c8b2f5f165612 in / 
# Tue, 09 Feb 2021 03:09:53 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:12:40 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d37dfb54bbee12f1ddd54773820dc4abe1d8525601798200ea891af443d2dcdd`  
		Last Modified: Tue, 09 Feb 2021 03:16:42 GMT  
		Size: 53.0 MB (53038778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8215e64d488ab092b48243d28efc203c56bd607a5fff0399fbfa72ca1d79679`  
		Last Modified: Tue, 09 Feb 2021 03:21:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:4529659655e2a20519662d52a4b1cc3830084d917f012b845c3bb2816606d16d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58695340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40f420644c06c7202adddb681d1d21b6300e0cb8630c190986d83845d9e30d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:52 GMT
ADD file:fda72555f400961c35bb2964a957d765f785218e1aa70a0245b08b2c647c1c42 in / 
# Tue, 09 Feb 2021 02:19:58 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:25:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fae168fbba50e1100b6e8fc677e92941a423415b78580f7d955f748fa78ca322`  
		Last Modified: Tue, 09 Feb 2021 02:28:25 GMT  
		Size: 58.7 MB (58695112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3075661d64a368f8bc2d05a97d9a49d14fe7baedf9700f7e49e1d18cd06a1`  
		Last Modified: Tue, 09 Feb 2021 02:31:42 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:a9500a0f3da9b1433faaeb9f3400e7dc4ce5719093216e9702e0035459741ca6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53060307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e323bccbad961429c2a9f208dd372a412a5c0b6e444d5d3e332f65691cefab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:21 GMT
ADD file:6b632451421e7f0411db1927a48466a6b3bc2f7e10a53b00a06799fbec279bdd in / 
# Tue, 09 Feb 2021 02:42:24 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:43:52 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3dd2606d37926391a1e8153ffefee2aaccae04bd432c37c97187880ba3ed01ea`  
		Last Modified: Tue, 09 Feb 2021 02:45:45 GMT  
		Size: 53.1 MB (53060083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd0ada58caa0facee9bb5a52ba05e2132fe55331c38fcd597b3094a2bc29739`  
		Last Modified: Tue, 09 Feb 2021 02:47:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
