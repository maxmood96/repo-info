## `archlinux:base`

```console
$ docker pull archlinux@sha256:4c24063e3e3fa753b0c1f5cd0486ed5bee0173da61b1e73a3fb872f10163f760
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:510bead7bcbe2a4c190c1f1db94763d1ea079cf4612688f3ccc9ddfb6147de49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129432783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff30320934df1071bb33892039bfb4aa21d2c72a78c9a040f12c67ac9460c72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:47:07 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:47:07 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:47:09 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:47:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:edfbbe617b176994dfb9c35ff5c72f5a5021c1716196804101a97c25fafd913e`  
		Last Modified: Mon, 13 Apr 2026 17:47:35 GMT  
		Size: 129.4 MB (129424120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229820f59e0fdb118794c698a40a0fc82ecea473c8e14450b8f6a95bdc06d70a`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 8.7 KB (8663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d52b5f2ccd08d6dbe7aaac42100605f6f4ed97675b2ab0b9d1b9d26d2a9ff095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8189956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0754ba67cd9dafd07ae5ff3d26801deefdf897b1900b56ac07eff89f4bc5e6`

```dockerfile
```

-	Layers:
	-	`sha256:5e94eedf2d40d7cae0d21ee55c053fac6252cd2e6497a3215e1350e5651f3c05`  
		Last Modified: Mon, 13 Apr 2026 17:47:33 GMT  
		Size: 8.2 MB (8178027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64d625bcea621f79c961584687324144e1f82c1a195eb77c7d1f43e6b9d04b4`  
		Last Modified: Mon, 13 Apr 2026 17:47:32 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
