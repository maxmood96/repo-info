## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:39c081e4dc9daf0ec65d013fa78f18b0003452002edbd01baedaf87efa66a9cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:edf6fa73a2df016545f2de3f583aaa55b5af04f208880101670f33509bd97c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286273018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ce695d356a0214533f6c3a01351d0d68fbe7dc3b0b2d2a0b5fc58ef53e73e8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=20250504.0.344409
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.created=2025-05-04T00:08:01+00:00
# Sun, 04 May 2025 00:08:02 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 May 2025 00:08:02 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250504.0.344409' /etc/os-release # buildkit
# Sun, 04 May 2025 00:08:02 GMT
ENV LANG=C.UTF-8
# Sun, 04 May 2025 00:08:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a4fd439567a9d24ca8781db745416caee4677d04a13f9d195223ae578eb21671`  
		Last Modified: Mon, 05 May 2025 17:14:32 GMT  
		Size: 286.3 MB (286263812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa4fcb1f89a3a7ecd401cce432f2b61bf7af1974ca9d8671fb89ad5d9224771`  
		Last Modified: Mon, 05 May 2025 17:14:28 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bbf0b33f53312c2ed65cbb6670515e5c6d3355143e1668dfa87caddabc481af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12038033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06e04ab7564cfc139eafb2a2a11dd3f3faaa082bfaa622ca76bb040357f3dc`

```dockerfile
```

-	Layers:
	-	`sha256:1b572c6fb90d2c20c4d7595612d9d5f172df82c824fbe5a0aaf1026bd5cdcc8c`  
		Last Modified: Mon, 05 May 2025 17:14:28 GMT  
		Size: 12.0 MB (12026280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb1c679a672423b2a482e59e3e2ed08816a5aa1f631bd21c02002458febfca0`  
		Last Modified: Mon, 05 May 2025 17:14:28 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json
