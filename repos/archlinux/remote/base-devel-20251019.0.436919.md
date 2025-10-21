## `archlinux:base-devel-20251019.0.436919`

```console
$ docker pull archlinux@sha256:943bdad9e9d0d23503f24797b44ce2cc1531bf101e18b3e7fb8c8776190dc45e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251019.0.436919` - linux; amd64

```console
$ docker pull archlinux@sha256:45507a3dd4b47f79e989d8f5c68f2a3ac4e7762ae02df1a9021079d46b31f8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290408468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cea3620a76cfbe078484b4e01d03e3fd3640a589136415e91779fa1004864ce`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.version=20251019.0.436919
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 19 Oct 2025 00:07:20 GMT
LABEL org.opencontainers.image.created=2025-10-19T00:07:20+00:00
# Sun, 19 Oct 2025 00:07:20 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251019.0.436919' /etc/os-release # buildkit
# Sun, 19 Oct 2025 00:07:20 GMT
ENV LANG=C.UTF-8
# Sun, 19 Oct 2025 00:07:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cf8eef8fdeb239bae8999d4e9016b367fd988645bc52e776cbf8b67ba86ca707`  
		Last Modified: Mon, 20 Oct 2025 22:50:29 GMT  
		Size: 290.4 MB (290399321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe63a10669129fcee9af6efb2bc0327e857aa6ba4510d960ca467c3493283cbd`  
		Last Modified: Mon, 20 Oct 2025 20:27:15 GMT  
		Size: 9.1 KB (9147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251019.0.436919` - unknown; unknown

```console
$ docker pull archlinux@sha256:1e04511da147209b36c93b070f72a58d7df620f98379b55a53ae8d1cf6304254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad73e5c8de29c9643e69ce0da9ebdd3b8cba9f7240da6fc79e1a47b701ca9255`

```dockerfile
```

-	Layers:
	-	`sha256:885961d144eb276f2ef524a9c5e8659f0490e9041c6df8b4fb82e5724eda3a4d`  
		Last Modified: Mon, 20 Oct 2025 22:48:23 GMT  
		Size: 12.1 MB (12118981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f78177bbbf877c7b57b597469b7b380326943486c084abd64cfe0961eed410`  
		Last Modified: Mon, 20 Oct 2025 22:48:23 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
