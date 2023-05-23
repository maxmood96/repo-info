## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:0ad6d58488ce8fe5ba8473e13bc91c48ab88291d5fcf3ae476efed57fe0a3392
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
$ docker pull debian@sha256:5320fd979eb4c96e378a017e6b3aa9e1c271c31b0feb54263d620b6ced390126
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55049294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8b31fdb72a124b4741af0508d3609e89b27c47d3443a69d216510abb3f55ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:46:53 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a442c07b2d1ef8a2d6e43f8b2694fc76ec6ae356eb5530a83ef0147f7f73d`  
		Last Modified: Tue, 02 May 2023 23:50:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:794232c222ea1dd82dfda8077a8752dccd843952f518f10deae65ee3638bae9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52546764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35a9214bc3631fec7084bea3dfae9516832dcd6cf2bf9f74cd1c0ab15076efa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:32 GMT
ADD file:9572a8fcb9c86e8a9dbfe623c732cc4ba1c4f5670490191a7e639a272d5b6e97 in / 
# Tue, 23 May 2023 00:48:33 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:48:36 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b053976742ca5b01bcefb7df8fc77a58d0becb4ce508792491574463930569c4`  
		Last Modified: Tue, 23 May 2023 00:50:55 GMT  
		Size: 52.5 MB (52546536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763d10c18c138464f06da4570d3ddee269ffe1685f23adbda6881e19e5c17344`  
		Last Modified: Tue, 23 May 2023 00:51:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:df52d9c9e9550901337c5304a8199f79b9c8056332f12836df99965c3f0a9d02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50210226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b358ca31b2a6fb007fee41a1a0e73dd3accae9f33043ff88e90db67b50917e69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:57:45 GMT
ADD file:d8748d34e524d93a6df76d2a8ea8ca32ca04897521719f9f1f2a88ec692dd69e in / 
# Tue, 23 May 2023 00:57:45 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:57:48 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:29949e2d07dd1e283862cb4c3d4ec3043f1d54a1ac59f7b7a998ed9038a0243c`  
		Last Modified: Tue, 23 May 2023 01:01:23 GMT  
		Size: 50.2 MB (50210000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592f062042c9992d4557c9f9bb30088115c88000e9f688f7348d53ff3bbac4d8`  
		Last Modified: Tue, 23 May 2023 01:01:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:44261a7d81d084bb4eee39092f845425c0ba2c35c952dc5503c70a6bc8bc85f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4564669f95dce68e7fdc1fe998139debe30a81667ff591068ab710bfec2bdd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6559675035180b04a0f4c79fa09d23e37035e4b20954d6135fd4d8249551f813`  
		Last Modified: Tue, 23 May 2023 00:45:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:4630974f5f2420d84c0a95b0992f31c2c425b23f8580a2b35c753d3725404572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56029398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4e4cec2e0e90a59b1af6fc97f3c88146c8d5c9ce68827010b5c9f966343b1e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:39:14 GMT
ADD file:acdf45f51b991111aa6c929fedd4e8de03e5d42578cca2f895f74697c3c66e33 in / 
# Tue, 23 May 2023 00:39:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:39:19 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c377769761bd9f2bd79d27a4f6dfa29be1047f4e6e8df1653027ef5262e020bb`  
		Last Modified: Tue, 23 May 2023 00:44:01 GMT  
		Size: 56.0 MB (56029173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070d765ba4fc1f2386c9e37931541f67d5d78ecfac54fbac61e7d4227ad47ab8`  
		Last Modified: Tue, 23 May 2023 00:44:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:af2006681e7b1d48a8c336d6c70e210bc8c3f75bef743fcb52a2c29256df7a93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53261357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80fc4bb462805d8363cf2f41fe1ae9349c51d9f43070cd044722b872737fdd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:09:32 GMT
ADD file:c4481c512145c216c0696b57b55890f49935871b934f1e23b24238871e88158c in / 
# Tue, 23 May 2023 01:09:38 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:09:48 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e72533d17b613b0fe30563d66f03850909770c19b7e44c2a94654ab9ba9aaad`  
		Last Modified: Tue, 23 May 2023 01:18:39 GMT  
		Size: 53.3 MB (53261128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502d889f9d0b8894a60cdc3c36e3ee10d655a00a9ce09f28f394b67011c17db7`  
		Last Modified: Tue, 23 May 2023 01:18:55 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b565e960061e7131473fbe0d34c4d7651ac8c77c3182966ddc4cfc56f4aa78e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58924173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0e1fcc8caaacd9052b814ca1bdc204da6df38096b466165baeaeafc4655cfa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:17:14 GMT
ADD file:ed39869ee4bb8e1901b71feb9cadfe754e42304e134f2542e516e162ca710ec8 in / 
# Tue, 23 May 2023 01:17:17 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:17:24 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f530a46e89ee571046fe19b22f563df6c84a31f6593a1e6ed49dbd16e34145de`  
		Last Modified: Tue, 23 May 2023 01:21:34 GMT  
		Size: 58.9 MB (58923948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75110241ee40aa3dbe71eb1b282457cbdbb95a9e6494f13bb4c49dda1ca5f196`  
		Last Modified: Tue, 23 May 2023 01:21:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:aa0c270c0542c113d210d2aa67f25570fa48941c47acc43b3b7a8c9d2d3fde17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53282338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c60a2044633b094aa6857bd63319515760e7dba7e39dbb4f93e5217caf7f40a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:42:35 GMT
ADD file:a054112be60c3f2d7811b27cde82bccfd1c2747f29b7611ee68b21cd9f3d3d54 in / 
# Tue, 23 May 2023 00:42:41 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:42:45 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:44d1d02f91725dd9ae742f7c70add814dc3da3fde438adb01e65e1f8b0eba613`  
		Last Modified: Tue, 23 May 2023 00:45:33 GMT  
		Size: 53.3 MB (53282114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ffc71f98ec65c66684a271b662f1f051e1afb8f7c290be1c5e263ff4b22934`  
		Last Modified: Tue, 23 May 2023 00:45:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
