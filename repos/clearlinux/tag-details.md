<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:f6314b68ababc9f1a1806a7a1c9fe41ddb968dc3552479920313b38d4ca79914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:4deeee5a323e5c2aaa5a6acc761b013a33b40b642360577bf4c49dce6056aa33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67702470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29da3a70257d6858d703f546d448b9d308daea6a24b30b9d22b258a38ae8860c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 18 Sep 2023 19:19:49 GMT
ADD file:20875d4924ce9b5a32d13639b0274931797aef70cb5e6d6bd27aa8627ab49e7b in / 
# Mon, 18 Sep 2023 19:19:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 18 Sep 2023 19:19:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1af81335be5c946622626982d5fbde68f4c93359b12dd643b16080c73b7cdd90`  
		Last Modified: Mon, 18 Sep 2023 19:20:07 GMT  
		Size: 67.7 MB (67702252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfc8d805b80d3848b88a46e679bbf0a8636244c8950c57210e2e71300405da3`  
		Last Modified: Mon, 18 Sep 2023 19:19:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:f6314b68ababc9f1a1806a7a1c9fe41ddb968dc3552479920313b38d4ca79914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:4deeee5a323e5c2aaa5a6acc761b013a33b40b642360577bf4c49dce6056aa33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67702470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29da3a70257d6858d703f546d448b9d308daea6a24b30b9d22b258a38ae8860c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 18 Sep 2023 19:19:49 GMT
ADD file:20875d4924ce9b5a32d13639b0274931797aef70cb5e6d6bd27aa8627ab49e7b in / 
# Mon, 18 Sep 2023 19:19:50 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 18 Sep 2023 19:19:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1af81335be5c946622626982d5fbde68f4c93359b12dd643b16080c73b7cdd90`  
		Last Modified: Mon, 18 Sep 2023 19:20:07 GMT  
		Size: 67.7 MB (67702252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfc8d805b80d3848b88a46e679bbf0a8636244c8950c57210e2e71300405da3`  
		Last Modified: Mon, 18 Sep 2023 19:19:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
