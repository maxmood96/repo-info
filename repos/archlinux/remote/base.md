## `archlinux:base`

```console
$ docker pull archlinux@sha256:ce4dddea70099cc8360478d162e478997420185683ce9de88223c3f316c17c1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:abd76aa5edede07476fabba538e80fdbd54d1326f32ae0bb64efcd3f17c362a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160247595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405a3273f1873dbaf19fb3c110b234dc6c38e7a205f6a6c78c34776545409810`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250420.0.338771
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 20 Apr 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-04-20T00:07:41+00:00
# Sun, 20 Apr 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250420.0.338771' /etc/os-release # buildkit
# Sun, 20 Apr 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 20 Apr 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a1b185628eec31bffbf020fe73a089e4b496c8822b25b0d53c34c05f589a91cc`  
		Last Modified: Mon, 21 Apr 2025 22:34:24 GMT  
		Size: 160.2 MB (160239247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757f0aa62ffe93c4e2a40ba1f2b59a886f3fe59733176db9fa3dca4b9e0276b`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 8.3 KB (8348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:3efcdf569b00489cc39a9006332f2f4ced799a4a69e32afeed2a427858ab4b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad01ac41f81be3bdd59e7fdcc2d38aaf3a8b6d6583f0162f42abb1351bca5ad`

```dockerfile
```

-	Layers:
	-	`sha256:96a14649829e65702c3656892ebef89369fa00c3e5b5cb2d1aa68db8f7435c86`  
		Last Modified: Mon, 21 Apr 2025 22:34:21 GMT  
		Size: 8.2 MB (8164628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775d65efbd7ee3566bd8680280f412e627b94e92fce89932f923fa9eee06b80c`  
		Last Modified: Mon, 21 Apr 2025 22:34:20 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
