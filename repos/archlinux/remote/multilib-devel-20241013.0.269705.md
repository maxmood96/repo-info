## `archlinux:multilib-devel-20241013.0.269705`

```console
$ docker pull archlinux@sha256:bc7b145c837776bc29c499b8fd55b9e229c73f1a118701ff33a4a1f74105f839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241013.0.269705` - linux; amd64

```console
$ docker pull archlinux@sha256:fa32ba9229770ff04b16774dec4d48906430c77116c36416b9056a39df728e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322061544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54daaf80f03e696bc16603bfa8cf8b50974634cc454461ff7d1c73a1eec227a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.version=20241013.0.269705
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.created=2024-10-13T00:07:34+00:00
# Sun, 13 Oct 2024 00:07:34 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241013.0.269705' /etc/os-release # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
ENV LANG=C.UTF-8
# Sun, 13 Oct 2024 00:07:34 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e8bac2ec1e9ac3fc4345cd625a0d59da834a50b49e726689c348241a2c6f19a6`  
		Last Modified: Mon, 14 Oct 2024 16:58:57 GMT  
		Size: 322.1 MB (322051434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4da072a877bc0e32c51ab1f51eacc501c455982eefa3f37dd4626e7026f20bb`  
		Last Modified: Mon, 14 Oct 2024 16:58:49 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241013.0.269705` - unknown; unknown

```console
$ docker pull archlinux@sha256:1d4f238f382dfce03e6d8922fd1db3798938b6b03a9ca5c27b85c85e25095a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3e1afcd0d17101f0e6764407b345358d84cbdc49a02ee0475bc7e09a675d35`

```dockerfile
```

-	Layers:
	-	`sha256:b8d0e62991372c675f0518d6f49053ee8298e00ccf68d7103f4d82c932e70a19`  
		Last Modified: Mon, 14 Oct 2024 16:58:49 GMT  
		Size: 12.2 MB (12167879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3ef50435a2011438c3c14cbb0220f599fbe105ed679c71cb3cf695fecde173`  
		Last Modified: Mon, 14 Oct 2024 16:58:49 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json
