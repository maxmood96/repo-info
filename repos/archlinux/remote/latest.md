## `archlinux:latest`

```console
$ docker pull archlinux@sha256:7dba90fa0171e5f23fd41500f15263b61bf4f95464f527d7152e15cb35e7a7d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2040d6337505c204e3991f509e62f728d8b4d465e9f8379815dce117c464143b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151183315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959149ca6d710bb267e4025fdc80deafc201371adab763a606162c80367e9dc7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a7eeb2be9236376dfb256be5af295b286214fd6f9583c91a99e5de0a412b7dd`  
		Last Modified: Mon, 26 Aug 2024 21:59:19 GMT  
		Size: 151.2 MB (151175032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a9bc48d5fff4402023f6b618fdb83fd6b9a9b04f7c497cd062bb71be893b7d`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 8.3 KB (8283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:10c1a6c09dbf2bd280b93d450f89ef49a8549ba4afcf1cbabc415c8f7a693366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1894bddefaab455d063d2508dd1891b6a343b81910c306fd2c9d0a5e8e74771`

```dockerfile
```

-	Layers:
	-	`sha256:12310cb0423ae8a5202e44d31c72d2e24683851a2e5bdee85393f4c62e20341a`  
		Last Modified: Mon, 26 Aug 2024 21:59:15 GMT  
		Size: 8.1 MB (8103979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acaeace8729b8b4f553c93549de5f6ddd4fc67c093f72be7f207096a840d51e`  
		Last Modified: Mon, 26 Aug 2024 21:59:14 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
