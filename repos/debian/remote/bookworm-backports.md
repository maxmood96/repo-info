## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:db1c098f52e566e8b010cf9758fd8cda0ea2497bec6d9879f3434d52329066af
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
$ docker pull debian@sha256:6bb4443584efe5bd17cb1357a3d4cf48e7b8376b58382fdd4b325895bfa1bcdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49043242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994575d89bb043a8465ff28ca3d4516f74e886e3e450d7130aa7761076929dfb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:50:57 GMT
ADD file:59c477049f0246331c6723687b7f8995e7a8946172b967d10fb8b67146220c33 in / 
# Sat, 04 Feb 2023 06:50:58 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:51:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:20aeb9ca89f41415a92cd1a5e9ff6c0280e09a250e0f950c9df57d97b0d3efb5`  
		Last Modified: Sat, 04 Feb 2023 06:55:19 GMT  
		Size: 49.0 MB (49043016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364446e13c57a5dc7f25f0f0ab5ddf702a5807454a4e5778e2ffb3a6eca2ea33`  
		Last Modified: Sat, 04 Feb 2023 06:55:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b19f676a358ab52a8e6116ef69a4fde4582fda2f3ea5c67d3bf58a80ef83a22a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47993509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0ea7cbcffc15ea46c75f954122a8e606b8d42b7b8f04e66be398c9f06ef095`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 02:45:51 GMT
ADD file:6283625dd02e5a15e67c45fb0ce9fec384c9086563a64fbd85ef7eec12283466 in / 
# Sat, 04 Feb 2023 02:45:52 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 02:45:59 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a4b4311a2a6055167419fac8cc987d97e7a797e53f6176ee2b5d0e6edbde230`  
		Last Modified: Sat, 04 Feb 2023 02:50:25 GMT  
		Size: 48.0 MB (47993284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355cf3055ccdf01c358e42064228c5592a2d3253077b89e34993a7dee866202c`  
		Last Modified: Sat, 04 Feb 2023 02:50:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6a067f1cb2df9098ffa527c3185c8b3d53d274fc6ca99809aae8b55330d06c7e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45794371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e446d2f5fe49ae18944001b29c97f6e8dcca77c06e30b52259ca7741b2e6760`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 09:58:46 GMT
ADD file:7fa388eb21c424f9b3d978f277c454b5cb8a4c4fc0dac864298e9cf12161b132 in / 
# Sat, 04 Feb 2023 09:58:48 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:58:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:16b554b0ae696936d2556c56490dc1cb7af234f9a415a93932213ba90d19bd85`  
		Last Modified: Sat, 04 Feb 2023 10:05:12 GMT  
		Size: 45.8 MB (45794144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9e569f839d2fad0b726f425a1e59ef6a3d189178054fa992fb32573590e9ee`  
		Last Modified: Sat, 04 Feb 2023 10:05:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e784b27e421caa256f7ced06baadf5259bae12b1e313e9824a1e7fb7ea3fe34b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49081764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2ab277049f112c441140e3e37d42bb01195bc3f5ac6e117d8ed31ebea08d7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:08 GMT
ADD file:b40ad920bd7dd081e20adf36435db50381b9998a1de3d2eac6b2c45734ce60b3 in / 
# Sat, 04 Feb 2023 06:17:09 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:17:11 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a43b5d5927a7651097e784be4430a6ade09951f5b6879cd06b0f51fc7c4812af`  
		Last Modified: Sat, 04 Feb 2023 06:20:30 GMT  
		Size: 49.1 MB (49081538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70e2280b33468d2625e4c3f0b1118f6062a3de0a8d94ad2ddbe1a53fae072a9`  
		Last Modified: Sat, 04 Feb 2023 06:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:bd0327bf106cf117e67bd4e1b172b643f0d1b8b860a3c70ca5c92f40b05fa58c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50093645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d96827d48440378f4f83a095bb6c21e323cd30d005806ec864adf9944fe61b6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:48:40 GMT
ADD file:71f93fd08314b2207fb2e5840185c4db4279fa8f008742cf35eaf4daf925d475 in / 
# Sat, 04 Feb 2023 07:48:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:48:46 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b6e1871a6864b2026696c7ffe48da3030a97146a6a0f3ca18f87c19b1ed6e05`  
		Last Modified: Sat, 04 Feb 2023 07:53:55 GMT  
		Size: 50.1 MB (50093420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c84dd66205bbceb2a8982ea924dc9a809d94f02299c6f7cb6723e23be013c1`  
		Last Modified: Sat, 04 Feb 2023 07:54:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:164abd1c2f537d21c47d02562743a3f1a078beb705562471b888322af9b85561
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49041116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0641cab7a05a4598ab6445c183c311d9c1fcdf6f7df2017e191813fc03e08552`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:13 GMT
ADD file:342f09d1a542544d0b028faf681c7e97bab2676412290d4af1ab83b550eb0404 in / 
# Sat, 04 Feb 2023 06:18:16 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:18:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:811d77d1a16ee11b725d10eee34b4675405052eeace5043fea40862dac9fd740`  
		Last Modified: Sat, 04 Feb 2023 06:26:25 GMT  
		Size: 49.0 MB (49040889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab687e7276112e91d1387548ce2e50d5f9fd6250e998ba9778564afe46de03`  
		Last Modified: Sat, 04 Feb 2023 06:26:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3065ec755d2234476eab4cbfa0532078538c547fad47e55473987df92003330c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54144078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c4f5b6c476dfc41c435c9a0a4e40f07114a35cad8abd72a28c62f8d292c64a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 03:48:20 GMT
ADD file:be85aca9c16cf896fbced9508d29913a52fd69f8b2fd24c49efca520a37eeb1e in / 
# Wed, 11 Jan 2023 03:48:23 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:752672804a573b7cec5745cda59b6068007db5af1aef95a3e7929331c20247e1`  
		Last Modified: Wed, 11 Jan 2023 03:54:09 GMT  
		Size: 54.1 MB (54143855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f50bc5edd6306858739dfdfd4a6f2ac8503b3879bee2a2f565415eed8a241ce`  
		Last Modified: Wed, 11 Jan 2023 03:54:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:0b048210194ed7bda1b53d377612c2d7c1fe46d63eaf12b9d219f791d2343b64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47429967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e301225ecdd78bc696f1573fb87e5a4f41be47b5c9c355fbd602169b98e87167`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 04:05:23 GMT
ADD file:cac3f762206c0f8ad807211cb73145ac093d8917f5b8cf3a79eea3ef1fd14eea in / 
# Sat, 04 Feb 2023 04:05:26 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 04:05:35 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5788bb4f4cdc5bb0c03495b0d17914750f0dffcbdc053321669358a95967dbed`  
		Last Modified: Sat, 04 Feb 2023 04:09:43 GMT  
		Size: 47.4 MB (47429742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e7b7436765e1be018822e6e3395895b6001d5822f0783fb46e8eba8985a5b0`  
		Last Modified: Sat, 04 Feb 2023 04:09:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
