## `archlinux:base-devel-20240721.0.248532`

```console
$ docker pull archlinux@sha256:21c96d7f815d65b5d7e87be20020bada9c60f2a7ad1a4157e8f0fa7526c755c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240721.0.248532` - linux; amd64

```console
$ docker pull archlinux@sha256:5a3f145cd6205f9480e180b03df29c34276d146543a627118e197f3b81ffe209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271452622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99722901cbc7ab7227f58a01e3920e2facd070a07204a4bb95db4ac3421ad372`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:68f76d89052db3b531b4590cccff8643757330318ed8f33f844421089f752f3e`  
		Last Modified: Mon, 22 Jul 2024 19:59:19 GMT  
		Size: 271.4 MB (271443577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa8e0950a2527369de29232564ffd6829fb4699835136a272beab8dd36fe0c0`  
		Last Modified: Mon, 22 Jul 2024 23:04:04 GMT  
		Size: 9.0 KB (9045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240721.0.248532` - unknown; unknown

```console
$ docker pull archlinux@sha256:cb81038d56830e6f5f56889fb2d1ea026eefb881f31f9ad0233e8f60ca13e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11800120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056cb290416967da90db0bb4f478fbb3a19038d8f87e58c4348155b84665bbbd`

```dockerfile
```

-	Layers:
	-	`sha256:886b21f78ce6f4051c16ba0d171ef99403666317438d0f044c11c40cc828970b`  
		Last Modified: Mon, 22 Jul 2024 23:04:05 GMT  
		Size: 11.8 MB (11788617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6241cbbf84a34a085d0f3be97bcf9be0cfcc3e75094f3da0789fcacb3fb51a1e`  
		Last Modified: Mon, 22 Jul 2024 23:04:04 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
