## `archlinux:base`

```console
$ docker pull archlinux@sha256:901cf83a14f09d9ba70b219e22f67abd4d6346cb6d3f0c048cd08f22fb9a7425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c6adc95d0eabb024edace76211d96a1c43846e475eee5ce7bbf71a444d332bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152724438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4c632eebd620b4f6201d93de0f3f339423c283c08aa3d7fc706c2797150e45`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7fa4bb7a964dac0c4b221a145e2f663e66dbe8ad7db623df9a05ea30a7c21cc3`  
		Last Modified: Mon, 16 Dec 2024 18:28:34 GMT  
		Size: 152.7 MB (152716125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d609407a8e75eb4be7200f664d3e143be31dc28d208ba378633e1bb3605ad0`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.3 KB (8313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:944eabb17f6b795d6dcd8f157b3bfc383572f18aaa45b1462d1b0e342f357e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f32a9b110dfd18d83ca8c8036b661cb40e1d5587fd59a1d2ae463987b87501`

```dockerfile
```

-	Layers:
	-	`sha256:aaec2d5338db11b50ca421b7cf99f0003a95b5308230b51736e08bf39306025c`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 8.1 MB (8089382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38229154eaac88caa23c818b99f6721a148abe74011f18b22a1ac82c866c0b01`  
		Last Modified: Mon, 16 Dec 2024 18:28:32 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
