## `archlinux:base-devel-20260301.0.494762`

```console
$ docker pull archlinux@sha256:a4e49d3505c6bad5909d292ef31ae7599aa58c1468c5d407883507d7d77ce3b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260301.0.494762` - linux; amd64

```console
$ docker pull archlinux@sha256:799c4c5935baaf7b4ca1ec216e55146dac5720c1de2e07608516c80f0c9206a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245924827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f0b7e135cf3b829df5466b5a0bd5ad6259b5b28a83776bbec12213a5863df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:13:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:13:19 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:13:19 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:13:19 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6d6e1ae42c059c45ffaf68544ea82d0b0ce2d8144da1734b551558eea33f3f4b`  
		Last Modified: Mon, 02 Mar 2026 19:14:02 GMT  
		Size: 245.9 MB (245915716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb94e2ef0f05673e841bb09b9c44d613bb9129d050bb58a399b988ec8e27ae1`  
		Last Modified: Mon, 02 Mar 2026 19:13:55 GMT  
		Size: 9.1 KB (9111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260301.0.494762` - unknown; unknown

```console
$ docker pull archlinux@sha256:17f7060aecc3e49017def05fc8406cd2a6db9d626ce614f19e3169eddc86919e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12250998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2fb327b75f9b5671e075f3b04ea3eee5c782ef68293bf26313bbff29bccb9a`

```dockerfile
```

-	Layers:
	-	`sha256:26eeb41ae39a9d0e42562a20eada6d5cf78ca5779955058c90d4a17a1da7823f`  
		Last Modified: Mon, 02 Mar 2026 19:13:56 GMT  
		Size: 12.2 MB (12239289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539c61b08285f85d9262884cc0464f287219f12f07bd7c9bf62687c3dc4b49f9`  
		Last Modified: Mon, 02 Mar 2026 19:13:55 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json
