## `archlinux:base`

```console
$ docker pull archlinux@sha256:3f2eefb6cbbdcb3a9677442d569c1f332706eb535da31275128508ca365af1b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a8323f89dfc10b4281ad3ce790de6541056fa03a348db0167b8759b64998f98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14be0997a90bec78c3c526042f8dc9474d073f718c0b3260afb7120a62c0adb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.version=20250413.0.335299
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.created=2025-04-13T00:07:50+00:00
# Sun, 13 Apr 2025 00:07:50 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250413.0.335299' /etc/os-release # buildkit
# Sun, 13 Apr 2025 00:07:50 GMT
ENV LANG=C.UTF-8
# Sun, 13 Apr 2025 00:07:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e480c905023911546029c27182f928580da4546c7dc85f842a974c9effe646ad`  
		Last Modified: Mon, 14 Apr 2025 18:00:53 GMT  
		Size: 160.2 MB (160218350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794c4182559636633d7d4f27839d8ea0d05f74dfdd184a988915008fcea6a10a`  
		Last Modified: Mon, 14 Apr 2025 18:00:50 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:2b7cefe5890586d1759be10fb001c913996872910b9bc30ee56af02da8bc1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b908d8d16d8c95b8a35eb435106613e5dfc865c6ca64a35470f3db5c3a06ec81`

```dockerfile
```

-	Layers:
	-	`sha256:383710fdac844c3ca7f15dc13ba8937b82d95427c153a1b1e6cc38fe3f6f9466`  
		Last Modified: Mon, 14 Apr 2025 18:00:51 GMT  
		Size: 8.2 MB (8164632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbed1ed9b4f213cd46a8ec3b943d348fd36a119420cf5cd035072449d4660bf`  
		Last Modified: Mon, 14 Apr 2025 18:00:50 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
