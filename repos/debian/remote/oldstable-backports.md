## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:7d0bde0771c47d2af9179490810fb3c117e9ab392ddad39276f838aa588576ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:72f92eecf81ae4c9d2c5f5bd0b7aa8dc5850701d2dea2d40150c61389d19a17e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d205b946a3a93480aadeeed34961a8f933b794f45336bdd6e7d3465d13d61bc2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:05 GMT
ADD file:9702ad73a9bdf05a3bfb1fdf00f4add7fe7d6423d816ea5736dc09c38571271e in / 
# Fri, 27 Sep 2024 04:30:06 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:30:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f25ed91b431651611133faee8034e0ff11333b8a3908f9c394e5eb7238a5d39`  
		Last Modified: Fri, 27 Sep 2024 04:34:07 GMT  
		Size: 55.1 MB (55081407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6577420bff5c6a4799ad60fabd1f888d644fb973c7bad7264aa062d8eb121b2`  
		Last Modified: Fri, 27 Sep 2024 04:34:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c1580383c1cf837ba5e240db1ba6a12b2d7a2b556411bb2154b483d3a98038de
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa71906ff756e3d2451e101bfd3323ff1a588029747a6590c1ce4f062696be5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:19 GMT
ADD file:bd0ed9cfc8e36589dbc245c580d4ffd634242bf14dffce7f811a3f97d60cb9f5 in / 
# Fri, 27 Sep 2024 05:14:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:14:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cbbc28287ddad776e3abdde94b49b7bc2afd4b03464c39bc1fd15508f1dbd6d6`  
		Last Modified: Fri, 27 Sep 2024 05:18:08 GMT  
		Size: 50.2 MB (50240384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a72b675927e6f63ce14fb7a309f8075a8dc392ea679296a6dfe137108ff300`  
		Last Modified: Fri, 27 Sep 2024 05:18:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4efa10feb56f76b32217bff214d705f2ca91a78e04b651e4c2d560529302b50b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53734068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaceb8d2077aa0611b7404ba0e8bf0724242a0fa73e6ba48c0e245883947ab6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:39 GMT
ADD file:dbceb67a4459d0f5870a40e38032da74fb1fd32243f3301f930ad8775661d894 in / 
# Fri, 27 Sep 2024 04:38:40 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:38:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:423f448f6c5029ccef4300fc9d14c8304a116615c4b5daf9470abe27f958cdab`  
		Last Modified: Fri, 27 Sep 2024 04:41:43 GMT  
		Size: 53.7 MB (53733847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c107c797ae49b0c9fd8478156100a74a82d035616f55af91fc5faca566522f44`  
		Last Modified: Fri, 27 Sep 2024 04:41:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:24b86377f3e011cb6971fa8deac9481144b5fb417cd1fc5ff0da1fe02d6697cb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723470b374f9cf55ced7d335502bbdf53f4eb2f66d7e0773898e48d510e02af2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:35 GMT
ADD file:0c161c5f0b49c8a337199fe0f7d5ce2d91b5b956d2c3d59616bbf3324dfdc73b in / 
# Fri, 27 Sep 2024 07:23:36 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:23:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b669acf6c5f0e73bc4af9bc4afd7a640c17cc1c04178ea190da45e9c525afa7a`  
		Last Modified: Fri, 27 Sep 2024 07:28:11 GMT  
		Size: 56.1 MB (56076521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f6cca54b669dd298effb2652a169fe592470c60a881adcb8586995d46a87a5`  
		Last Modified: Fri, 27 Sep 2024 07:28:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
