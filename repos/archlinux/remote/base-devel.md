## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:925a18f3b29708f2e9b7850c58a71b65f36cbcaddc8e5f1ba3a77057b9bdb88e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:985d1236e051b95d80e20755349061919ca0349925c2caacdaace92d2991d5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92845b5741df93ac770a34717e57613b3d2c3d1e571456119b7b2eac2210a946`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.version=20250817.0.405639
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 17 Aug 2025 00:07:25 GMT
LABEL org.opencontainers.image.created=2025-08-17T00:07:25+00:00
# Sun, 17 Aug 2025 00:07:25 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250817.0.405639' /etc/os-release # buildkit
# Sun, 17 Aug 2025 00:07:25 GMT
ENV LANG=C.UTF-8
# Sun, 17 Aug 2025 00:07:25 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:06a1f21ad0ba1fa6a4658ca8f40bebce6a25dc164953f4315389efc6704cbe3f`  
		Last Modified: Mon, 18 Aug 2025 19:50:18 GMT  
		Size: 289.1 MB (289118842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd76bccf9cb696f47f05a25b6df108f9826f8ad738a740be6a7baf5c3fd3a222`  
		Last Modified: Mon, 18 Aug 2025 16:54:53 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:7016575e94761e34c1def92921e37b33b38a09b56197ae1dbfca8a94414b9649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12075561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cbc1d27eb10e72f2654c2dcc1f6e7eae46e1e34b79f76d4bc73114199020b5`

```dockerfile
```

-	Layers:
	-	`sha256:0ab47556f945a32b9880aa4d76995465a9c8367b4585ad4ca5a117883cb63adb`  
		Last Modified: Mon, 18 Aug 2025 19:48:21 GMT  
		Size: 12.1 MB (12063807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2015cfd4cc960e8b811a0e00c77f9f00f3e41b9f46537e8a49be274723d30b`  
		Last Modified: Mon, 18 Aug 2025 19:48:23 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
