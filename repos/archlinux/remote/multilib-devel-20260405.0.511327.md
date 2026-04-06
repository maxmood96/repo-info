## `archlinux:multilib-devel-20260405.0.511327`

```console
$ docker pull archlinux@sha256:f02e8deedf73c48aa71ce29c8ae4de5f681991125ef6c627d4eef9e657a3507a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260405.0.511327` - linux; amd64

```console
$ docker pull archlinux@sha256:4a8aa2fad48d940a0084f4c99cc0b92484e0d9b18d722afe74add42ff5491754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268641078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f817144db725d1c67e2d186a6b80a74fc3381a29148257dc3a1683b7ea284`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.version=20260405.0.511327
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 06 Apr 2026 18:07:57 GMT
LABEL org.opencontainers.image.created=2026-04-05T00:07:03+00:00
# Mon, 06 Apr 2026 18:07:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 06 Apr 2026 18:08:03 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260405.0.511327' /etc/os-release # buildkit
# Mon, 06 Apr 2026 18:08:03 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:08:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:68571b5330036f5d6913e7b3579ec3358f381968b99a3cee984742027bcea8ed`  
		Last Modified: Mon, 06 Apr 2026 18:08:55 GMT  
		Size: 268.6 MB (268630768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8802103e1d0f4f426aed3656c2ad0fa433dda130f7351925ff64d09fe40cfb`  
		Last Modified: Mon, 06 Apr 2026 18:08:48 GMT  
		Size: 10.3 KB (10310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260405.0.511327` - unknown; unknown

```console
$ docker pull archlinux@sha256:82ee2d0174b6984698b05db4aa49f0e78216aae8e618c7ce8775d619c2a115f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12216339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9029ad14072fb30ca7ba99c46fb5f89de23d9374d760be00f657fdf22337aa3`

```dockerfile
```

-	Layers:
	-	`sha256:020b6df1b2b0428d27b8f9f7f0492bc1ccbfb4e77d23ed9d774cc56adfcb54b5`  
		Last Modified: Mon, 06 Apr 2026 18:08:48 GMT  
		Size: 12.2 MB (12204571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7748bae67c70dea5f06af7977d6da537c679483418da19dafb7c78bf90a0a0fa`  
		Last Modified: Mon, 06 Apr 2026 18:08:47 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
