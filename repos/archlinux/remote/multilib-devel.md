## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:382026febe9d0647082ecc0004aee156bdc8b571d8ff427d9dbb4b7a7f7f52c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:dc4817e2db60ecb6ad8ba795d6e292ea003d0caa83fd5bf309a847145334c8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340455063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06393749d4c9af90d7870c757bb1f227addde5e2aa079a00d142dfd9de82b739`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.version=20250824.0.410029
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 24 Aug 2025 00:07:29 GMT
LABEL org.opencontainers.image.created=2025-08-24T00:07:29+00:00
# Sun, 24 Aug 2025 00:07:29 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250824.0.410029' /etc/os-release # buildkit
# Sun, 24 Aug 2025 00:07:29 GMT
ENV LANG=C.UTF-8
# Sun, 24 Aug 2025 00:07:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a18a861ef7fafe9556993468d877ce370d9029dfd521ac9f6e65ed986e505cf6`  
		Last Modified: Mon, 25 Aug 2025 23:31:18 GMT  
		Size: 340.4 MB (340444765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022e18f0432d86e9257f25999b3cfc3b6edce6537d7f35e4c7c0fc2d4acf9ff`  
		Last Modified: Mon, 25 Aug 2025 19:54:04 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:fb60cd6ff4e3b67a47eb9e99ae9405759666babec479a0abf483ae22b73ff418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c536f1e8d7954b1ccb2156e8629904bcff0a986f6fbef851fa122fb7bea2605`

```dockerfile
```

-	Layers:
	-	`sha256:95c826324f897edf831dd6b29b3f9b79526319e26fac7b6675aed6d8f026cc49`  
		Last Modified: Mon, 25 Aug 2025 22:48:27 GMT  
		Size: 12.3 MB (12332701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f67b9447269510a2ba67ca37df865df646c31c25c714783a834c1ac9b3fc40`  
		Last Modified: Mon, 25 Aug 2025 22:48:28 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
