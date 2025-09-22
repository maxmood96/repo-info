## `archlinux:base-devel-20250921.0.423275`

```console
$ docker pull archlinux@sha256:0589aa8f31d8f64c630a2d1cc0b4c3847a1a63c988abd63d78d3c9bd94764f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250921.0.423275` - linux; amd64

```console
$ docker pull archlinux@sha256:f1e466354b09be5e39c3c776436ea23407fe3d9fdbc0909b9e1e1cdb07fff006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289784440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc65acfd58b235826af8c7dd44a1e845dc3c3f6a9afcbd53492b85897b0a649`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8f0661e86a4352a5b41461a186a2ef2918ccfda12cf00f17378f3b5ccaa68223`  
		Last Modified: Mon, 22 Sep 2025 19:52:56 GMT  
		Size: 289.8 MB (289775279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d2d390041c4c695fd932609a8370c07aba9831b0a94c06d0ba07bf269e5d4`  
		Last Modified: Mon, 22 Sep 2025 16:53:07 GMT  
		Size: 9.2 KB (9161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250921.0.423275` - unknown; unknown

```console
$ docker pull archlinux@sha256:d884c4c9df27612319f2ccdb141cef3683df392c89e658c0d48e8d6be96fa9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490a6ecb8ba6e8348eef396e995f4932eceb54df33b0fa9ee097c9edf946ac7`

```dockerfile
```

-	Layers:
	-	`sha256:2eff59a3d6270a9bfa995791356d63c4c2970b85cbda690ec76f8b81d0bf40e9`  
		Last Modified: Mon, 22 Sep 2025 19:48:23 GMT  
		Size: 12.1 MB (12118397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eae29ffd01c3fced7c68f387fbb9a16f93228397b7c237212f826eda99586f0`  
		Last Modified: Mon, 22 Sep 2025 19:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
