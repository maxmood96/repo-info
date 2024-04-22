## `fedora:latest`

```console
$ docker pull fedora@sha256:5045ac20dad29edb7ebd98dffdbadc8e0af6f2feec62ec3d2066251f0b25a54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:830a6bcb5c9b30bfa77479b747a904bed02151e9de7ceeb8a1d117b574571fa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64614010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f878605acd6f24f3f11e4085544caf61b046378b31d6b3aa0677a7a3dbe0a17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:20:05 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 20 Feb 2024 23:21:04 GMT
ADD file:cdbc7eeb8f0a474970be6c866f99789fb8be4d72874e68cf75461403c8c2651e in / 
# Tue, 20 Feb 2024 23:21:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:353b74d8db1cf655e87c780b9ac49f52ed72dfaa3ecc4bb0e9245e72c98a45b5`  
		Last Modified: Tue, 20 Feb 2024 23:22:06 GMT  
		Size: 64.6 MB (64614010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:79c6d37cfa65044246e2b7a42e6ac47a71b498c6aaf79ef18ce27b8f1912b1c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79367012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d6fb7e34f429aff9b43a21cb73fa4dbae594ba953bd9fce4ac032a52560e66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 18:40:13 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 17:40:15 GMT
ADD file:1bf0fdbfbbeb01d9eed9abaaae9674d9776bdb82bd19adc6749241584eae7668 in / 
# Mon, 22 Apr 2024 17:40:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a7f8330e54b855763da0bc8407ecf81fc62c1dd60505d287531b3137e8d45a8`  
		Last Modified: Mon, 22 Apr 2024 17:41:17 GMT  
		Size: 79.4 MB (79367012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:31ada6630c60b0490b1c0c58d35cbd86c5f37a0bb386b2ed8375fa7a88d25d90
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71270715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812bf49f6c7ae7fb39faff0cf47d1d1d431845ee548ecd93da6dcb8680ad2d2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:18:04 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 20 Feb 2024 23:16:54 GMT
ADD file:3a03036a8b4dc61fc94f3e81bb11a30ed95eae1210a8e79b5bc1b6ad6e818981 in / 
# Tue, 20 Feb 2024 23:17:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7ffa12982fec21fc386c2cf79e61ccdc6344da79bbb8210fdb7b2c38c1aea1f5`  
		Last Modified: Tue, 20 Feb 2024 23:18:19 GMT  
		Size: 71.3 MB (71270715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:27a37ecf220ba9e504774f9d8ae261fd0f081cdfaa46ad73f8b0af4805c8b3ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65157283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c87e1a3e27e7ac4d1973b70e6eff561ffe8ccc02f7a64165ae8a7f615b2f683`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:43:12 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 20 Feb 2024 23:59:06 GMT
ADD file:cddc4a1c7cd44f6ccc70e15259bdcc1823807d940c41ed36babd8efe849da9f6 in / 
# Tue, 20 Feb 2024 23:59:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a46dda40509b26159a2954f418c75d9b2c5ed6692461e99f38eb84948fde5d85`  
		Last Modified: Wed, 21 Feb 2024 00:03:31 GMT  
		Size: 65.2 MB (65157283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
