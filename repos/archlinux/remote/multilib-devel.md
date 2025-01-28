## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:6a6ed840566e5a6f0ae94a0ce81f0b0885aea54cabd5cf3383b3e2d41744ac30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ba2faadfd27d4dc3835ce585240e0f61b24c0347024fc381ef63f49d4a5370a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328458128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da3b92cbdf48e6bd8e0e1327994a7eeed4691d633598a3b9622518cece59626`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250126.0.301347
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 26 Jan 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-01-26T00:07:29+00:00
# Sun, 26 Jan 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250126.0.301347' /etc/os-release # buildkit
# Sun, 26 Jan 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 26 Jan 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c0cb1c42aed3f18ffffa74aa3110b16b2521df6a774df4fae59723b41af39564`  
		Last Modified: Tue, 28 Jan 2025 01:29:05 GMT  
		Size: 328.4 MB (328447889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118b2175bf5367c509c7e2493b81f4717b24f8959859ceb3b93ef1e574faba4`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:6591c7430bc90b971b71db2058b6ea3370669151f36b7e19fa98a56eb9dce7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c41a172bbdce816661967c7773378b8fd4edad74e4a1ce17329245f02d1558`

```dockerfile
```

-	Layers:
	-	`sha256:8d110d462a67c4970847158d6e37d2a66b7ae6e8f784ae97f2a052d77bd29cd6`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289b3359781f1e395184a1f08a761c9bd6867811dbb07f19f4c211c981cf639f`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 11.8 KB (11809 bytes)  
		MIME: application/vnd.in-toto+json
