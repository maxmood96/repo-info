## `debian:buster-backports`

```console
$ docker pull debian@sha256:338dc6e6f6f1cc38ae7e7f3dd6e52c56bbe768df7b4a95680d0c1d3f633e0677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:c97176e853afb74ecc2266b2908c8b6d14075f834e15d31c576d1400e516bc04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a4d6a4d8be9c010de70c8ba68b5f489b2c8f1b84d04aadbbbf86a75b24f0e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:09 GMT
ADD file:9ea7d74fdfdb29946ab72e1aea5810331debe27db7e50a0fc4e0d5a192ab6166 in / 
# Wed, 01 Mar 2023 04:10:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:10:13 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d8a6bce2a40cb0c3e3cc6646bfeccfb2ac5b303c39ea70d67e30406d270f2009`  
		Last Modified: Wed, 01 Mar 2023 04:14:42 GMT  
		Size: 50.4 MB (50449101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677475448416d3e70baa61558566cc4f68798fa4d84afd1d977b6ea0cbfc00b3`  
		Last Modified: Wed, 01 Mar 2023 04:14:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:eeae0d3db925fd25c87c8c1bc32c7e5b9ed770dc3c2c3edc1af3d158ff83f57f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67921a291ec60d425185d46864747730d814c5580f87c17efa9de4d5ce9aedf1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:03 GMT
ADD file:28e7414281fcd12661d43cccdf7062bf4aa15641f986cae3aa3260fcb8e16bb5 in / 
# Wed, 01 Mar 2023 01:58:03 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:58:07 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4ba30d485dd0583b3079a70184a97c458599a0629e661b1382394653cb802242`  
		Last Modified: Wed, 01 Mar 2023 02:03:25 GMT  
		Size: 45.9 MB (45916077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c6c7f0b1a5a34ab09103b36d3b463539941e1efb36f145736389f21db4b407`  
		Last Modified: Wed, 01 Mar 2023 02:03:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:20dd7e5f81dfcb2fb69b737dc38bb7bf201cf5f559d49e04de03ced3fa51c810
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49240226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2445dd0a377ca3c14ed74b63c82abb61d2355e519bf137487704376243d4606f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:20:50 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b4100b4f3a54ce87f23cd172b3bea3362fbad39a63c7056762de6c95ab6a53`  
		Last Modified: Wed, 01 Mar 2023 02:24:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:af29fa680a43f55b344d2a89759ff7bf8c94e4b2b0c8c68592a3ff7b976faad2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e7721c696dc28737a8cf24ecdf0d90f38b1d03c359ed5deef6d99bd814596b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:23 GMT
ADD file:4a87d706ba1c6cdeab729abca0c932709611862dfdf5d46d9f07660a549fd043 in / 
# Wed, 01 Mar 2023 01:39:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:39:28 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:965c7d391035444250e8549e1aa77d80a0692089e844b5c3d6f4e4924f096a99`  
		Last Modified: Wed, 01 Mar 2023 01:45:08 GMT  
		Size: 51.2 MB (51207396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939f8486e8e5fe4510f15bae40896c76e6bdc1f22d6a7e0cdf8b3974dcb7afb`  
		Last Modified: Wed, 01 Mar 2023 01:45:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
