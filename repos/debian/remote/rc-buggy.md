## `debian:rc-buggy`

```console
$ docker pull debian@sha256:060db2cb1139886e649b1fc2d631ba9f62c3e2f84b969d4b24cf1dbdff91bb3b
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
$ docker pull debian@sha256:540cc9150888cee6c90ab3db572512a725df4163821e355249033fdaec43347c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56801187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7eabf1ea54d82c1561b5b5e8f612ff45d9d13eea971e9c224d773e535cd64a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:34:16 GMT
ADD file:f1c9279b9eb3b88b40c4958324519afa81185c0383ed51d5138ebf2a0eff6d7e in / 
# Tue, 12 Jan 2021 00:34:17 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:36:22 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:abc50f4e181143f18afce1a5282914e00abd896a798d96f7514e728b30f0988d`  
		Last Modified: Tue, 12 Jan 2021 00:41:42 GMT  
		Size: 56.8 MB (56800959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22a6c92647b6ff524ffc29cb666b5630f4adc66994ff00d5018efe7007fcbe4`  
		Last Modified: Tue, 12 Jan 2021 00:44:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:8738e512bb9fcac5e17c8819d67fe2f2630b0f838ae38b61070455a687cd7123
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 MB (54362267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086a510af1e4d38f493623ed8cea42da3c19e7e1ed0c17f86c350b1230c4aa6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:53:57 GMT
ADD file:7c196731dd997fe0c289ed02eba35ecfe200559ab33bcd6e863f39d8dd0ea362 in / 
# Tue, 12 Jan 2021 00:53:59 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:57:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8703e0802b99292f132d58e67ad879ab0ffa44370ae81a8ca7a93ee05c332d4d`  
		Last Modified: Tue, 12 Jan 2021 01:03:20 GMT  
		Size: 54.4 MB (54362040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ba130bc18e8fa0b805263fd904c2b8c40a559f337a82e2ec3c4345d8652fb5`  
		Last Modified: Tue, 12 Jan 2021 01:07:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:94f22f218e8dc7d962283b91c25735dcdb083ef0fe8dee3a423ad39fb78014df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51902399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbf3a6dc20bba4d4070b5fc8d40d8104e109869f1b2c205986b6a3590388618`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:03:45 GMT
ADD file:a459be4601ccf608a415f6ce53ea885edd1a9a10ba1205f3e8493e277e6a7faf in / 
# Tue, 12 Jan 2021 00:03:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:08:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2fdfe7e087b5c823888d02320fcca90d4debb7a7d0ead6a978abb2de6acbbc00`  
		Last Modified: Tue, 12 Jan 2021 00:13:47 GMT  
		Size: 51.9 MB (51902171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04e4d48d4306261c82287a4e9b188e46036368fa815fb29f745e50987d7c97e`  
		Last Modified: Tue, 12 Jan 2021 00:18:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ba48d5489fe06d863d5b897dae8e21531bd28fd9a393e44822ce954708ada750
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55538044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153dedc09ed8bf7d1fe3dd795b05a429e3fd99381128c40dd598b50076135dfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:27 GMT
ADD file:ba9ce45e2c6743713798982615c806de6db6d8fd9a0d8734c8a69d80f3959eb6 in / 
# Tue, 12 Jan 2021 00:42:35 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:48:31 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:01dba80e9024f3ac734ae74a14f2997ea67918b4de57aef778ed839a508baab1`  
		Last Modified: Tue, 12 Jan 2021 00:53:15 GMT  
		Size: 55.5 MB (55537816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c286a2b07f62fe475a9fd91bc3185ab24fb546e07afd07e449f4666153f08514`  
		Last Modified: Tue, 12 Jan 2021 00:57:32 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:0e3fcd81615345b4089209cf2c4af6d1babb4aff344217d1d272142baa1b77ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57940730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3dc96665401d0c52a7d7d9d9ce602b8cde503bc8b969bbdfa91a2d3aab4ac7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:09 GMT
ADD file:f368e139210fa607baf12a595022c06210c9840e9f988eed126d02b3ed2abafb in / 
# Tue, 12 Jan 2021 00:41:09 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:43:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e50ef36c9f800462aaf97a2c77ececa8643ebfa28c18c3c5df44156f678ce9de`  
		Last Modified: Tue, 12 Jan 2021 00:49:10 GMT  
		Size: 57.9 MB (57940505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3673ef79e7a8391bf8ed371292eee17e81637ee5113f46c45055ba4e27d782cc`  
		Last Modified: Tue, 12 Jan 2021 00:52:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:4708d7281f5407d3b96489f60143d9430daad33478342fcc3fae6a0b80a51dfd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52069953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6c7a105528be98295e67a1accaf18b2c86545953fe0f43db6f4ce482cdd51c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:55 GMT
ADD file:144f263fbf8197586830814ff675d3c7d3ac8e3df7debe6633a1e91f84ff845b in / 
# Fri, 11 Dec 2020 02:03:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 02:06:44 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9b60fb1f705939e8d3e124cd99cb825ac48613619a7a75de5656f0bde8bb1f05`  
		Last Modified: Fri, 11 Dec 2020 02:11:04 GMT  
		Size: 52.1 MB (52069726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a6189be891e628d5c95e9b3acaf591bf414db17d21b01593e3fdbacfaed493`  
		Last Modified: Fri, 11 Dec 2020 02:16:05 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:55dd4c257c67778c04369f251cf6201a26061fc3f1937b8953fd3f7639b84411
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61048955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfed633b21b8cafacb34a02d2259a081319663575fa0b75a6c8d1750c1ca794c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:25:40 GMT
ADD file:f289d6dea557bc0563fd9221c4857a56c56bb52d981a3ec90ade2f1b76980794 in / 
# Tue, 12 Jan 2021 00:25:56 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:31:02 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:594e638823d3ce0bbedac4d1aebea00f91d28a98d7b98ca680fd90e4c0fc8850`  
		Last Modified: Tue, 12 Jan 2021 00:34:46 GMT  
		Size: 61.0 MB (61048727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f260a3524930382290d8166e699052f3c93f7fc5abc69b9c5f84c1711f99742d`  
		Last Modified: Tue, 12 Jan 2021 00:38:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:74e7aca70d71765edcfeaa96f89f009e03d0ce2eb36786383f29d4fdd82cce1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55038703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b743f0f7f9e4f047d6eee0a2146eee0e7220523dea8d5acfea3af14ab165217`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:33 GMT
ADD file:168fa93b7a5e386f9127b8b0d3ef48b98f82ba06ff1d48ac529b03d704687af9 in / 
# Tue, 12 Jan 2021 00:42:37 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:44:08 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c7a519e99fa2bc8473c6755b8e9be0f1d685a3d42426bbd0d3e942b5d1f9a4e8`  
		Last Modified: Tue, 12 Jan 2021 00:54:49 GMT  
		Size: 55.0 MB (55038475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d471895bd191187506a8c61f47633514c126a514fa3e4a5d8e09d9ac4b295916`  
		Last Modified: Tue, 12 Jan 2021 01:08:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
