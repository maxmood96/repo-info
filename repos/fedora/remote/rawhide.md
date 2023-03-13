## `fedora:rawhide`

```console
$ docker pull fedora@sha256:97f095c0794737b1cda571adc6d4b794c0449b6a4f836b4c632ca064ebe7569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:d09662d6ba85fef498c641a8307ea948b0d26a755fadc8b72bd63cf28bd2ed80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67494255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb301b374251a99a16d3752ef152222ca35e4a5b321403ccde7726e783884d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 22 Feb 2023 18:23:48 GMT
ADD file:f0d15beab7354c02bbc8f6e0d01550c9ed26603e80cd6a25cd67856f63b8b35a in / 
# Wed, 22 Feb 2023 18:23:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:260cc00e3ee427105c1dc7a6d0e6cc23deb2854b5d1a8fee48f60b446bc10955`  
		Last Modified: Wed, 22 Feb 2023 18:24:44 GMT  
		Size: 67.5 MB (67494255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:a3b60051e90e137894d98a6c17a14c494fff5416ac90395cd80a04eb652c8ff2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67097464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2163c8c14f4a2401ceb29aff9a32936650674b0ac602c21db6529a859365e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:39:50 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Mon, 13 Mar 2023 20:39:54 GMT
ADD file:b79560da0658c2ad81a7da33589db60bf43e0451cb41b876c130061fea5f4f70 in / 
# Mon, 13 Mar 2023 20:39:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c91e95a07b9f5226cc89e04e3bc3abf4367a4bd299948672c8300af0afd6c4f6`  
		Last Modified: Mon, 13 Mar 2023 20:40:57 GMT  
		Size: 67.1 MB (67097464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:265583b7bea060688b41105d4480ac34f719b6a0c3a103049b6904936f47b689
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74230988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7533ac2cf60ea2ad1f7aa391464474e2dc24efa75cd5c9d5f04167d2900d9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 22 Feb 2023 18:21:31 GMT
ADD file:0708c77e5ae2211ab58a06d2206219f84bffff4f008b2f101e33ea7059e32e57 in / 
# Wed, 22 Feb 2023 18:21:35 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e9600fee99bd6ee3645d26d458edbf1266e2798215022b8ca176ab5289e6b67f`  
		Last Modified: Wed, 22 Feb 2023 18:23:05 GMT  
		Size: 74.2 MB (74230988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:00a6ffa46b060204ea7bb5e2c694f64db869e9c22b97ab19a4b2b662fc1bede0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68996332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ed16f3b3c4a06ebb23fc1134f71da802a3c4bfe3d9765d263ddc2e508e74d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:43:12 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Mon, 13 Mar 2023 20:43:16 GMT
ADD file:ba6865fcd8d3da01d4c4bdde7bbf23566ab06293a5c8a032ea3a55f4312aecd7 in / 
# Mon, 13 Mar 2023 20:43:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b99e3c9872466bb30081769f0d3f0a919a8f7123c7027c82146858713c7eb646`  
		Last Modified: Mon, 13 Mar 2023 20:44:29 GMT  
		Size: 69.0 MB (68996332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
