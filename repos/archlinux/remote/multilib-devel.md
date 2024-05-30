## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:ad0fb9c2da48cbb7c38ec278819fa6c0ccf321e910750059ffd3311478aa4a68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e178965db0bcd548d8708b185b75bbf7baa9610c87707395e09a4b3936db24fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316042474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c36062429000daee9967c3a6c523fbf4b7025aeb4408f69746b60e5c9d29d1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35515117493e52c38adb77412e5d70e1c716a60977e0d1bad3b1ed7e46700be3`  
		Last Modified: Wed, 29 May 2024 19:57:38 GMT  
		Size: 316.0 MB (316032410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad89dbd88444ae98e574e40539b211581ed6c64271ddf0e53c7b32fa645b974`  
		Last Modified: Wed, 29 May 2024 19:57:34 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:6203d19901e030ab0daec80b608b3db9e3fe8051d6f16aa6401075a7a51871b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11702905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a656c662bc10d622ea50e9941ccb5df83f39084ad8014f45a12734f6053ebf85`

```dockerfile
```

-	Layers:
	-	`sha256:2196da55d05a9d7a7fb16e898751b96da5e8ba62b27b617af1c53f23a3404d9b`  
		Last Modified: Wed, 29 May 2024 19:57:34 GMT  
		Size: 11.7 MB (11691394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2c8dc4fc5ca08b34ef8009248a3fb39dbea4ab5c111952b3d8622e6eb3d702`  
		Last Modified: Wed, 29 May 2024 19:57:33 GMT  
		Size: 11.5 KB (11511 bytes)  
		MIME: application/vnd.in-toto+json
