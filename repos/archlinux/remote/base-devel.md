## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:52caef7ac18d69010f97ebb0b0d23cbb02e0b9bfc5715f044508b3552beaa419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7dd35e9ca75b183042a9f22b8106b19d9511a5b610039072546ba6c5c3a81af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289366809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87221098b9c69429253a9100b1c3f3aa2e8967c9e2968512dccc9861c26ff697`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 07 Sep 2025 00:07:51 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:ac0c9d6e9598df47eb858042b1f9b6e70be0ac5bb78c53e2dd86c0e3a7ad926c`  
		Last Modified: Mon, 08 Sep 2025 19:49:56 GMT  
		Size: 289.4 MB (289357647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa474f8ed776670f9356c8bafbabcc3de7a582a1184f2b08dd6a8f695cefffe`  
		Last Modified: Mon, 08 Sep 2025 17:16:28 GMT  
		Size: 9.2 KB (9162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:23fd162a0710e105899d86115d9408eac294799a94247f2886a3dbf30591a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12094679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4627380783c74775050cd4c7173492d7d4c0fc2a4f2469804185595e497348`

```dockerfile
```

-	Layers:
	-	`sha256:62ad2a8ad3aa16dd6a6c452b96982b184bbe1b16e888c18ea0d6e33644945fe4`  
		Last Modified: Mon, 08 Sep 2025 19:48:29 GMT  
		Size: 12.1 MB (12082925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63f333a0f76bc63fbc19f6663bd01ea8fac4c8bad0669e40ccd8463b35399f7`  
		Last Modified: Mon, 08 Sep 2025 19:48:30 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
