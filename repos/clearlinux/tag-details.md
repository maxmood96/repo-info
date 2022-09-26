<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clearlinux`

-	[`clearlinux:base`](#clearlinuxbase)
-	[`clearlinux:latest`](#clearlinuxlatest)

## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:f0eb4e03a261bec198664c7807d7bd59907dad4701ec76db8d6b224757ad24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:bea39763120dffab75a216da096433bb70e49e31a5b0e0cf0a75632a58d851d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68973043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d4d4e9c4a58e98e225388e7480df3d704797eacbc0c9d1a3b2da606cea7975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 26 Sep 2022 20:19:35 GMT
ADD file:ab40b7d4a6fc8c61818620a74f57c66f0e4d7ac61f1fed0115d12bfad9ae35ec in / 
# Mon, 26 Sep 2022 20:19:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 26 Sep 2022 20:19:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:85f056445156951c9fe2bbda7a5b73183f2a8de7fa46aaf1ea7746dfde56725d`  
		Last Modified: Mon, 26 Sep 2022 20:19:56 GMT  
		Size: 69.0 MB (68972826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513932d4f6d6f12a0d587b17911c9c45718cf122c687cd223085a91b4298a10b`  
		Last Modified: Mon, 26 Sep 2022 20:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clearlinux:latest`

```console
$ docker pull clearlinux@sha256:f0eb4e03a261bec198664c7807d7bd59907dad4701ec76db8d6b224757ad24b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clearlinux:latest` - linux; amd64

```console
$ docker pull clearlinux@sha256:bea39763120dffab75a216da096433bb70e49e31a5b0e0cf0a75632a58d851d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68973043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d4d4e9c4a58e98e225388e7480df3d704797eacbc0c9d1a3b2da606cea7975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Mar 2021 00:22:54 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Mon, 26 Sep 2022 20:19:35 GMT
ADD file:ab40b7d4a6fc8c61818620a74f57c66f0e4d7ac61f1fed0115d12bfad9ae35ec in / 
# Mon, 26 Sep 2022 20:19:36 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     grep root /usr/share/defaults/etc/shadow > /etc/shadow
# Mon, 26 Sep 2022 20:19:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:85f056445156951c9fe2bbda7a5b73183f2a8de7fa46aaf1ea7746dfde56725d`  
		Last Modified: Mon, 26 Sep 2022 20:19:56 GMT  
		Size: 69.0 MB (68972826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513932d4f6d6f12a0d587b17911c9c45718cf122c687cd223085a91b4298a10b`  
		Last Modified: Mon, 26 Sep 2022 20:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
