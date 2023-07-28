## `debian:buster-backports`

```console
$ docker pull debian@sha256:a44d00c25f7d3680dde400ec87987b5dc1af38491e79710f1dc6bf025a4b54f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:f3e8e0246128e168ab920c41a1deeacfb43ecc4042f440dc44b62565cf114d98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50498218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3041f3132cbf399a5ecebf3553b74f4601808c0f9b2a4758828c53b8d7e8c6d4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:17 GMT
ADD file:46b31c893ada083f38702e21d80e5ea4b674cbc78bddd3d80020d7b8e8beb467 in / 
# Thu, 27 Jul 2023 23:25:18 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:25:21 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9918064ebccea7fc961fe71dad46105b217763b4b1b3a9dfa7bee2ab29d2039b`  
		Last Modified: Thu, 27 Jul 2023 23:30:27 GMT  
		Size: 50.5 MB (50497996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1adb90102c9953be6d13fd7052c8a1f97cdbc8b47220306166c2ca8614b0b73`  
		Last Modified: Thu, 27 Jul 2023 23:30:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4d606d81710f8ef27a5dcb3794b131baa42a2528f8ab6d4b1d3eb40266e88390
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dff89de3aafd2eebc3d90f50a53a2fd93d84e04ee0cf7cf9d509f11f8665a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:31 GMT
ADD file:234aa079d01de7f7d69cc8831073e3937debd44f772b3a29bbc3d9cac070812c in / 
# Thu, 27 Jul 2023 23:58:31 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:58:36 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3d63dc62bf43740491cd4bcda82a28e35ed3655623dd102a9fd80eec2889986c`  
		Last Modified: Fri, 28 Jul 2023 00:04:15 GMT  
		Size: 46.0 MB (45966204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0266e129b27d30b18f1c8aba9b6f8de99bab2d24d17b065f6e8e4a8d71a925`  
		Last Modified: Fri, 28 Jul 2023 00:04:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b453432ee281e0235c5f6963f5fc0db7db3a31180a426726353ba4dc89feab96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49291121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cefbf485b02b52f9897dcf04cd0830f84f2017b7d1957b3de9d9d4262c5f73f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:21 GMT
ADD file:7472c3a6e583fa549b0fdf510b32407a4ed40f255a30199cdd2c5fb367794d45 in / 
# Thu, 27 Jul 2023 23:43:21 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:43:24 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:89b61c8397133d3e1d24ef0453eec8370033046cc0fc0854b595eb1e3c6d73e7`  
		Last Modified: Thu, 27 Jul 2023 23:47:32 GMT  
		Size: 49.3 MB (49290895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac6ad18f3a5f5f5ed25ec5a88de53def4d0095a4b0683dcaf0d7cbd2b117db0`  
		Last Modified: Thu, 27 Jul 2023 23:47:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:57c5973a4af6d7f7062c983d7392ca29f75fd50a3dd944821e940d97f24c2716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5edde7a388358c410bc3ba820fb8c34a873223db61a48832bafebce9916800`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:29 GMT
ADD file:a4caa39d69b463e1f2628cb32f33763655fd873129cf98dd26c431183c53b6d6 in / 
# Thu, 27 Jul 2023 23:39:29 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:39:31 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4b5eb5e3691ae17e5aaa83c175523a7a17d58c9c61698ed6bba826d9acc809ec`  
		Last Modified: Thu, 27 Jul 2023 23:44:34 GMT  
		Size: 51.3 MB (51255427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe25337926828ef30fa3b5ab085618292d61b428aadf63160afcde8cf0bc928`  
		Last Modified: Thu, 27 Jul 2023 23:44:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
