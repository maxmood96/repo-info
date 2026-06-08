## `archlinux:base-devel-20260607.0.541780`

```console
$ docker pull archlinux@sha256:dd60dfcca90f1ee6c2dd265ed27062070a1fb2e3b307723838a9d97741284722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260607.0.541780` - linux; amd64

```console
$ docker pull archlinux@sha256:f557e49eaad9b696f0ef71cd12f2a2418407c8d4c441f311c38bd95186afd85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303239264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc16ee0e5ffe5c241a261f07c78777b0cfc4b0b38456930bf2179fdabb7fa034`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.version=20260607.0.541780
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 08 Jun 2026 18:51:18 GMT
LABEL org.opencontainers.image.created=2026-06-07T00:09:31+00:00
# Mon, 08 Jun 2026 18:51:18 GMT
COPY /rootfs/ / # buildkit
# Mon, 08 Jun 2026 18:51:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260607.0.541780' /etc/os-release # buildkit
# Mon, 08 Jun 2026 18:51:25 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jun 2026 18:51:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:011844ffd4c148ed1ec219c23df98cce9131911699615bbfab580bda4db5ae24`  
		Last Modified: Mon, 08 Jun 2026 18:52:22 GMT  
		Size: 303.2 MB (303227863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b02c2b8021a1d28b03a38d0831afce2be8c98cb144398fd5ae3456d3a071cd9`  
		Last Modified: Mon, 08 Jun 2026 18:52:15 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260607.0.541780` - unknown; unknown

```console
$ docker pull archlinux@sha256:33fc398841b252e7e2878e984122ff50851b08c29a081b3e089362d98794dfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14397498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14261b8fd4b8b8dbfff97eb0fa942351512c96f58d1072c3f32bec47992145f6`

```dockerfile
```

-	Layers:
	-	`sha256:d94d3b6c8ed5a2e3a7aaef3a2f556ce6f645cc89d6c56d8640f3838cc7abc89f`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 14.4 MB (14385786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783351bb6d2edb4b4c0a2ca43ae7ba325a8b63037c9b1cb16c2586da79a13a3e`  
		Last Modified: Mon, 08 Jun 2026 18:52:15 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
