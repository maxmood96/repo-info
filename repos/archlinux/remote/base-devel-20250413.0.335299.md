## `archlinux:base-devel-20250413.0.335299`

```console
$ docker pull archlinux@sha256:6c2b425acd8752cf50a78c33b360811cacbe71c4b596838f4aa8752469955269
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250413.0.335299` - linux; amd64

```console
$ docker pull archlinux@sha256:6eb91015bcc283a912a302a7b22665d98461816a75c220b4944d840581c3adbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281765810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053cdbf777e997f66204ce3cc14db807b624970e99bc5e746c3213ef8c9c967a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Apr 2025 00:07:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:c282d2893b767f376f8dcaccecd0f322acb7c7a95a74873bea131260cacf7493`  
		Last Modified: Mon, 14 Apr 2025 18:01:26 GMT  
		Size: 281.8 MB (281756646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6f3bdec2aaa51e14106d14b92ea2fc8750ec87497a1e8fa60fbbc9a9d78cef`  
		Last Modified: Mon, 14 Apr 2025 18:01:21 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250413.0.335299` - unknown; unknown

```console
$ docker pull archlinux@sha256:76202b7b85b92c5aef23bb4b68f4897b8aae95c70ce0841ecc0809e1e18b4a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11996818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c397ebe69b37e683423f766bf710a1b309f1801de60ad61e658ffba47bac0dbe`

```dockerfile
```

-	Layers:
	-	`sha256:e4c55bc06c1cf576ec10b1d3484db55fda70fb102ebaeda37aaec6880cc97998`  
		Last Modified: Mon, 14 Apr 2025 18:01:22 GMT  
		Size: 12.0 MB (11985064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7fcc3706f198d4ff6ac55086d1eecbe551e7d17f20e4e841cda7b48950ad270`  
		Last Modified: Mon, 14 Apr 2025 18:01:21 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
