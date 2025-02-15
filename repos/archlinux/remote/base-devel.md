## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:2e64be3bcaeb69bff00ba401cce9b26277ca29ac3f4ef661f3a31d803e96a58f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e5c8d0ccd853f86c2eaa3148cd4c51062229014d80f1c8efed99993c3ed00eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278801075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261975b3eff42077ac4c418afc8197ae290e843228e6cdda4875ec84c84bb29b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.version=20250209.0.306557
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.created=2025-02-09T00:07:51+00:00
# Sun, 09 Feb 2025 00:07:52 GMT
COPY /rootfs/ / # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250209.0.306557' /etc/os-release # buildkit
# Sun, 09 Feb 2025 00:07:52 GMT
ENV LANG=C.UTF-8
# Sun, 09 Feb 2025 00:07:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:597f8ce19d766bcdf33ec6a6ec4f60bc434037a9a9efc05adab134ffa7dd739a`  
		Last Modified: Mon, 10 Feb 2025 20:50:42 GMT  
		Size: 278.8 MB (278792008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33041fa63b5c1f16df393202a8baafc5957fd71dc5714f2cf458084031584a25`  
		Last Modified: Fri, 14 Feb 2025 23:49:31 GMT  
		Size: 9.1 KB (9067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:18402c1595b399977631d7a471a62f3a338cfea6ef9dda2670e55f79fc00dece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a6b942484670819e0f1c230103efc62d510b64d984eb1d8aeb77c585a8210`

```dockerfile
```

-	Layers:
	-	`sha256:dd1cb379753c056fab3676446e4f6895da435bb22b038213636e3b54e1a04698`  
		Last Modified: Fri, 14 Feb 2025 23:48:23 GMT  
		Size: 11.9 MB (11896538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1543f0e932a83cb097159173b2a84b2e5360ad919c82829cd5e10feb7495db4`  
		Last Modified: Fri, 14 Feb 2025 23:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
