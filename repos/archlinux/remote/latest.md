## `archlinux:latest`

```console
$ docker pull archlinux@sha256:36e14d971d587c5cc7e2c832bd8789b27cabfd75e0be8e4f79bc162468c5043b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:5c3fb7b417945a3d6ff506f5d8764385956d629ad37b480ed3416240ae54b2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151205810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e84141a99956b46bb2f3a1adeeffaaebbb5a2e1d2779b501c87453abd62a63`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:d9de125b2003639366eb85bf6b0a340229a9b2be0a2efda65f3abd97be902d88`  
		Last Modified: Mon, 14 Oct 2024 16:57:58 GMT  
		Size: 151.2 MB (151197584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0a06a02c96571f8b86f75e0eed3087a35d16edbeb7d30381616407009b1fc`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:4c02f4ffb27e355e1d8f773fb2b46d0e8973f71ac155aea3074b2b9f160ca9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c96c8fb166dba210683a94477cf8b404d8efa1d8ded09034e8b307d8299d21f`

```dockerfile
```

-	Layers:
	-	`sha256:f15845601f16bf05c20abd228626ea0e99da93c5db5602b10cfaf28f5a58219c`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 8.1 MB (8102276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629057bec6b0b13bb93048c0cdeba5f187d5a2f660360f65b542e6eda13fa75f`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json
