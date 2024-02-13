<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:d6c291efe0ba183a08cb30a4c700b4418113898bea6bcfe9aa4f96b2378593a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:4cde873a9a48237f697d99188a43399b3e582c46d9361f9baf970c87809f17d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16eebb474f362b8b8a759da372c705ee8cd4b772ff486bb9f844db3e60493e75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 12 Feb 2024 20:34:42 GMT
ADD file:2c65fb1e2a47eb5d679feacf35ab3151cca48174d7d618f4e29390d5513233b2 in / 
# Mon, 12 Feb 2024 20:34:43 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 12 Feb 2024 20:34:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8ee6ab1c5d74c8077893294139a6ebded6b0d2089226a6805da535bd64b4b124`  
		Last Modified: Mon, 12 Feb 2024 20:34:59 GMT  
		Size: 64.1 MB (64146634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe1fac073b590ee3a7bb5fcd99d4eb568bc49a284ff2dbe3cca73939a1b8004`  
		Last Modified: Mon, 12 Feb 2024 20:34:51 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:d6c291efe0ba183a08cb30a4c700b4418113898bea6bcfe9aa4f96b2378593a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:4cde873a9a48237f697d99188a43399b3e582c46d9361f9baf970c87809f17d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16eebb474f362b8b8a759da372c705ee8cd4b772ff486bb9f844db3e60493e75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 12 Feb 2024 20:34:42 GMT
ADD file:2c65fb1e2a47eb5d679feacf35ab3151cca48174d7d618f4e29390d5513233b2 in / 
# Mon, 12 Feb 2024 20:34:43 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow
# Mon, 12 Feb 2024 20:34:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8ee6ab1c5d74c8077893294139a6ebded6b0d2089226a6805da535bd64b4b124`  
		Last Modified: Mon, 12 Feb 2024 20:34:59 GMT  
		Size: 64.1 MB (64146634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe1fac073b590ee3a7bb5fcd99d4eb568bc49a284ff2dbe3cca73939a1b8004`  
		Last Modified: Mon, 12 Feb 2024 20:34:51 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
