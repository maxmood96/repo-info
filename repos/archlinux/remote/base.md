## `archlinux:base`

```console
$ docker pull archlinux@sha256:601140151f85e9f33ac42ebdd671061b109ad3ed83d794e2399bbfa6ccf30543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9196779c67e7509190eccbfd1a5149cbf43712bfd142dba8d893fe291912b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174698916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddb1ff8c1c65c7a3bc3d3b2bf28d1ac30edc9ab525c1cdfaaa652c462db7c1e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.version=20260104.0.477168
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 05 Jan 2026 18:16:13 GMT
LABEL org.opencontainers.image.created=2026-01-04T00:07:17+00:00
# Mon, 05 Jan 2026 18:16:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260104.0.477168' /etc/os-release # buildkit
# Mon, 05 Jan 2026 18:16:16 GMT
ENV LANG=C.UTF-8
# Mon, 05 Jan 2026 18:16:16 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:74d5579544e6f07f058114dd075f29694904ace100d660e3a2db3086d13ef796`  
		Last Modified: Mon, 05 Jan 2026 18:17:36 GMT  
		Size: 174.7 MB (174690249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920abf4e07e67ddc3105f7a0e85308fbcdb232b073d817adc40f1f048c92dd`  
		Last Modified: Mon, 05 Jan 2026 18:17:06 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:9f7a0c109b5d4f6965b049b94057e6ba33b69df49f0f3e8aad409745ed453e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755165ae56408573555e536074dbc169adfcd95711f4377dc369c4bf42cdbbec`

```dockerfile
```

-	Layers:
	-	`sha256:3c234121efd0eda9b56a029e610b3af82f4a0d24da77b5de71d10cd67e856718`  
		Last Modified: Mon, 05 Jan 2026 20:48:16 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfba4161778a662772d8088f287c9b9469556bf6b6850661db05606515d3865c`  
		Last Modified: Mon, 05 Jan 2026 20:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
