## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:881022c38f3338dd74f06ee0bf5ac05748e40efc6162a23dbbdbfef14634e506
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:445aaca11be510adf10b9ddcf30259d4ae4c8474530a8d5d71ca93199184ee70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (325975046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae6b25d6884216d69cdf94215f539a6531cc5365f409d2aecf40e54d93c75ec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.version=20260517.0.530531
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 18 May 2026 21:50:23 GMT
LABEL org.opencontainers.image.created=2026-05-17T00:09:11+00:00
# Mon, 18 May 2026 21:50:23 GMT
COPY /rootfs/ / # buildkit
# Mon, 18 May 2026 21:50:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260517.0.530531' /etc/os-release # buildkit
# Mon, 18 May 2026 21:50:31 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 21:50:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:218564e2f8d63e6df94802e5115b23deb1041ba00fc7cf32cf180e239b11c7c2`  
		Last Modified: Mon, 18 May 2026 21:51:32 GMT  
		Size: 326.0 MB (325962465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26746621d3475df01f66df81be8930f7f25274c51a57a80bb03ea9537fe52cfd`  
		Last Modified: Mon, 18 May 2026 21:51:25 GMT  
		Size: 12.6 KB (12581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3b08d6810090289dfc5f1994d8a38d2f7a74ab5fc489aaf0cbb4502cb5a8acbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14667077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c43c7b9e0e77008c941959f6a9b99be5759270793c210268ab3286eef3a1c2`

```dockerfile
```

-	Layers:
	-	`sha256:790db6cb300f80a3b1ae5e1007a4876f01ffc72106844cef06ee6a2ae945c10d`  
		Last Modified: Mon, 18 May 2026 21:51:26 GMT  
		Size: 14.7 MB (14655309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b66f7e1795b0bd401264c978fd0736e749f900a939bdd0d3895918c7640bbeb`  
		Last Modified: Mon, 18 May 2026 21:51:25 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
