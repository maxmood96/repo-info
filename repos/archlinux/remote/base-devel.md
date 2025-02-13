## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:d35892b93859c4170d753fe7efdd98b4f38c9d4539435e9bab71d1ccc9ab0483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f5e17fd8666fe0d4432ea83289ece234312368a8c5cc2c2f7a23d7c7e1abf147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278801050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3df05114946e71bcb5db0623d86d7e7a9a1273d084c1dc1b76ab624d60324`
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
	-	`sha256:b222395fbe2616d512cc313813a661864b31323d3f0ec9883e4943b3f7c2d37c`  
		Last Modified: Mon, 10 Feb 2025 20:50:07 GMT  
		Size: 9.0 KB (9042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8eaeda8723c8a1156cc2dee3dec8820a770bb14047abb2d16601a5a392e6ff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae86713e6adf9e81b8380fcadb96457ded4d366f83832e85a24b15ad3443ca2`

```dockerfile
```

-	Layers:
	-	`sha256:e313ac902394ecdd87f7ed42a8194660134c93c8095d1742100c091e1607fa13`  
		Last Modified: Tue, 11 Feb 2025 07:41:55 GMT  
		Size: 11.9 MB (11896538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cdd40f761b97830706c748190103ecd552bfb753aeaf7bc5c3e5873a6d4cb9`  
		Last Modified: Tue, 11 Feb 2025 09:01:16 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
