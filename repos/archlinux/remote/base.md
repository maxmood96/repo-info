## `archlinux:base`

```console
$ docker pull archlinux@sha256:e25a13ea0e2a36df12f3593fe4bc1063605cfd2ab46c704f72c9e1c3514138ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:58a1cde0acb1a9fa847c5d829e0349ab76d6fb0893c47f3dad176d2cdf301ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128266383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453453af7a6f321d70c1d0855ce385fb1bbbc622b8213d7981bf205409e4f9de`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.version=20260215.0.490969
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.created=2026-02-15T00:06:54+00:00
# Tue, 17 Feb 2026 18:11:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Feb 2026 18:11:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260215.0.490969' /etc/os-release # buildkit
# Tue, 17 Feb 2026 18:11:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 18:11:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b2d9d946693ed5d2ad46777157e06c2ee1aa6270da5007dee549f429dc470ae1`  
		Last Modified: Tue, 17 Feb 2026 18:11:55 GMT  
		Size: 128.3 MB (128257808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad61ad26ec7862a5bde2fb078d78122d2fd61ea72bcff6fae75d4af471275894`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 8.6 KB (8575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:f3b95755139ca0c40f929333ad9e1d059ae51e97a10de774b712e5efb9848cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8471516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326176095077c0180d2d9fd7b86ae55d9c967fc6fb79db5f33e555cf1e698f78`

```dockerfile
```

-	Layers:
	-	`sha256:89840e3003f3914213acec748e5b71a6b0cb1686004af093d93b35dede08ecd5`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 8.5 MB (8459587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd221151afb6b3bf1abbccb5fc84852dc2f5d714e7bdfbddb3feb52aca5a061e`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
