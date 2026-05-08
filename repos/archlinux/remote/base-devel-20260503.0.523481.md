## `archlinux:base-devel-20260503.0.523481`

```console
$ docker pull archlinux@sha256:fdff15f24df062598faebf380430955a9bd2109736e179ebb354f1208f725774
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260503.0.523481` - linux; amd64

```console
$ docker pull archlinux@sha256:dbe52370858ec341af9035cb657939eb912a7b825899cd766f01bc5a775587db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253375736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4030ab66d9e6f3f244d4874300669fe58da4920187b9694e3f9b4c7fd17ea3ec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.version=20260503.0.523481
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Fri, 08 May 2026 00:02:27 GMT
LABEL org.opencontainers.image.created=2026-05-03T00:09:00+00:00
# Fri, 08 May 2026 00:02:27 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 00:02:32 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260503.0.523481' /etc/os-release &&     true # buildkit
# Fri, 08 May 2026 00:02:32 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:02:32 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3ef99323a2e4c453b3d861ac76d5966c9160bff61b25b544b5adfdea2179dd8b`  
		Last Modified: Fri, 08 May 2026 00:03:19 GMT  
		Size: 253.4 MB (253366574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a5eaa38a5eaa31d519fbc7a9817247635c214f85295bd2e918a7bd90b30e65`  
		Last Modified: Fri, 08 May 2026 00:03:13 GMT  
		Size: 9.2 KB (9162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260503.0.523481` - unknown; unknown

```console
$ docker pull archlinux@sha256:16254c9d175cffe887e692f22065d24cbbb6151221f3401c4aeda5c5fc0a7c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12048095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eeff322de4b768e5bcbce348b1ae918c73bcbb50e695aedd51d5a7414a71a1`

```dockerfile
```

-	Layers:
	-	`sha256:36ff033c1cf7e71c88132887e083a57ea7a2c08e61ab5746a57271c962b126a9`  
		Last Modified: Fri, 08 May 2026 00:03:14 GMT  
		Size: 12.0 MB (12036306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a125e56997e4919053a4fbc29f6d864aa7ee5cc5d9b96717f0ccfb10019b322`  
		Last Modified: Fri, 08 May 2026 00:03:13 GMT  
		Size: 11.8 KB (11789 bytes)  
		MIME: application/vnd.in-toto+json
