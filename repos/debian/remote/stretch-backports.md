## `debian:stretch-backports`

```console
$ docker pull debian@sha256:e749847b42c8abe1ceff17be82e5076195a9deb138ca80dcecc63175f22c97da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:0aecb2b76aab34cd1629a2be570420223d91c9035d1bff2fdaf6b09c3081e977
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b5d8bcfb7c46c8a418977ef33be8c1ebdba75d842b79c71410188555333c85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:23:20 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1617c889aa992572bd78afef99cfd31f21fed8eb6ecb4f89819b1aedd5a34cb`  
		Last Modified: Tue, 09 Feb 2021 02:29:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:0ce5c329f71fbbef0665c3224dbf6cee541660bb400233cbc2506e2d5027664d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44091763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9172b2084237e619c92627a453ee8267489a8925a33db4d9aa107b0a41d1830`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:54:21 GMT
ADD file:4a3e3822cf3025351ee745e9adfe582c57bf68032749bb1f77594e37892e9976 in / 
# Tue, 09 Feb 2021 02:54:22 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:54:31 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:824fd5bfbc8362cd95df386c15b08b44f2ffd373830fe89693ee02957cc452d1`  
		Last Modified: Tue, 09 Feb 2021 03:02:51 GMT  
		Size: 44.1 MB (44091538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f80b9097e1c7925d19d4a73aea025f33f521d8e92e995bd870cb5f41ebcd5a`  
		Last Modified: Tue, 09 Feb 2021 03:03:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:577ed44f9c3736a0e1daaca5073b4a247ebee53d0a0bdd4e04d472f53694a687
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f00574da67b828d787a145c81d686167f5d6447c084c13153eb8cde005aab8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:04:53 GMT
ADD file:f884b9fc23d1b8ad0bd21aa823afd0ee186bdebb6829ccba72f77caaeffd8d12 in / 
# Tue, 09 Feb 2021 03:04:55 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:05:03 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5275c778c803ce7d82407c77cfad4fb07fd1ec80fc99ba94cef475a92e4d090c`  
		Last Modified: Tue, 09 Feb 2021 03:13:25 GMT  
		Size: 42.1 MB (42119892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e975dda9f08c6b12aed767fdd86e74d6233a5bfb40b4c4273b108c8f93b2c3`  
		Last Modified: Tue, 09 Feb 2021 03:13:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:81441acc7bd9d630435a87baad01dd8bc53e980dc3b5be2d0279e01bee467bb4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08e35bffa102bbd53226bcbc1439132ecb9a3ec26428c56f32c9bc42e71a361`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:17 GMT
ADD file:fb69ff7b2a28f793efbd16e04b74ffb4557d39e1844b3789075b4d3ff97a0eaa in / 
# Tue, 09 Feb 2021 02:43:20 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:43:27 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:296c9f0bf5f2cf24e87bc5abd674fc486e8df419d4aa2d362453f64d38900504`  
		Last Modified: Tue, 09 Feb 2021 02:49:43 GMT  
		Size: 43.2 MB (43177550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af72abcf3b781c45d0690d38155d9c1d0afa301e54d379f2ad0ad9ae44d1ea0`  
		Last Modified: Tue, 09 Feb 2021 02:49:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:ed9be763ecce409afe0a7f2ed5d3d4006ac9063e1e0e2b7ea92741fda0a2f923
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd00cf8693c18cef3443c84d872eeefc4937ff7de829c046605207093fa87a29`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:08 GMT
ADD file:4c25bc56152d0955bbdef26f612b172a90484913cbd1ab3332b3444c8c0c012e in / 
# Tue, 09 Feb 2021 02:42:09 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:42:14 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d7d8e56e51b8663a269c93107dcdf848d2f6a4f73ca51bb1ced208a1fa80c32`  
		Last Modified: Tue, 09 Feb 2021 02:49:23 GMT  
		Size: 46.1 MB (46097671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12e2c3985be81d30a9b6c45f5174638b8e72d120ec50949317920ea5c7397b0`  
		Last Modified: Tue, 09 Feb 2021 02:49:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
