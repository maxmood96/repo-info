<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:4b17818baa31c48b37d9a2d556e335ed693f8478bd0a3889e2e5ffc145ffaad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:d59cfcc7fc791a812d83ffb7ab4da3207ba7a6f8c7185cb91b672d966759280f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96648639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab635ae245988a50f76dfc6af761dffbd41858eb5a9b53cf11225889ac11572`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 15 Aug 2022 17:23:10 GMT
ADD file:d4074aa9e8f901366f485e1980769eef1363f148a111d80bb2623704ed74f021 in / 
# Mon, 15 Aug 2022 17:23:11 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 15 Aug 2022 17:23:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a966fd2ca4530801f2d40ede9fb26a8dcf77b0475aeca71f40285e3bf4fbdeb`  
		Last Modified: Mon, 15 Aug 2022 17:23:36 GMT  
		Size: 96.6 MB (96648422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f321d5715d0bc75ea6480ecd6ff6b531ce99b2e07ad9473c762730d0c677a`  
		Last Modified: Mon, 15 Aug 2022 17:23:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:4b17818baa31c48b37d9a2d556e335ed693f8478bd0a3889e2e5ffc145ffaad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:d59cfcc7fc791a812d83ffb7ab4da3207ba7a6f8c7185cb91b672d966759280f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96648639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab635ae245988a50f76dfc6af761dffbd41858eb5a9b53cf11225889ac11572`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 15 Aug 2022 17:23:10 GMT
ADD file:d4074aa9e8f901366f485e1980769eef1363f148a111d80bb2623704ed74f021 in / 
# Mon, 15 Aug 2022 17:23:11 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 15 Aug 2022 17:23:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a966fd2ca4530801f2d40ede9fb26a8dcf77b0475aeca71f40285e3bf4fbdeb`  
		Last Modified: Mon, 15 Aug 2022 17:23:36 GMT  
		Size: 96.6 MB (96648422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f321d5715d0bc75ea6480ecd6ff6b531ce99b2e07ad9473c762730d0c677a`  
		Last Modified: Mon, 15 Aug 2022 17:23:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
