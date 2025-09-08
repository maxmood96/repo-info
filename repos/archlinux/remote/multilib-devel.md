## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:0cd3f227a24ba5110d93ddd83a45f8634edaea544dc497474a22953346c80357
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c8dc88a3af806c0a7a108a22623f78e0da02430451d6fa4835091e8c622a1eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340679545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63c8652702a57d1f5c496f1b41a6e33a0f11a572dc038f44133336b88e3d630`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.version=20250907.0.417472
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.created=2025-09-07T00:07:51+00:00
# Sun, 07 Sep 2025 00:07:51 GMT
COPY /rootfs/ / # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250907.0.417472' /etc/os-release # buildkit
# Sun, 07 Sep 2025 00:07:51 GMT
ENV LANG=C.UTF-8
# Sun, 07 Sep 2025 00:07:51 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e7abf3d7da9943cb2159eaebfb57c876d373acb19f559c2f4b7f37e05ca632aa`  
		Last Modified: Mon, 08 Sep 2025 20:15:47 GMT  
		Size: 340.7 MB (340669290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a478f69a8846193264085a9c6342534acee5a921a258862cc5a42af8cb2a1a`  
		Last Modified: Mon, 08 Sep 2025 17:23:20 GMT  
		Size: 10.3 KB (10255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a180945ad55c76d33fcbf7c45dc698e91d076c09f0b75045d01fbbcaa229d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12363630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cff58e2624aad65f050ab06dbc13b218ab028b7662202d8e5cdb8dfbfa3d85d`

```dockerfile
```

-	Layers:
	-	`sha256:a6594782c8cd07a748c297b67c55038b9373ebbcee1b4e2d09958dec0a2cb081`  
		Last Modified: Mon, 08 Sep 2025 19:48:33 GMT  
		Size: 12.4 MB (12351819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6007a7a1382493e7433eefb0cc17838d0027b52bf6b47a519ae37b626d4095fe`  
		Last Modified: Mon, 08 Sep 2025 19:48:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
