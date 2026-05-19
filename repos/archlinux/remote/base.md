## `archlinux:base`

```console
$ docker pull archlinux@sha256:1047e6e7878d58e4ee47e1cd6459a32fab41246b0efc4109e11b7ef16f50b14d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:42215a8ac2213d27d2bebd539737196b1bcea14382c375a5ff5a166408074fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131531164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95026cd5ba836e50589e3ccf1ebabddc5ca562e8e27c1dcddbbc7e140cf58c8b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.version=20260517.0.530531
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 18 May 2026 21:49:13 GMT
LABEL org.opencontainers.image.created=2026-05-17T00:09:11+00:00
# Mon, 18 May 2026 21:49:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 18 May 2026 21:49:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260517.0.530531' /etc/os-release # buildkit
# Mon, 18 May 2026 21:49:15 GMT
ENV LANG=C.UTF-8
# Mon, 18 May 2026 21:49:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:54b8626685668f7f8af95a079ff42364fac0252de2e6a4080bf1ae6363bc1f18`  
		Last Modified: Mon, 18 May 2026 21:49:47 GMT  
		Size: 131.5 MB (131522499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d2dac6ee5f200ecc82f8cbeaebb86261dca5de1552b71a47a953c6d2ba2e7f`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 8.7 KB (8665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:e01962c564f0d3c980a949782a4558a51a1599a0b786394e2d244958728a2905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8193065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c72c339fb8f01e8e158d7fe54967e96c09ba91ac985e6ef09dad3b36484673`

```dockerfile
```

-	Layers:
	-	`sha256:688e0a39cb99915dc563d9588850c7d3b3543dd9286cf2793eb7ad1a5b6b68a8`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 8.2 MB (8181137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e261ca3733559df04d34bc4ea600670046a2ee9bb08854de1ecd8dcd577ba5a2`  
		Last Modified: Mon, 18 May 2026 21:49:39 GMT  
		Size: 11.9 KB (11928 bytes)  
		MIME: application/vnd.in-toto+json
