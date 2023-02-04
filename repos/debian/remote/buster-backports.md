## `debian:buster-backports`

```console
$ docker pull debian@sha256:6a9971decbf55a626cf9211dc379c6603568c445437f6a613a7c1be64b1cda5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:97d71e41eef64d2452f353a8945895440c97da3e6b142a6471c1e5c499556bc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de801612a3a144764b0749c809db078cebab00297bc4af63d38f97b236060233`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:51:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70780302ce6197a81918fee3ed94c6571b11ab4a1e1c2564f6b2fcbaff02c9f`  
		Last Modified: Sat, 04 Feb 2023 06:56:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:83e731de3ddce924a1142f626ca7e4fa54228d3a61a19cdd09fffb35ec7f4874
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c67192bb0acfb0fa84784de6d4d09356c2395c07a5ba5431d5d3287f12912b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 09:59:50 GMT
ADD file:afaf1103e4ec74dcbbf13ec6a8049b78c15a909b8713dce5796a5ef6d7d5cbd4 in / 
# Sat, 04 Feb 2023 09:59:50 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 09:59:56 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6dcab737b693be9e498f0363e4109adad2721ce23274f5579d19c70a85bd0dd6`  
		Last Modified: Sat, 04 Feb 2023 10:06:48 GMT  
		Size: 45.9 MB (45915803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eabc0f31b05ed5895e1440263bd8c57b30120a83ff7016c7ef930fa4afe1b4a`  
		Last Modified: Sat, 04 Feb 2023 10:07:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:43d7fdb3b1ef361d7fc724179d391befdd110f211f6484e38b27846e42655fb2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49239595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a000fe61c9979777340faf5359541c0305bae3d36bd5aef50b740e162e35ae7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:17:48 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a381fc4bfb362bd8aeb0644985222866bcc0da00c4b3a45c8d1c940514f53`  
		Last Modified: Sat, 04 Feb 2023 06:21:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:fdbc9883a625afee0c4183acd4c68065b18e67e70e2f20ff7e59a1839197f656
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ba93fcbdc2b53ec8cce9e00355c7c3b0ec3e525c42edd09bd754845f2f01c5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:33 GMT
ADD file:23aa007679cd84321e9278c9f6261256b1734b2e27727d84ecd3e3418e6b8dff in / 
# Sat, 04 Feb 2023 07:49:34 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:49:39 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:18e547e593209084f2c8150bc5b70229a02a902a855c32fb560765e6a40891a2`  
		Last Modified: Sat, 04 Feb 2023 07:55:26 GMT  
		Size: 51.2 MB (51207661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e04e4292b3c422cb10c9dc48ad222f7204c92d9581ebef91f4fe19be535c9e`  
		Last Modified: Sat, 04 Feb 2023 07:55:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
