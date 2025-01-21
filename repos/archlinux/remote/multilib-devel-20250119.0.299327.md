## `archlinux:multilib-devel-20250119.0.299327`

```console
$ docker pull archlinux@sha256:ff6470d224bb12bb677a6b08a6124a9b008f3ea3b69703cc84625e0ce4602fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250119.0.299327` - linux; amd64

```console
$ docker pull archlinux@sha256:95a4ea960d5ddda41f534cb47aa833e0ab1311577a6ecb6ad6f25a36f66415ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328347414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4797ad20713e5f74fc1dba1d956832c9cb11e214884f872614d757634b379b2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250119.0.299327
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-01-19T00:08:08+00:00
# Sun, 19 Jan 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250119.0.299327' /etc/os-release # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 19 Jan 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5d7fac93d56c1bd297bc1d6bfd88706513aebd832974fd49c8b251f381157415`  
		Last Modified: Tue, 21 Jan 2025 18:28:41 GMT  
		Size: 328.3 MB (328337189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dd54ca61fdf27372b360d168518b8c0d98f2dd1ec4317534b4572ba93cc401`  
		Last Modified: Tue, 21 Jan 2025 18:28:35 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250119.0.299327` - unknown; unknown

```console
$ docker pull archlinux@sha256:f77ba332d5c101dba25b236bfdba894211f57f575514744e9dc8d65d11d4115c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12175015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd206ec2c5dfc6423da23a7599c1d9c41d17306a50ca964aaf35da895095832f`

```dockerfile
```

-	Layers:
	-	`sha256:df24ec1b18f79dec2c2c9e8df22562c87c2e719fd05a1ef53adc337265b7f9e7`  
		Last Modified: Tue, 21 Jan 2025 18:28:35 GMT  
		Size: 12.2 MB (12163204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c61aad88faf255738d0ed376dda4ac8a18dde8e9a949ef3f2074e143692ee81`  
		Last Modified: Tue, 21 Jan 2025 18:28:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
