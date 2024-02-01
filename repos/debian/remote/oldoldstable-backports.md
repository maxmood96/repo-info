## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:813ce79e3bb66a1dbed437da4e275e9b6ed7b543f4c7ab7ca583cd67936a7516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:112b14bd25d529b526637095d8d29201b9717e409be04cc1df1a0479ca1f42ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50500950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdbce11fc26b1a46b70b82e60a266207e12b0145ceeb6b80e697770b5603e8c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:13 GMT
ADD file:f518aa0791f5c77eb628e419c73b0c1367b32acc18ed1efda669cf4794636251 in / 
# Wed, 31 Jan 2024 22:36:13 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:36:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb6e0306ca19c88b6a71b5fc26295c41ed73074b99608476462b30da9701483d`  
		Last Modified: Wed, 31 Jan 2024 22:41:50 GMT  
		Size: 50.5 MB (50500724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b723631970bf6b95791681fe579ab159fd0a6eb4d124daf2fb6b7a95f41db3`  
		Last Modified: Wed, 31 Jan 2024 22:41:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:737172a41c56c33bd51b7eefbb42eaee5a5eabf6d6dd7879d82f5adccf092a4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bdb7c5a7c146fc6f28e75107efcbd600e35b5ab3712c3872faeb8b65817f5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:14 GMT
ADD file:73e89a632e3aee443f64108378c8c2ec3f311a468d4ace72f0a057b85175934e in / 
# Wed, 31 Jan 2024 22:45:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:45:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:229c6d554defd31a672ae172d451123d40422945e673445aee5ec75150c5c889`  
		Last Modified: Wed, 31 Jan 2024 22:50:40 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c366e6264be28f766c59e604d62aa1623552375f1fa1ca28a902faebae916d`  
		Last Modified: Wed, 31 Jan 2024 22:50:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ba8ce05bcaf00b1b6fce8ac8d1705400f396fac30cea69dc5863ad7ffa7fcb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49289779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1b01033cfddd74a32bff8319b936d8089dc31dd909e50b653a3ed2d63183be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:04 GMT
ADD file:2d605c7598a4e5016f8a7683240d469ad2bb31a6e2836696eec0a96356866596 in / 
# Wed, 31 Jan 2024 22:45:04 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:45:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76279046f344f5a667060aa92ddff76b47e29d71c120021251feb5ab9a8561d0`  
		Last Modified: Wed, 31 Jan 2024 22:49:54 GMT  
		Size: 49.3 MB (49289553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd747b7f7e58f9c246a3e167c7f5929e6c35660460940fdc85b001c9d50e2f`  
		Last Modified: Wed, 31 Jan 2024 22:50:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:74a29a86de80ac27f23bdb56ef45413f2e68a3c84c73b460222a5d0814707dcc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2661a1c3495b3c3b0d71eca7b47fe6f9bb9efa806318acbd23b56e2431135103`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:55 GMT
ADD file:c1e0513d2c6a754023445dda9e3ae58295f157419d61aecfcab69c26b7ecb238 in / 
# Wed, 31 Jan 2024 22:39:55 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:39:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e160489fa50f178536afdac33c4608bd3bf06838b3bbbbec70501cca589a4300`  
		Last Modified: Wed, 31 Jan 2024 22:45:49 GMT  
		Size: 51.3 MB (51255234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bb0356d2c7367e0a66a638f82380b7f1b6ce03e69a17433ed66956eba1f086`  
		Last Modified: Wed, 31 Jan 2024 22:45:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
