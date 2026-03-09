## `archlinux:base-devel-20260308.0.497099`

```console
$ docker pull archlinux@sha256:b3c1ff749031ca2e06df1cd83fda74df13206a047b7b0f96b818825d9dc60785
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260308.0.497099` - linux; amd64

```console
$ docker pull archlinux@sha256:42a29e6cc13502f8f80cb260300a9c6b1e6008c2308032b98e0c2e3663c6bce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245847356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a733d65c09f048602156757aefd83904a48faff31a7bdc33950e01d12a67ea47`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:59:41 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:59:41 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:59:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:59:47 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:59:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:94a058dd3ee0bc361e3cb4973ff16d37231e1333ac7e7f49783edec0f3468358`  
		Last Modified: Mon, 09 Mar 2026 18:00:31 GMT  
		Size: 245.8 MB (245838229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2199aa76033b1b31fe873642bdbb34e21cf45649d13b5f0137cf27f7fdd98811`  
		Last Modified: Mon, 09 Mar 2026 18:00:27 GMT  
		Size: 9.1 KB (9127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260308.0.497099` - unknown; unknown

```console
$ docker pull archlinux@sha256:251f8f567b3250ae10f7489bc177c1eedf5a121c3cd9ce2b696fe17a9a53b7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11897139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb53b193f55d8cc4931c198251c78f1671166490391dea0f46f66af19164a88`

```dockerfile
```

-	Layers:
	-	`sha256:0bc4454778b0713a90c8361ede5789da48af8c4d5762f13effb53005189eeb69`  
		Last Modified: Mon, 09 Mar 2026 18:00:31 GMT  
		Size: 11.9 MB (11885428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf2cb5383c0020b1ca882eec73638a1142eb21363ed263c5acd57721e22b40a`  
		Last Modified: Mon, 09 Mar 2026 18:00:28 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
