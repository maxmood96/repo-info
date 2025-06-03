## `archlinux:multilib-devel-20250601.0.358000`

```console
$ docker pull archlinux@sha256:3cc1f84a3d30af91a961939003511e14f055a79b51995268a56c61c5821287ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250601.0.358000` - linux; amd64

```console
$ docker pull archlinux@sha256:0c5dc362cc9f9f5038a1af45508f5c617ef9c501f9d0ff49529dbe11ab3c3a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338277512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0acf492e5b791dd24f739431f626d44643590aad0defa786e144748617a7914`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250601.0.358000
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 01 Jun 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-06-01T00:08:08+00:00
# Sun, 01 Jun 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250601.0.358000' /etc/os-release # buildkit
# Sun, 01 Jun 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 01 Jun 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:12fc202400169e3d4e72f4fcd423ace9fbf29163322ea51c21ec76f9acf93b60`  
		Last Modified: Tue, 03 Jun 2025 13:58:50 GMT  
		Size: 338.3 MB (338267185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043f027ba9731cbcf066d48c033293a39d0250988ac4814e3098923b3ddddfa5`  
		Last Modified: Tue, 03 Jun 2025 13:58:43 GMT  
		Size: 10.3 KB (10327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250601.0.358000` - unknown; unknown

```console
$ docker pull archlinux@sha256:981313fe9db3103fc34231ccfc19f7e8c9662d4eaf220eaeb887a7ef9b8511c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12310843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacdd8c2029fb859fe9a3472e1f55c65a951c6d28c05a03eb48a2c0055797f71`

```dockerfile
```

-	Layers:
	-	`sha256:dbf46450f15bc13a9243f81ccfe97652be728992ef72454183344ce075364f5b`  
		Last Modified: Mon, 02 Jun 2025 16:52:54 GMT  
		Size: 12.3 MB (12299032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d0142f06753a116a2a8199a20c5179834d61f50a5c455408c59b4e388e240b`  
		Last Modified: Mon, 02 Jun 2025 16:52:53 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
