## `fedora:latest`

```console
$ docker pull fedora@sha256:a1347432284b0361f472ebc7c00874cf084e93bc2d9c78fe19f9840da9514789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:5338b5f562faa57f365ed978d384b3d334e6146ecd24867ab9b27d5f96c5deff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68302915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6126bb20b2b5afafd50ce8c42b8d48891ca19517ffc0b1d4396ffe6ad2eb330e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Wed, 21 Jun 2023 00:15:38 GMT
ADD file:60de36361209c75bed38814f7c155f63354606368986c85bd103b47202c2d84c in / 
# Wed, 21 Jun 2023 00:15:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49281dc4aaa45434f7feec6fced1103b97a657809858f8501bf589e4088f943e`  
		Last Modified: Wed, 21 Jun 2023 00:16:24 GMT  
		Size: 68.3 MB (68302915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:4fc1ddfb4c01afd5dbd1e34b554157235e14184adbed6222723700375b4d8649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67057126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba921a5e918410083549a2142da0ec063c6f1341db73b0901aaa392dcfd59d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 20 Jun 2023 22:41:00 GMT
ADD file:e1af2d14efd2bc54300585fa1ae9b7bf845e8d6a948db0ed61aa8c826a929305 in / 
# Tue, 20 Jun 2023 22:41:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9887f655ffe6443a8674e4433950b274e2a8b7265069a444db775d293cf74da`  
		Last Modified: Tue, 20 Jun 2023 22:41:40 GMT  
		Size: 67.1 MB (67057126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:3ba6705122b0f215ad2ca08834deb2ff7b353f7a6b2ecca3d7a9ac5373dbbbfa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75044114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071bc60d34cba21fb7a0be08f3a46c9388fb4c278e375a7e5e31809ade8666e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 20 Jun 2023 23:42:21 GMT
ADD file:b6a2aef5ebcdac31e39f71ce3d6bb2759b88914147e3bd96a8e1d33236256dc4 in / 
# Tue, 20 Jun 2023 23:42:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed57ba46d01965dded3e94fe3372c12a3907215059d57e4aa8ffdca8aac9ae49`  
		Last Modified: Tue, 20 Jun 2023 23:43:52 GMT  
		Size: 75.0 MB (75044114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:b766297005dfc4fa7b222386089601421c65bbd4af28203d6427a80cc3137a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68880144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4282604cdc90b4fb52329ce3dee4ceb3749dbd15ab590359e821a958dabe42d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 20 Jun 2023 22:43:13 GMT
ADD file:ca7ca36c3ae04ec89859c84588cf8c9c06ec3360cb66d180de209649826d7f5d in / 
# Tue, 20 Jun 2023 22:43:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8daeecf2a7f8b1e288ef0ba871a4a34acf6b97f092e964b48466bee3d8b924f6`  
		Last Modified: Tue, 20 Jun 2023 22:44:23 GMT  
		Size: 68.9 MB (68880144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
