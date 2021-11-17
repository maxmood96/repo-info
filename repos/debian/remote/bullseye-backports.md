## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:8d312115abc63f36333804abf457bb38c27f63f1aaefae3666ea6185b8a891ef
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:8350438c4551fb45d6d07af8dc528d941e4a73b8bedcce45e0b3f27727c7e48a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54932999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2589353678e1cbcf321112690526d5402cddd994873a0f91e1f9008573e76eb8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:30 GMT
ADD file:5259fc086e8295ddbf02e48abef38e9bf93a183079d3631aa7a59306b7f2f9df in / 
# Wed, 17 Nov 2021 02:20:31 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:20:34 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:647acf3d48c2780e00cd27bb0984367415f270d78477ef9d5b238e6ebd5290da`  
		Last Modified: Wed, 17 Nov 2021 02:25:17 GMT  
		Size: 54.9 MB (54932774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80eca9b7964a1743355cf46926471d01ad57d02a0dff9e9b6880b83044bb299e`  
		Last Modified: Wed, 17 Nov 2021 02:25:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ee099c1e52cb7482f2b689d327b06841f3da705a6e7a4992debbe9745a79b343
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52468133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecd6529211c2cb8fed5939084081632ecc2f8450e46f5baeaa38ac38737e595`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:50:02 GMT
ADD file:48c0196bfa5dfd1137285bf9104248d62f15a734133d8df549f35b6f7989ca19 in / 
# Wed, 17 Nov 2021 02:50:03 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:50:19 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce39e946c04dab3f8b463d502d71849e8e6d7291ece7e323f0ec9dac1061af26`  
		Last Modified: Wed, 17 Nov 2021 03:05:19 GMT  
		Size: 52.5 MB (52467904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887b594cee331bf5136b3fcee568a446ad2d334db748314aa88c0d5115478761`  
		Last Modified: Wed, 17 Nov 2021 03:05:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e957db4d555fdc3eb86f8e8b749b895a1b1e2643e198bd4731ea63535b14b90b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50134378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e13e5a51bfa3cb0ea7f1f5da62f8dff94648e23e5ffcbe32e8f76771d7c544`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 01:59:07 GMT
ADD file:43b45f65ff4ba720f6f9a107b5f80818d5ea6ebc4835840b11e9a506351da32f in / 
# Wed, 17 Nov 2021 01:59:08 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 01:59:24 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dbbf55137aab3c7acd1e012a70f1ea1adeaef8d39b474829965d3480a02bf572`  
		Last Modified: Wed, 17 Nov 2021 02:14:27 GMT  
		Size: 50.1 MB (50134152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9e428fdd0c08de2640f62c0f97e2c0e6b0ca158776b1827dd6d8027dbed114`  
		Last Modified: Wed, 17 Nov 2021 02:14:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3a8d9af8333e83826eb18c646dcfa9d4f1fec3dab122b099fcb7cd972b683976
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53619250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8b0682757566bfa1dfe014d98b27f436ef8569fde461f45066822ecb5c86b3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:59 GMT
ADD file:eb667e18226da8a1ca5a41beacddc65cd1efec01c3d01e50845c5e89e91ea17c in / 
# Wed, 17 Nov 2021 02:40:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:40:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ce18cd0ba11c2dfa8c1a2d2b325e1e019b14d4ae25ffdeffb0f9686c5496bf5c`  
		Last Modified: Wed, 17 Nov 2021 02:46:45 GMT  
		Size: 53.6 MB (53619024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb6423c474eee9c8b503cb8e03df9c3ff5413232ce19f719c10ea2f7ef4efcb`  
		Last Modified: Wed, 17 Nov 2021 02:47:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:23b79124d800145cbe0e6b36770ea9ecc9603fd8054a221062b1b75c56d29f59
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55937812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d7829ff0e20953100e39fe1b235e5d646b32eb0067bb2e7957ae08fd5d7167`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:36 GMT
ADD file:b8f9021573a53ec69fa566a396d9a8c68392bd6d659a665c0aea8fbd00164f12 in / 
# Wed, 17 Nov 2021 02:39:37 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:39:44 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d649f3a0e8410b121648ccc552acdac0960691a4da33ff4db9825f9b51ff3f4`  
		Last Modified: Wed, 17 Nov 2021 02:47:12 GMT  
		Size: 55.9 MB (55937586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e456f6e9727774f8218282b1edae9d69130820f39dfb0a375fb52a59260fed`  
		Last Modified: Wed, 17 Nov 2021 02:47:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ce23e59d80507bf0cf6cbc033a00e89d6b0ff962c29681a897a58a527fc757a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53184034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47991a7daa6d994337c8b9ad33f8963ae32917653605014a2aef3fda1e531aca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:09:46 GMT
ADD file:2971df49f24648b8d5166d87e392e2547d5b03469356f20d112ce6feb3c329fc in / 
# Wed, 17 Nov 2021 02:09:47 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:09:54 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b095a0b63d99a4c4cd9c1c353f381a69ef041e6f80798d807ae51a34b04920a0`  
		Last Modified: Wed, 17 Nov 2021 02:18:22 GMT  
		Size: 53.2 MB (53183806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b9277a0cbe5e8322155dd006220ee30deec9b1b7209a682bf52db18282e887`  
		Last Modified: Wed, 17 Nov 2021 02:18:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:dc5bd3960c610318d5ed435bd1652bce56065f6e66fa6598f9db710cf4fd16b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58819733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425eb4520a7d1ec9dc7e77c095c26c51396bc7ec6d20542135bd8b385e9bffa4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 03:27:04 GMT
ADD file:85375acb19da58f9eabaa67f8cb425cd1ff2dadb2888bbd9dbfa6223d16fef23 in / 
# Wed, 17 Nov 2021 03:27:20 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:27:56 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ede9cd7c8f1d380c971a130fb3d8a3914bf3a9106702164c23b2cce536fa618c`  
		Last Modified: Wed, 17 Nov 2021 03:52:39 GMT  
		Size: 58.8 MB (58819505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db37e9eb2f72ebe52d30bc2bd731d6081d570c5a021ad20f2bc558d789078a60`  
		Last Modified: Wed, 17 Nov 2021 03:53:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:e93a27f13cc196aaf71d6c9214ab1b44fdf00598bcf436267b61bba3ae525871
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53207405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccfcf32dcf1e4d5c1c23a51b0179888a1674ddbf1d123c9f43f6477fa17d37c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:07 GMT
ADD file:b7524e775a2033d246d1096765a0eb6eaa5ba6ed6c8b395522579d2c4e7a2e38 in / 
# Wed, 17 Nov 2021 02:42:09 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:42:18 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ffa47acd07831fbc96680a705da20704bac0016c20dc3c454ecd45cda44b368d`  
		Last Modified: Wed, 17 Nov 2021 02:48:05 GMT  
		Size: 53.2 MB (53207179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a435f0d5379ec0cf1aa220b8bd1d996c89718af0408de28ddc2e7ac478b3c7d`  
		Last Modified: Wed, 17 Nov 2021 02:48:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
