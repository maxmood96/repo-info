## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:d53a6f8e38e34d617d6da3635fa8be86568d7792838251cbb2d84d899dc8d752
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:919905a090e8d49ba5d7a1b62a26af6016389a085af0d0252f16985e2f457d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281771197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c321285d574578c45f4d1dd1a74facdb5271887db7bf78f3d2a7e783a6f10`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.version=20250427.0.341977
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.created=2025-04-27T00:07:36+00:00
# Sun, 27 Apr 2025 00:07:36 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250427.0.341977' /etc/os-release # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
ENV LANG=C.UTF-8
# Sun, 27 Apr 2025 00:07:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:22e021f6cca4506347a8504ef5f7d98fb55f44265e6d381984cf83be8addc8b5`  
		Last Modified: Mon, 28 Apr 2025 17:56:34 GMT  
		Size: 281.8 MB (281762017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49958c0a82c2db177e9881e674cf552bfe465942bc6682b50c957d88399675c`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:78ab8f93f149ac6aa15e82b7b8d50f494de8ea994c9b18f27a5748c37eb66349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11998050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e855a60d201ea38495d8c496fad5e421ee1f776f1e325b588aad33af926cb4`

```dockerfile
```

-	Layers:
	-	`sha256:5f38931604a46f289adc88e5740283474134b52ed8e60b8a545e1a34b5f47d14`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 12.0 MB (11986296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2806408a7c642875f06e0ffab1769721eb5da70a433686ac43da0a8e3f181f9`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
