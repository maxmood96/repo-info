## `archlinux:multilib-devel-20250209.0.306557`

```console
$ docker pull archlinux@sha256:99ef0cdee7a0a6fc5b75e0161a0df351cf2346c470ffdf441b31184c3e34aeac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250209.0.306557` - linux; amd64

```console
$ docker pull archlinux@sha256:796848981fcaecd6c813511ef4ddedb760551a5e96b6733ca61a8096778b05c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328815904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a708a49e93e712a9348ee8c9f4eff429a0d9c653ba4e62e3b7bfc2c0862c11`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 09 Feb 2025 00:07:52 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
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
	-	`sha256:61c8fceafc7f0cdee9f810aaad8a75bd636d2b072b8452854e73c7c6f001b2c0`  
		Last Modified: Mon, 10 Feb 2025 21:05:30 GMT  
		Size: 328.8 MB (328805658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1c112cbef5f8327a79e16e83f249659b9bc4892c80fac781df8687965444f8`  
		Last Modified: Mon, 10 Feb 2025 21:05:19 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250209.0.306557` - unknown; unknown

```console
$ docker pull archlinux@sha256:97630311ffdd0fb5af4fcbf1829ffe91130322f79f395c811a0eaedf57524a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6e9545b31c45aa124916e93c02f42ed4e9e8ece4af2e8273323e2f480e983a`

```dockerfile
```

-	Layers:
	-	`sha256:eead521916ca67a28a7a761d802c8c64c0db9d5e235fc77b77d0127f4010d077`  
		Last Modified: Tue, 11 Feb 2025 09:01:16 GMT  
		Size: 12.2 MB (12165053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fc9e7c2cc63c105ee8aa59dd68eb15d7bd136027cfac645a94c000eeb737e7`  
		Last Modified: Mon, 10 Feb 2025 19:29:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
