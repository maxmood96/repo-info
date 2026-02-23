## `archlinux:base-devel-20260222.0.493200`

```console
$ docker pull archlinux@sha256:f7227efe3682a77c6243ac2a1649d3bc93905655a4ddbb540844a3c037ed166e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260222.0.493200` - linux; amd64

```console
$ docker pull archlinux@sha256:4de1c037a3250981f3927b888f922a9aed8ff6398233213b71cac2997d588e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245854781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69d5ebd524e60d08a5f7a464fadac8e073606eb860bb26fdf2439bbc5c60086`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.version=20260222.0.493200
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 23 Feb 2026 19:08:43 GMT
LABEL org.opencontainers.image.created=2026-02-22T00:06:47+00:00
# Mon, 23 Feb 2026 19:08:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Feb 2026 19:08:48 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260222.0.493200' /etc/os-release # buildkit
# Mon, 23 Feb 2026 19:08:48 GMT
ENV LANG=C.UTF-8
# Mon, 23 Feb 2026 19:08:48 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f4781d5d587803a33e56cfc1497b8f654f4e958c4748a88bdfed42d8f936fa3`  
		Last Modified: Mon, 23 Feb 2026 19:09:32 GMT  
		Size: 245.8 MB (245845650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9f282a8b5b877ddf817a2013db21d2b5c8c31ec67b8a3e61de3d26f325ebf`  
		Last Modified: Mon, 23 Feb 2026 19:09:27 GMT  
		Size: 9.1 KB (9131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260222.0.493200` - unknown; unknown

```console
$ docker pull archlinux@sha256:c19ed3c9484fc41a0687c7ef0a2f1531c59ed3396483aba5cd6d8526eb033239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12251627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ddbacc4dc79038f460f4b33777290be965650480569f72d6fe772585bce273`

```dockerfile
```

-	Layers:
	-	`sha256:e167bad5d2e01fe4405279e10a1d5e8a97541ee220e80dcc14fbd4053a180917`  
		Last Modified: Mon, 23 Feb 2026 19:09:28 GMT  
		Size: 12.2 MB (12239916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df4eca89c7d4b5bf89b616ed0c460ba8b60136ffd2f364def51874a811ee332`  
		Last Modified: Mon, 23 Feb 2026 19:09:27 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
