## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:39b9ff8523d7f0d652f8b155968e52eba17ffbc8cb9f53c2b810e5b4cd39039c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6c5c0c4a833c46b9b5ddcb482eef88635250f24d012b5939dbcf05549690045c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272518295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cec44a713cc07615d3666d038c0634c4b9a8ed17eae181417b54e69f0e6457c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.version=20241201.0.284684
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.created=2024-12-01T00:07:55+00:00
# Sun, 01 Dec 2024 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241201.0.284684' /etc/os-release # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 01 Dec 2024 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:447fa0c2d9a0915f5b9414e2bc17f366afc9fb0a3280b4e20729471c6b0d7b69`  
		Last Modified: Mon, 02 Dec 2024 20:24:56 GMT  
		Size: 272.5 MB (272509211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f39869530ba41899d092435e7a3512c797f8f92f760d2a5dd1a49409273d55`  
		Last Modified: Mon, 02 Dec 2024 20:24:50 GMT  
		Size: 9.1 KB (9084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0159e907ee9fa393b4c5371177e93d102fe8634799b508f85b7f41ac9cc21795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527fff2b6a6ac438af00aba56b6fcee8ef8abbf85d80bbc6b46747e2ec868d4`

```dockerfile
```

-	Layers:
	-	`sha256:93058253ef010c77395ffabfa35e0e7e41eb8ea5d8fad30d0c7a4a84fa42e351`  
		Last Modified: Mon, 02 Dec 2024 20:24:51 GMT  
		Size: 11.9 MB (11896380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8eac43fb0af2ddb48c958e7a43ef436174af91884efa80599e28427ff483993`  
		Last Modified: Mon, 02 Dec 2024 20:24:50 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
