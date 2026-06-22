## `archlinux:multilib-devel-20260621.0.546891`

```console
$ docker pull archlinux@sha256:b3d3414c33e700ea0268cfd98f7b93ad15eae04820c18e15f4206951c33c17ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260621.0.546891` - linux; amd64

```console
$ docker pull archlinux@sha256:5018ebf50dc41326b5becee912df1861158257ebd8b085ed6e64d7a9080c1cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325876711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909e126b2bc9284d6e50fbde442f865cd15c9fd76527a6c666d14dc26829696`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.version=20260621.0.546891
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 22 Jun 2026 19:45:39 GMT
LABEL org.opencontainers.image.created=2026-06-21T00:09:09+00:00
# Mon, 22 Jun 2026 19:45:39 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 19:45:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260621.0.546891' /etc/os-release # buildkit
# Mon, 22 Jun 2026 19:45:47 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:45:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:26a2f4e971794b5cd538bb8bfc45e2c869ff01f072afebb464bf1501e121888d`  
		Last Modified: Mon, 22 Jun 2026 19:46:47 GMT  
		Size: 325.9 MB (325864186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465090eae9f4efa8090ac4f85c7fdc8d05a57c4fd0817cc085ddadac7c829ff2`  
		Last Modified: Mon, 22 Jun 2026 19:46:41 GMT  
		Size: 12.5 KB (12525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260621.0.546891` - unknown; unknown

```console
$ docker pull archlinux@sha256:4f9b35e2ef52d379cfb5628136579061b32e7d0f086929c01c75738cfb0b93b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14662862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056cb1773884c4aeb4c2e1fa3733484a39b2d218db54d8ac3a981d1456618435`

```dockerfile
```

-	Layers:
	-	`sha256:f2f07abf78a99d12b4b363543abc33c63cd23d15325c6ad1a2da1679dfe41cb9`  
		Last Modified: Mon, 22 Jun 2026 19:46:42 GMT  
		Size: 14.7 MB (14651094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4f474d86efa9ddf01100075fba24f3e4be97255c17266ed4dbc75c179a30c9`  
		Last Modified: Mon, 22 Jun 2026 19:46:41 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
