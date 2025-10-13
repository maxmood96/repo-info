## `archlinux:base`

```console
$ docker pull archlinux@sha256:0423e31111e93087aef7a46f999a91e892a8d1b49e9de939e3e660e34ce42fe8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c7f7b9545dd34e5e990b3dba126ac890dca86a19a76931d0de121fad65ba0830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165313794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db23cb19a4c6eca9c4cf961d71db72d3f5c248008bd8de249deab687952155ca`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:25614b3b15cb8475f385228ace25cfdcdc8d8dfcd68fd1ec0ad41ef2a0b6a5b7`  
		Last Modified: Mon, 13 Oct 2025 17:57:18 GMT  
		Size: 165.3 MB (165305454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c93813b9937c66e353d01fc7b735a1adc10009c67423b0aab18ec1ed5e86857`  
		Last Modified: Mon, 13 Oct 2025 17:57:08 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:c7ef8dbfe8001330188cc9e181a2808d99d9a63ac664b941ad8139369bd9f77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ada5774aa56fe9940eda50ff0140f7c6302f446a7efc8c4031f7df7d314f84`

```dockerfile
```

-	Layers:
	-	`sha256:31f2e6481e4179f7706a75b3895be983357599af96ab71a311bd7a2e2b884b06`  
		Last Modified: Mon, 13 Oct 2025 19:48:17 GMT  
		Size: 8.2 MB (8217611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798bcd34d6e682ba6aaadb75bd492c7c101a5883c926e86a59b1c7a8f3277d20`  
		Last Modified: Mon, 13 Oct 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
