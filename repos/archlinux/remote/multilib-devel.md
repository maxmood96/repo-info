## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:e6f380814330655127d3992645edea1f3eedbb64ebc104c1720cab5ba5b8edc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8469ab5c69f1418d7d383f8efed700dc534a0c805318fa6c2a2d3a75f801be5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343393692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e88f1c7781849036177cd9cab713eff2f6bc6532c8b239357d60f1dd9b930e9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Mon, 15 Dec 2025 18:33:04 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Mon, 15 Dec 2025 18:33:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Dec 2025 18:33:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Mon, 15 Dec 2025 18:33:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Dec 2025 18:33:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7b1e20b4fe65799151a60bf5d121f5f6f83fcd2aca9d80b1b2515a189308c3fd`  
		Last Modified: Mon, 15 Dec 2025 18:34:37 GMT  
		Size: 343.4 MB (343383370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac785afd68e3d429e4a59200c9e62541df8f9ebe66a65d85c9944e885b89ceaf`  
		Last Modified: Mon, 15 Dec 2025 18:34:28 GMT  
		Size: 10.3 KB (10322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:734e6d85dff9efb2f64c23577d82df79d53f939e36b4c76f12109a73dda8a89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecec4fa283964a4341ef8428286b33c6a0ffc909779810155c0d6b27717c18a`

```dockerfile
```

-	Layers:
	-	`sha256:596d9cf7986b992d90f6ff15fafbccc6568ed3ab316908216ff6cdeb4bebf85c`  
		Last Modified: Mon, 15 Dec 2025 20:48:30 GMT  
		Size: 12.4 MB (12399954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ced505fb617f128419ebe504694162a1a214ad01a774ed1720bdb86c3d61dfe`  
		Last Modified: Mon, 15 Dec 2025 20:48:31 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json
