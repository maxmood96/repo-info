## `archlinux:multilib-devel-20250112.0.297543`

```console
$ docker pull archlinux@sha256:13b1036c6c31622d924812de5ebc41353e0cf0a20dce28f2633385dc94b9a607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250112.0.297543` - linux; amd64

```console
$ docker pull archlinux@sha256:0e70b49bf26e1c17fe6c9bdf1f1fb49cbd3eb93ce2f7dce22521199cd8b2538e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324100005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ae797a5b95acbbc644e03de6411b8833ccb24eafe2b9a1d8b09aec1410d959`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250112.0.297543
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 12 Jan 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-01-12T00:07:47+00:00
# Sun, 12 Jan 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250112.0.297543' /etc/os-release # buildkit
# Sun, 12 Jan 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 12 Jan 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c8449f073c3e398c721f972d23d1572901515bfa70be188a331897942c0ef478`  
		Last Modified: Wed, 15 Jan 2025 00:06:43 GMT  
		Size: 324.1 MB (324089754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a546a2758b768631b3aeab8ab930c455db81ff37e4d540a676c9a9b33cf5452a`  
		Last Modified: Tue, 14 Jan 2025 21:16:19 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250112.0.297543` - unknown; unknown

```console
$ docker pull archlinux@sha256:87272d00fd78879b7156e469e97936274f59c1b0531c532ddc48d637812c05c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11546494ab0da0ce3d273f535973ffb098f0cb4936738ea7f66c6e847d9f4d45`

```dockerfile
```

-	Layers:
	-	`sha256:674f22cd0d28f3b3135fbce0f9d3b3d30d081aefbc303ce42ec5432f92ea9c28`  
		Last Modified: Mon, 13 Jan 2025 19:29:22 GMT  
		Size: 12.2 MB (12164242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5919c5ab0ea9cfc5108838cd2b99a023a245f65fa0adf6792623e84bf459099e`  
		Last Modified: Mon, 13 Jan 2025 19:29:22 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
