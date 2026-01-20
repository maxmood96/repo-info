## `archlinux:base-devel-20260111.0.480139`

```console
$ docker pull archlinux@sha256:84c36fa73fc692775e6b99de0d6a10967005b459ef170fc4faea426673b5e7b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260111.0.480139` - linux; amd64

```console
$ docker pull archlinux@sha256:bb59138e0f1735a5c4449c39cc0d72ea7592beb3fdc46b8166538e5b326ef4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293731041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1512daf7f17af1c7641bacad417e4cc12edcc901c32891b39d8e0f5dc524bb4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:43:02 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:43:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:43:09 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:43:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cc32ee06ac77e6731f18c764c2e72a887ff547d69de10ec09dda33ed3f0eefc6`  
		Last Modified: Mon, 12 Jan 2026 19:44:15 GMT  
		Size: 293.7 MB (293721693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e569b708c9698e5117c1d999863a141d95f2b0b0538f21711097755c00ec120`  
		Last Modified: Mon, 12 Jan 2026 19:44:06 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260111.0.480139` - unknown; unknown

```console
$ docker pull archlinux@sha256:57f28034d876181e06208e27d98e61b1cb5378c2b876757d88a5ff5af98ff8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89818d2877e388bfe99270ac7912ba87ff3cc1e86b5ff6fdb4b536e795d620fd`

```dockerfile
```

-	Layers:
	-	`sha256:9316ce4f66cb865108f677a609fffd32e148844e06bf6db744466aea30322db5`  
		Last Modified: Mon, 12 Jan 2026 19:43:53 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090dcb99cca41d0874b08a89776bf6cf00ede46ddbeb24da8ee5536acb48df8b`  
		Last Modified: Mon, 12 Jan 2026 19:43:52 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
