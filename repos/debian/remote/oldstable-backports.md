## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:d737eff98c5211cd95e822194f152a636635f6aab52ef8910980da745c34ec0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:65e76e1920abc3a461a612b25f1ad0940029d7b7491ead4d74ae4df70b11eb73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50440514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b79b9c854b15b12fa017abfb3000c2c7e7ff9f3b12f9afbc98eb226e8746d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:19 GMT
ADD file:8ebd6a66970a5ed6186f96a2784a6b8208056a43745b6284d2043b94860d99c8 in / 
# Tue, 23 Aug 2022 00:21:20 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:21:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:801919852e75a5009405dc3b1f5db150acebfa9741295d491acb310d6daa4359`  
		Last Modified: Tue, 23 Aug 2022 00:26:04 GMT  
		Size: 50.4 MB (50440287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d265931968edc2229d21c71a5fa9ed0709b02b5b07bc37499a7a58694c94ed`  
		Last Modified: Tue, 23 Aug 2022 00:26:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5ce49d564bde2080f30b4597aed9f4babb19a0032088ad07aa57ca425f57f2b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d040121335d12c6bc1a6d99aef448e44dd56837e2e7645099c33db9b6987ffd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:00:03 GMT
ADD file:48f605475438bf0b8deab56ae6fc53da6e75a92b21d8296876fe739ae1f303ce in / 
# Tue, 02 Aug 2022 01:00:03 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:00:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a918af2085b17a0ecf8fbcec83b3852f8a05e6224faa0cb548c2412994b3bed`  
		Last Modified: Tue, 02 Aug 2022 01:08:15 GMT  
		Size: 45.9 MB (45915828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2e64cfdd5f8fd4bc07c96f1c8eb78b99348205c1d8d90c883e62b599d3ddc7`  
		Last Modified: Tue, 02 Aug 2022 01:08:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:dac17d7c13b6b6808c7e2f83343a2c02b3b6d8b40e12624823bc252ee3327923
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a63171844d5662d3652760d26651e965544d459b61660e4bfcbfe4cff37720`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:41:14 GMT
ADD file:b91f60d57948d67bc2971c4580d040b317d99d49817693ce287b8693969ebd31 in / 
# Tue, 02 Aug 2022 00:41:15 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 00:41:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:99a39853f3afc8d4418fee49977675d2e19b1e66220c37c26ced6d0067277b46`  
		Last Modified: Tue, 02 Aug 2022 00:47:19 GMT  
		Size: 49.2 MB (49229047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8a1c457a33dca69b1a791f729c4726b241831b1858770b47f6032f4041e2d9`  
		Last Modified: Tue, 02 Aug 2022 00:47:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:1e0b9619f4b647a0d15740689bc12c79b36987bfaa966f1d409098f1478040dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8ebebddb915020c9a237c5b67454613797a81b609631ff1c3692b69ae4dfeb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:58 GMT
ADD file:b8e12261a22f8571c7147f6c022dce8169487d1b35567042cf1abbb763838031 in / 
# Tue, 02 Aug 2022 00:39:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 00:40:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:36f4f30c7baac798cef0027e1ae19534a4afcf1b861196029bedd806ae22191b`  
		Last Modified: Tue, 02 Aug 2022 00:46:37 GMT  
		Size: 51.2 MB (51204276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd42540b88ebe8a6214a4a613dc0b59efd12af0e10594ee14e5115500b7555c`  
		Last Modified: Tue, 02 Aug 2022 00:46:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
