## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:2dbc47450069bc6adb633d22eaabbd3a0cf9966eaa8af818a2a54bd477b95a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:22044536be46c0788023a6a18306cd36bd3f4d336d9e2096678df0ca62d1ace9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436c75bab11d7d7ea74d7bb487c5e9426d1be0a86a1c5ea34c33b5de53ad24b3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:32 GMT
ADD file:e02b534997345e0a8d36ca5cce2bafdec3dee7b4d6c7126d114150f23c2bfe7a in / 
# Sat, 10 Apr 2021 01:20:32 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:20:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bea94887e88d6f200cd3ff9bf3ee509bee5453dc694a00c3de1bdca3c0e78c0c`  
		Last Modified: Sat, 10 Apr 2021 01:25:42 GMT  
		Size: 45.4 MB (45380043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0045b406180b9ee5652d9573dae6af19dcf7ce96d6aeaa959413540043acc45`  
		Last Modified: Sat, 10 Apr 2021 01:25:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5171fe4d6ef2797e86ea17ef2eb699986f93f76b604932aef1715d9fa8063f93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de1cfede1eb3d60513e3c55c93cfc131a5e790af57aa55e91cb85f34bf234c2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:51:52 GMT
ADD file:2fdf5aed116b6e9057fb47a7e05e4261fc512bbd5dab91fdeb8a7dec29ba4870 in / 
# Sat, 10 Apr 2021 00:51:57 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:52:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:48fb44bfbfafefc7574a9d141fe167083e9504fbd493326c3daeccd69c41f053`  
		Last Modified: Sat, 10 Apr 2021 00:59:45 GMT  
		Size: 44.1 MB (44092032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25832b812be6e57297ef2a2b1f1194fb8d1103f5f9783fd6135019b0b5edc44`  
		Last Modified: Sat, 10 Apr 2021 00:59:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:70debc49c6db5ee7ebf0f0fd99ee602e4948b27b56901db8195643046b151634
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b59910468f2ad52e46ec10b3b174f001ced0dc6ae120003a47510c81d37c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:00:08 GMT
ADD file:a47f2ee3f0ee7cbf1669fdfee7e777c89e1d56a279db9aa5ab7fc7b0af1f516f in / 
# Sat, 10 Apr 2021 01:00:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:00:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ef1968a35de5c32281733c3c0653c4aebdaa4476cacfcc2583dc951bce35112d`  
		Last Modified: Sat, 10 Apr 2021 01:08:12 GMT  
		Size: 42.1 MB (42120276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968c657af93de59487a9a202f6354185be184135b9b94575f69f1c8d50bb6cdb`  
		Last Modified: Sat, 10 Apr 2021 01:08:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:28d70f6156c446d00d3801551b8405d117e45e77268f7a0284321ae9fa23d4b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43178028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed1a21fe43ffe4f4f4aebb318167954e11e9a14be4ed15c347fff187872a4b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:45 GMT
ADD file:0347e35673a479bfe13185228f472da380c8e6fb93cc014b2e9512b97731ac0c in / 
# Sat, 10 Apr 2021 00:41:48 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:41:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a0888c116db6837c2747a648185e16971729e0d5f2f0408c1aa8e44e39ecb3be`  
		Last Modified: Sat, 10 Apr 2021 00:48:12 GMT  
		Size: 43.2 MB (43177801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f453321840a1457857b5541087446b811be97b22f079b776acdf765a119b898f`  
		Last Modified: Sat, 10 Apr 2021 00:48:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:b3f41b148d5e68425ff94a0923f6f669ccc14e70549bcce99a7d7046cb2c27cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2930b7dc27b0f56ecd80b125970f98f5451663ce41d50cbb2cccc76116141c16`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:39:55 GMT
ADD file:d8f7f36f24bfa18f39f5079651a86591728c532d73ebe84a8468b25b74476251 in / 
# Sat, 10 Apr 2021 00:39:56 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 00:40:01 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0313955408c943c20478a21d3f0ee153c47503baf54f05e7a5e871a3220357ab`  
		Last Modified: Sat, 10 Apr 2021 00:46:33 GMT  
		Size: 46.1 MB (46098694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e2a22f7a59de4dbab2b6129deadc5eefaab534fbff3b76d6747546a8477251`  
		Last Modified: Sat, 10 Apr 2021 00:46:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
