## `debian:testing-backports`

```console
$ docker pull debian@sha256:ff1579d5a33bfa6c012214ab26b2840d470a3129f5840d09387475449e88456b
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:77f83908f3abf7439fd3e471f23dd1ff8ebd02d0a6156149a924ffce9cf805df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50297224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382d56940e5b874cabe17d5e36167182acf95aa461c49bb0849472d8fde08e8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:06:20 GMT
ADD file:442a58a8a0d41cd269373f2e1fd60b46002638595c2b0e987d2c1798845e5e7c in / 
# Tue, 15 Nov 2022 04:06:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:06:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3667b1f15d6858775d2e9a42b78a451e9ae20dab217acefc24ca8eba6328823f`  
		Last Modified: Tue, 15 Nov 2022 04:11:15 GMT  
		Size: 50.3 MB (50297002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21af49a0b39c1795fe6dc6c566dba1ff65e668938d103f45a6e1526047b7de`  
		Last Modified: Tue, 15 Nov 2022 04:11:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ef7601456a31fe41107bb9ce2583dad4946334592583920b5430738044f564a6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49265986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e59d704ec8c8775cb0873b9febbe69bb27faaed02f2f17f09eec514b967f2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:50:23 GMT
ADD file:16568fb759ceb462231d22ab7c278ae2e1b526365a2a566b89e5b362f5e4940f in / 
# Tue, 15 Nov 2022 01:50:25 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:50:33 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:96f91e79e634251e31aa0e00987321c959339c5fcfc0995a352e4890c38507db`  
		Last Modified: Tue, 15 Nov 2022 01:56:06 GMT  
		Size: 49.3 MB (49265766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158d9a7af8643ab11a54f6881a481f65b84abbd464f1f8eb9ed4d8db4a4cbc9c`  
		Last Modified: Tue, 15 Nov 2022 01:56:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:77155fdafcb858b5c0eb89f61b6b540e527d1245ea0ea84f6fecfad51d01414f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47088690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b4305f331b1d563a3d9a8d7f6c71738b4e4b0554ef9350164ae09ac659428c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 03:45:36 GMT
ADD file:474bc1f44be7364d4e048fd26797082710be5c9fe6f49ea6cc27d268da5c7f21 in / 
# Tue, 15 Nov 2022 03:45:37 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 03:45:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6dbd9ec32c835e958c5ac5b241cfad08165523004615fefe27a9c73605a9e59`  
		Last Modified: Tue, 15 Nov 2022 03:53:15 GMT  
		Size: 47.1 MB (47088466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164bce67fc8aaed920fc959a3b88f6639dbac3dcad6046205784b8727d408d8`  
		Last Modified: Tue, 15 Nov 2022 03:53:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0a53028a11897db37191b4f570a0e20714dbad423a0a02d4901dc53ce63b0b8f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50353485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6c426c96a8f42a046222d9ac4c692307b37d169bca51311777ad02e37c8ab4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:19 GMT
ADD file:2bc0616483d1e16809c0470524d86af55e90a09ceb74b617580dfa92d09d282f in / 
# Tue, 15 Nov 2022 01:42:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:42:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:499857e816a533a8819d6e1bd0f92e958be533067b7f23a182eab91b27bfef2c`  
		Last Modified: Tue, 15 Nov 2022 01:46:54 GMT  
		Size: 50.4 MB (50353260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2755ab5562bc9580880e37c88a2b99a0052915be6349a52bd1a5d7c093c0a586`  
		Last Modified: Tue, 15 Nov 2022 01:47:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:0e9f6b0a94fcd1186d4820bf1099c12faa3864c4a8fdc2b0fbcfbac079dabd00
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51345155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4747aea9e03777f4b82b87b971ca7d75ab6678cbdc9373d43b5597d173a127`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:43:16 GMT
ADD file:29b8a27f62c9f0ad0d3dc76bbea47baeb2928c02fd7c5be6293779715f8c3f4f in / 
# Tue, 15 Nov 2022 01:43:17 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:43:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f3d7727f0422cb9ead707b304859c1f0bb81f173a525802ee1f675fb3d3c0c68`  
		Last Modified: Tue, 15 Nov 2022 01:49:56 GMT  
		Size: 51.3 MB (51344933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa0337d9244a26865205e8ca3096691ec9f2940275fb9f06c38468734461cad`  
		Last Modified: Tue, 15 Nov 2022 01:50:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:366f244c043e592242d9ef71762cc7ef34a86b9c5b4151e3e9e88833cf1ec9c1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50314390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c46dbae2e4335512045bad238c071d8d142d2d317ce22e746666fd07e6aa5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:16:16 GMT
ADD file:0bf967c48413d797fcdce6409d58e3afd112d6c2c27143d282a889e30a368591 in / 
# Tue, 15 Nov 2022 04:16:21 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 04:16:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8bb5316c788baa715b2f0363e24207959c3fd829b827cee9a75842909be99f4d`  
		Last Modified: Tue, 15 Nov 2022 04:24:18 GMT  
		Size: 50.3 MB (50314165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d149068d80974f77977e97431635e969b20552f99850eca95a94b3de7e3158`  
		Last Modified: Tue, 15 Nov 2022 04:24:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:7ee3fe003c021425348daeccf242502c1e9ca531a1b7599664a2823946e56121
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55338954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07a04ffb30db62f97b9948132c41c34cde8bcbe0858c8537ab3a77f4dcaf889`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:17 GMT
ADD file:eb3294b440b1de7e5e420328a146136657392ed0568fcc54a574e171e31558a1 in / 
# Tue, 25 Oct 2022 03:15:20 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 03:15:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e78937113e3c6d6902831ab5c7cb1ac7b54dd956b0a882adb2b81160f0cd0833`  
		Last Modified: Tue, 25 Oct 2022 03:21:41 GMT  
		Size: 55.3 MB (55338729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4b811f6057e845be5e7ea7cc69391617926f6d6ba7e24914e26685e9cc4851`  
		Last Modified: Tue, 25 Oct 2022 03:21:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:cd18ff0841b626c48e0b3aabc83c9985c07d0eb9e2e7b83ac8c0d8a0cdac4f87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48707610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603726d4f99a3f14b8a3e1de830abb2aede3a26f85dd8f8d0be85fb25c048aa6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:44:11 GMT
ADD file:403c66034fd293d5edbcbe296c26995a9b30999f3da0a93f1fe90cc9017a29f6 in / 
# Tue, 15 Nov 2022 01:44:15 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 01:44:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8c10a082b604dee529dc8ed1c48821561d13eddefbaa728947aa2eedcefbe3ce`  
		Last Modified: Tue, 15 Nov 2022 01:48:43 GMT  
		Size: 48.7 MB (48707389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315abd68ab7f2a02843151e96042281cdd2f76278305274c3ab95b935b68d829`  
		Last Modified: Tue, 15 Nov 2022 01:48:50 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
