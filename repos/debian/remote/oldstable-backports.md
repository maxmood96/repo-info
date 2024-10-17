## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:8df885851fce20d6ce722c62feff39f7242039e65abd8d5dd9953466beea70e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:3a11906dc02aca0eb0d6d9b05c4a1256d9313aef7c678ced21bcca8414d2ed06
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55080862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2023418993ed777a978238914ca7bb5b09e11953f785b12082e3685cc4188`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:01 GMT
ADD file:8f3ee56a8d465cbde69dc2488a717f0af92d3576ba504baa9ecf4a44bceb0ba2 in / 
# Thu, 17 Oct 2024 00:21:01 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:21:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45b81c812f9140c27b65b7cef4ac4bef82357b8e87f35328ec1acc9d529a2f30`  
		Last Modified: Thu, 17 Oct 2024 00:24:52 GMT  
		Size: 55.1 MB (55080638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a28dc9a4dd00b97c702291ee98f32f6c5173b27fbb439382ecf4dffcddfbdb`  
		Last Modified: Thu, 17 Oct 2024 00:25:00 GMT  
		Size: 224.0 B  
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
$ docker pull debian@sha256:041f88daf094deb20486c6ea6260d208f49489f3cdc50614dbecfc1bc546d82d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56078045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4f7d6c6f2aa8ccc628c2c034e5a2224cf080a4c6be74a09946ef1c390b35b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:30 GMT
ADD file:55edb81e795f579b3a7e08f1359e6196988284f303649d34491783a36cebbba6 in / 
# Thu, 17 Oct 2024 00:39:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:39:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fef51032d42b4132aebafad5bbaea13516d3a06fc7af7490027b0d30eabb39e6`  
		Last Modified: Thu, 17 Oct 2024 00:43:35 GMT  
		Size: 56.1 MB (56077821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d705e81f52e8782208ebce1abf3934bbb6754451274852a873f89bbc60c4082`  
		Last Modified: Thu, 17 Oct 2024 00:43:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
