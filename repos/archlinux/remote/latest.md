## `archlinux:latest`

```console
$ docker pull archlinux@sha256:58fd363480dc61d0c657768605bca3c87d5b697cb8c2fe0217aad941c6a8a508
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e6e48cdbca990bddabe31dccc340d3989cb6951380e3aa69b350e246a8f489c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152724049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d45be0b24be4f044711c0033fe7ee2265ea357134c82c2e4311ad1672eafb7c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241222.0.291122
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-12-22T00:07:56+00:00
# Sun, 22 Dec 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241222.0.291122' /etc/os-release # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 22 Dec 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7150b2dfc4ac7f06e85313fa003b954d50d19dcb209af67a1b1e297ea0ec9085`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 152.7 MB (152715741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f6c0877756d57f5161544f13a5dd64e5653d5afa08880d6f8d0effaa659611`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 8.3 KB (8308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:284a09242e8ec48d05dbff4dfc1890d630d90749612b03079aecb3a09c64bf71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8087855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a089c590b6f05127ecff19707c673f5aa2e90fbae31d3c640e0ab99caf0baa8e`

```dockerfile
```

-	Layers:
	-	`sha256:af334dbbff0b5b9d2938efda66c9b20e1758b4f2cb1b121af3352ac80ac54c7e`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 8.1 MB (8075883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e111e40a728d2de21b287174abf303769fc7f548488d84eb6e1bc59c8cf4a63`  
		Last Modified: Tue, 24 Dec 2024 21:32:41 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
