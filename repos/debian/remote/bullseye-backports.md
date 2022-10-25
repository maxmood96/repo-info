## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:1e443d186c7457a39f739e3df6951ddb85182d43a42de5c90c1dd7a8c095666f
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
$ docker pull debian@sha256:fedf51c398206775c017d5d178d00886f9276e283af15b7e885a9e3a9c3fb376
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55046559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8685fbf169b1e0a9107b32d57f5d1e855c41c6326d19d4dea33a0556f1da898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:43:46 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a52ddb2faea46d24c36492e711d991fac328e4f4ef8bf6a4272f932a5ac452`  
		Last Modified: Tue, 25 Oct 2022 01:47:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a9926e2d70605935d0480a9cd9c95b5cf2b79ed663e31a810972707303d34055
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52547699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de0ef40d7ce4a29e44c9124350e061ca2a0fb00dd1d1fd08b8f95ea18ed9a68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:19 GMT
ADD file:b314b98654e8532fd10a08a172ea5c3edb7d7a36c7faf85d06d14be12f7b83ef in / 
# Tue, 25 Oct 2022 03:06:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:06:28 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f0ecb08923b99bef3f82c2e88603bb53e3ed084c13252275c05039cc279c158`  
		Last Modified: Tue, 25 Oct 2022 03:11:15 GMT  
		Size: 52.5 MB (52547473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34274d627c5ef2ac22bdd2731ecdecff7ced5cea36abccdbe0f515a36c6dcd5`  
		Last Modified: Tue, 25 Oct 2022 03:11:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1ba6f40586baf9ff6799a9ac4f61dc2d1df8d133a0adef8ac9b2a70cf772e5cc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50210215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41d570dd349f8783c63bc76d62a341fe91629bf0fa66cf526f1fe163de901b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:06 GMT
ADD file:94d6b607b174c11c18753fac156b0ca5ecda941da3d456e136b8b14457810d37 in / 
# Tue, 25 Oct 2022 03:14:06 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:14:17 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a9bec1cbb822a75428a679c01f232b1af10cce0bdc1bf6507d26e8d79ad54300`  
		Last Modified: Tue, 25 Oct 2022 03:20:41 GMT  
		Size: 50.2 MB (50209987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da746bcfb8603636992f6bf8854476c5665d51a59ddc949f0ccd6b2880819f60`  
		Last Modified: Tue, 25 Oct 2022 03:21:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:421bcb39cf3597a945491b0613e3b0586830cb87d6358cc5b29fabd8597c267b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60836a486e3dedadd42c5eb6bc16cb708a106474a4cf4f4050efc797ad6e37d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Tue, 04 Oct 2022 23:44:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cb4d1cc1c47818ba7b48d6f1654fcc01782df7c92ef4bc7522dc195036e24e`  
		Last Modified: Tue, 04 Oct 2022 23:50:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:3bde188840c95426e82e22238e3988171872c69d2b600add8d2d2628aef6bea2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56024186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc579d5a26e0164a3332c97a42dc02faf6143dafb7b8dbef9104253df3ce52d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:19 GMT
ADD file:aa26f69b37c3e144d08e17bb9be7302ec89ae0579121c874a35f336d7077fd3b in / 
# Tue, 25 Oct 2022 02:22:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:22:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8caf426a2703f99fb0be4b03411ecaa580d102f7c47ef43b422b6d7c13c380e2`  
		Last Modified: Tue, 25 Oct 2022 02:27:54 GMT  
		Size: 56.0 MB (56023960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251a5ab043a2908629548afd90a2fe5c4447e713e131bc78624c8f1b32cbcc52`  
		Last Modified: Tue, 25 Oct 2022 02:28:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a6cfb98098fc8ffca520a7cfb549607ac8644975cba11c73850344f37cde75d5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53266076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f47f31a696e14531030db2a9367313a1c32298013f05afc6b06dc4de97cbc7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:38:51 GMT
ADD file:617ca04150550c7e3a178e3ac85bb359b17a390090ce6ce72a6f2ed1db10ab63 in / 
# Tue, 25 Oct 2022 04:38:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:39:06 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e3c84cb4c321de8db072180e3509c5bbcf8e562ff11c03241bdf082184fe74d6`  
		Last Modified: Tue, 25 Oct 2022 04:46:42 GMT  
		Size: 53.3 MB (53265848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7303b7ee77047d78b98772d1d9207210c2141113739ec268905cf7e3d6a94a1`  
		Last Modified: Tue, 25 Oct 2022 04:46:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:89fba975e8def2a536f772998f810a202d56b7bef1fbb4c55fc692083640d75f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58916602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ce34f205ee9d5ebf2e12517d62ecaededde4332df1c80dbc8dbbc78798bef7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:28 GMT
ADD file:c01a6cc4222fbeeda5c2d679c5b355539880a02c792c64861eb17b81a3678f45 in / 
# Tue, 25 Oct 2022 03:13:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:13:38 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ee5a342763ed1d31bef8cebe9f4cc5dd6d427f630da679a87da0427be7b22e3d`  
		Last Modified: Tue, 25 Oct 2022 03:18:52 GMT  
		Size: 58.9 MB (58916374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528daf7fc5de6c675bd00de91ea9ef2d8798240304d0d7572e2d27241c202b8`  
		Last Modified: Tue, 25 Oct 2022 03:19:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:ecb899df1bf1c6dc735d44d72672f9c700c5aa2064add61eb9ec2288d172c11d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53279332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854f86818df518fbbd8e1a07665212ba69d31812e95a3031395632674c7ab0d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:24 GMT
ADD file:06f15d8a3c04752d271a052e820fb13fcdb76f0d18f6c9afb6e70391d10348ec in / 
# Tue, 25 Oct 2022 01:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 01:14:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a556186e8bea4ba9925d0c17bea2c12bfbb931653cfab1b980036800482cf0ad`  
		Last Modified: Tue, 25 Oct 2022 01:18:39 GMT  
		Size: 53.3 MB (53279106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df24abe952c77dafb89ceef29a5c3b51ad93dec220f4f1beb4162770ef179dce`  
		Last Modified: Tue, 25 Oct 2022 01:18:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
