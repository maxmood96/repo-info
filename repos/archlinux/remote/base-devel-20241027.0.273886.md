## `archlinux:base-devel-20241027.0.273886`

```console
$ docker pull archlinux@sha256:d1182fe9683fd80afac359754f606aa1fbb74aa2e6f65a9395be83a95bb8f953
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241027.0.273886` - linux; amd64

```console
$ docker pull archlinux@sha256:39908e5005aa727e93e36fa4b741a1ed22fd7b2db83e264ce0acdc7aea334397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272205935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b21ceeb73c50dc0b884143ea2feed0a0b9c919cfa42b8f38336d80a4c7ffa7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:02a5a1341bbcd83e0148b5fd871fbadb41badae053e4d579e9fc6fe7b740ea1b`  
		Last Modified: Mon, 28 Oct 2024 17:58:12 GMT  
		Size: 272.2 MB (272196934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de547d0c8aa87918635917dd8ca511ca2788075fa3529c53b174d64c69ecae21`  
		Last Modified: Mon, 28 Oct 2024 17:58:03 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241027.0.273886` - unknown; unknown

```console
$ docker pull archlinux@sha256:8efad37ba464c1863be291efef4ece9e74041c53fc6b6f4b24f8bcabeba05357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11962175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aadfeb0ee6b15d9c7c106617a93fe593349825f5112c9145c345a6b030794d`

```dockerfile
```

-	Layers:
	-	`sha256:de5c521344689eb688ae68a376b9bdcc5a4d4375089c843e5e108f47bb390cdb`  
		Last Modified: Mon, 28 Oct 2024 17:58:04 GMT  
		Size: 12.0 MB (11950638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add305c0d4ca9e7110af0d941275e8ed60f89ca5bd83f12865dd009a49d5da6f`  
		Last Modified: Mon, 28 Oct 2024 17:58:03 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
