## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a921b6864609280975d8269df323c2f4f478cdc9d0f5479e70c3fb5e710d1b11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:e7eda50a054df84145bd4b9ef1231d0efae47b4fab526eb8df171cacc5766565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163065097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683780d7bb0bd9086019f3ff532ef3a75b3f4a8143b4bbb0ac640ec4d1f2de90`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250622.0.370030
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 22 Jun 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-06-22T00:07:28+00:00
# Sun, 22 Jun 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250622.0.370030' /etc/os-release # buildkit
# Sun, 22 Jun 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Jun 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9d37d6e63884857da7d1b14c93a397e958c93ba2ed8a5d80ca61722c48c9fbdf`  
		Last Modified: Mon, 23 Jun 2025 18:35:13 GMT  
		Size: 163.1 MB (163056750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd720a8b0d34871aa7ad437d570670de7eb94c7e7a2a43694ae3f27b273287b3`  
		Last Modified: Mon, 23 Jun 2025 16:52:06 GMT  
		Size: 8.3 KB (8347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:de1c487256a3b6c00c8490bc8c3d947ae88146b591a70b6f5aeb70fd7cc91029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8160112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b21c0d991dd08e679964c41de77dfb2c8c8a405f1dd24b0c9c28225200df64`

```dockerfile
```

-	Layers:
	-	`sha256:ede6771150cd0113fe48afbf2e5fc38584daed1537b80feb81cdb9c4abf93275`  
		Last Modified: Mon, 23 Jun 2025 19:48:16 GMT  
		Size: 8.1 MB (8148140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126ea1eb77f86ad9cdcc639ad746568837ab37c787aa9ce17a64ebb05697fe9a`  
		Last Modified: Mon, 23 Jun 2025 19:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
