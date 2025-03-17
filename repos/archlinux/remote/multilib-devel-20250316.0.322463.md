## `archlinux:multilib-devel-20250316.0.322463`

```console
$ docker pull archlinux@sha256:06e35cfb67ecad7144e7eed47f0da72c1a13e8a79fc4046c4b36c8a7bd3f6870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250316.0.322463` - linux; amd64

```console
$ docker pull archlinux@sha256:9f3207a2265872f633478d58172d5795ad09d993b68360b472084b88067d0d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330699684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b450e5273289f2bd202e2485e6f90ddfe79b44bcc8c80bf27f1273ec961abf13`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250316.0.322463
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 16 Mar 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-03-16T00:07:29+00:00
# Sun, 16 Mar 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250316.0.322463' /etc/os-release # buildkit
# Sun, 16 Mar 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 16 Mar 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a1901b4f066c719dceb6c165206acab439c74d74d988ec790c5f7a451744703c`  
		Last Modified: Mon, 17 Mar 2025 17:50:46 GMT  
		Size: 330.7 MB (330689448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb9c4d85f3a66cad602fc0d5fd2f688b737b7a8aa491129d8a1cbe4c1ef88e`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250316.0.322463` - unknown; unknown

```console
$ docker pull archlinux@sha256:2ad9fafdb7e0bf20f3b4f60901b7bb54746ed84c6ccb0a69178569e75ed75aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12256242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408ad6539d1eee021b1a5bd7832c4b0ec8609f68c12323e38b01514adde08eeb`

```dockerfile
```

-	Layers:
	-	`sha256:bcf04837141ed06b7ff89c56dd4b2d8f642010514665d8dcd7b8ace4ee5fabc5`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 12.2 MB (12244432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e783cba17439c127bdea0ac2ef1de2870f3333afd29f4c66ff3e6c05588a4e8f`  
		Last Modified: Mon, 17 Mar 2025 17:50:41 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
