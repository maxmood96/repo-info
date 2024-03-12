## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:6e0ae366cc836adfd69a8fc9c58daa27bdaeb4e636cd900a62daeed66f6b1656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:9ea059862441652080eacced6532559f8d4ff1170a09ecdd04fdf49c6bdaf844
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50501027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908e08d9e2f45c3fb6b84c088a05a00c311670f74fea2d0354924f9c642f9a20`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:54 GMT
ADD file:da27aad08354e0083651b02bd70f02b99c2c85a8f9ca84980918f7c007bb549f in / 
# Tue, 12 Mar 2024 01:21:55 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:21:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c2169833c09ea513d2094969617db42ff49a77d6340bf792580125a780cae453`  
		Last Modified: Tue, 12 Mar 2024 01:27:16 GMT  
		Size: 50.5 MB (50500801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b13baada693eddf1c29f549792ccdb771f052dddee5a3d803d84e7ee1446ad`  
		Last Modified: Tue, 12 Mar 2024 01:27:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4b566a566e347efae729a4f7bcdff07cac6d65a982d63ae7b06e5b640ccbea49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45967519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b225d904d600e28bbc830837ba8813407795a7f8aea8ca2f33d3ea3be14ad69a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:00:05 GMT
ADD file:65143abb31e1fca9dd2afbeed0d22aa36ba011c3c2671395cb6e234c8bda4213 in / 
# Tue, 12 Mar 2024 01:00:07 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:00:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8089adf0a32633ec4df7c9bbee1ed346bd999b75f420e67853efc6d9e7474f6c`  
		Last Modified: Tue, 12 Mar 2024 01:05:27 GMT  
		Size: 46.0 MB (45967293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e446e19dc9807741ea08ed6357519694fc7d4c4b3c99e7a08632e86ba1165294`  
		Last Modified: Tue, 12 Mar 2024 01:05:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ca2da33e10effcde9208653fad2a9b25bece8c0cb37432a338bfa6110c3c95aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49290054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8807ac34856a5c9aec8840e68b4f83df8ad1152178e2fe30050ad080dba869a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:12 GMT
ADD file:f0b12e194a395367a9c2aec5a874f1d159f595ed472e6c479464819b8185861d in / 
# Tue, 12 Mar 2024 00:46:13 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:46:15 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:93410cb9dfd8b96d6538b6847b0b6309196d4ea4108c683af28b8778a98f204b`  
		Last Modified: Tue, 12 Mar 2024 00:50:26 GMT  
		Size: 49.3 MB (49289828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164dcd3ea8940e9fe1f6b72037316e0c3cc9d0ed7b11ffab9f5b7262d48d93b`  
		Last Modified: Tue, 12 Mar 2024 00:50:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:3c7b69a0dd5c65702a88f7c9883586e0a1b35d7f975d02534545ceefb89bc12c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdd059b1fdbf899c6e31f4c12a087636c63930b6c9bca4eab1086fa35c19ceb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:56 GMT
ADD file:232fb10972beb7a1749f5b49cf5b4efb9147e32fe8b4b76e4933b714eab78950 in / 
# Tue, 12 Mar 2024 00:58:56 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:59:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6435306e5407f23561b349debe2766afa345b2f9b0f2ca20b8437bb6e1353265`  
		Last Modified: Tue, 12 Mar 2024 01:04:36 GMT  
		Size: 51.3 MB (51255578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1e534c8bb5d2d21ac0a9a3eb1e3950a7c221173d85e336b1fcdb8544043202`  
		Last Modified: Tue, 12 Mar 2024 01:04:45 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
