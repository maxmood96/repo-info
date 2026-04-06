## `archlinux:base-devel-20260405.0.511327`

```console
$ docker pull archlinux@sha256:4a48384d9725d1901fca133f43b6a41dee98acee2c9379c4b4d81bed77051cdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260405.0.511327` - linux; amd64

```console
$ docker pull archlinux@sha256:e1b8968819709959fec2cd9115822300e1ae9e4ab436234445fe6229a7ce0677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246478432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7f571c205bee9bfa5e886814f50a918a626847aafa9ba3a7db8443542f3e00`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.version=20260405.0.511327
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 06 Apr 2026 18:07:51 GMT
LABEL org.opencontainers.image.created=2026-04-05T00:07:03+00:00
# Mon, 06 Apr 2026 18:07:51 GMT
COPY /rootfs/ / # buildkit
# Mon, 06 Apr 2026 18:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260405.0.511327' /etc/os-release # buildkit
# Mon, 06 Apr 2026 18:07:56 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:009772841e8246ba72583eea022399749cacc094fee5279ea7e29f66196abc27`  
		Last Modified: Mon, 06 Apr 2026 18:08:40 GMT  
		Size: 246.5 MB (246469311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00216238e42ffc58161f8b6ab72ce4e2805ffbe72fbe0cdd1f52137530b764`  
		Last Modified: Mon, 06 Apr 2026 18:08:34 GMT  
		Size: 9.1 KB (9121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260405.0.511327` - unknown; unknown

```console
$ docker pull archlinux@sha256:0d05689f7bbe1df2c8784ff215e3d7357e07ea158d6e9f383b3a787fedeebac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11946412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd758ae78da41d848bff8569a7bfe6b8987a42b7ddcd1b748c6465f59ce4dc7`

```dockerfile
```

-	Layers:
	-	`sha256:4fde26159ffe8a2c5bf51ba8f5aa0d7d7b404db30ec7b4ccd2d1b7b3cd471e5d`  
		Last Modified: Mon, 06 Apr 2026 18:08:35 GMT  
		Size: 11.9 MB (11934701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc852de4f7a8d5b5d7a64bb46cba0934679e404a0c8955c6614b380b03d85521`  
		Last Modified: Mon, 06 Apr 2026 18:08:34 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
