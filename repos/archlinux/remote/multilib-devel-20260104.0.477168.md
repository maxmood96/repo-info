## `archlinux:multilib-devel-20260104.0.477168`

```console
$ docker pull archlinux@sha256:400068c34425fddb5c5e1120e55f0cc30603d798cdef20d782d75768ff42aa22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260104.0.477168` - linux; amd64

```console
$ docker pull archlinux@sha256:ad458d551f760c99654cbadaf418f9d52511604462be3838fe183a6d042b58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343555316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58c3573b89670d991522dc02fe0af37058eb86726274fbc857faaf48d697f11`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:18:08 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:18:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:18:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:18:16 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:18:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4d8551d0b9caf25071addc6296ecff628973b4a1a667a059e49416651d1c7c69`  
		Last Modified: Mon, 05 Jan 2026 18:19:57 GMT  
		Size: 343.5 MB (343545027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf22f956b7a5c45d9c5f5f4173de6f3a94afae9cd604a8becb0ff08f8fa44ec`  
		Last Modified: Mon, 05 Jan 2026 18:19:22 GMT  
		Size: 10.3 KB (10289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260104.0.477168` - unknown; unknown

```console
$ docker pull archlinux@sha256:688beac2cd317902b7090fe5cb9ed03a86c232ca342c0a228ecd9065e50d7a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12426291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac60ffb3e72456f93090eff387acd287765fe0df936a0ca9bf2f8d80d002095`

```dockerfile
```

-	Layers:
	-	`sha256:4e57fa88627ab907121956a8754186cc6e5d9d7a73927afb2fe4436e042e5033`  
		Last Modified: Mon, 05 Jan 2026 20:48:32 GMT  
		Size: 12.4 MB (12414523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b40d404f0849662b16f2ef8020130fb4e98daf60a5a01dbcc380c18a7412bc5`  
		Last Modified: Mon, 05 Jan 2026 20:48:33 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
