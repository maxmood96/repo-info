## `archlinux:base-devel-20250525.0.354646`

```console
$ docker pull archlinux@sha256:cc583ad12f43f59a25c9833b638b5656ab5941fefb92404f95e8c15ca162b62b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250525.0.354646` - linux; amd64

```console
$ docker pull archlinux@sha256:80db78991e3b8cbc06978080b9aecacf44b45ae8dcf9df665d6b5822ad615a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287058217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8936d8d04f80e46c73351fd816703abd057ef4a6cdb3d397015356f42f79791c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.version=20250525.0.354646
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 25 May 2025 00:07:55 GMT
LABEL org.opencontainers.image.created=2025-05-25T00:07:54+00:00
# Sun, 25 May 2025 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 May 2025 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250525.0.354646' /etc/os-release # buildkit
# Sun, 25 May 2025 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 25 May 2025 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c184cf66b9fc050ddf0631ef482f6eed24164bd8b38afc0e99cd7eec8f405ebc`  
		Last Modified: Tue, 27 May 2025 18:51:44 GMT  
		Size: 287.0 MB (287049022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a85f83999853f4bf40957a392bfe9255c9d7f7965de183da977cf3dff8a9ad`  
		Last Modified: Tue, 27 May 2025 18:51:40 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250525.0.354646` - unknown; unknown

```console
$ docker pull archlinux@sha256:977d8218552496dfe26fa64f871cac5418f5b1e5ba7eb785426320d68c492913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12041372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4042b5cb0aac9e8ba643a1fc1a0b8cce4c538743f3d0a3c31015909fe68d1f93`

```dockerfile
```

-	Layers:
	-	`sha256:f7bc271bfb97491614ad4a39b17aac91c8e9057d7c662ba1e539ded9cd134cb4`  
		Last Modified: Tue, 27 May 2025 18:51:40 GMT  
		Size: 12.0 MB (12029618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3ad2a9fa377d8a76c100a382e45575753f7ccc2faa032018cbeab06304b27e`  
		Last Modified: Tue, 27 May 2025 18:51:40 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
