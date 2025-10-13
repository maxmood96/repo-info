## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:87a967f07ba6319fc35c8c4e6ce6acdb4343b57aa817398a5d2db57bd8edc731
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3f87d6fd1d3575adf372fc3a89d121ada49c739e6874b686929a0c7688f96e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290402693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce4eac8f0e1b2294a65f237e72d1c2f1245917250421c5971f44720cf75a73e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:40a5c65700b7d7b9416f35272ff2779a3f3035c353228939aa7268bd91207d0b`  
		Last Modified: Mon, 13 Oct 2025 19:49:57 GMT  
		Size: 290.4 MB (290393539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b296d3961febf0ff21ae29828097127758a3e0c33c1d9a773190e62c10f5b`  
		Last Modified: Mon, 13 Oct 2025 18:11:15 GMT  
		Size: 9.2 KB (9154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:87221a39386272fb2224c1d549abad3a1006068b2e114c388e7197ffa7e45589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af776174d14756c9c8e7b84f821c6f233a5dd6220db892b39b36b6b28992398`

```dockerfile
```

-	Layers:
	-	`sha256:dc43627b48bcccd7efc9e7e39b71658b9413cd55547fba96351b98e9b58b70fe`  
		Last Modified: Mon, 13 Oct 2025 19:48:23 GMT  
		Size: 12.1 MB (12118947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f5e55db58632671fc5395c94a39ce7582e9b2a90267a2bcf9a4c4ef30aa968`  
		Last Modified: Mon, 13 Oct 2025 19:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
