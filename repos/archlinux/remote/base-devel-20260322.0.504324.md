## `archlinux:base-devel-20260322.0.504324`

```console
$ docker pull archlinux@sha256:233f52197321141f63c1d389284c868101dc94ef8f46ac31b908e3e4b6ea7cb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260322.0.504324` - linux; amd64

```console
$ docker pull archlinux@sha256:351ef3518e944780972d651e6961d69d050350c31fcc973c9b463fa8665988f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246275217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace0273710d59d9137247f8c89c3763796cbde392da16cb0b8e2bbb49bdb59fc`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.version=20260322.0.504324
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Mar 2026 16:51:06 GMT
LABEL org.opencontainers.image.created=2026-03-22T00:06:34+00:00
# Mon, 23 Mar 2026 16:51:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Mar 2026 16:51:11 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260322.0.504324' /etc/os-release # buildkit
# Mon, 23 Mar 2026 16:51:11 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 16:51:11 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:361908d86bc2bc504d2c2942eecfbc836824e2e38e2799388d65ed96f7dfd4d7`  
		Last Modified: Mon, 23 Mar 2026 16:51:58 GMT  
		Size: 246.3 MB (246266088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4126aa50fdb3f9d29dfb3d546b11b936a4dbbc548dd815ece5e7e4a43bb92b`  
		Last Modified: Mon, 23 Mar 2026 16:51:52 GMT  
		Size: 9.1 KB (9129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260322.0.504324` - unknown; unknown

```console
$ docker pull archlinux@sha256:e61294dc413506b17260eeac9efb6e4c352292316f92e960534e1b8d367ac22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11938961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0eca649dafb6c72883aeab81116d7b9c2106d2f4e94b403141147dc4742316`

```dockerfile
```

-	Layers:
	-	`sha256:f2b5bcb6da6d99a4e998446b5cee23b8b28a8d57776e312faa5311d6689acae4`  
		Last Modified: Mon, 23 Mar 2026 16:51:53 GMT  
		Size: 11.9 MB (11927250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67bb9328e839ec28cbb18f5911cdfdd8f481f547c7eea494f43c32ac389529a`  
		Last Modified: Mon, 23 Mar 2026 16:51:52 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
